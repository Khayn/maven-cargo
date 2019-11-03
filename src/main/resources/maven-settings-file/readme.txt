As shown here:
https://www.baeldung.com/tomcat-deploy-war
put settings.xml in %M2_HOME% folder

create system variable named CATALINA_HOME, put your Apache Tomcat path in there (in my case, D:\apache-tomcat-9.0.27)
add %CATALINA_HOME%\bin to system path
add Tomcat roles as shown, or use supplied 

Maven Cargo plugin will do the rest, as shown in linked above tutorial
