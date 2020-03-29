# &#x1F538; Python Work Flow and Definitions &#x1F538;

## &#x1F538; How Python Uses Indentation to control Flow:

Python indentation is a way of telling a Python interpreter that the group of statements belongs to a particular block of code. A block is a combination of all these statements. Block can be regarded as the grouping of statements for a specific purpose. Python uses Whitespce for indentation. All statements with the same distance to the right belong to the same block of code. If a block has to be more deeply nested, it is simply indented further to the right. Without indentation, Python does not know which statement to execute next or which statement belongs to which block. This will lead to IndentationError.The use of indentation in Python makes the code look neat and clean.
For example:

if True:

    print('Hello')
    
    a = 5
and

if True: print('Hello'); a = 5

both are valid and do the same thing. But the former style is clearer.

Incorrect indentation will result into IndentationError.

## &#x1F538; Don't Repeat Yourself Principle in Python:

DRY principle is a software development practice which aims at reducing repetition of information.
For Example:
```
fruit = 'mango'
fav_fruit = ['Orange', 'Apple', 'Cherry', 'mango', 'Strawberry']
if fruit in fav_fruit:
    print ('I love Mango!')
```

## &#x1F538; Design Patterns from Gang of Four:
Design patterns are a common way of solving well known problems. Gang of Four provides a set of design patters for overall architecture of the system and its related design decisions. GOF defined two main principles at the bases of the design patterns:

1. *Program to an interface not an implementation.* :
In this principle, the nature or type of the object is not in concern. The goal of this principle is to see if the object does	what it is suppose to. The interface is programmed instead of the implementation. For example, consider that we want to check if an animal can bark. So below is the example:
```
try:
    animal.bark()
except AttributeError:
    self.lol()
```    
2. *Favor object composition over inheritance.*
Composition is natural & elgant to python. As per this principle, instead of inheriting a class it is better to restrict what methods of the wrapped class to expose.For example:
```
class User:
    _persist_methods = ['get', 'save', 'delete']

    def __init__(self, persister):
        self._persister = persister

    def __getattr__(self, attribute):
        if attribute in self._persist_methods:
            return getattr(self._persister, attribute)
```
It is possible to inject the persister instance in runtime! For example, today we are using a relational database, but tomorrow it could be whatever, with the interface we need. So this principle is beneficial here.

## &#x1F538; Class

Python is an “object-oriented programming language.” This means that almost all the code is implemented using a special construct called classes. Programmers use classes to keep related things together.This is done using the keyword “class,” which is a grouping of object-oriented constructs.
A Class is like an object constructor, or a "blueprint" for creating objects.

Example-Create a class named MyClass, with a property named x:

class MyClass:

  x = 5
  
## &#x1F538; Static Methods in Python:

Static Methods are similar to the class methods in python. The difference detween staic methods and class methods is that staic methods bound to a class rather object of a class.So, staic methods can be called without object of a class.

## &#x1F538; Objects in Python:

Creating a class means creating a new type of object, allowing new instance of that type to be made. Object can have multiple names and can be bound to the same class.

## &#x1F538; Attribute/Property:

### Attribute

Python is an object-oriented language, which provides two scopes for attributes: class attributes and instance attributes.

While the instance attribute in Python has exactly the same characteristics and definition as the other object-oriented languages, the class attribute is always mistakingly considered to be the exact equivalent of the static attribute in Java or C++. To be accurate, class attributes in Python and static attributes in Java or C++ have a lot in common, however, they have behavioral differences that I will highlight in this article.

Class Attribute vs. Instance Attribute
Let's start with the basics:

An instance attribute is a Python variable belonging to one, and only one, object. This variable is only accessible in the scope of this object and it is defined inside the constructor function, __init__(self,..) of the class.

A class attribute is a Python variable that belongs to a class rather than a particular object. It is shared between all the objects of this class and it is defined outside the constructor function, __init__(self,...), of the class.

### Property

A class in Python can include properties by using the property() function. The property() method in Python provides an interface to instance attributes.
Consider the following Python script which defines the life class as having the getter and setter methods. The getname() method returns the value of the private instance attribute __name, while the setname() method assigns the value to the __name attribute.

Example:

class life:
    
    def __init__(self, name="Guest"):
        
        self.__name=name
    
    def setname(self, name):
        
        self.__name=name
    
    def getname(self):
        
        return self.__name

## &#x1F538;  Methods in Python: 
A method is a label that can be called on an object. It is a piece of code to execute on that object. And its creation requires it to be put inside a class.
```
class Test:
    def __init__(self):
     pass
    def printhello(self,name):
        print("Hello", name)
        return name
obj=Test()
obj.printhello('Varsha')

Output: 
Hello, Varsha
‘Varsha’
Here, the method printhello() has a name, it takes a parameter, and also returns a value.
```

## &#x1F538; Exceptions in Python:

Errors detected during the execution are called as exceptions. They can be not severe errors though. There are different kinds of exceptions in python. The last line of error message is the exception which you have occured. Some of the exceptions which can occur are 'Zero Division Error', 'NameError', 'TypeError','Arthemetic Error', etc.

