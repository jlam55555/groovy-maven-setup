# groovy-maven-template
Basic Maven setup for a Groovy project that will be compiled into an executable uber-JAR.

This uses [Maven wrapper][2] for install-less Maven and the [gmavenplus plugin][3] for easily compiling Groovy from maven.

### Configuration
Change the artifact details in [pom.xml][1].
```xml
<groupId>com.example</groupId>
<artifactId>groovy-maven-template</artifactId>
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
[2]: https://github.com/takari/maven-wrapper
[3]: https://groovy.github.io/GMavenPlus/