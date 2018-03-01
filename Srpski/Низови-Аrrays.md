## ARRAYS ИЛИ НИЗОВИ


У овој лекцији ћемо научити како на најлакши начин исписати низове неких података. Користићемо сложени тип варијабле - Arrays или низове.
Низ је колекција променљивих истог типа и у примерима ће бити приказани низови за сваки тип варијабле посебно.

Када је потребно чувати списак вредности, као што су на пример бројеви, можемо их ускладиштити у низу, уместо да уписујемо одвојене варијабле за сваки број као што ће бити приказано у првом примеру.


**Пример 1:** Написати банковни рачун корисника са подацима о имену, полу, стању рачуна и податцима да ли је корисник подигао кредит. 

Овако би изгледало појединачно писање података, односно писање одвојених варијабли за сваки String или низ карактера:


```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {

		String person0 = "Valentina" ;
		String person1 = "Marija" ;
		String person2 = "Marko" ;
		String person3 = "Djordje";
		//etc.
	}
}
```

У меморији, физички ти низови, односно подаци се налазе једно поред другог као што је приказано на слици и чини једну целину: 

СЛИКА

Предходни пример писања низова је практично исти као и следећи који ћемо написати, међутим у програмирању имамо синтаксу за писање низова који је ефикаснији што се тиче меморије програма. Конкретно, у следећем примеру ћемо писати списак од четворо људи, а користићемо варијаблу која означава низ карактера,а то је *String*: 


**Пример 2:** Написати низ који ће садржати списак људи који имају рачун у банци, користећи тип која означава низ карактера, а то је *String*:


```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {

//Array of strings (name of people who have bank account)

		String[] people = new String[4]; // array of string containing space for 4 strings
		people[0] = "Valentina";
		people[1] = "Marija";
		people[2] = "Marko";
		people[3] = "Djordje";
	}
}
```


*Напомена:* String[] people = new String[4]; - што би значило 'направи нови низ карактера и нека њихова дужина буде 4'

*Напомена:* String[] - ове заграде значе array of strings - низови карактера или стрингова. Исто тако уколико бисмо имали низ од целовитих бројева, синтакса би изгледала овако -> int[] num;

У низу, елементи низа су поређани и сваки има специфичну и константну позицију, која се зове индекс. Индекс позиције сваког елемента низа се налази унутар угластих заграда. 


**Пример 3:** Написати низ података који одређује стање на рачуну - *Balances*. За ове податке ћемо користити тип варијабле која одређује децималне бројеве, а то је *Double*.


```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {

//Array of doubles (the bank accounts balance of those people)

		double[] balances = new double[4];
		balances[0] = 400.23;
		balances[1] = 800.24;
		balances[2] = 950.324;
		balances[3] = 28300.23;
	}
}
```


*Напомена:* Позиције података у оквиру индекса почињу од 0. Такво је правило у Јава програму док се у неким другим програмима почиње од 1. 

*Напомена:* Називе варијабли код низова - 'Arrays' пишемо у множини : balances, haveLoans, genders, accountIds... 


**Пример 4:** Написати низ којим ћемо приказати да ли корисници имају отворен кредит - *haveLoans*. За ову операцију ћемо користити тип варијабле која има две вредности, тачно или нетачно а то је Boolean тип.


```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {

//Array of boolean values ()

		boolean[] haveLoans = new boolean[4];
		haveLoans[0] = true;
		haveLoans[1] = true;
		haveLoans[2] = false;
		haveLoans[3] = true;
	}
}
```


*Напомена:* Називи Boolean варијабли, почињу са have, has, is итд. 


**Пример 5:** Написати низ којим ћемо представити број рачуна. Пошто су у питању цели бројеви, користићемо варијабле типа *Integer*


```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {

//Array of integers

		int[] accountIds = new int[4];
		accountIds[0] = 10001;
		accountIds[1] = 10002;
		accountIds[2] = 10003;
		accountIds[3] = 10004;
	}
}
```


**Пример:** Написати низ којим ћемо представити пол корисника. Користићемо тип варијабле за карактере, а то је *Character*


```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {

//Array of characters

		char[]genders = new char[4];
		genders[0] = 'F';
		genders[1] = 'F';
		genders[2] = 'M';
	}
}
```		

=======

