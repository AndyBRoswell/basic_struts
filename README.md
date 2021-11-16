# basic_struts

This Repository Is a Simple Demo of Struts 2.5.26 with Tomcat 9.0.54 and Maven.

## Notes

Now Java Web framework Struts 2 is NOT frequently used. It is certainly not recommend to create new Struts 2 projects unless you're required to maintain old projects or merely cope with exams.

## Essential statements

This repo is constructed in accordance of the official guide [Getting Started](https://struts.apache.org/getting-started/) and you should use IntelliJ IDEA to make use of the repo.

This README file is an auxiliary doc of the official guide, aiming at having you create a simple Struts 2 project and learn the fundamentals of Struts 2, avoiding twists and turns.

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

because Tomcat 10 uses Servlet 5.0 API, part of Jakarta EE 9. Hence, the highest version of Tomcat you can use is 9.0.55 up to when this README was created.