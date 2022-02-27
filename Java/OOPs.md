## Class & Objects
- Class is a template of an object and the object is an instance of class
- `what is instance ?` so instance means physical stuff of that class
- **Ex**- Human is a class that is made by the God, this is a rule but the baby is the instance of the human classes
- So we can say that Class is a **Logical Construct** and the instance is **Physical Reality** and this is the thing that is actually occupying the space in the memory.
- **Properties Of An Object** - Objects are characterized by three essential properties: state, identity, and behavior.
	- The state of an object is a value from its data type.
	- The identity of an object distinguishes one object from another. It is useful to think of an object’s identity as the place where its value is stored in memory.
	- The behavior of an object is the effect of data-type operations.
- `what is instance varialbes ?` instance variables are nothing but the variables inside the object 
- `How to access instance varialbes ?` By using the Dot Operator, The dot operator links the name of the object with the name of an instance variable. and remember the dot operator is actually called as **Separator**
- `How to create objects ?` The **'new'** keyword dynamically allocates *(that is, allocates at run time)* memory for an object & returns a reference to it.
	- This reference is, more or less, the address in memory of the object allocated by new.
	- This reference is then stored in the variable.
	- Thus, in Java, all class objects must be dynamically allocated.
## Abstract Classes
- You have to declare the class as abstract if it contain one or more than one abstract methods
- Abstract classes nothing but the incomplete classes where we define only functions, that's it and the body is defined by the class which inherit it
- `can we have variables in abstract classes ?`Abstract classes have its own data member and whenever it inherited by any class this variable comes in play
- we cant use abstract keyword in variables or data member
- `why cant we create the objects of the abstract classes ?` if we create objects then it will throw an error when we call or invoke the methods of that class because they are empty, that's why
- `can we have constructor in abstract classes ?` See, we can't generate any object of abstract classes that's why we don't need constructor but we can define constructor inside the abstract classes just to assign the data members of the abstract class
- `can we use static variables inside the abstract classes ?` as we know that abstract classes must be overridden, and static variables can't overridden that why we cant define static variables
- `can we define non abstract methods in the abstract class ?` yes we can but it is unnecessary because we cant create objects or instances of the abstract class but yes the child class can use those classes
- `can you manipulate with return types or parameters in the child class ?` No we cant, we have to implement the body according to the same skeleton defined in the parent class
- `can we create abstract static methods ?` No because static methods are not overridden and abstract methods are meant to be overridden, so that's why we cant
- `can we have the final abstract classes ?` we already knew that final classes cant be overridden and abstract classes are meant to be overridden, so that's why we cant
- `what are the use cases of the abstract class ?`
- `so tell me why we have to interfaces instead of abstract class ?` so the use cases is much similar, but the main difference is as we can define normal methods inside the class that's why the problem of the multiple inheritance is still there that's why we have to use interfaces
## Interfaces
- `which type of data members we can use in the interfaces ?` as we know that we can't create any objects of an interface that's why the data members of an interface is by default static as well as final.
- `why by default data members are final in interfaces ?` so interface has no constructor and final members are need to be initialized, so that's why we it is final and it is initialized by the child class