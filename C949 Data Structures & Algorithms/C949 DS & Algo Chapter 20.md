20.1 Classes: Introduction
	Grouping Related Items Into Objects
		-[Objects]: grouping of data (variables) and operations that can be performed on that data (functions or method)
		-creating a program as a collection of objects can lead to a more understandable, manageable, and properly executing program
	Abstraction/Information Hiding
		-[Abstraction]: occurs when a user interacts with an object at a high level, allowing lower-level internal details to remain hidden(aka information hiding or encapsulation)
		-objects support abstraction by hiding entire groups of functions and variables and exposing only certain functions to a user
		-[Abstract Data Type (ADT)]: data type whose creation and update are constrained to specific well-defined operations. a class can be used to implement an ADT
20.2 Classes: Grouping Data
		-multiple variables are frequently closely related and showed be treated as one variable with multiple parts 
			Ex: two variables called hours and minutes might be grouped together in a single variable called time
		-class keyword can be used to create a user-defined type of object containing groups of related variables and functions
		-a class defines a new type that can group data and functions to form an object
		-the object maintains a set of attributes that determines the data and behavior of the class
		-programmer can then use instantiation to define a new Time class variable and access that variable's attributes
		-an [instantiation] operation is performed by "calling" the class, using parenthesis like a function call as in my_time = Time()
		-instantiation operation creates an [instance], which is an individual object of the given class
		-automatically call the init_method  defined in the class definition
		-[method]: a function defined within a class
		-[init_method]: commonly known as a [constructor], is responsible for setting up the initial state of the new instance
		-programmer can create multiple instances of a class in a program, with each instance having different attribute values
		*-good practice is to use initial capitalization for each word in a class name
			Ex: LunchMenu, CoinAmounts, or PDFFileContents*
20.3 Instance Methods
		-function defined within a class
		-can be referenced using dot notation
		-[Special Method Name]: the method implements some special behavior of the class
		-init__special behavior is the initialization of new instances
		-double underscores that appear before and after an identifier
		-Good practice is to avoid using double underscores in identifiers to prevent collisions with special method names, which Python interpreter recognizes and may handle differently
		-Common error for new programmers is to omit the self argument as the first parameter of a method
20.4 Class and Instance Object Types
		-[Class Object]: acts as a factory that creates instance objects
			-when created by the class object, an [instance object] is initialized via the init method
		-calls and instance objects are namespaces used to group data and functions together 
		-[class attributes]: shared among all instances of that class. Class attributes are defined within the scope of a class
		-an [instance attribute] can be unique to each instance
		-instance attributes are created using dot notation, as in self.speed = 0 within a method, or runner1.speed = 7.5 from outside of the class's scope
		-Instance and class namespaces are linked to each other 
		-if a name is not found in an instance namespace, the the class namespace is searched
20.7 Class Interfaces
		-consists of the methods that a programmer calls to create, modify, or access a class instance
		-a class may also contain methods used internally that a user of the class need not access
		-class can be used to implement the computing concept known at ADT, whose creation and update are constrained to specific, well-define operations (the class interface)
		-key aspect of an ADT is the internal implementation of the data and operations are hidden form the user (information hiding), which allows the ADT user to be more productive by focusing on higher-level concepts
		-information hiding also allows the ADT developer to improve the internal implementation without requiring changes to programs using the ADT
		-programmers commonly refer to separating an object interface from its implementation (internal methods and variables); the user of an object needs to know only the object's interface
20.8 Class Customization
		-process of defining how an instance of a class should behave for some common operations
		-such operations might include printing, accessing attributes, or how instances of that class are compared to each other
		-to customize a class, a programmer implements instance methods with special method names that the Python interpreter recognizes
		-class customization can redefine the functionality of built in operators like >,<, =,+,- and * when used with class instances, technique known as [operator overloading].
20.10 Memory Allocation and Garbage Collection
		-[Memory Allocation]: the process of an application requesting and being granted memory
		-memory used by a python application must be granted to the application by the operating system
		-operating system can choose to grant or deny request
		-Python runtime handles memory allocation for the programmer
	Garbage Collection
		-[Memory Deallocation]: the act of freeing the memory that stores variables or objects in a program
		-when an object is no longer referenced by any variables, the object becomes a candidate for deallocation
		-[Reference Count]: integer counter that represents how many variables reference an object
		-when an object's reference count is 0, that object is no longer referenced
		-python's garbage collector will deallocate objects with a reference count of 0
		-time between object's reference count becoming 0 and that object being deallocated may differ across different python runtime implementations