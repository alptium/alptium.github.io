## The difference between object-oriented programming and non-object-oriented programming

### Тhemes:
- Class
- Attributes
- Methods
- Objects

This lesson will explain object-oriented programming that talks about how the concept of one software is formed.

Object-oriented programming is not related to Java or any other program for programming, it is actually a style of thinking.

First, we will explain the concept of object-oriented programming.

In the example below, we have printed nouns, or examples of nouns:

- Nouns:

hospital

school

a teacher

doctor

patient

athletes

the student

credit

bookstore

a book

a table

lap top

clock

glass



Then we will print examples of some verbs:


- Verbs for the noun doctor, student:


doctor - asks questions, checks, writes diagnoses, writes therapy ...

student - learns, reads, drinks coffee

teacher - writes, lectures ..



How is all this connected?



Names are in the programming of classifications of something (class doctor, class student, class teacher ...). So they mean one class.


For the 'doctor' class we have information about specific doctors:

Dr Petar Petrovic

Dr Marija Marjanovic

Dr Jovan Jovanovic

...


For the class 'student' we have information about concrete students:

Jelena Jovanovic

Vasilija Vasiljević

...


How does this translate into programming?


Specific instances of certain classifications are the names that we have written and these are class objects. Object or instance are synonyms.
So, for the doctor class, the object is Dr. Petar Petrovic, for the student class, the object is Jelena Jovanovic etc.

Verbs determine some operations or actions, or what the object is doing.


Objects from the class doctor can do the following:


-View of the patient

- Diagnosis of the disease

-Treatment therapy, etc.


All these operations are called programming in the programming - **methods**.

The doctor is a **class**, Doctor Petar Petrovic is a **object**, and what the object does is a **method**.


What information do we have about a doctor?

-Ime (String)

-Prezime (String)

-Specialization (String)

-Date of birth (Integer)

-Full time employee (Boolean)


These examples are basically nouns, but they represent primitive nouns and they are called **attributes**. Attributes actually contain information about each object in the class. The bracket contains the attribute information type.

Ово све представља анализу софтвера. Одређујемо шта су класе, атрибути, методе.


Applied in writing code and programming these data will look like this, but one way to write code that is not object-oriented will be shown first:

Reminder how to write an array of names that has 3 elements in a row:

String names[] = new String[3];


```
package hospital;

public class Main {

	public static void main(String[] args) {
	
		System.out.println("Welcome to this hospital");
		
		/// Data types (String, int, double, boolean)
		
		// Doctor - 
		// Array of 3 elements: indexes can be only: 0, 1, 2
		
		String names[] = new String[3];
		String surnames[] = new String[3];
		int birthYears[] = new int[3];
		boolean areFulltimeEmployees[] = new boolean[3];
		
		names[0] = "Petar";
		names[1] = "Marija";
		names[2] = "Jovan";
		
		surnames[0] = "Petrovic";
		surnames[1] = "Marijanovic";
		surnames[2] = "Jovanovic";
		
		birthYears[0] = 1954;
		birthYears[1] = 1965;
		birthYears[2] = 1928;
		
		areFulltimeEmployees[0] = true;
		areFulltimeEmployees[1] = true;
		areFulltimeEmployees[2] = false;
		
		for(int i = 0; i < 3; i++)
		{
			System.out.println();
			System.out.println("Name: " + names[i]);
			System.out.println("Surname: " + surnames[i]);
			System.out.println("year of Birth: " + birthYears[i]);
			System.out.println("Are employed fulltime: " + areFulltimeEmployees[i]);
		}
		
	}

}
```


*Note* :

 System.out.println(); - the printed syntax in this way prints an empty line in the program.



![screenshot of github desktop](/slike1/28.JPG)



If we want Petar Petrović to write in the same place and to provide information about Petar in one place, then we will group them.

Let's open a new class we call a doctor and first define methods: all methods always begin with a verb

*Note:*void means that this method does not return any result, or some data, while return returns the result, that is, the data. Example:


```
public String getName() {
	return name;
}
```


This syntax returns the String, the next one written in the code also returns String, and the next returns int.

View the Doctor class in the code:


```
package hospital;

public class Doctor {
	
	// Atributes of the class Doctor
	
	private String name;
	private String surname;
	private int birthYear;
	private boolean isFulltimeEmployee;
	
	
	// Constructor for the class Doctor

	public Doctor(String name, String surname, int birthYear, boolean isFullTimeEmployee) {
		this.name = name;
		this.surname = surname;
		this.birthYear = birthYear;
		this.isFullTimeEmployee = isFullTimeEmployee;
	}
	
	// Methods of the class Doctor
	
	
	public String getName() {
		return name;
	}
	
	public String getSurname() {
		return surname;
	}
	
	public int getbirthYear() {
		return birthYear;
	}
	
	public boolean isFulltimeEmployee() {
		return isFulltimeEmployee;
	}
	
	public void examinePatient() {
		System.out.println("Examining patient..");
	}
	
	public void diagnoseIllnes() {
		System.out.println("Diagnosing illness...");	
	}
	public void prescribeTherapy() {
		System.out.println("Prescribing therapy...");
	}
}
```


