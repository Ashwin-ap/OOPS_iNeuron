Python OOP Assignment

Q1. What is the purpose of Python's OOP?
- The purpose of Python's object-oriented programming (OOP) features is to provide a way to organize and structure code in a way that is efficient and easy to understand and maintain. OOP allows for the creation of reusable code, encapsulation of data, and the ability to model real-world objects and their interactions within a program. This can make it easier to design, debug, and modify a program as it grows in complexity.

Q2. Where does an inheritance search look for an attribute?
- when an attribute is accessed on an object, the interpreter performs a search for the attribute starting with the object's class, and then moving up the class hierarchy. This is known as the "method resolution order" (MRO).

The interpreter looks for the attribute in the following order:

The object's own dictionary
The class's dictionary
The base class's dictionary and so on, until the entire inheritance tree has been searched.

Q3. How do you distinguish between a class object and an instance object?
- A class object is a blueprint for creating instances. It defines the properties and methods that instances of the class will have. It is created when the class is defined, and it remains in memory until the program ends. It can also be used to create new instances of the class.

An instance object, on the other hand, is an actual object that is created by calling the class object. It is created at runtime and is specific to a given set of property values. Each instance object has its own set of properties and methods, which are defined by the class object. It also can have its own state and behavior, which may differ from other instances of the same class.
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

ford = Car('Ford', 'Mustang') 
Here, the class Car is a class object and ford is an instance object.

Q4. What makes the first argument in a class’s method function special?
- the first argument in class's method function, often called "self", is special because it allows the method to access and modify the properties and state of the instance and also to call other methods on the same instance.
Using "self" makes it clear that the method is being called on an instance of the class, and it helps to distinguish it from other variables or arguments that may be used in the method.

Q5. What is the purpose of the init method?
- The init method is also called as constructor method. The purpose of the __init__ method is to initialize the state of a new instance of a class when it is created. It sets the initial values for the instance's properties and also allows the user to set initial values for properties when the instance is created.

Q6. What is the process for creating a class instance?
- The purpose of creating a class instance is to instantiate an object that belongs to a specific class, which allows you to access and utilize the attributes and methods defined in the class. It is a way to create an object with its own unique set of characteristics and behavior.

Q7. What is the process for creating a class?
1. Choose a name for the class and start with the "class" keyword, followed by the class name and a colon.
2. Define class attributes, which can include instance variables and class variables. These are typically defined inside the class but outside of any methods.
3. Define the class's constructor method, __init__, which is called when an object is created from the class and is used to initialize the object's attributes.
4. Define any additional behavior methods as needed. These are defined using the same syntax as any other function.
5. End the class definition with a newline.

Q8. How would you define the superclasses of a class?
- In object-oriented programming, a class can inherit attributes and behavior from one or more superclasses, which are also known as base classes or parent classes. The process of defining a class's superclasses is called inheritance.

Q9. What is the relationship between classes and modules?
- a module is a file containing definitions and statements, while a class is a blueprint for creating objects. The relationship between classes and modules is that classes are defined within modules. A module can contain one or more classes, as well as other definitions and statements.

Modules provide a way to organize and structure your code into reusable and self-contained units. You can import the module and its classes into other parts of your code to use its functionality.

Q10. How do you make instances and classes?
- 
class Employee:
    def__init__(self, name, salary):
        self.name = name
        self.salary = salary
    
    def displayInfo(self):
        print(f'Employee name is {self.name} and salary is {self.salary}')              #class
    
emp1 = Employee('Ashwin', 5)                                                            #instance

Q11. Where and how should be class attributes created?
- Class attributes in Python can be created either directly within a class definition, or outside of a class definition, but within the same module.

withing class :
class MyClass:
    class_attribute = 42

outside class :
class_attribute = 42

class MyClass:
    pass


Q12. Where and how are instance attributes created?
- Instance attributes in Python are created within the __init__ method of a class. The __init__ method is a special method that is automatically called when a new instance of a class is created.

class MyClass:
    def __init__(self):
        self.instance_attribute = 42



Q13. What does the term "self" in a Python class mean?
- The term self in a Python class refers to the instance of the class. It is a convention to use self as the first parameter of each method in a class. When you call a method on an instance of a class, the instance is automatically passed as the first argument to the method, and this argument is stored in self.

