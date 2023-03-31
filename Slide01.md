## **OBJECT**

→In computer science 

    - Objects can be a variable, a data structure, a function, or a method
    - Essentially a location in memory having a value that can be referenced by an identifier
→In object oriented programming (OOP)

    - An instance of a class where this object can be either a variable, a function, a data structure or a combination of such

A combination of data and functional code. This is because real-world objects have states and behaviour

_States_ → The characteristic, Measurable data of an object
_Behaviour _→ The available functionality of the object (what can it do?)

## **WHAT IS OBJECT ORIENTED PROGRAAMMING (OOP)?**

	- Programming practice to design reusable software systems
	- OOP designs programs with creation of Objects
	- An approach that focuses on the definition of data rather than the IPO logic (OOP vs procedure-oriented programming)
	- The goal is to create an object that we can define and provide functionality to solve problems

## **COMPUTATIONAL DIFFERENCES**

→ Procedure-oriented programming

	- A human may require:
		- Calculations
		- Logical Evaluations
		- Complete Repetitive tasks
		- Database
		
→ Object oriented programming

	- Creating a human object
		- What’s their name
		- What’s their address
		- What functions can this object have?
  
***OOP focuses on HOW to manipulate the data of the object rather than the logic required to manipulate them***

## **AN OBJECT IS AN INSTANCE**

_Instance_ → an instance is a specific realization of any object. An object may be different in several ways, and each realized variation of that object is an instance. The creation of a realized instance is called instantiation.

_Object’s Data _→ called: attributes

_Object’s Code_ → called: methods

_Attributes_ →  a data element representing the quality or state of the class or object. An attribute defines a particular property of an object

_Method_ → a procedure associated with a message and an object. An object consists of state data and behavior; these compose an interface, which specifies how the object may be utilized by any of its various consumers. A method is a behavior of an object parametrized by a user.

#### EXAMPLE

→Dog may have the following _attributes_

	- Name
	- Color
	- Breed
	- isHungry
	- isThirsty
	
→Dog may have the following _methods_

	- bark()
	- eat()
	- sleep()

*If we populate the Dog’s attributes (Name,Color…) then we have an instance; therefore, an object.*

## **WHAT IS A CLASS**

- An abstract description of all objects that can be made from this set class where an object can be instantiated from.
- A Class Contains Attributes

1. Fields: Variables that belong to an object or a class
	- Type 1: It belongs to the instance of the class
	- Type 2: It belongs to the class itself
2. Methods: Functions that the object or the object can call
	class | keyword | → A built-in keyword in Python 3 that allows us to create our own classes.

#### **EXAMPLE**
```python 
class Name: # Class names are CAPATILIZED
	pass 
#end of ClassName

obj = ClassName() # creating instances of Name class
print(obj) # printing object
```
## **HOW TO CREATE A CLASS**
1. First define the name of the class with the keyword: class
2. In its code block (indentation) define its attributes
3. Then you can assign a variable with an instantiation of the class to interact with it
Make sure to use parentheses when calling the class name.

Classes can have methods. In Python 3, we just declare them like a new function (it doesn’t always need to return).

#### **EXAMPLE**
```python 
class Person:
	def greet(self): # method 
		print(‘Hello, how are you?’)
	#end of class Person
	
	p = Person() # creating instance
	p.greet() # outputs the greet message # calling method 
```
## **__init__  method and self parameters**
def __init__(self): → The __init__ method 
- The initialization method is executed as soon as an object of the class is instantiated
- It helps us to do any initialization for the object’s attributes
- self parameter is used to denote that the method is applied and accessible for the object itself
- self will also treat its own attributes as local
- The self variable is used to represent the instance of the class which is often used in object-oriented programming. It works as a reference to the object. Python uses the self parameter to refer to instance attributes and methods of the class.

*Double Underscore ??? → These are key hidden features of Python that allow us to do some overwriting of Python features and hidden content*

#### **EXAMPLE**
```python 
class Person:
	def __init__(self, name):
		self.name = name
	#end of initialization
	
def greet(self): # the self parameter is always required
		print(“Hello, my name is”, self.name)
	#end of greet
#end of class Person

p = Person(‘Mr. Park’)
p.greet()
```
