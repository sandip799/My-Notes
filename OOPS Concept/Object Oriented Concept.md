# OOPS Concept
- it is a set of rules and ideas and concepts it is basically a standard in programming that we use to solve a specific type of problem
- besides object-oriented paradigm there are other programming paradigms as well you may ask why well we as humans have a lot of different types of problems and our computers help us solve those different types of problems and if one paradigm is good to solve one type of problem for example that does not necessarily mean that it is good to solve all other types of problems that we have
- so the idea behind object-oriented paradigm is we want to be able to represent real-life objects real-life entities together with their characteristics with their attributes and their behaviors we want to be able to explain those objects to our computer and to represent those objects in our program and that is exactly what oops is used for

#### Example
- Lets understand this concept with real world example
- a car as an entity in real life has many different attributes many different characteristics and some of those are manufacturer of that car so is that car a volvo a ferrari or a ford or some other type of car and then that car certainly has a color, it has price, it has max speed that the car can obtain and many more characteristics
- then some of the behaviors of a car are for example a car can drive a car can accelerate it can stop, you can open the door of a car, you can tank your car so you can put fuel in your car and then you should also have the option to show how much fuel that car has left so those would be some behaviors that car has
- as i said object oriented programming the idea of object oriented programming is to be able to represent that car from real life in your program so how do we do that how can i represent a real life entity like a car in my program or another entity like a game or a sport or student or a book or animal you know so the answer to this question is by using classes

## Class
- class is very important concept in oops class is building block of object oriented programming and um a class is basically user-defined data type
- class is a little bit more complex data type and in what way well let's say for example that in your program you want to represent username of your user in order to be able to do that you will just create a variable of type string and call it username and you should be able to store the username of your user in that variable but what happens if you want to store the entire user in your program that user has many more characteristics than just username, user has his name as well as gender and email address and then he has height and width, weight and then he also has some other characteristics and all of these characteristics are going to be variables that have its own type and then all of these variables together are going to make one group which will be a class that represents your user
- one thing to keep in mind though is that you will need to store the information that is important for your specific program for example if we are talking about facebook user then height and weight of that user is not that important but if you are building a fitness application then height and weight of your user is extremely important so you should store the information that is important for your specific program

#### Example
- Lets create a class of employee
- now the members of this class are going to be its attributes and its behaviors so `what kind of attributes an employee has?` well an employee definitely has a name, company and age, just keep it simple
```cpp
class Employee {
	string Name;
	string Company;
	int Age;
	}
```
- so this class here does not represent data, this class here represents a blueprint so whenever you want to create an employee this class here will serve as a model for that employee
- then here question arises `how do you create an instance of this class how do you create an object of this class?` answer is when you define a integer variable in your program, then you first write its data type and then you write its name, similarly here the user defined data type is Employee class and you can gave a name to your object, let say employee1, so it looks like
```cpp
int main () {
	Employee employee1;
}
```
- then you have to specify the name of the employee, then company name and age, so how can we do this, so in c++ we can access this using dot operator with object name, but here in this example you cant access all the member variables, why because by default the access specifier of the class is private 
- then again question arises that `what is access specifier ?`
-  +++++++++++++++++++++++++++=
-  so first update the class access specifier to public, so if we wrote like this, then this is a explicit way to tell the class is "hey employee class, please change your access specifier to public"
```cpp
class Employee {
public :
	string Name;
	string Company;
	int Age;
	}
```
- lets now set the value to that employee 1 that we defined
```cpp
int main () {
	Employee employee1;
	employee1.Name = "Sandip";
	employee1.Company = "IGIT";
	employee1.Age = 21;
}
```
- but we also said that we can describe behaviors as well so `how can we describe a behavior of an employee?`
-  let's first think of a behavior that an employee has let's say for example that he can introduce himself so he comes to work and he says hello my name is Sandip and i work for IGIT and i am 21 years old so `how can we describe that behavior in this class here?` 
-  well we can describe that with a class method and `what a class method is?` it is basically a function so we are going to create a function inside this class employee
-  lets name this function as IntroduceYourself
```cpp
void IntroduceYourself () {
	cout<<"Name:-" <<Name<<endl;
	cout<<"Company:-" <<Company<<endl;
	cout<<"Age:-" <<Age<<endl;
 }
```
- suppose we have to introduce 5 times then if we didn't have this class method here we would have to copy this code five times so each time that we want to introduce our user we can introduce 
-  instead of doing that we can create a class method which represents a behavior and then we can invoke that class method whenever we need it and if i run this program this user should introduce himself five times
```cpp
Name:-Sandip
Company:-IGIT
Age:-21
Name:-Sandip
Company:-IGIT
Age:-21
Name:-Sandip
Company:-IGIT
Age:-21
Name:-Sandip
Company:-IGIT
Age:-21
Name:-Sandip
Company:-IGIT
Age:-21
```
- lets create another employee in our program and give all the details
```cpp
int main()
{
	 Employee employee1,employee2;
	 employee1.Name = "Sandip";
	 employee1.Company = "IGIT";
	 employee1.Age = 21;
	 employee2.Name = "Siba";
	 employee2.Company = "BPUT";
	 employee2.Age = 21;
	 return 0;
}
```
- so here , the problem is let suppose if we have to create 1000 more employees then we have to define each attributes for every employee like above example, that increases complexity of the program.
- there is a better approach of constructing our objects and that magic concept is constructor

