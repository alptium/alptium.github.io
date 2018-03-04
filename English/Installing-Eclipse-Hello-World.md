## Starting "Hello world" in Eclipsе program and creating variables <h2>

**Which method prints in Јава program?** →System.out.println()

System .out.println (“Hello World!”); 

1. **File** → **Save** → and a step to start by clicking on **Run main** 

![screenshot of github desktop](/slike/eklipse9.png) 
 
*Note:* 

**System.out.println** → the method prints the line of text on the screen, in this case the text line is ‘Hello World!”;

**;** → In Java, each command must end with this sign.

![screenshot of github desktop](/slike/4a.png)
 
Computer memory can be explained on the case of boxes. It consists of boxes that have their own names, and within each box there is some content:

![screenshot of github desktop](/slike/tip1.png) 

![screenshot of github desktop](/slike/tip2.png) 

In order to process the data, it is necessary to store them somehow. Storage is done in variables or variables that are defined in Java in the beginning. Therefore, most programming languages have multiple types of information that are entered into variables. We can split them into simple or primitive types and complex or complex types.
Examples of simple or primitive types are:

**Int** – **Intеger** = A variable type that prints whole numbers.

**Double** – **Double precision floating number** = A variable type that prints decimal numbers.

**Char** - **Character** = A variable type that prints a single character, sign, or symbol.

**Bool** – **Boolean** = A variable type that can have only two values, true or false, or rather True или False.

An example of a complex type is:

**String** - a complex complex type consisting of multiple characters.


**Example:** the task is to create a variable * type *intiger (int)* under the name **ab** that will contain a value of "14". The command to do this would look like this.

```
                int ab = 14;
		int lala = 150;
		int zebra = 234;
		int luk = 45;
```

**Example:** the task is to create a variable *character ( char )* under the name **jkl** that will contain a character  ‘a’.

```
                char jkl = 'a' ;
		char gh = '8' ;
		char sfgs = '$' ;
```
 
*Note:* characters are always recorded with the alleged characters **‘** → ’character’

**Example:** the task is to create a variable type *boolean (bool)* under the name **yt** that will contain a value True.
 
```
                boolean yt = true;
		boolean lop = false;
		boolean df = true;
```

*Note:* Boolean a type can only contain two values, either True or False.

**Example:** the task is to create a variable type *double* under the name **ujl** that will contain a decimal number 45,89.

```
                double ujl = 45.89;
		double er = 786579.982;
		double vb = 0.06864;
``` 

*Note:* decimal numbers are separated by a dot in Java instead of a comma.


So far, these have been examples of simple types. The next type is complex, it consists of more than one character.

**Example** complex type of variable *String*  under the name **jds** which contains characters “Marija Marjanovic”

```
                String jds = "Marija Marjanovic";
		String ywe = "Ulica 5, Beograd";
		String ulo = "Fly to the moon";
``` 

*Note:* the content of this type is always written with double allegations **“**.








**How to make a new project?**


We will create a simple program that will show us on the screen „Hello World!”

Click on **File** -> choose **New**, then click on -> **Java project**

 ![screenshot of github desktop](/slike/eklips3.png)

After this command, a window will appear in which the name of the new project is entered (in these case ‘Test project 2’ ) and -> Finish

![screenshot of github desktop](/slike/eklips4.png)

In the Eclipse program, the folder that we created with the name we selected for the project is displayed.
     
![screenshot of github desktop](/slike/eklips10.png) 
 
![screenshot of github desktop](/slike/3a.png)

Next step is :

Double click on **TestProject2**  when new fields are opened in the folder.

Note: **‘src’**-source represents a file within a program for storing program codes. 

Right click on **‘src’** -> **New** -> **Class** 
 
![screenshot of github desktop](/slike/eklips5.png)

After this step, a window that we name **‘Main’** is opened and we mark the box under the name **‘public static void main’**

 ![screenshot of github desktop](/slike/eklips11.png)

At this point, the program has generated the assigned commands and applied them to the initial (work) page of the Eclipse program.
 
![screenshot of github desktop](/slike/eklips12.png)

Note: 

**public class** = every file in Јava program is marked with ‘class’ , which means that each line of the running code should be within the ( ‘class’) class. In this case, we named the 'class' as Main
 
**public static void main (String[] args)** -> This tells the program that this is the first method that the program will execute. The program is a list of instructions that we want to execute.

In Java, each application has a starting point (input point), which is a method that is designated as 'main'. This means that each Java program starts with the main method.

**public:** anyone can access
	
**static:** Static means that the variable or method marked as such is available at the class level. The static keyword in java is used for memory management mainly. We can apply java static keyword with variables, methods, blocks and nested class. The static keyword belongs to the class than instance of the class.
	
**void:** The keyword void simply tells the compiler that main( ) does not return a value. *void* is the return type. It means "this method returns nothing"
	
**main:** Name of the method
