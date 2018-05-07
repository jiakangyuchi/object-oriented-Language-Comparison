

# object-oriented-Language-Comparison

   [Go to README.md](README.md)
   
   [Go to code.txt](code.txt)
    
Compare Python and Java


* Language purpose/genesis
  * Why was the language created? 
  
    java: Because of the consumer electronics manufacturers market’s demand for CPU flexibility back in 1991, development need to be more platform-neutral process. The popular language at that time, C++, could not enable logic part to website pages. Java is intended to let application developers "write once, run anywhere", meaning that compiled Java code can run on all platforms that support Java without the need for recompilation, which enable Internet developers to explore without having to share their source code. 

    python: Python is a general-purpose programming language that emphasizes code readability, notably using significant whitespace. It enables clear programming on both small and large scales. 
    
  * What problems was the language trying to address? 
     
    java: Enable creation of applets for the World-Wide Web and make program portable and be able to operate in distributed environments. Besides, Java improved on simplicity compared to C/C++.
    
    python: The ancestor of Python, ABC language was lack of extensibility. At that time, the creator was working in the Amoeba distributed operating system group at CWI. Amoeba had its own system call interface which wasn’t easily accessible from the Bourne shell. Thus, Python was created, a scripting language with a syntax like ABC but with access to the Amoeba system. Moreover, instead of being an Amoeba-specific language, Python is generally extensible.
    
  * Is the language a reaction to a previous language or a replacement for another language?
   
    Java: Java derives much of its syntax from C and C++ but is with more high-level facilities.
    
    Python: 'A descendant of ABC that would appeal to Unix/C hackers.' , says the creator of Python, Guido van Rossum. Python is a successor to the ABC language and is capable of exception handling and interfacing with the Amoeba operating system. 
    
* Unique features of the language
  * Does the language have any particularly unique features? 
  
    Java: Java is Platform Independent by compiling in bytecode which can be interpreted on any system which have JVM; Java is Robust. It has the strong memory allocation and automatic garbage collection mechanism; Java is multithreaded.
    
    Python: Python is easy to code and read. Its formatting is visually uncluttered, and it often uses English keywords where other languages use punctuation ; Python was designed to be highly extensible, which enables adding programmable interfaces to existing applications; Coding methodology of Python: "there should be one—and preferably only one—obvious way to do it"; Python comes with a large standard library that covers areas such as string processing (regular expressions, Unicode, calculating differences between files), Internet protocols (HTTP, FTP, SMTP, XML-RPC, POP, IMAP, CGI programming), software engineering (unit testing, logging, profiling, parsing Python code), and operating system interfaces (system calls, filesystems, TCP/IP sockets).

* Name spaces
  * How are name spaces implemented?
      
    Java: In Java, the idea of a namespace is embodied in Java packages. 
    
    Python: Python implements namespaces as dictionaries. There is a name-to-object mapping, with the names as keys and the objects as values. Multiple namespaces can use the same name and map it to a different object.
    
  * How are name spaces used?
  
    Java: All code belongs to a package, although that package need not be explicitly named. Code from other packages is accessed by prefixing the package name before the appropriate identifier.
    
    Python: Local Namespace is created when a function is called, and it only lasts until the function returns; Global Namespace is created when the module is included in the project, and it lasts until the script ends; Built-in Namespace includes built-in functions and built-in exception names.

* Types
  * What types does the language support?
  
    Java: boolean, char, byte, integral including byte, int, long, short and floating-point types including float and double.
    
    Python: Python is dynamically-typed. This means that the type for a value is decided at runtime, not in advance. Python's Built-in Data types include numeric types (int, long , float, complex), boolean, sequences (str, bytes, byte, list, tuple), sets, mappings and some others such as type and callables.
    
  * Are both reference and value types supported?
  
    Java: Yes.
    
    Python: No. Python is neither "call-by-value" or "call-by-reference". It is a "call-by-object" model, which means In Python a variable is not an alias for a location in memory. Rather, it is simply a binding to a Python object.
    
  * Can new value types be created?
  
    Java: No.
    
    Python: Yes, Python allows programmers to define their own types using classes.
  
* Inheritance/extension 
  
    Java: everything is an object，and the root of all types is the Object class.
    By extending another class, a class inherits its fields and methods. There are two advantages on extending another class: first,         write less code, and secondly, reuse of code makes it easier to debug your program.
    In java, it only supports single extension, which means multiple extension is not allowed.

    python: see the code part.