class MyClass:
    def __init__(self, attribute_value):
        self.attribute = attribute_value

    def modify_attribute(self, new_value):
        self.attribute = new_value


Q14. How does a Python class handle operator overloading?
- In Python, operator overloading is accomplished by defining special methods in a class with a double underscore (__) prefix and a suffix that corresponds to the operator being overloaded.
class MyClass:
    def __init__(self, value):
        self.value = value

    def __add__(self, other):
        return MyClass(self.value + other.value)

>>> a = MyClass(42)
>>> b = MyClass(15)
>>> c = a + b
>>> c.value
57


Q15. When do you consider allowing operator overloading of your classes?
- operator when used with instances of a class. This can make code using the class more readable and expressive, but it can also be confusing if the overloaded operator does not match the expected behavior.

Consistency: If you allow operator overloading in a class, it is important to ensure that the overloaded operators behave consistently with other classes in the same domain.

Complexity: Overloading operators can add complexity to a class, as well as to the code that uses the class. This can make the class harder to maintain and understand.

Clarity: Operator overloading can make code using the class more concise and readable, but it can also make the code more difficult to understand if the overloaded operators have unexpected or non-standard behavior.


Q16. What is the most popular form of operator overloading?
- The most popular form of operator overloading in Python is overloading arithmetic operators, such as addition (+), subtraction (-), multiplication (*), and division (/). Overloading these operators is common in mathematical classes, such as matrices or complex numbers, where the operations are used to perform calculations on instances of the class.


Q17. What are the two most important concepts to grasp in order to comprehend Python OOP code?
- To comprehend Python OOP (Object-Oriented Programming) code, two of the most important concepts to grasp are:

Classes: Classes are user-defined blueprint or prototype for objects, providing a means of grouping data and methods that operate on that data within a single unit.

Objects: Objects are instances of a class, created at runtime, that can contain data and methods. Objects inherit the attributes and methods defined in the class, and can also have their own unique attributes and methods.


Q18. Describe three applications for exception processing.
- Input validation: Exception handling can be used to validate user input and ensure that it meets certain conditions before being processed. For example, you might use exception handling to check that a user has entered a valid integer value before converting it to an int.

Resource management: Exception handling can be used to manage resources, such as files or network connections, that need to be opened and closed properly. For example, you might use exception handling to ensure that a file is closed properly even if an error occurs while reading it.

Error reporting: Exception handling can be used to provide meaningful error messages to the user when something goes wrong in your code. For example, you might use exception handling to catch a specific error and provide a user-friendly error message, rather than a stack trace.


Q19. What happens if you don't do something extra to treat an exception?
- If you don't do anything to treat an exception in your code, it will propagate up the call stack until it is caught by the Python interpreter or reaches the top-level code. When this happens, the interpreter will terminate your program and display an error message, also known as a traceback.

The traceback will contain information about the exception that was raised, including the type of the exception, the location in your code where it was raised, and a description of the error. The traceback can be helpful for debugging your code and understanding what went wrong, but it may not be user-friendly or appropriate to display to an end-user.

By not treating the exception, your program will terminate abnormally and may not complete the intended tasks. This can result in unexpected behavior, lost data, or other unintended consequences, depending on the specific situation.

Q20. What are your options for recovering from an exception in your script?
- Logging the exception: You can choose to log the exception, along with any relevant information, such as the location in your code where it was raised and the type of the exception. Logging the exception can be useful for debugging your code and tracking down the root cause of the problem.

Displaying an error message: You can choose to display an error message to the user, indicating that an exception has occurred and providing any relevant information, such as what the user can do to resolve the issue.

Retrying the operation: You can choose to retry the operation that caused the exception, if it is safe to do so and you believe that the error may have been temporary.

Terminating the program: You can choose to terminate the program gracefully, after cleaning up any resources that have been allocated and storing any data that needs to be saved.

Propagating the exception: You can choose to propagate the exception to a higher level of the call stack, where it can be handled by a more general handler or by the Python interpreter.


Q21. Describe two methods for triggering exceptions in your script.
- 1.Raising exceptions explicitly: You can raise exceptions explicitly by using the raise statement. The raise statement allows you to throw an exception of any type, including built-in exception types or custom exception types that you have defined. You can provide a message or additional information to the exception, which can be used to provide more context to the error.

