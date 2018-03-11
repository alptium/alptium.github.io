## Искази кондиционала - IF / ELSE и Boolean логика
		

Ова лекција ће показати практично основу целог програмирања. Сваки задатак у оквиру програма се базира на исказима кондиционала IF / ELSE и упоредним операцијама односно Boolean логици.

На почетку ћемо приказати операције који се користе за формирање услова у задацима.
		 
			
		**Comparison operators - Упоредне операције**


**<**	Less than - Мање од

**<=**	Les than or equal to - Мање или једнако

**>**	Greater than - Веће од 

**>=**	Greater than of equal to - Веће или једнако

			
		**Equality operators - Операције једнакости**
	
	
**==**	equal to - Једнако

**!=**	not equal to - Није једнако

			
		**Boolean operations - Boolean операције**


**&&**	"AND" - и

**||**	"OR" - или

**!**	"NOT" - негација


					
Задатак је да направимо банкарски програм са следећим условима, који ће бити приказани у оквиру типова:		
	
	
		double salary = 200.34;
		char gender = 'F';
		int age = 18;
		boolean isEmloyed = true;
		boolean isChild = true;
		


**Задатак 1:** Направити банкарски програм који одређује услов да клијент има примања до одређене вредности и уколико се испуњава тај услов, кредит се може одобрити. 



```
package conditionals;

public class Main {

	public static void main(String[] args) {
		
		//symple: only salary is condition
		
		if (salary > 300.56) { // vece od / greater than
			System.out.println("Your loan has been approved");
		}else {
			System.out.println("Your loan has been declined / rejected");
		}
	}
}
```


Овај услов значи да ако је зарада корисника већа од 300.56, програм ће исписати да је кредит дозвољен или да кредит није дозвољен. С обзиром да наш корисник има зараду од 200.34 еура, а услов је да ће кредит бити дозвољен уколико је зарада већа од 300.56, програм ће исписати да кредит није дозвољен -> 'Your loan has been declined / rejected'. 

На овом примеру се примећује практична примена Boolean логике, када на основу почетне ситуације и услова који се поставе, програм одређује да ли је нешто тачно или нетачно, односно да ли је или није изводљива нека акција.



**Задатак 2:** Направити банкарски програм који одређује услов да клијент има примања до одређене вредности и (&&) услов да је клијент женског пола. 



```
package conditionals;

public class Main {

	public static void main(String[] args) {
		
		// Complex: must have both salary "AND" be female
		
		if(salary > 300.56 && gender == 'F') {
			System.out.println("Your loan has been approved");
		}else 
			System.out.println("Your loan has been declined / rejected");
		}
	}
}
```



Овај услов значи да ако је зарада корисника већа од 300.56 и (&&) ако је корисник женског пола, програм ће исписати да је кредит дозвољен или да кредит није дозвољен. С обзиром да наш корисник има зараду од 200.34 еура (мање од услова) и да је женског пола, а услов је да ће кредит бити дозвољен уколико је зарада већа од 300.56 и (&&) да је женског пола, програм ће исписати да кредит није дозвољен -> 'Your loan has been declined / rejected'. Код  && услова, и једна и друга вредност морају бити истините да би се услов испунио.


		
**Задатак 3:** Направити банкарски програм који одређује услов да клијент има минимум примања одређене вредности или (||) 18 година. 



```
package conditionals;

public class Main {

	public static void main(String[] args) {		
		
		// comlex: if either the person has minimun required salary, OR age is 18

		if(salary > 300.56 || age == 18) {
			System.out.println("Your loan has been approved");
		}else 
			System.out.println("Your loan has been declined / rejected");
		}
	}
}
```



Овај услов значи да ако је зарада корисника већа од 300.56 или (||) корисник има 18 година, програм ће исписати да је кредит дозвољен или да кредит није дозвољен. С обзиром да наш корисник има зараду од 200.34 еура, што је мање од услова, али испуњава други услов а то је да има 18 година, програм ће исписати да је кредит дозвољен -> 'Your loan has been approved'. Код || услова, једна од вредности мора бити истинита да би се услов испунио.


		
**Задатак 4:** Направити банкарски програм који одређује услов да клијент има минимум примања одређене вредности или (||) има 18 година или више од 18 година.		