* Reflection
  * What reflection abilities are supported?
    
    Java: Java includes a Reflection API which can be used to inspect a class, fields and methods.
    For the fields, we can only examine the public ones.
    
    python: Python has the ability to use reflection to see what type, class, fields, and methods the object has.
    
  * How is reflection used?
    
    See the code part.

* Memory management
  * How is it handled?
    
    Java: All Java objects,such as String, Integer are stored in the heap.
    Variables are a reference to the object, and local variables are stored on the stack.
    This heap is divided into two areas. The first is the nursery and second is called the old space. 
   
    python: All objects and data in a program are stored on a private heap managed by the Python interpreter.
   
  * How does it work?
   
    Java: Objects first enter the nursery when they are instantiated. When the nursery becomes full, the objects are then moved       to      the old space. When the old space becomes full, the objects are deleted.
   
    python:Python memory manager interacts with the operating system to request and ensure there is enough memory. It then can              allocate space for the requested object.
   
* Garbage collection?
   
    Java:when objects are not referenced anymore,their memory is freed, which is pretty similar to python.
    Advantage:can handle retain cycle, process regularly, and run on backend
    Disadvantage:cannot determine release time, when GC run, it may cause resources shortage so that we may suspend some threads with lower priority.

    python:Handled by an algorithm that utilizes reference counting to determine if an object should be freed.
   
* Automatic reference counting?
   
    Java:No, Java uses the GC instead of reference counting.
   
    python:Yes, it is how Python knows if an object is no longer in use or being referred. 
    Disadvantage:cannot handle retaining cycle
    Advantage:release accurately, and more efficiency because of no backend process.

* Comparisons of references and values
  * How are values compared? (i.e. comparing two strings)
    
    Java: we use == to compare between primitive types, like int,bool,double, and we use the method .equals() for comparisons               between reference types.
    see the code part.

    python: we can use the == operator to determine if two are equal 

* Null/nil references
  * which does the language use? (null/nil/etc)
   
    Java:Java uses the null keyword
   
    python:None keyword, which is an object representing a state of nothing.
 
  * Does the language have features for handling null/nil references?
 
    Java:Yes, it is the NullPointerException, which will be thrown on any method invocation on a null reference. I think it is not  a       good way to deal with null values compared to Python, which can limit which variables can be null.

    python:Yes, we can use "is" to determine if an object has a state of None.
		
* Errors and exception handling
    
    java:The error reporting functions allow you to customize what level and kind of error feedback is given, ranging from simple notices to customized functions returned during errors.
    
    python:It is possible to write programs that handle selected exceptions. Look at the following example, which asks the user for input until a valid integer has been entered, but allows the user to interrupt the program (using Control-C or whatever the operating system supports); note that a user-generated interruption is signalled by raising the KeyboardInterrupt exception.


* Lambda expressions, closures, or functions as types

  python: Python supports the creation of anonymous functions (i.e. functions that are not bound to a name) at runtime, using a construct called "lambda". This is not exactly the same as lambda in functional programming languages, but it is a very powerful concept that's well integrated into Python and is often used in conjunction with typical functional concepts like filter(), map() and reduce().

  java:a lambda function is an anonymous java function that can be stored in a variable and passed as an argument to other functions or methods. A closure is a lambda function that is aware of its surrounding context.

* Implementation of listeners and event handlers

  check code.txt please.

* Singleton
  * How is a singleton implemented?
  
    python:Possibly the simplest design pattern is the singleton, which is a way to provide one and only one object of a particular type. To accomplish this, you must take control of object creation out of the hands of the programmer. One convenient way to do this is to delegate to a single instance of a private nested inner class
    
    java:In the singleton pattern a class can distribute one instance of itself to other classes.
  
  * Can it be made thread-safe?
  
    java: yes, but your java version has to be thread-safe.
    
    python: yes
  
  * Can the singleton instance be lazily instantiated?
  
    python:yes
    
    java:yes
  
* Procedural programming
  * Does the language support procedural programming?
    
    python:yes
    
    java: yes
    
* Functional programming
  * Does the language support functional programming?
  
    python: yes, but it is not very good for functional programming.
    
    java:yes
    
* Multithreading
  * Threads or thread-like abilities
  
    python: only one thread can safely execute code in the interpreter at the same time.
    
    java: java is not a threaded language : its engine and its code don't manage threads to parallelize its own internal work. java doesn't offer threads to users : You can't use threads with the java language natively. 
  
  * How is multitasking accomplished?
    
    java: it hides the complex async work behind a promises-based interface.
    
    python: MultiTasking is a tiny Python library lets you convert your Python methods into asynchronous, non-blocking methods simply by using a decorator.
    








    
   [Go to README.md](README.md)
   
   [Go to code.txt](code.txt)
