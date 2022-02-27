# What are the use of Structure?
- Structures allow to store different data types information inside it at contiguous memory location
- It is a collection of different different data types which are at contiguous memory locations.
- it is like array in c but where array stores same type of data while structure stores different types of data.
- If we want to represent too many information(too many variables) of same data type as an single entity then we go for Array but if we want to represent too many information(too many variables) of different different data types as an single entity then we go for Structure.
- When a structure is defined, it creates a user-defined type but, no storage is allocated.
	#### Use of Structure
	- You can create a real life entity / object having a bunch of attributes
	- It’s also useful in defining data structures like linked list, trees, graphs etc since they are a combination of various data types.
	- suppose you have to pass all the details about a student like name, roll, mark etc to a function , then it helps to pass the different types of data using a single reference

#### Real life Example
- A showroom of cars:-. A car showroom must have 2 important resources:  
1) Cars  
2) Employees  
Now, look at the below structure code for cars:
```c
	struct Cars {
		char Car_Maker_Brand[50]; 
		char Car_Model[50]; 
		int year_Of_Manufacture; 
		float Price; 
		int Seating_Capacity; 
		int Maximum_Speed; 
		float Fuel_tank_volume;	
		...
		...
		...
		...
	  }
```
![[Pasted image 20210820111347.png]]
- If you have to store the details of numerous cars, as in case of a car showroom it is their necessity, maintaining a structure array is much more easier than maintaining variables for each property of car.

#### Another Example
 - Suppose you are having record of 100 students. Each student is having name(which is of char[] type), id(int type) and marks(float type). All these three properties is uniquely owned by each student. Each student will carry this three different data type information.
	- Now, suppose you have to pass complete information of all students to one function for some reason. At that point rather than passing each and every information(name, id, marks, etc...) one by one for every student will not be a good way of programming. In such case we will prefer approach in which can pass complete student information as an single entity of one by one student.
	- So, where ever we need to refer different data types information as an single entity then we go for structure and above is the real time example where we would like to go for structure.