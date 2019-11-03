As shown here:
https://www.baeldung.com/tomcat-deploy-war
put settings.xml in %M2_HOME% folder

create system variable named CATALINA_HOME, put your Apache Tomcat path in there (in my case, D:\apache-tomcat-9.0.27)
add %CATALINA_HOME%\bin to system path
add Tomcat roles as shown, or use supplied - if you set your own admin password, remember to update it in Maven's settings.xml as well!

Maven Cargo plugin will do the rest, as shown in linked above tutorial

in case you have different local paths, remember to edit tomcat location in pom /plugins
