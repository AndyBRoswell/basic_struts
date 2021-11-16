# basic_struts

Last Modified: 2021-11-16

This Repository Is a Simple Demo of Struts 2.5.26 with Tomcat 9.0.55 and Maven.

## Notes

Now Java Web framework Struts 2 is NOT frequently used. It is certainly not recommend to create new Struts 2 projects unless you're required to maintain old projects or merely cope with exams.

## Essential statements

This repo is constructed in accordance of the official guide [Getting Started](https://struts.apache.org/getting-started/) and you should use IntelliJ IDEA to make use of the repo.

This README file is an auxiliary doc of the official guide, aiming at having you create a simple Struts 2 project and learn the fundamentals of Struts 2, avoiding twists and turns.

Necessary knowledge is attached in the comments of the files in this repo in order to reduce the time spent in searching for these pieces of knowledge. These comments are mainly adapted from official docs (i.e. guides and references).

The official document of Struts 2 says

> The framework documentation is written for active web developers and assumes a working knowledge about how Java web applications are built.

It is needed to indicate that this README decrease the requirement on the knowledge of how Java web apps are built.

The chapters of this README is organized according to the official guide of Struts 2. The major contents of each chapter are the supplements required to successfully build this demo application.

## Dependencies

- Java 17 LTS
- Maven integrated in IntelliJ IDEA (3.6.6 when 2021-11)
- Struts 2.5.26 (stable release on 2020-12-06)
- Tomcat 9.0.55

IMPORTANT: Since Tomcat 10 all packages referenced with

```java
import javax.*
```

are replaced by

```java
import jakarta.*
```

Because Tomcat 10 uses Servlet API 5.0 (released in 2020-09-07), part of Jakarta EE 9. Hence, the highest version of Tomcat you can use is 9.0.55 up to when this README was created. Using Tomcat 10 or later will cause the exceptions like

```java
java.lang.NoClassDefFoundError: javax/servlet/Filter
```

If you want to uninstall a particular version of Tomcat and install another version, then you should uninstall it with the methods of uninstalling softwares recommended by your OS. E.g., "Apps & Features" in Windows 10.

# How to Create a Struts 2 Web Application



# Hello World Using Struts 2