2.Triggering exceptions implicitly: Certain operations in Python can trigger exceptions implicitly, without the need for an explicit raise statement. For example, dividing by zero, accessing an index that is out of range, or trying to access an undefined variable will all trigger exceptions implicitly.

Q22. Identify two methods for specifying actions to be executed at termination time, regardless of
whether or not an exception exists.
- There are two methods for specifying actions to be executed at termination time in Python:

Using the "finally" clause in a try-except block: The "finally" clause is used to specify actions that will always be executed, regardless of whether an exception occurs or not. The syntax for using the "finally" clause is:

try:
# code that might raise an exception
except [ExceptionType1 [as var1]]:
# code to handle ExceptionType1
except [ExceptionType2 [as var2]]:
# code to handle ExceptionType2
finally:
# code that will always be executed

Using the "with" statement: The "with" statement is used to wrap the execution of a block of code to ensure that specified cleanup actions are always executed, regardless of whether an exception occurs or not. The syntax for using the "with" statement is:

with open("file.txt", "r") as file:

Q23. What is the purpose of the try statement?
- The try statement is used to handle exceptions, or run-time errors.
try:
    # code that might raise an exception
except [ExceptionType1 [as var1]]:
    # code to handle ExceptionType1
except [ExceptionType2 [as var2]]:
    # code to handle ExceptionType2
...
The code inside the try block is executed. If an exception occurs, the code inside the corresponding except block is executed. The except blocks can be used to handle specific types of exceptions and to provide a recovery mechanism for the program. If no exception occurs in the try block, the code inside the except block is skipped.

Q24. What are the two most popular try statement variations?
- 1. Try-Except: The try-except statement is used to handle exceptions that occur during the execution of a program.

If an exception occurs in the try block, the corresponding except block is executed to handle the exception. If no exception occurs, the except block is skipped.

2. Try-Finally: The try-finally statement is used to specify actions that will always be executed, regardless of whether an exception occurs or not.

The code inside the finally block is executed whether an exception occurs or not, and is typically used for cleanup operations such as closing files, releasing resources, or undoing actions.

Q25. What is the purpose of the raise statement?
- The raise statement in Python is used to raise an exception. It can be used to raise a specific exception or to re-raise the current exception.
raise ExceptionType("error message")
The purpose of the raise statement is to force the program to raise an exception, either to signal an error condition or to indicate that some specific action has failed. This allows you to create custom exception types and to propagate exceptions up the call stack, making it easier to handle and diagnose errors.


Q26. What does the assert statement do, and what other statement is it like?
 - The assert statement in Python is used to check if a given condition is True, and if it is not, raise an AssertionError.
 assert condition, error_message
The condition is the expression that you want to test, and the error_message is an optional string that will be displayed if the condition is False.

The purpose of the assert statement is to provide a simple and readable way to check for error conditions in your code. If the condition is False, the AssertionError is raised, indicating that an error has occurred and that further action is needed to resolve it.

The assert statement is similar to a if statement.

Q27. What is the purpose of the with/as argument, and what other statement is it like?
- The purpose of the with statement is to ensure that the expression is properly managed and cleaned up, even if an exception occurs during the execution of the code block. The expression is evaluated, and its result is assigned to the variable if the as clause is used.

The with statement provides a convenient and readable way to manage resources such as files, sockets, and databases, and to ensure that resources are properly acquired and released. The with statement also makes it easy to handle exceptions that might occur while accessing these resources.

with open("example.txt", "r") as f:
    contents = f.read()
    # do something with contents

The with statement is similar to the try-finally statement, with the difference that the with statement is more concise and easier to read, and also provides a more convenient way to manage resources. 

Q28. What are *args, **kwargs?
*args is used to send a non-keyworded variable length argument list to the function. Essentially, it allows you to pass a variable number of arguments to the function, which are then collected into a tuple. The syntax for using *args is as follows:
def function_name(*args):
    # function body

**kwargs is used to pass keyworded variable length of arguments to a function. It allows you to pass keyworded arguments to the function, where the keywords are mapped to a dictionary, and the values of the arguments are stored in the dictionary. The syntax for using **kwargs is as follows:
def function_name(**kwargs):
    # function body


Q29. How can I pass optional or keyword parameters from one function to another?
ou can pass optional or keyword parameters from one function to another in Python by using default values for the parameters in the second function and passing the arguments as keyword arguments when calling the second function from the first.

