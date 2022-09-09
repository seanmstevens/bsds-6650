# CS6650 Fall 2022  Assignment 1

COMING SOON!


## Additional Useful Information
### Building Swagger Client with Java 11
You need to modify your POM, add the following dependencies:
```
<dependency>
    <groupId>javax.xml.bind</groupId>
    <artifactId>jaxb-api</artifactId>
    <version>2.2.11</version>
</dependency>
<dependency>
    <groupId>com.sun.xml.bind</groupId>
    <artifactId>jaxb-core</artifactId>
    <version>2.2.11</version>
</dependency>
<dependency>
    <groupId>com.sun.xml.bind</groupId>
    <artifactId>jaxb-impl</artifactId>
    <version>2.2.11</version>
</dependency>
<dependency>
    <groupId>javax.activation</groupId>
    <artifactId>activation</artifactId>
    <version>1.1.1</version>
</dependency>

<dependency>
    <groupId>javax.annotation</groupId>
    <artifactId>javax.annotation-api</artifactId>
    <version>1.3.2</version>
</dependency>
```

### Problems with GSON import in .war filr in Intellij
Sometimes there's an issue building the GSON jar file into a servlet, such that when the servlet is deployed it fails because GSON is missing.

Try adding the gson jar to your project from the [Maven website](https://mvnrepository.com/artifact/com.google.code.gson/gson)

For IntelliJ you also need to:

1. Go to project structure
1. choose the artifacts tab
1. select the gson maven package and put it into the lib directory of the artifact. 

Compile and deploy ... and cross your fingers and toes!!

For more details [check this out](https://stackoverflow.com/questions/1051640/correct-way-to-add-external-jars-lib-jar-to-an-intellij-idea-project)


### Randon number generation in Java Threads
Worth a read for [random number generation](https://plumbr.io/blog/locked-threads/shooting-yourself-in-the-foot-with-random-number-generators) in your client ;)