## Introduction in JAVA programming<h2>

**To whom the tutorial is dedicated?**

Tutorial is dedicated to all begginers, as well as to those who has some experience in programming.


**What is necessary to have?**

At the beginning, you need to have installed programs Java JDK and Eclipse as well as Git Hub Desktop (Particular chapter is dedicated to installation of programs). This means that we will use JDK (Java Development Toolkit) and some of IDE (Integrated Development Environment) tools, as it is Eclipse program. 

**What is actually Java and what Eclipse program?**

**Java** – Java is an independent platform program. This means that, when we once make our program in Java, we can apply and activate it using many different platforms. 

**Eclipse** - It is integrated Development Environment (IDE), written in Java. It can be also used for implementation of applications in other programming languages.

## How to create a new program in Java?  <h2> 

We will create simple program, which will have the task to show at the screen text “Hello World”

1. Click on ** File** -> choose *New*, then click on -> **Java project**

![screenshot of github desktop](/slike/eklips3.png)

2. After this command, it will shows up a window in which we enter the name of a new project (in this case ‘Test project 2’ )  -> **Finish**

![screenshot of github desktop](/slike/eklips4.png)

3. In Eclipse, now it will show up a folder, which we’ve made with a name which we choose for project.   
  
![screenshot of github desktop](/slike/eklips10.png) 
 
![screenshot of github desktop](/slike/3a.png)

4. Double click on **TestProject2** and the new fields will open within project

*Note:* **‘src’**-source represents file within project for storing programming codes. 

5. Right click on **‘src’** -> **New** -> **Class** 
 
![screenshot of github desktop](/slike/eklips5.png)

6. After this, it will open the window for defining the class. We should put the name – “Main” and tick the field **‘public static void main’**

 ![screenshot of github desktop](/slike/eklips11.png)

7. From this moment, the program generated commands and it applied at the page of Eclipse program.
 
![screenshot of github desktop](/slike/eklips01.JPG)

*Note:* Numbers of program lines are part of a program, we are not writing them, but they are there for making program more readable. Program represents set of instructions, which we want to be executed.

Line 3: **public class** -> Each file in Java program, which we make, is labeled with “class”, which means that each line of code needs to be within that class. 
In this case, we give the name for this class “Main”.  By convention, names of classes are usually written with first capital letter. У овом случају ми смо ‘class’ или класу именовали као Main. 

Line 5: **public static void main (String[] args)** ->  This command is the first and main method which program will execute. Class can have many methods. We can say that a method represents a set of statements in program which are grouped to execute some operation. 

**public** - Represents that everyone can access  
	
**static** -  
	
**void** -  
	
**main:** -  Name of a method

In Java, each application has “start position” and that is a method ‘main’. This means that each Java program starts with this main method.

*Note:* Name of a class should be written by first capital letter (here example: “Main”), but the name of a method with small letters (here example: “main”). 

**Which method prints a text in Java program?** →System.out.println()

Line 6: System.out.println (“Hello World!”); 

1. File → Save → and then click **Run main** 

![screenshot of github desktop](/slike/eklipse9.png) 
 
*Note* - System.out.println** → method which prints a line in the screen. In this case it will be written “Hello World”.

**What did we create by this?**

We have created a class, which has Main method. In this program, Main method contains command System.out.println. This command prints, at the screen, string or array of characters which we put within quotation marks. 

*Note:* In Java, each command must have this sign (semicolon) -> ; <- in the end. 

![screenshot of github desktop](/slike/4a.png)
 
Curly brackets {} -> in a program, they are used to divide classes, methods or other structures.

