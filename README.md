# Advanced_Java

# Testing Commit.

Types of memory in java:

1. Method area
    - Static variables
2. Stack memory
    - local variables
3. Heap  memory
    - Instance and non-static variables
4. Native method stack
5. PC register

Static methods:

1. Static methods can be accessed by two ways, classname.method() and  refrence.method()
2. Static method is normal java method with static keyword, it is a set of instructions and it will be recognized and executed the moment when we access  that method.
3. Static methods are accessed either by using the respectinve class object ref variables  or by using respective class name directly.
4. Static methods don't allow this keyword in its body. but to access current class static methods from some other methods we can use this keyword.
5. Only Static variables can be accessed into static methods.


IN java application , if we want to load byte code, without creating object, we use Class.forName();

When JVM encounters Class.forName() it does following things;

1. Recognize c variable.
2. JVM search for .class files at 3 locations, ( current location | java predefined library | Location referred by class path environment variable )

    If the .class file is not found in the all 3 locations , JVM will raise an Exception (ClassNotFoundException).
    
    
    
> When we start a java program and run it from CMD, cmd generates the inputstream object ,which is predefined