Here is the link for [Built in exceptions](https://docs.python.org/3/library/exceptions.html#bltin-exceptions) documentation.

### &#x1F538; Handiling Exceptions in Python:

It is possible to handle the exceptions using try, catch bock statements and writing the exception statements for handling the exceptions.
```
while True:
     try:
         x = int(input("Please enter a number: "))
         break
     except ValueError:
         print("Oops!  That was no valid number.  Try again...")
```

## &#x1F538; Unit Test:

In Python, Unit Test supports test automation, sharing of setup and shutdown code for tests, aggregation of tests into collections, and independence of the tests from the reporting framework.  unittest supports some important concepts in an object-oriented way:

test fixture

A test fixture represents the preparation needed to perform one or more tests, and any associated cleanup actions. This may involve, for example, creating temporary or proxy databases, directories, or starting a server process.

test case

A test case is the individual unit of testing. It checks for a specific response to a particular set of inputs. unittest provides a base class, TestCase, which may be used to create new test cases.

test suite

A test suite is a collection of test cases, test suites, or both. It is used to aggregate tests that should be executed together.

test runner

A test runner is a component which orchestrates the execution of tests and provides the outcome to the user. The runner may use a graphical interface, a textual interface, or return a special value to indicate the results of executing the tests.

## &#x1F538; Constructors in Python:

A constructor is a special kind of method used for initializing the instance variables/members while creation of an object of a class.
There are two types of Constructors:

1.	Default Constructor: No arguments are present in this constructor.
Example:
```
class Test:
    def __init__(self):
        self.num = 5
    def read_num(self):
        print(self.num)
object = Test()
object.read_num()

Output: 5
```

2.	Parameterized Constructor: As the name suggests, parameters are accepted during object creation in these constructors, which in turn are used by the constructor to initialize the instance members of that object.
Example:
```
class Test:
    def __init__(self, num1):
        self.num = num1
    def read_num(self):
        print(self.num)
object = Test(101)
object.read_num()
object1 = Test(1076)
object1.read_num()

Output: 101
	1076
```

## &#x1F538; Factory Methods in Python:

The factory pattern comes under the creational patterns list category. It provides one of the best ways to create an object. In factory pattern, objects are created without exposing the logic to client and referring to the newly created object using a common interface.

The following python code includes the logic of html tags, which specified value. The end user can have a look on the HTML file created by the Python code.

```
class Button(object):
   html = ""
   def get_html(self):
      return self.html

class Image(Button):
   html = "<img></img>"

class Input(Button):
   html = "<input></input>"

class Flash(Button):
   html = "<obj></obj>"

class ButtonFactory():
   def create_button(self, typ):
      targetclass = typ.capitalize()
      return globals()[targetclass]()

button_obj = ButtonFactory()
button = ['image', 'input', 'flash']
for b in button:
   print button_obj.create_button(b).get_html()
```
## &#x1F538; Decorator:
Decorators are very crucial and useful tool in Python since it allows programmers to modify the behavior of function or class. Decorators allow us to wrap another function in order to extend the behavior of wrapped function, without permanently modifying it.

In Decorators, functions are taken as the argument into another function and then called inside the wrapper function.

Syntax for Decorator:

filter_none

brightness_4

@gfg_decorator

def hello_decorator(): 
    
    print("Gfg") 
  
'''Above code is equivalent to - 
  
def hello_decorator(): 
    
    print("Gfg") 
      
hello_decorator = gfg_decorator(hello_decorator)'''

## &#x1F538; Extend Class in Python:

In Python, a subclass can define a function that already exists in its parent class in order to add additional functionality, the function in the subclass is said to be an extended method and the mechanism is known as extending. This is how the property of polymorphism is shown by Python. This is similar to overriding in Java and other Object-oriented languages. Calling the instance of the subclass executes the subclass’s version of the function. To call the parent class's version super() method is used. The Primary advantage provided by extending a method is that the code can be made reusable. Multiple subclasses can share the same code along with some modifications as per specifications and requirements.
```
Simple example showing extend functionality
class Rectangle:
	def __init__(self, length, width):
        	self.length = 12
        	self.width = 13

	def area(self):
    		return self.length * self.width
		
	def perimeter(self):
   		 return 2 * self.length + 2 * self.width
		 
class Square(Rectangle):
    def __init__(self, length):
        super().__init__(length, length)
```

## &#x1F538; CSV Files in Python:

CSV files in python can be implementes using the csv modules in the python libraries. It implements the classes to read and write the tabular data in csv format. we can iterate through the rows and coloumns in the csv file and use to import or export data.

```
import csv
 with open('eggs.csv', newline='') as csvfile:
     spamreader = csv.reader(csvfile, delimiter=' ', quotechar='|')
     for row in spamreader:
         print(', '.join(row))
```
## &#x1F538; Reading Files:

There are actually a number of ways to read a text file in Python, not just one. 

If you need to extract a string that contains all characters in the file, you can use the following method: 


file.read() 

The full code to work with this method will look something like this: 


file = open(“testfile.text”, “r”) 

print file.read() 

The output of that command will display all the text inside the file, the same text we told the interpreter to add earlier. There’s no need to write it all out again, but if you must know, everything will be shown except for the “$ cat testfile.txt” line. 

 

Another way to read a file is to call a certain number of characters.  

For example, with the following code the interpreter will read the first five characters of stored data and return it as a string: 


file = open(“testfile.txt”, “r”)
 
print file.read(5) 