## Constructor
- so first question comes to our mind is, `what is constructor ?`
- a constructor is a special type of method that is invoked **each time** that an object of a class is created 
- so whenever you create an object of a class a constructor is invoked so `does that mean that constructor is invoked in above program that we created recently?` the answer to that question is yes
- now you may wonder okay, we have not created any constructor, you must be lying 
- well let me demonstrate you something, let's comment all the attribute assignment code, lets see what happen
```cpp
int main()
{
	 Employee employee1,employee2;
	 // employee1.Name = "Sandip";
	 // employee1.Company = "IGIT";
	 // employee1.Age = 21;
	 // employee2.Name = "Siba";
	 // employee2.Company = "BPUT";
	 // employee2.Age = 21;
	 employee1.IntroduceYourself();
	 employee2.IntroduceYourself();
	 return 0;
}
```
- so we are not assigning any values to the attributes of this employee, if i run my program let see what happens
```cpp
//OUTPUT
Name:-
Company:-
Age:-16389740
Name:-
Company:-
Age:-6422376
```
- basically it assign some garbage value to all the attributes , so this is the work of **_Default Constructor_**
- `what is default constructor ?` 
- default constructor is a term to describe a constructor that is automatically generated by your compiler so in case that you don't create a constructor of your own, your compiler is going to automatically give you a constructor which is called default constructor
- let's see `how we can create our own constructor` because those values that you saw that is something that we cannot work with
- so there are 3 rules when it comes to creating a constructor
	1. a constructor is just a method but unlike other methods a constructor does not have a return type
	2. second rule is that a constructor has the same name as the class that it belongs to so the constructor of class employee will be called employee
	3. the third rule is that constructor must be public, now this i'm seeing as a rule at this basic level of knowledge because a constructor does not necessarily need to be public always, there are certain specific situations when you would want to make your constructor private but at this basic level of knowledge i would advise you to make sure that your constructors are public because if you remember when we talked about access modifiers and when we said what private means everything that is private is locked is hidden inside your class and you most definitely don't want to make your constructor hidden
- lets make our own constructor
```cpp
 Employee (string name, string company, int age) {
 name = name;
 company = company;
 age = age;
 }
```
- after writing our own constructor again it shows an error

![[constructor 1.jpg]]

- `what is the error?`

![[{FA995731-028E-457D-AC68-848E919D2594}.png 1.jpg]]

- it says no default constructor exists for class employee so `what this error here means?` it means that when we decided to create our own constructor at that moment we lost the default constructor that was automatically generated for us so when you decide to create your own constructor you are going to lose that default constructor and you can fix that by either making your own default constructor or by providing here these three values that we have specified that our constructor is going to receive
```cpp
int main()
{
 Employee employee1 = Employee ("Sandip","IGIT",21);
 employee1.IntroduceYourself();
 return 0;
}
```
- now as you can see, we can get rid of all these unnecessary lines by using constructor

## Four Important OOPs Principles
### Encapsulation
- Encapsulation is an Object Oriented Programming concept that to the **bundling of data, along with the methods that operate on that data, into a single unit**. and that keeps both safe from outside interference and misuse. Data encapsulation led to the important OOP concept of data hiding.
- A [[Class]] is an example of encapsulation in computer science in that it consists of data and methods that have been bundled into a single unit.
- Object - it's just a state and behavior. Each class has interface - set of public methods
- Encapsulation may also refer to a mechanism of restricting the direct access to some components of an object, such that users cannot access state values for all of the variables of a particular object.
- Encapsulation tells us that we should know just an interface of class to be able to use it. We don't have to know anything about internals of class to be able to use it.
-  The best example of encapsulation could be a calculator. We understand its interface from first sight and we don't have to know how it works inside. We know that we can press 2+2 then = and see the result on display.
	#### Example
	- Suppose lets think TV as a class, it has some properties or characteristics like its type (LCD or LED), its size (32inch, 56 inch), color etc and it has some behaviour like playing videos, volume up, volume down, changing channel and so on
	- so if we want to decrease our TV volume we just use the volume down function that is given to user but we don't directly access the speaker and modify its sound
	- again there is an instruction written in that TV box is, don't open it otherwise you will loose your warranty, `why this instruction is written ?` because the company wants to hide all the hardware, if user directly interact with the internal data or hardware then there might be many problem arises.
	- basically all the hardware of the TV and the methods to use the TV properly are bundled together, that is the concept of encapsulation
- `How we can achieve encapsulation in our employee program ?` by restrict the data from outside user. 
- yes, we provide security but we have to provide few methods, so that we can able to interact with the data of the class
- here a protection layer is created by the programmer
- and to communicate with the data we use set and get methods
- lets apply all these methods in our employee class
- first we have change the access specifier for the data from public to private
```cpp
private:
 string Name;
 string Company;
 int Age;
```
- then we have to define the set and get method , so that we can interact with the data
```cpp
void setName(string name) {
 Name = name;
 }
 void setCompany(string company) {
 Company = company;
 }
 void setAge(int age) {
 Age = age;
 }
 string getName() {
 return Name;
 }
 string getCompany() {
 return Company;
 }
 int getAge() {
 return Age;
 }
 ```
