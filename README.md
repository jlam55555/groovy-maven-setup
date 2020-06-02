# groovy-maven-setup
Basic Maven setup for a Groovy project that will be compiled into an executable uber-JAR.

### Configuration
Change the artifact details in [pom.xml][1].
```xml
<groupId>com.example</groupId>
<artifactId>groovy-maven-setup</artifactId>
<version>0.0.1-SNAPSHOT</version>
```
Change the main manifest under the `maven-jar-plugin` configuration to the name of your main class.
```xml
<mainClass>HelloWorld</mainClass>
```

### Build
Linux/Mac:
```shell script
./mvnw clean package
```
Windows:
```batch
mvnw.cmd clean package
```
The generated uber-JAR will be located in the target directory, and can be run as normal with `java -jar GENERATED_JARFILE.jar`.

[1]: ./pom.xml