# basic_struts

Last Modified: 2021-11-16

This Repository Is a Simple Demo of Struts 2.5.26 with Tomcat 9.0.55 and Maven.

## Warnings

Now Java Web framework Struts 2 is **NOT** frequently used. It is certainly not recommend to create new Struts 2 projects unless you're required to maintain old projects or merely cope with exams.

However, that is not to say learning these frameworks is entirely meaningless. The fundamental ideas behind these frameworks can be referred in our future studies. But we really don't need to learn them in depth. The degree of popularity of every framework alters swiftly. What is the most significant is that we **MUST** master the capability to learn to use a new framework within a short period of time.

## Essential statements

This repo is constructed in accordance of the official guide [Getting Started](https://struts.apache.org/getting-started/) and you should use IntelliJ IDEA to make use of the repo.

This README file is an auxiliary doc of the official guide, aiming at having you create a simple Struts 2 project and learn the fundamentals of Struts 2, avoiding twists and turns.

Necessary knowledge is attached in the comments of the files in this repo in order to reduce the time spent in searching for these pieces of knowledge. These comments are mainly adapted from official docs (i.e. guides and references).

The official document of Struts 2 says

> The framework documentation is written for active web developers and assumes a working knowledge about how Java web applications are built.

It is needed to indicate that this README decrease the requirement on the knowledge of how Java web apps are built.

The chapters of this README is organized according to the official guide of Struts 2. The major contents of each chapter are the supplements required to successfully build this demo application.

## Dependencies

We know that most of us tend to download the latest version of the components we need to use. Therefore, I will make my best effort to keep the versions of the dependencies appear in this tutorial newest.

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

If you receive an error when trying to run this project, indicating the port 8080 is in use, you can end the process of running Tomcat instances (i.e. with Taskmgr on Windows), run Tomcat9w.exe in the installation path of Tomcat 9 and configure the "Startup type" to "Manual".

# How to Create a Struts 2 Web Application

## Prerequisites

IntelliJ IDEA Ultimate provides supports of Java EE / Jakarta EE. If you are a student or a faculty member from universities and research institutes, you are allowed to apply for an edu mail. Use this email to obtain free access to all JetBrains softwares and plugins of non-community versions.

## Create an IntelliJ IDEA Project for this Struts 2 Demo

To follow the official guide,
- Select "Maven" at the left side of the "New Project" window.
- Check "Create from archetype" and choose "org.apache.struts:struts2-archetype-starter".
- Name your project, specify the project location and set the GroupId you want to have.
- Finally, click "Finish".

## (Alternative)

If the project is built using the upper method but can't be launched, try this alternative:

- Select "Java EE (Legacy)" at the left side instead of "Maven" in the "New Project" window.
- Select "Java EE 8" as the Java EE version (the latest one before Jakarta EE 9).
- Choose a Tomcat version before Tomcat 10.
- Check the "Struts 2" checkbox in the "Additional Libraries and Frameworks".
- Use downloaded Struts 2 libraries, or manually specify the location of the libraries of Struts 2.
- Name your project and specify the project location.
- Click "Finish".
- Then, IntelliJ IDEA will load the project. At the "Project" sidebar close to the top left corner, 

## After the Creation

Follow the official guide. If the IDE prompts that newer versions of dependencies can be used, you may update them by operating in the IDE.

Maven depends the pom.xml to correctly manage the dependencies demanded. Though the IDE has generated a pom.xml file, it is not close to perfect. You can attempt to modify it. For example, use properties (variables) more frequently. See [POM Reference](https://maven.apache.org/pom.html).

## Eliminating the Errors Reported by the IDE

In the "web.xml", replace the line

```xml
<filter-class>org.apache.struts2.dispatcher.ng.filter.StrutsPrepareAndExecuteFilter</filter-class>
```

to

```xml
<filter-class>org.apache.struts2.dispatcher.filter.StrutsPrepareAndExecuteFilter</filter-class>
```

The upper one doesn't exist in Struts 2.5.x. As from Struts 2.5 all filters were moved to top package.

## Edit Configurations for Debugging and Running

On the top right corner of the IDE, enter "Edit Configurations...".

Create a new config, select the proper version of Tomcat (in this example, 9.0.55). 

Choose any one browser you want to launch for this project.

In the open window, the URL should match the official guide:

> http://localhost:8080/basic-struts/index.jsp

In the "Deployment" tab, select an artifact following the prompts of the IDE.

Then, build and run this application.

# Hello World Using Struts 2

