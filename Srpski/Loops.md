## LOOPS или ПЕТЉЕ - WHILE / FOR


У овој лекцији ћемо научити како да мењамо вредности у меморијским кутијицама, а коришћењем петљи односно Loops.

Петља омогућава понављање неког исказа или групе исказа. 


**Пример:** Овај пример ће нам помоћи да разумемо како функционишу петље:


Уколико бисмо мењали вредност која се налази унутар меморијске кутијице, предходна вредност која је била унутар меморијске кутијице би се избрисала. To ћемо приказати на следећим примерима. Притом треба нагласити да може постојати само једна вредност унутар једне меморијске кутијице: 


```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {
		
		int lala2 = 5; //creating box in memory (informal) ---initialization and assigment
		lala2 = 7; //updating the value inside the box in memory (informal)--assingment dodeljujemo vrednost
		lala2 = 100; //updating the value inside the box in memory (informal)--assingment dodeljujemo vrednost
		
		
		boolean mek = true;
		mek = false;
		mek = true;
		mek = true;
	}
}
```


Ако у меморији програма имамо низ неких података, на пример низ имена на одређеним позицијама, као што је приказано у следећем примеру: 

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

..а желимо да нам програм сам исписује те низове, онда уводимо нову синтаксу, а то је 'counter' или бројач који ће олакшати процес понављања неке операције. Објаснићемо га у следећем примеру где је 'i' бројач или counter и овај пример ће нам уједно приказати примену  два типа варијабли, Integer и Boolean.


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

		int i = 0; // што значи да је кутијица у меморији, назив те кутијице у меморији је 'i' , тип кутијице је целовити број, односно integer, и има вредност 0 
		
		while (i < 4) { // док је 'i' мање од  4, одради све што је између заграда { }
			
			System.out.println(people[i]); // испиши елемент из низа 'people' na poziciji 'i'			
			i = i + 1; //EQUIVALENT TO : i++;
		}
	}
}
```

			
Ово значи да је у кутијици 'i' вредност 0: **int i = 0;**. Међутим, поставили смо услов да је 'i' мање од 4: **while (i < 4)**. 


i = i + 1; ово се чита с десна на лево, а преведено значи резултат **i + 1;** пребаци у кутијицу **'i'**

Кад се ова операција примени у систему петље, односно понављања, програм ће се овако понашати:

1. Ако је вредност кутијице 0, програм поставља питање на основу услова, да ли је 0 < 4. С обзиром да је то истинита тврдња, он ће иштампати вредност под редним бројем 0. Ми смо предходно одредили да 'people' на индексу од 0, или под редним бројем 0, има вредност 'Valentina' и то је оно што ће програм штампати.

2. Затим петља прелази на следећу вредност у низу, с тим што се предходна вредност кутијице 0 брише и сада је ту нова вредност због услова који смо написали у програму **while (i < 4)**, а то је вредност 1.

3. Ако је вредност кутијице 1, програм поставља питање на основу услова да ли је 1 < 4. С обзиром да је то истинита тврдња, програм ће иштампати вредност из низа 'people' на позицији 1. Ми смо предходно одредили  да 'people' на индексу од 1, или позицији 1, има вредност 'Marija' и то је оно што ће програм штампати.

4. Ако је вредност кутијице 2, програм поставља питање на основу услова да ли је 2 < 4. С обзиром да је то истинита тврдња, програм ће иштампати 'people' на позицији 2. Ми смо предходно одредили  да 'people' на индексу од 2, или позицији 2, има вредност 'Marko' и то је оно што ће програм штампати.

Програм ће понављати ову радњу све док се не појави следећа ситуација:

5. Ако је вредност кутијице 4, програм поставља питање на основу услова да ли је 4 < 4. С обзиром да је то нетачна тврдња, ту се петља завршава. 

Ово укратко значи да је нама програм исписао имена људи које смо одредили да буду у низу до броја 4. 



Имамо још једну синтаксу која има идентичну функционалност али другачје изгледа: 


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

		for (int j = 0; j < 4; j++) {
			System.out.println(people[j]); // ispisi element iz niza na poziciji ј 
			j = j + 1;
		}
	}
}
```


Ово укратко значи:
- да ј има вредност 0.
- Изврши команде унутар тела петље.
- Увећај бројач за један (ј++). 
- Ово радити све док је 1<4.
				
===========================================================================
