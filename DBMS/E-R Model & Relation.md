# E-R Model & Relationship
Before dive into this topic first understand what is [[DBMS]]
- First question arises `Why we need ER Diagram?`
- basically this is a graphical representation.
- those people who don't have any knowledge about the dbms and they want to implement database in their business then to understand them that how data flows in the dbms we use the er diagram,so they can understand the whole model easily

## ER Model
`What is ER Model?`
- ER Model is a conceptual model by which you can conceive the structure of the database, maintain relationship between different components and identify the constraints that occurs in the integrated design of complete data base system
- There are three components 
	1. Entity
	2. Attributes
	3. Relationship

	#### Entity
	`What is entity`
		- real world object that can be distinguishable is known as entity
		- Ex- compiler book and dbms book ..these two are real world object and different from each other....but book is a entity set
	`What is entity set?`
		- before going to that first tell me `what is the definition of set?`
		   collection of similar types of elements
		- so similarly entity set is collection of entities that can share some properties
		- an entity set is a set of entities of the same type that share the some properties
		- book is an entity set which have properties like price, name, year-pub, issn, publisher etc 
		- properties and attributes both are same

	#### Attributes
	- attribute is a specify part of an entity structure
	- it is a mapping from its entity set to its domain value
	- domain value means suppose book has the attributes like name publisher, issn,year of pub etc and domain means type means book name is type of string it will not a numeric value similarly year is integer type so this is domain.
	- so basically we can say that domain is like data type
			
		#### Types Of Attributes
		1. Single Valued Attributes:- those attributes which contain a single value for ex-adhar no, voter id number, age 
		2. Multi Valued Attributes:- those attributes that attributes contain more than one value for a single entity for ex-phone no
		3. Composite Attributes:- those attributes which can be further divided for ex-name..it can be divided into first name and last name
		4. Simple or Atomic Attributes:- those attributes which can not be further divided. ex-age,phone no
		5. Stored Attributes & Derived Attributes:- stored attributes are those which is already stored in the database, ex-suppose you store your dob then subtract it from the present date then you find your age..so here your dob is stored attribute and the age is derived attribute
			similarly marks is a stored attributes and grades is the derived attribute
	 #### Relationship
	 - **Def**- a relationship is an association among several entities
	 - we denote this using diamond symbol
	 - Types Of Relationship
		 1. One to One
		 2. One to Many or Many to One
		 3. Many to Many
		 - ![[Pasted image 20210820004711.png]]
		 #### Example
		 `every empolyee works for exactly one department and a department can have more than one employee , new department need not have any employee`
		 - **Degree**- Number of entities participate in a relationship is known as degree
		 - So in this example degree is 2, one is employee and another one is department 
		 - **Cardinality Ratio**- Maximum no of times entity can be participate in a relation
		 - **Participation or Existence**- Minimum no of times entity can participate in a relationship is known as participation or existence 
		 - **NOTE**-Whenever participation or existence is non zero then we can say participation of entity is total otherwise partial.
		 - **NOTE**-Cardinality ratio or participation also known as [[Structural Constraints]]



