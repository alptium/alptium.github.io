## ARRAYS ИЛИ НИЗОВИ


У овој лекцији ћемо научити како на најлакши начин исписати низове неких података. Користићемо сложени тип варијабле - Arrays или низове.

Задатак: Написати банковни рачун корисника са подацима о имену, полу, стању рачуна и податцима да ли је корисник подигао кредит. 
  
Ако имамо задатак да напишемо списак неких података, на пример списак људи, да не бисмо писали хиљаде неких линија када пишемо листе, онда ћемо користити код за низове односно Arrays.

Овако би изгледало појединачно писање података:

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

У меморији, физички ти низови, односно подаци се налазе једно поред другог као што је приказано на слици: 

СЛИКА

Предходни пример писања низова је практично исти као и следећи који ћемо написати, међутим у програмирању имамо код за писање низова који је ефикаснији што се тиче меморије програма. Конкретно, у следећем примеру ћемо писати списак од четворо људи, а користићемо варијаблу која означава низ карактера,а то је *String*: 



**Пример:** Написати низ који ће садржати списак људи који имају рачун у банци, користићи варијаблу која означава низ карактера, а то је *String*: :

```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {

//Array of strings (name of people who have bank account)

		String[] people = new String[4]; // array of string containing space for 4 strings
		people[0] = "Iva";
		people[1] = "Marija";
		people[2] = "Marko";
		people[3] = "Djordje";
	}
}
```

*Напомена:* String[] people = new String[4]; - што би значило 'направи нови низ стингова и нека његова дужина буде 4'

*Напомена:* String[] - ове заграде значе array of strings - низови стрингова

И сада имамо четири низа, односно кутијице са подацима о именима коеисника.


**Пример:** Написати низ података који одређује стање на рачуну, односно на енглеском језику - *Balances*. За ове податке ћемо користити варијаблу која одређује децималне бројеве, а то је *Double*. 

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

*Напомена:* Набрајање од 0 почиње јер је уведено тако као правило. У неким другим програмима се почиње од 1. 

*Напомена:* Називе ваијабли код низова - 'Arrays' пишемо у множини : balances, haveLoans, genders, accountIds... 


**Пример:** Написати низ којим ћемо приказати да ли корисници имају подигнут кредит или не - *haveLoans*. За ову операцију ћемо користити варијаблу која има две вредности, тачно или нетачно, а то је Boolean тип.

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

*Напомена:* Boolean тип варијабле, односно имена кутијица почињу са have, has, is итд. 


**Пример:** Написати низ којим ћемо представити број рачуна. Пошто су у питању цели бројеви, користићемо варијабле типа *Integer*

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


**Пример:** Написати низ којим ћемо представити пол корисника. Користићемо варијаблу за карактере, а то је *Character*

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
