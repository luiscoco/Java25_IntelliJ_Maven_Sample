# Java25_IntelliJ_Maven_Sample

## 1. Download and Install IntelliJ Community Edition

We navigate to the IntelliJ official web page and we download the Free Community Edition:

https://www.jetbrains.com/idea/download/

<img width="1918" height="807" alt="image" src="https://github.com/user-attachments/assets/fa521347-6cc2-42d4-a059-ff737eb166cf" />

## 2. We install the AI programmer agents (Copilot and Gemmini Code Assistant)

<img width="1023" height="449" alt="image" src="https://github.com/user-attachments/assets/8c1e46cc-22c9-4d89-94b2-ccfc6545b988" />

## 3. How to create your first Java Application with IntelliJ

We run IntelliJ and we select "New Project" option

<img width="1052" height="807" alt="image" src="https://github.com/user-attachments/assets/29501302-af69-45ff-8056-efa1bab83451" />

We input the project name and location

We select the Build System Maven and the JDK Oracle OpenJDK 25

<img width="980" height="897" alt="image" src="https://github.com/user-attachments/assets/81653802-d154-4f98-9494-bf70ba6fe748" />

We review the new project structure

<img width="444" height="541" alt="image" src="https://github.com/user-attachments/assets/1e6d5b86-86f9-4286-b097-29fea8b81c7c" />

We also review the **Main.java** file content:

```java
package org.example;

//TIP To <b>Run</b> code, press <shortcut actionId="Run"/> or
// click the <icon src="AllIcons.Actions.Execute"/> icon in the gutter.
public class Main {
    static void main() {
        //TIP Press <shortcut actionId="ShowIntentionActions"/> with your caret at the highlighted text
        // to see how IntelliJ IDEA suggests fixing it.
        IO.println("Hello and welcome!");

        for (int i = 1; i <= 5; i++) {
            //TIP Press <shortcut actionId="Debug"/> to start debugging your code. We have set one <icon src="AllIcons.Debugger.Db_set_breakpoint"/> breakpoint
            // for you, but you can always add more by pressing <shortcut actionId="ToggleLineBreakpoint"/>.
            IO.println("i = " + i);
        }
    }
}
```

Finally, we could review the **pom.xml** content:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>org.example</groupId>
    <artifactId>demo</artifactId>
    <version>1.0-SNAPSHOT</version>

    <properties>
        <maven.compiler.source>25</maven.compiler.source>
        <maven.compiler.target>25</maven.compiler.target>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    </properties>

</project>
```

## 4. How to run the application

<img width="1918" height="1012" alt="image" src="https://github.com/user-attachments/assets/5ff983e0-b287-4efe-92c7-a5b59c3df7d1" />

## 5.  How to run the application with Mave

We input this prompt in Gemini Code Assistant:

Prompt:

I would like to run the application with Maven

<img width="537" height="825" alt="image" src="https://github.com/user-attachments/assets/d77dc183-352d-42a4-afdc-9ab2b7e3301a" />

The AI programmer agent, Gemini Code Assistant, will introduce several changes in Main.java and in pom.xml files

We review the new Main.java and pom.xml files content:

**Main.java**

```java
package org.example;

//TIP To <b>Run</b> code, press <shortcut actionId="Run"/> or
// click the <icon src="AllIcons.Actions.Execute"/> icon in the gutter.
public class Main {
    static void main() {
        //TIP Press <shortcut actionId="ShowIntentionActions"/> with your caret at the highlighted text
        // to see how IntelliJ IDEA suggests fixing it.
        System.out.println("Hello and welcome!");

        for (int i = 1; i <= 5; i++) {
            //TIP Press <shortcut actionId="Debug"/> to start debugging your code. We have set one <icon src="AllIcons.Debugger.Db_set_breakpoint"/> breakpoint
            // for you, but you can always add more by pressing <shortcut actionId="ToggleLineBreakpoint"/>.
            System.out.println("i = " + i);
        }
    }
}
```

**pom.xml**

```
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>org.example</groupId>
    <artifactId>demo</artifactId>
    <version>1.0-SNAPSHOT</version>

    <properties>
        <maven.compiler.source>1.8</maven.compiler.source>
        <maven.compiler.target>1.8</maven.compiler.target>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    </properties>

    <build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-jar-plugin</artifactId>
                <version>3.4.1</version>
                <configuration>
                    <archive>
                        <manifest>
                            <mainClass>org.example.Main</mainClass>
                        </manifest>
                    </archive>
                </configuration>
            </plugin>
            <plugin>
                <groupId>org.codehaus.mojo</groupId>
                <artifactId>exec-maven-plugin</artifactId>
                <version>3.0.0</version>
                <configuration>
                    <mainClass>org.example.Main</mainClass>
                </configuration>
            </plugin>
        </plugins>
    </build>

</project>
```

Now we request to Gemini the maven command to run the application:

