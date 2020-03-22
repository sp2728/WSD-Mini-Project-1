# &#x1F538; Python Work Flow and Definitions &#x1F538;

## &#x1F538; Don't Repeat Yourself Principle in Python

DRY principle is a software development practice which aims at reducing repetition of information.
For Example:
```
fruit = 'mango'
fav_fruit = ['Orange', 'Apple', 'Cherry', 'mango', 'Strawberry']
if fruit in fav_fruit:
    print ('I love Mango!')
```

## &#x1F538; Static Methods in Python

Static Methods are similar to the class methods in python. The difference detween staic methods and class methods is that staic methods bound to a class rather object of a class.So, staic methods can be called without object of a class.

## &#x1F538; Objects in Python

Creating a class means creating a new type of object, allowing new instance of that type to be made. Object can have multiple names and can be bound to the same class.

## &#x1F538; Exceptions in Python

Errors detected during the execution are called as exceptions. They can be not severe errors though. There are different kinds of exceptions in python. The last line of error message is the exception which you have occured. Some of the exceptions which can occur are 'Zero Division Error', 'NameError', 'TypeError','Arthemetic Error', etc.

Here is the link for [Built in exceptions](https://docs.python.org/3/library/exceptions.html#bltin-exceptions) documentation.

### &#x1F538; Handiling Exceptions in Python

It is possible to handle the exceptions using try, catch bock statements and writing the exception statements for handling the exceptions.
```
while True:
     try:
         x = int(input("Please enter a number: "))
         break
     except ValueError:
         print("Oops!  That was no valid number.  Try again...")
```

## &#x1F538; Factory Methods in Python

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
## &#x1F538; CSV Files in Python

CSV files in python can be implementes using the csv modules in the python libraries. It implements the classes to read and write the tabular data in csv format. we can iterate through the rows and coloumns in the csv file and use to import or export data.

```
import csv
 with open('eggs.csv', newline='') as csvfile:
     spamreader = csv.reader(csvfile, delimiter=' ', quotechar='|')
     for row in spamreader:
         print(', '.join(row))
```