```
package conditionals;

public class Main {

	public static void main(String[] args) {		
		
		// comlex: if either the person has minimun required salary, OR age is greater than or equal 18
		
		if(salary > 300.56 || age >= 18) {
			System.out.println("Your loan has been approved");
		}else 
			System.out.println("Your loan has been declined / rejected");
		}
	}
}
```



Овај услов значи да ако је зарада корисника већа од 300.56 или (||) корисник има 18 или више година, програм ће исписати да је кредит дозвољен или да кредит није дозвољен. С обзиром да наш корисник има зараду од 200.34 еура, што је мање од услова, али испуњава други услов а то је да има 18 или више година, програм ће исписати да је кредит дозвољен -> 'Your loan has been approved'.



**Задатак 5:** Направити банкарски програм који одређује услов да клијент има минимум примања одређене вредности или (||) има преко 18 година.



```
package conditionals;

public class Main {

	public static void main(String[] args) {
		
		// comlex: if either the person has minimun required salary, OR age is (strictly) greater than 18
		
		if(salary > 300.56 || age > 18) {
			System.out.println("Your loan has been approved");
		}else 
			System.out.println("Your loan has been declined / rejected");
		}
	}
}
```



Овај услов значи да ако је зарада корисника већа од 300.56 или (||) корисник има  више од 18 година, програм ће исписати да је кредит дозвољен или да кредит није дозвољен. С обзиром да наш корисник има зараду од 200.34 еура, што је мање од услова, и не испуњава други услов а то је да има више од 18 година, програм ће исписати да је кредит није дозвољен -> 'Your loan has been declined / rejected'.

		
**Задатак 6:** Направити банкарски програм који одређује услов да клијент има минимум примања одређене вредности и (&&) да је клијент запослен.



```
package conditionals;

public class Main {

	public static void main(String[] args) {
		
		// comlex: if either the person has minimun required salary, AND person is emloyed
		
		if(salary > 300.56 && isEmployed) {
			System.out.println("Your loan has been approved");
		}else 
			System.out.println("Your loan has been declined / rejected");
		}
	}
}
```



Овај услов значи да ако је зарада корисника већа од 300.56 и (&&) да је корисник запослен, програм ће исписати да је кредит дозвољен или да кредит није дозвољен. С обзиром да наш корисник има зараду од 200.34 еура, што је мање од услова, а други услов испуњава а то је да је корисник запослен, програм ће исписати да кредит није дозвољен јер се не испуњавају оба услова-> 'Your loan has been declined / rejected'.


**Задатак 7:** Направити банкарски програм који одређује услов да клијент има минимум примања одређене вредности и (&&) да клијент није дете.		



```
package conditionals;

public class Main {

	public static void main(String[] args) {

		// comlex: if either the person has minimun required salary, AND person is "NOT" a child
		
		if(salary > 300.56 && !isChild) {
			System.out.println("Your loan has been approved");
		}else 
			System.out.println("Your loan has been declined / rejected");
		}
	}
}
```



Овај услов значи да ако је зарада корисника већа од 300.56 и (&&) да корисник није дете, програм ће исписати да је кредит дозвољен или да кредит није дозвољен. С обзиром да наш корисник има зараду од 200.34 еура, што је мање од услова, а други услов испуњава а то је да корисник није дете, програм ће исписати да кредит није дозвољен јер се не испуњавају оба услова-> 'Your loan has been declined / rejected'.


**Задатак 8:** У овом задатку смо поставили почетну ситуацију да корисник има приступ интернету, има електронски уређај и да има 10 година. Међутим услови нашег програма одређују да профил на друштвеној мрежи може имати особа која има приступ интернету, има електронски уређај и има најмање 12 година.



```
package conditionals;

public class Main {

	public static void main(String[] args) {
	
		// account manager for Facebook, who makes accounts for people on Facebook
		
		// conditions - person must have acess to internet , must have electronic device, at least 12 years old
		// has internet access AND has electronic device, AND is at least 12

		boolean hasInternetAccess = true;
		boolean hasElectronicDevice = true;
		int age2 = 10;
		
		System.out.println();
		System.out.println();
		System.out.println();
		
		if(hasInternetAccess && hasElectronicDevice && age2 >= 12) {
			System.out.println("Your account has been created");
		}else 
			System.out.println("Your account has not been created");
		}
	}
}
```



С обзиром да корисник не испуњава један од три услова, програм ће одредити да корисник не може отворити профил на друштвеној мрежи. 


========================================================================
