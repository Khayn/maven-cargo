# maven-cargo
<h2>local deployment</h2>
<p>Do as follows:

<ul>
<li>as shown <a href="https://www.baeldung.com/tomcat-deploy-war">here</a>, put settings.xml from src/main/resources in %M2_HOME% folder</li>
<li>Create system variable named <b>CATALINA_HOME</b>, put your Apache Tomcat path in there (in my case, D:\apache-tomcat-9.0.27)</li>
<li>add %CATALINA_HOME%\bin to system path</li>
<li>add Tomcat roles as shown, or use supplied - if you set your own admin password, remember to update it in Maven's settings.xml as well!</li>
</ul>

Maven Cargo plugin will do the rest, as shown in linked above tutorial

<b>In case you have different local paths, remember to edit tomcat location in pom/plugins</b>
</p>

<br/>

<h2>remote deployment</h2>
<p>Do as follows:

<ul>
<li>make sure your passes are stored in your maven settings.xml file (in case of Windows, inside %userprofile%./m2/)<br/>

		<servers>
			<server>
				<id>TomcatServer</id>
				<username>YOUR_LOGIN</username>
				<password>YOUR_PASSWORD</password>
			</server>
		</servers>


</li>
<li>server's id is used in pom configuration, so make sure it stays the same - also, no need to put your passes in open text in pom, that's always nice
<li>run mvn tomcat7:deploy</li>
</ul>

...and that's it!
based on https://mkyong.com/maven/how-to-deploy-maven-based-war-file-to-tomcat/
</p>