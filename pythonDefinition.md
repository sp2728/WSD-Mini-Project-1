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

