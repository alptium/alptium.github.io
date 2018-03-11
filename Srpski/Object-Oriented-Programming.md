## Разлике између објектно оријентисаног програмирања и програмирања које није објектно оријентисано

### Теме:
- Класе
- Атрибути
- Методе
- Објекти

У овој лекцији ће бити објашњено објектно оријентисано програмирање који говори о томе како се формира концепт једног софтвера.

Објектно оријентисаано програмирање није везано за Јаву или неки други програм за програмирање, оно заправо представља стил размишљања.

Прво ћемо објаснити концепт објектно оријентисаног програмирања.

У примеру испод имамо исписане именице, односно примере именица: 

- Именице:

болница

школа

наставник

лекар

пацијент

спортиста

студент

кредит

књижара

књига

сто 

лаптоп

чаша


Затим ћемо исписати примере неких глагола:

- Глаголи за именицу доктор, студент:

доктор - поставља питања, ради прегледе, пише дијагнозу, пише терапију...

студент - учи, чита, пије кафу..

наставник - пише, предаје..


Како је све ово повезано?


Именице су у програмирању класификација нечега (класа лекар, класа студент, класа наставник...). Значи оне означавају једну класу.

За класу 'лекар' имамо податке о конкретним лекарима:

Др Петар Петровић

Др Марија Марјановић

Др Јован Јовановић
...

За класу 'студент'имамо податке о конкретним студентима:

Јелена Јовановић

Василија Васиљевић
...

Како се ово преводи у програмирању?

Конкретне инстанце одређене класификације су имена која смо написали и то су објекти класе. Објект или инстанца су синоними.
Значи, за класу доктор, објекат је др Петар Петровић, за класу студент, објекат је Јелена Јовановић итд.

Глаголи одређују неке операције или радње, односно шта је то што објекат ради.

Објекти из класе лекар могу да раде следеће:

-Преглед пацијента

-Дијагностика обољења

-Препицивање терапије итд.

Све ове операције се у програмирању називају - **методе**.

Лекар је **класа**, доктор Петар петровић је **објекат**, а оно што објекат ради је **метода**.

Које све податке имамо о лекару?

-Име (String)

-Презиме (String)

-Специјализација (String)

-Датум рођења (Integer)

-Запослење на неодређен временски период (Boolean)

Ови примери су у основи именице, али представљају примитивне именице и њих називамо **атрибути**. Атрибути заправо садрже податке о сваком објекту из класе. У загради се налази тип података о атрибуту.

Ово све представља анализу софтвера. Одређујемо шта су класе, атрибути, методе.


Примењено у писању кода и програмирању ови подаци ће изгледати овако, али прво ће бити приказан један начин писања кода које није објектно оријентисано:

Подсетник како се пише низ имена који има 3 елемента у низу:

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


*Напомена*:

 System.out.println(); - овако исписана синтакса нам у програму исписује празну линију



![screenshot of github desktop](/slike1/28.JPG)



Ако желимо да на истом месту пише Петар Петровић и да на једном месту буду подаци о Петру онда ћемо те податке груписати.

Отворимо нову класу коју називамо лекар и прво дефинишемо методе: све методе увек почињу са глаголом

*Напомена:* void значи да та метода не враћа никакав резултат, односно неки податак, док return враћа резултат, односно податак. Пример:


```
public String getName() {
	return name;
}
```


Ова синтакса враћа String, следећа исписана у коду такође враћа String, а следећа враћа int.

Приказ класе Doctor у коду:


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


Сада хоћемо да креирамо конкретне лекаре.

Имамо класу доктор и унутар те класе атрибуте. Сваки доктор који је објекат има атрибуте (име, презиме, датум рођења...) и креирамо те атрибуте у коду тако да ће се информације које убацујемо о конкретном доктору, чувати у овом делу кода који је доле приказан:


```
// Atributes of the class Doctor
	
	private String name;
	private String surname;
	private int birthYear;
	private boolean isFulltimeEmployee;
```


*Напомена:* this.name - ово у синтакси значи да име које је прослеђено о конкретном објекту тј. доктору, да се сачува.


Oво до сада објашњено није било објектно оријентисано.

Сада ће бити објашњено како се креирају објекти, али у склопу објектно оријентисаног програмирања.
 
Поента је да се поједностави писање кода тако да имамо груписане информације о једном доктору, а не да за сваки податак пишемо линију у коду појединачно.

Ако је задатак да направимо низ од три доктора треба нам синтакса за ту команду, међутим за то ће нам бити потребни сложени типови, јер следећи подаци које ћемо користити, а желимо да буду груписани на једном месту, не могу се уградити у оквиру једноставних или примитивних типова. 

Сложени или композитни типови су:

- String

- Date

- Doctor - је сложени тип који смо ми измислили зато што садржи више типова информација у себи.

Значи испишемо низ од 3 доктора:
 
Doctor doctors[] = Doctor[3];
		
		doctor[0] = new Doctor("Petar", "Petrovic", 1954, true);
		doctor[1] = new Doctor("Marija", "Marijanovic", 1965, true);
		doctor[2] = new Doctor("Jovan", "Jovanovic", 1928, false);

Затим  пишемо синтаксу којом ће програм вући податке о сваком доктору и исписивати их:


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


*Напомена:* када смо у програму укуцали doctor па тачку -> [System.out.println("Name: " + doctor.getName());] Eclipse је одмах препознао и понудио методе које смо ми дефинисали ( getName, getSurname, getbirthYear, getisFulltimeEmployee )


И сада већ уочавамо да имамо два начина програмирања:

Један начин програмирања - runDemo 1:


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


И други начин програмирања - runDemo 2:


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


runDemo1 и runDemo2 су исти што се тиче понашања али је начин програмирања другачији.

Разлика је у једноставности. Други начин програмирања је једноставнији, краћи, другачији начин структуирања података. Он садржи податке о једном конкретном доктору на једном месту, односно подаци су заједно исписани, а у другом су одвојени у низовима.


Да лакше упоредите оба начина програмирања, кодови ће бити исписани у следећем примеру на једном месту:


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

И код за класу 'Doctor':


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
