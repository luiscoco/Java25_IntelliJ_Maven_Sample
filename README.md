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

## 4. How to run the application

<img width="1918" height="1012" alt="image" src="https://github.com/user-attachments/assets/5ff983e0-b287-4efe-92c7-a5b59c3df7d1" />

