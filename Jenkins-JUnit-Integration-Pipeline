# integratejunitwithjenkinsexp13
# Experiment 13: Integrating JUnit with Jenkins

## Objective
To integrate JUnit test cases with Jenkins and execute them automatically as part of CI (Continuous Integration) pipeline and view test reports.

---

## Prerequisites
- Java JDK 17 installed
- Maven installed
- Jenkins installed and running
- Git installed
- Basic knowledge of Maven and JUnit

---

## Project Structure

---

## Step 1: Create Maven Project

```bash
mvn archetype:generate
Enter:

groupId: com.bnmit
artifactId: jenkins-junit-demo
version: 1.0-SNAPSHOT
cd jenkins-junit-demo
Step 2: Create Java Source File
mkdir -p src/main/java/com/bnmit
notepad.exe src/main/java/com/bnmit/Calculator.java



package com.bnmit;

public class Calculator {

    public int add(int a, int b) {
        return a + b;
    }

    public int multiply(int a, int b) {
        return a * b;
    }
}

Step 3: Create JUnit Test File
mkdir -p src/test/java/com/bnmit
notepad.exe src/test/java/com/bnmit/CalculatorTest.java
CalculatorTest.java


package com.bnmit;

import static org.junit.jupiter.api.Assertions.*;
import org.junit.jupiter.api.Test;

public class CalculatorTest {

    Calculator calc = new Calculator();

    @Test
    public void testAdd() {
        assertEquals(5, calc.add(2, 3));
    }

    @Test
    public void testMultiply() {
        assertEquals(6, calc.multiply(2, 3));
    }
}


Step 4: Configure pom.xml
notepad.exe pom.xml
pom.xml



<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0
         http://maven.apache.org/xsd/maven-4.0.0.xsd">

    <modelVersion>4.0.0</modelVersion>

    <groupId>com.bnmit</groupId>
    <artifactId>jenkins-junit-demo</artifactId>
    <version>1.0-SNAPSHOT</version>

    <properties>
        <maven.compiler.source>17</maven.compiler.source>
        <maven.compiler.target>17</maven.compiler.target>
    </properties>

    <dependencies>

        <!-- JUnit 5 -->
        <dependency>
            <groupId>org.junit.jupiter</groupId>
            <artifactId>junit-jupiter-api</artifactId>
            <version>5.9.3</version>
            <scope>test</scope>
        </dependency>

        <dependency>
            <groupId>org.junit.jupiter</groupId>
            <artifactId>junit-jupiter-engine</artifactId>
            <version>5.9.3</version>
            <scope>test</scope>
        </dependency>

    </dependencies>

    <build>
        <plugins>

            <!-- Maven Compiler Plugin -->
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>3.11.0</version>
            </plugin>

            <!-- Maven Surefire Plugin (JUnit Execution) -->
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-surefire-plugin</artifactId>
                <version>3.0.0</version>
            </plugin>

        </plugins>
    </build>

</project>






STEP 5: RUN TESTS LOCALLY
mvn clean test
STEP 6: JENKINS CONFIGURATION
1. Install Plugins:
   - Maven Integration Plugin
   - JUnit Plugin

2. Create New Job:
   - Freestyle Project

3. Git Repo:
   - Add repository URL

4. Build Step:
   Goals:
   clean test
STEP 7: POST BUILD ACTION
Publish JUnit test result report
Path:
target/surefire-reports/*.xml

STEP 8: RUN IN JENKINS
Click: Build Now

STEP 9: VIEW REPORT
Project → Build → Test Result

You will see:

Passed tests
Failed tests
Execution details



