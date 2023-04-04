# Inheritance 

  → When an object or class is based on another class; where its features are from a parent class
## Types

_Single Inheritance_→ A subclass inheriting the features of a single superclass / parent class
_Multiple Inheritance→_ A subclass inheriting the features of a multiple parent classes
_Multilevel Inheritance→_ A subclass is inheriting from another subclass… A → B → C ( grandparent → parent → child) 

**Inheritance can have an hierarchy (branching like a tree) and/or be a hybrid: mixing the types of inheritances**

## What can we do with inheritance?

  → A child will receive all attributes and methods of the parent
  → A child can then enhance itself with new attributes and new methods
  → A child can **OVERRIDE** attributes and methods for their own liking/speciality

**If** a child class inherits the parent class:

  → The child **does not** need a new __init__() method _**UNLESS**_ it requires new attributes
  →The child does not need to reinstate the parent’s methods UNLESS you override them

#### Example

```python 
class Person:
  def __init__(self, name):
  	self.__name = name 
  
  def getName(self):
    return self.__name

class Student(Person):
  def __init__(self, name, num):
    Person.__init__(self, name)
    self.__sNum = num
  
  def getStudentName(self):
    return("%s: %s" % (self.__sNum,self.getName()))

Execution 
p = Person(“Mr. Park”)
s = Student(“Random Child”, “1234”)
print(p.getName()) # Output: “Mr. Park”
print(s.getStudentName(), “and” , s.getName()) # Output: “1234: Random Child and Random Child”
```
## super()
  → is a built-in method for classes to refer their parent class
  → prevents us from doing ParentClass.method(self) → (The self with self gets confusing)
  
#### Example

```python 
class Person:
  def __init__(self, name):
  	self.__name = name 
  
  def getName(self):
    return self.__nam
class Student(Person):
  def __init__(self, name, num):
    super().__init__(name)
    self.__sNum = num
  
  def getStudentName(self):
    return("%s: %s" % (self.__sNum,self.getName()))
```
## Types of multiple inheritances

  1. Multi-generational
      Grandparent → Parent → Child
  2. Mulitparent ( NOT limited to two)
  3. Mixture of 1 and 2

## Polymorphism with a inheritance kick

  → quick refresher: A method that can be used across different classes and object that is dependent on the parameters.
  → Different Classes (non-inherited) can have the same named methods (Simple) → Polymorphism
  → Within a set of inherited classes have the same methods
  → Inherited Classes modifying Inherited Methods (Overriding) → Polymorphism in Python 3

#### Example

```python
class Parent:
	def method(self):
		pass

class Child(Parent):
	def method(self):
		# something different
		# Polymorphed to something else…
		# Same method name!
		pass
```
