## UML (Unified Modelling Language) - forming (implementation of) diagrams and connecting classes

Topics:

- Class diagrams and methods's visibility 

- Relationships between classes using examples (Doctor, Patient, Vaccination, PatientVaccination)

 

UML (Unified Modelling Language) represents standard language for specification, visualisation and documentation of software system. In other words, it is a standard international notation for object oriented modelling of a system. 

How we represent classes by diagrams?

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


We will use the date from class 'Doctor', which we've made:

1. Firstly, in title we have Doctor as a class.

2. Class 'Doctor' has 4 attributes: 

- name: String

- surname: String

- yearOfBirth: int

- isFullTimeEmployee: boolean


3. Then, there are methods:

+ getName()

+ getSurname()

+ getBirth Year()

+ isFullTimeEmployee()

+ examinePatient()

+ diagnoseIllness()

+ pescribeTherapy()

The minus before attribute represents that in program it is written **private**, while plus before attribute represents that it is written **public** in program.

**What does it mean?**

public - it means that it is visible for all

private -  it is not visble for all.

**For what is for?**

Attributes are usually private, because we don't want to allow direct access to data, while methods can be private or public.


We will present data for class 'Doctor':


Class Doctor 

- name

- surname

- birthYear

- is FullTimeEmployee


Then objects:


Object

new Doctor("Petar", "Petrovic", 1954, true);

new Doctor("Marija", "Marjanovic", 1965. true);


In memory, this is represented like below:

| Petar       |                 
| Petrovic    |         
| 1954        |                
| true        |          


| Marija       |
| Marjanovic   |
| 1965         |
| true         |   


How the class 'Patient' by UML will look like in memory:


| Patient                              |
|------------------------------------- |
| - id: int                            |
| - name: String                       |
| - surname: String                    |
| - yearOfBirth: int                   |
| - hasCertifiedHealthBook: boolean    |
| - cartonNumber: int                  |
| - vactinations: PatientVaccinations[]|

However, when we talk about patient's vaccination, within it, we will have many of data connected to vaccination. In this case, we have to open new class, class 'Vaccination', because within class we have complex data types.


Representation of class 'Vaccination' by UML:


| Vactination                        |
|------------------------------------|
| - id: int                          |
| - name: String                     |
| - description: String              |
| - isRevaccinationNeeded: boolean   |
| - activeDurationYears: int         |


Now, when we have data of patient, doctor and vaccination in different classes, then we want to connect these data from classes:

We will do that by adding an array in the class 'Patient':

PatientVaccinations[]

How to connect data about patient to data about vaccination?

We will add ID number, because it represents the simple solution considering database. The number as data type is easier when operations are taken into consideration as well as it takes less space.  


Representation of class ' PatientVaccination' :


| PatientVaccination          |
| ----------------------------|
| - patientId: int            |
| - vaccinatiodId: int        |
| - doctorId: int             |
| - vaccinationDate: int      |


We always make identifiers to be Integer data type, because of performances.

Syntax for array which we have made in class 'Patient':

**PatientVaccinations[]** program will recognize and connect with class 'PatientVaccination'.

If we want to get data about some doctor, through particular vaccination, we need an attribute which is reference to class 'Doctor' as an object. Also if we want data about vaccination, then we add the following attributes to previous table: 


| PatientVaccination          |
| ----------------------------|
| - patientId: int            |
| - vaccinatiodId: int        |
| - doctorId: int             |
| - vaccinationDate: int      |
| - patient: Patient          |
| - vaccination: Vaccination  |
| - doctor: Doctor            |


Now, we will write real data for classes, data for object within classes 'Patient', 'Vaccination' и 'Doctor':
 

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
|------------------------------------|
| Petar                              |          
| Petrovic                           |              
| 1954                               |             
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


**- patient: Patient** from table 'PatientVaccination' contain data from table 'Patient object'.

**- vaccination: Vaccination** from table 'PatientVaccination' contain data from table 'Vaccination object'.

**- doctor: Doctor** from table 'PatientVaccination' contain data from table 'Doctor object'.
    
    
=========================================================================
