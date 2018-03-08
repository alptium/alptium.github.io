## UML (Unified Modelling Language) - формирање дијаграма класа и видљивост метода (јавно/приватно)

Теме:

- Дијаграми класа и видљивост метода 

- Однос између класа коришћењем правих примера (Доктор, пацијент, Вакцинација, ПацијентВакцинација)

 

UML (Unified Modelling Language) је стандардни језик за спецификацију, визуализацију и документовање софтверског система. Стандардна интернационална нотација за објектно оријетисано моделовање система и друге дијаграме.

Како репрезентујемо класе кроз дијаграме?

| Doctor                         |
|--------------------------------|
| - name: String                 |
| - surname: String              |
| - yearOfBirth: int             |
| - isFullTimeEmployee: boolean  | 
|--------------------------------|
| + getName()                    |
| + getSurname()                 |
| + getBirthYear()               |
| + isFullTimeEmployee()         |
| + examinePatient()             |
| + diagnoseIllness()            |
| + prescribeTherapy()           |


Користићемо податке из класе 'Doctor' коју смо направили:

1. Прво у наслову имамо Доктор као класу.

2. Класа 'Доктор' има 4 атрибута : 

- name: String

- surname: String

- yearOfBirth: int

- isFullTimeEmployee: boolean


3. Затим смо имали методе:

+ getName()

+ getSurname()

+ getBirth Year()

+ isFullTimeEmployee()

+ examinePatient()

+ diagnoseIllness()

+ pescribeTherapy()

Овај минус испред атрибута означава да је у програму написано **private**, док плус испред атрибута означава да је у програму написано **public**.

Шта то значи?

public - значи да је свима видљиво 

private -  није свима видљиво.

Чему то уопште служи?

Атрибуте стављамо да буду приватни да не би дозволили директан приступ подацима, док методе могу бити или јавне или приватне.


Представићемо податке за класу 'Doctor':


Class Doctor 

- name

- surname

- birthYear

- is FullTimeEmployee


Затим објекте:


Object

new Doctor("Petar", "Petrovic", 1954, true);

new Doctor("Marija", "Marjanovic", 1965. true);


Ово у меморији изгледа овако:

| Petar       |         
|-------------|        
| Petrovic    |
|-------------|         
| 1954        |         
|-------------|       
| true        |          


| Marija       | 
| ----------   |
| Marjanovic   |
|--------------|
| 1965         |
| ------------ |
| true         |   


Како би изгледао кроз UML изгледао приказ класе 'Patient' у меморији:


| Patient                              |
|------------------------------------- |
| - id: int                            |
| - name: String                       |
| - surname: String                    |
| - yearOfBirth: int                   |
| - hasCertifiedHealthBook: boolean    |
| - cartonNumber: int                  |
| - vactinations: PatientVaccinations[]|

Међутим када говоримо о вакцинацији пацијента, у оквиру тога ћемо имати више неких података који су везани за вакцинацију. У том случају морамо отворити нову класу, класу 'Vaccination'јер унутар те класе имамо сложене типове података.


Приказ класе 'Vaccination' кроз UML:


| Vactination                        |
|------------------------------------|
| - id: int                          |
| - name: String                     |
| - description: String              |
| - isRevaccinationNeeded: boolean   |
| - activeDurationYears: int         |


Сада када имамо податке о пацијенту, доктору и вакцинацији у различитим класама, онда желимо да повежемо те податке из класа:

То ћемо урадити тако што ћемо у класу 'Patient'  убацити низ :

PatientVaccinations[]

Како да повежемо податке о пацијенту са подацима о вАкцинацији?

Тако што ћемо додати  ID број, зато што је то једноставно решење што се тиче базе података, а и бројеви као типови су лакши што се тиче операција, и заузимају мање места.


Приказ класе ' PatientVaccination' :


| PatientVaccination          |
| ----------------------------|
| - patientId: int            |
| - vaccinatiodId: int        |
| - doctorId: int             |
| - vaccinationDate: int      |


Увек правимо да нам идентификатори буду типа Integer због перформанси.

Синтаксу за низ који смо написали у класи 'Patient', а која гласи:
 **PatientVaccinations[]** програм ће препознати и повезати са класом 'PatientVaccination'.

Ако желимо да кроз одређену вакцинацију добијемо податке о доктору, треба нам атрибут који реферише класу 'Doctor' као објекат, а исто тако хоћемо да имамо податке о вакцинацији. Онда додајемо следеће атрибуте на предходн табелу:


| PatientVaccination          |
| ----------------------------|
| - patientId: int            |
| - vaccinatiodId: int        |
| - doctorId: int             |
| - vaccinationDate: int      |
| - patient: Patient          |
| - vaccination: Vaccination  |
| - doctor: Doctor            |


Сада ћемо убацити реалне податке за класe, односно податке за објекте унутар класа 'Patient', 'Vaccination' и 'Doctor':
 

| Patient  object                    |
|------------------------------------|
| - 1                                |
| - Pavle                            |
| - Nikolic                          |
| - 1982                             |
| - true                             |
| - 1                                |
| -                                  |


| Vactination  object                |
|------------------------------------|
| - 13                               |
| - BCG                              |
| - Vakcina protiv tuberkuloze       |
| - true                             |
| - 10                               |


| Doctor  object                     |
|----------------------------------- |
| Petar                              |       
|------------------------------------|      
| Petrovic                           |        
|------------------------------------|      
| 1954                               |     
|------------------------------------|        
| true                               |     


    
| PatientVaccination          |
| ----------------------------|
| - 1                         |
| - 13                        |
| - 86                        |
| - 1987                      |
| - patient: Patient          |
| - vaccination: Vaccination  |
| - doctor: Doctor            | 


**- patient: Patient** из табеле 'PatientVaccination' садржи податке из табеле 'Patient object'.

**- vaccination: Vaccination** из табеле 'PatientVaccination' садржи податке из табеле 'Vaccination object'.

**- doctor: Doctor** из табеле 'PatientVaccination' садржи податке из табеле 'Doctor object'.
    
    
=========================================================================
