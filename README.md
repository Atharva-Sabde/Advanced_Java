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


### Stream :

`Stream` is a medium , or channel which is able to carry data continuously from input devices to java application and vice versa.

1. Byte-oriented Streams             [ Allows data in the form of bytes ]
    1. Input Stream        ( From input devices to  java program)
    2. Output Stream     ( From java program to output devices)
2. Character-oriented Streams    [ Allows data in the form of characters ]
    1. Reader                  ( From input devices to  java program) 
    2. Writer                   ( From java program to output devices)

Dynamic  Input-Output Approaches:

What is Dynamic input? : When we provide the input data to the java application at runtime, then it is called dynamic input.

1. BufferedReader            [ java.io.BufferedReader ]
    - </>

        CMD → [System.in](http://system.in) →  byte → InputStreamReader → character → BufferedReader → String  → javaAppl .

        `BufferedReader br = new BufferedReader(new InputStreamReader(System.in));`

        InputStreamReader converts the binary data from CMD to character form

        BufferedReader converts the character data from InputStreamReader into String form.

        `readLIne()` → reads whole string

        `read()` → reads only a character

        To take input using Dynamic Input method by BufferReader

        1. Read data as String by using readLine()
        2. Convert data from String type to primitive type by using parseXXX() methods (wrapper classes)

        This method is complex and timeconsuming, so instead of this conversion we use Scanner.
2. Scanner            [ java.util.Scanner]
    - </>
        1. Create Scanner class object.

            `Scanner s = new Scanner(System.in);`

        2. Read dynamic input from Scanner

            (a) To read primitive data as dynamic input :
                      public xxx nextXxx()

                `public int nextInt()`

                `public float nextFloat()`

            (b) To read String data as dynamic input:

                `public String next()`

                `public String nextLine()`

            BufferReader and Scanner needs two instructions to take dynamic input i.e  : 1. Display request message
            2. Read the dynamic input

            BufferReader and Scanner do not provide the security to our data. (passwords , pins)

            To overcome above problems , we use Console.
3. Console       [ java.io.Console]
    - </>

        Displays message waits for user to input data and then take input, all in one single instruction.

        1. Create Console object.
         `public static Console console()` from system class.

            `Console c = System.Console();`

        2. Read Dynamic input through Console:
            1. To display a request message and read String data as dynamic input.

                public String readLine(String message)

                `String uname = c.readLine("Username   : ");`

            2. To display a message and read password data in the form of char[] :

                public char[] readPassword(String message)

                `char [] pwd = c.readPassword( "Password  : ");`

                `String upwd = new String(pwd);` // converts char array into String.
