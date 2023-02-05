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

Q23. What is the purpose of the try statement?

Q24. What are the two most popular try statement variations?

Q25. What is the purpose of the raise statement?

Q26. What does the assert statement do, and what other statement is it like?

Q27. What is the purpose of the with/as argument, and what other statement is it like?

Q28. What are *args, **kwargs?

Q29. How can I pass optional or keyword parameters from one function to another?

Q30. What are Lambda Functions?

Q31. Explain Inheritance in Python with an example?

Q32. Suppose class C inherits from classes A and B as class C(A,B).Classes A and B both have their own versions of method func(). If we call func() from an object of class C, which version gets invoked?

Q33. Which methods/functions do we use to determine the type of instance and inheritance?

Q34.Explain the use of the 'nonlocal' keyword in Python.

Q35. What is the global keyword?