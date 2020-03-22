# How Python Uses Indentation to control Flow 

Python indentation is a way of telling a Python interpreter that the group of statements belongs to a particular block of code. A block is a combination of all these statements. Block can be regarded as the grouping of statements for a specific purpose. Python uses Whitespce for indentation. All statements with the same distance to the right belong to the same block of code. If a block has to be more deeply nested, it is simply indented further to the right. Without indentation, Python does not know which statement to execute next or which statement belongs to which block. This will lead to IndentationError.The use of indentation in Python makes the code look neat and clean.
For example:

if True:

    print('Hello')
    
    a = 5
and

if True: print('Hello'); a = 5

both are valid and do the same thing. But the former style is clearer.

Incorrect indentation will result into IndentationError.

# Class

Python is an “object-oriented programming language.” This means that almost all the code is implemented using a special construct called classes. Programmers use classes to keep related things together.This is done using the keyword “class,” which is a grouping of object-oriented constructs.
A Class is like an object constructor, or a "blueprint" for creating objects.

Example-Create a class named MyClass, with a property named x:

class MyClass:

  x = 5
  
# Attribute/Property

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

# Unit Test

In Python, Unit Test supports test automation, sharing of setup and shutdown code for tests, aggregation of tests into collections, and independence of the tests from the reporting framework.  unittest supports some important concepts in an object-oriented way:

test fixture

A test fixture represents the preparation needed to perform one or more tests, and any associated cleanup actions. This may involve, for example, creating temporary or proxy databases, directories, or starting a server process.

test case

A test case is the individual unit of testing. It checks for a specific response to a particular set of inputs. unittest provides a base class, TestCase, which may be used to create new test cases.

test suite

A test suite is a collection of test cases, test suites, or both. It is used to aggregate tests that should be executed together.

test runner

A test runner is a component which orchestrates the execution of tests and provides the outcome to the user. The runner may use a graphical interface, a textual interface, or return a special value to indicate the results of executing the tests.

# Decorator
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