Now we want to create specific doctors.

We have a class doctor and within that class the attributes. Every doctor who has an object has attributes (name, surname, date of birth ...) and we create those attributes in the code so that the information we are inserting about a particular doctor will be stored in this section of the code that is shown below:


```
// Atributes of the class Doctor
	
	private String name;
	private String surname;
	private int birthYear;
	private boolean isFulltimeEmployee;
```


*Note:* this.name - this in syntax means that the name that has been forwarded to a specific object, i.e. Doctor, to be saved.


This has not been object-oriented so far.

Now it will be explained how objects are created, but within object-oriented programming.

The point is that we simplify the writing of the code so that we grouped information about one doctor, not for each data that we enter the line into the code individually.

If the task is to create an array of three doctors, we need a syntax for that command, but for this, we will need complex types, because the following data we use and which we want to be grouped in one place cannot be embedded within a simple or primitive type.

Complex or composite types are

- String

- Date

- Doctor - is a complex type that we have invented because it contains several types of information in itself.

So we are writing an array of 3 doctors:
 
Doctor doctors[] = Doctor[3];
		
		doctor[0] = new Doctor("Petar", "Petrovic", 1954, true);
		doctor[1] = new Doctor("Marija", "Marijanovic", 1965, true);
		doctor[2] = new Doctor("Jovan", "Jovanovic", 1928, false);

Then we write a syntax with which the program will draw information about each doctor and print them:


```
for(int i = 0; i < 3; i++)
{
	Doctor doctor = doctors[i];

	System.out.println();
	System.out.println("Name: " + doctor.getName());
	System.out.println("Surname: " + doctor.getSurname());
	System.out.println("Year of Birth: " + doctor.getbirthYear());
	System.out.println("Are employed fulltime: " + doctor.isFulltimeEmployees());
```


*Note:* when we included the doctor in the program and the point -> [System.out.println("Name: " + doctor.getName());] Eclipse immediately recognized and offered the methods we defined ( getName, getSurname, getbirthYear, getisFulltimeEmployee )


And now we will notice that we have two programming modes:

One way of programming - runDemo 1:


```
// NON OBJECT-ORIENTED DOCTOR
	
	private static void runDemo1() {
		
		/// Data types (String, int, double, boolean)
		
		// Doctor - 
		// Array of 3 elements: indexes can be only: 0, 1, 2
		
		String names[] = new String[3];
		String surnames[] = new String[3];
		int birthYears[] = new int[3];
		boolean areFulltimeEmployees[] = new boolean[3];
		
		names[0] = "Petar";
		names[1] = "Marija";
		names[2] = "Jovan";
		
		surnames[0] = "Petrovic";
		surnames[1] = "Marijanovic";
		surnames[2] = "Jovanovic";
		
		birthYears[0] = 1954;
		birthYears[1] = 1965;
		birthYears[2] = 1928;
		
		areFulltimeEmployees[0] = true;
		areFulltimeEmployees[1] = true;
		areFulltimeEmployees[2] = false;
		
		for(int i = 0; i < 3; i++)
		{
			System.out.println();
			System.out.println("Name: " + names[i]);
			System.out.println("Surname: " + surnames[i]);
			System.out.println("year of Birth: " + birthYears[i]);
			System.out.println("Are employed fulltime: " + areFulltimeEmployees[i]);
		}	
	}
```


And second way of programming - runDemo 2:


```
private static void runDemo2() {
		
		Doctor doctors[] = new Doctor[3];
		
		doctors[0] = new Doctor("Petar", "Petrovic", 1954, true);
		doctors[1] = new Doctor("Marija", "Marijanovic", 1965, true);
		doctors[2] = new Doctor("Jovan", "Jovanovic", 1928, false);
		
		for(int i = 0; i < 3; i++)
		{
			Doctor doctor = doctors[i];
		
			System.out.println();
			System.out.println("Name: " + doctor.getName());
			System.out.println("Surname: " + doctor.getSurname());
			System.out.println("Year of Birth: " + doctor.getbirthYear());
			System.out.println("Are employed fulltime: " + doctor.isFulltimeEmployees());
```


runDemo1 and runDemo2 are the same as for behavior, but the programming mode is different.

The difference is in simplicity. The second way of programming is a simpler, shorter, different way of the data structure. It contains information about one particular doctor in one place, that is, the data is printed together, and in the other they are separated into sequences.

To easily compare both programming modes, the codes will be written in the following example in one place:


