# maven-cargo
<p>Do as follows:</p>

<ul>
<li>as shown <a href="https://www.baeldung.com/tomcat-deploy-war">here</a>, put settings.xml from src/main/resources in %M2_HOME% folder</li>
<li>Create system variable named <b>CATALINA_HOME</b>, put your Apache Tomcat path in there (in my case, D:\apache-tomcat-9.0.27)</li>
<li>add %CATALINA_HOME%\bin to system path</li>
<li>add Tomcat roles as shown, or use supplied - if you set your own admin password, remember to update it in Maven's settings.xml as well!</li>

</ul>

Maven Cargo plugin will do the rest, as shown in linked above tutorial

<b>in case you have different local paths, remember to edit tomcat location in pom/plugins</b>
