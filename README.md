SETUP
creare image stream redhat-openjdk18-openshift da registry.redhat.io/redhat-openjdk-18/openjdk18-openshift 
git clone https://github.com/marcorosati/java-serverhost.git
git reset --hard eb1700868ee40c23d6278a9696452affac1e9fe7
git push -f
 
TASK
-Deploy app
	project name-> manage-builds
	app name-> jhost
	image stream->redhat-openjdk18-openshift
	variabile build MAVEN_MIRROR_URL=https://repo1.maven.org/maven2
	https://github.com/marcorosati/java-serverhost.git
-Route jhost.xxxx (path per test /HelloWorldExample/hello)
-Update code app e redeploy





Note app code:
https://examples.javacodegeeks.com/enterprise-java/spring/boot/spring-boot-hello-world-example/  (change port in application properties from 8082->8080)