```
package hospital;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		System.out.println("Welcome to this hospital!");
		
		// Non Object Oriented Programming (non-OOP)
		runDemoNonOop1();
		runDemoNonOop2();

		// Object Oriented Programming (OOP)
		runDemoOop1();
		runDemoOop12(); // OOP with console reading in/out
		runDemoOop2();
	}
	
	private static void runDemoNonOop1() {
		System.out.println("Running Demo - Non Object Oriented - Single record...");
		
		String name = "Petar";
		String surname = "Petrovic";
		int birthYear = 1954;
		boolean isFullTimeEmployee = true;
		
		System.out.println("Name: " + name);
		System.out.println("Surname: " + surname);
		System.out.println("Year of Birth: " + birthYear);
		System.out.println("Is employed fulltime: " + isFullTimeEmployee);
	}
	
	private static void runDemoNonOop2() {
		System.out.println("Running Demo - Non Object Oriented - Multiple records...");
		
		String names[] = new String[3];
		String surnames[] = new String[3];
		int birthYears[] = new int[3];
		boolean areFulltimeEmployees[] = new boolean[3];
		
		names[0] = "Petar";
		names[1] = "Marija";
		names[2] = "Jovan";
		
		surnames[0] = "Petrovic";
		surnames[1] = "Marjanovic";
		surnames[2] = "Jovanovic";
		
		birthYears[0] = 1954;
		birthYears[1] = 1965;
		birthYears[2] = 1928;
		
		areFulltimeEmployees[0] = true;
		areFulltimeEmployees[1] = true;		
		areFulltimeEmployees[2] = false;
		
		for(int i = 0; i < 3; i++)
		{
			System.out.println("=============================================");
			System.out.println("Name: " + names[i]);
			System.out.println("Surname: " + surnames[i]);
			System.out.println("Year of Birth: " + birthYears[i]);
			System.out.println("Is employed fulltime: " + areFulltimeEmployees[i]);
			System.out.println("=============================================");
		}
	}
	
	private static void runDemoOop1() {
		System.out.println("Running Demo - Object Oriented - Single record...");
		
		Doctor doctor = new Doctor("Petar", "Petrovic", 1954, true);
		
		System.out.println("=============================================");
		System.out.println("Name: " + doctor.getName());
		System.out.println("Surname: " + doctor.getSurname());
		System.out.println("Year of Birth: " + doctor.getBirthYear());
		System.out.println("Is employed fulltime: " + doctor.isFullTimeEmployee());
		System.out.println("=============================================");
	}
	
	private static void runDemoOop12() {
		System.out.println("Running Demo - Object Oriented - Single record...");
		
		try(Scanner scanner = new Scanner(System.in)) {
			System.out.println("Enter the doctor name");
			String name = scanner.next();
			
			System.out.println("Enter the doctor surname");
			String surname = scanner.next();
			
			System.out.println("Enter the doctor birthyear");
			int birthYear = scanner.nextInt();
			
			System.out.println("Enter if the doctor is a full time employee (true/false)");
			boolean isFullTimeEmployee = scanner.nextBoolean();
			
			Doctor doctor = new Doctor(name, surname, birthYear, isFullTimeEmployee);
			
			System.out.println("=============================================");
			System.out.println("Name: " + doctor.getName());
			System.out.println("Surname: " + doctor.getSurname());
			System.out.println("Year of Birth: " + doctor.getBirthYear());
			System.out.println("Is employed fulltime: " + doctor.isFullTimeEmployee());
			System.out.println("=============================================");
		}
	}
	
	
	
	private static void runDemoOop2() {
		System.out.println("Running Demo - Object Oriented - Multiple records...");
		
		Doctor doctors[] = new Doctor[3];
		
		doctors[0] = new Doctor("Petar", "Petrovic", 1954, true);
		doctors[1] = new Doctor("Marija", "Marjanovic", 1965, true);
		doctors[2] = new Doctor("Jovan", "Jovanovic", 1928, false);
		
		for(int i = 0; i < 3; i++)
		{
			Doctor doctor = doctors[i];
			
			System.out.println("=============================================");
			System.out.println("Name: " + doctor.getName());
			System.out.println("Surname: " + doctor.getSurname());
			System.out.println("Year of Birth: " + doctor.getBirthYear());
			System.out.println("Is employed fulltime: " + doctor.isFullTimeEmployee());
			System.out.println("=============================================");
		}
	}
}
```

And the code for the class 'Doctor':


```
package hospital;

public class Doctor {
	
	// Attributes of the class Doctor
	
	private String name;
	private String surname;
	private int birthYear;
	private boolean isFullTimeEmployee;
	
	// Constructor for the class Doctor
	
	public Doctor(String name, String surname, int birthYear, boolean isFullTimeEmployee) {
		this.name = name;
		this.surname = surname;
		this.birthYear = birthYear;
		this.isFullTimeEmployee = isFullTimeEmployee;
	}

	// Methods of the class Doctor
	
	public String getName() {
		return name;
	}
	
	public String getSurname() {
		return surname;
	}
	
	public int getBirthYear() {
		return birthYear;
	}
	
	public boolean isFullTimeEmployee() {
		return isFullTimeEmployee;
	}
	
	public void examinePatient() {
		System.out.println("Examining patient...");
	}
	
	public void diagnoseIllness() {
		System.out.println("Diagnosing illness...");
	}
	
	public void prescribeTherapy() {
		System.out.println("Prescribing therapy...");
	}
}
```

========================================================================
