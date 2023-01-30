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

Q12. Where and how are instance attributes created?

Q13. What does the term "self" in a Python class mean?

Q14. How does a Python class handle operator overloading?

Q15. When do you consider allowing operator overloading of your classes?

Q16. What is the most popular form of operator overloading?

Q17. What are the two most important concepts to grasp in order to comprehend Python OOP code?

Q18. Describe three applications for exception processing.

Q19. What happens if you don't do something extra to treat an exception?

Q20. What are your options for recovering from an exception in your script?

Q21. Describe two methods for triggering exceptions in your script.

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