For example, let's say you have two functions: first_function and second_function. first_function calls second_function, and you want to pass an optional parameter param1 with a default value of None to second_function:
def second_function(param1=None):
    # function body

def first_function():
    # function body
    second_function(param1="Hello")

You can also pass keyword parameters from one function to another using the **kwargs syntax. **kwargs allows you to pass any number of keyword arguments as a dictionary to the function. For example:
def second_function(**kwargs):
    param1 = kwargs.get("param1", None)
    # function body

def first_function():
    # function body
    kwargs = {"param1": "Hello"}
    second_function(**kwargs)


Q30. What are Lambda Functions?
- Lambda functions in Python are small, anonymous functions that are defined using the lambda keyword. They are often used as an alternative to writing a full-fledged function using the def keyword. Lambda functions are often used in combination with higher-order functions, such as map, filter, and reduce, to perform operations on lists or other data structures. 

>>> square = lambda x: x**2
>>> square(5)
25

lambda functions are limited in their functionality and can only contain a single expression. For more complex operations, it's usually better to write a full-fledged function using the def keyword.


Q31. Explain Inheritance in Python with an example?
- Inheritance is a fundamental concept in object-oriented programming (OOP) that allows you to create new classes based on existing classes. The new class inherits attributes and behaviors from the existing class and can add new attributes and behaviors of its own. This helps you to reuse existing code and build new classes more easily.


class Animal:
    def __init__(self, name, species):
        self.name = name
        self.species = species

    def make_sound(self):
        print("Some generic animal sound")

class Dog(Animal):
    def __init__(self, name, breed):
        Animal.__init__(self, name, species="Dog")
        self.breed = breed

    def make_sound(self):
        print("Woof!")

dog = Dog("Fido", "Labrador")
print(dog.name)
print(dog.species)
print(dog.breed)
dog.make_sound()


Q32. Suppose class C inherits from classes A and B as class C(A,B).Classes A and B both have their own versions of method func(). If we call func() from an object of class C, which version gets invoked?

- when a class inherits from multiple classes (also known as multiple inheritance), the method resolution order (MRO) determines the order in which the parent classes are searched for a method. The MRO is determined by a linearization of the inheritance hierarchy and is used to resolve method name conflicts between multiple parent classes.

The MRO in Python follows the C3 linearization algorithm, which gives priority to the leftmost parent class in the inheritance hierarchy. This means that if class C inherits from class A before class B (i.e., class C(A, B)), then the version of func() defined in class A will be invoked.

Q33. Which methods/functions do we use to determine the type of instance and inheritance?

- type: The built-in type function returns the type of an object. For example, type(x) returns the type of x.

isinstance: The built-in isinstance function checks if an object is an instance of a particular class or a subclass of that class. For example, isinstance(x, MyClass) returns True if x is an instance of MyClass or a subclass of MyClass.

issubclass: The built-in issubclass function checks if a class is a subclass of another class. For example, issubclass(MySubClass, MyClass) returns True if MySubClass is a subclass of MyClass.

__class__ attribute: Every instance in Python has a __class__ attribute that stores the type of the instance. For example, x.__class__ returns the type of x.

Q34.Explain the use of the 'nonlocal' keyword in Python.
The nonlocal keyword in Python is used to refer to a variable defined in the nearest enclosing scope that is not global. It is used within a nested function to indicate that a variable is not local to the inner function, but is instead defined in the nearest enclosing scope.

def outer_function():
    x = 10
    def inner_function():
        nonlocal x
        x = 20
    inner_function()
    print(x)

outer_function()

output - 20

The nonlocal keyword is used to modify variables in an outer scope from within a nested function. Without nonlocal, any assignment to a variable would create a new local variable in the inner function scope, hiding the variable in the outer scope. The nonlocal keyword allows you to modify the value of a variable in the nearest enclosing scope, rather than creating a new local variable with the same name.

Q35. What is the global keyword?

- The global keyword in Python is used to indicate that a variable is a global variable. A global variable is a variable that is accessible from anywhere in the code, not just within the current function or module.

x = 10

def my_function():
    global x
    x = 20

my_function()
print(x)

output : 20

It's important to use the global keyword carefully, as modifying global variables can make your code harder to understand and maintain. In general, it's better to avoid using global variables and instead pass values as arguments to functions and return values from functions. The global keyword should only be used when necessary, such as when you need to access or modify a global variable within a function.