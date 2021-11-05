# C# (C-Sharp)

# Table of contents
1. [Comments](#Comments)
2. [Variables](#Variables)
3. [Constants](#Constants)  
4. [Identifiers](#Identifiers)  
5. [Data Types](#Data-Types)  
    5. 1. [Numbers](#Numbers)  
    5. 2. [Booleans](#Booleans)  
    5. 3. [Characters](#Characters)  
    5. 4. [Strings](#Strings)  
6. [Type Casting](#Type-Casting)
7. [Output](#Output)
8. [User Input](#User-Input)
9. [Operators](#Operators)  
    9. 1. [Arithmetic Operators](#Arithmetic-Operators)  
    9. 2. [Assignment Operators](#Assignment-Operators)  
    9. 3. [Comparison Operators](#Comparison-Operators)  
    9. 4. [Logical Operators](#Logical-Operatorss)  
10. [Math](#Math)
11. [conditional statements](#conditional-statements)
12. [Loops](#Loops)
13. [Break and Continue](#Break-and-Continue)
14. [Arrays](#Arrays)




## Comments <a name="Comments"></a>

Single-line Comments 

    // This is a comment
    
Multi-line Comments 

    /* The code below will print the words Hello World
    to the screen, and it is amazing */

## Variables <a name="Variables"></a>

Variables can be writen with ***var*** and the compiler will automatacly detect the varibale type 

    var name = "My Name"; // the var will be a string type
    var number = 10; // the var will be a intergen

Variable Types

    int - stores integers (whole numbers), without decimals, such as 123 or -123
    double - stores floating point numbers, with decimals, such as 19.99 or -19.99
    char - stores single characters, such as 'a' or 'B'. Char values are surrounded by single quotes
    string - stores text, such as "Hello World". String values are surrounded by double quotes
    bool - stores values with two states: true or false
    
Declaring Variables

    type variableName = value;
    
    Examples:

    // This will create an integer variable and assing it the value of 1
    int MyNumber = 1;
    
    // This will create a string variable named MyString and assing it the value of Bob
    string MyString = "Bob";
    
    // This will create a string variable named MyString but with no value
    string MyString
    // a value can be assing to it latter
    MyString = "Bob"
    
    Others:

    int myNum = 5;
    double myDoubleNum = 5.99D;
    char myLetter = 'D';
    bool myBool = true;
    string myText = "Hello";
    
Display Variables
    
    // To combine both text and a variable, use the + character:
    string name = "John";
    Console.WriteLine("Hello " + name);
    
    // You can also use the + character to add a variable to another variable:
    string firstName = "John ";
    string lastName = "Doe";
    string fullName = firstName + lastName;
    Console.WriteLine(fullName);
    
    // For numeric values, the + character works as a mathematical operator.
    int x = 5;
    int y = 6;
    // Print the value of x + y
    Console.WriteLine(x + y);
    
Declare Multiple Variables(Same Type)
    
    VarType VarName = value, VarName = value, VarName = value;
    VarType VarName, VarName, VarName;

    // example
    int x = 5, y = 6, z = 50;
    Console.WriteLine(x + y + z);
    
    // or assing values latter
    string var1, var2, var3

## Constants <a name="Constants"></a>

Declaring Constants
    
    Const VarType variableName = value;
    
    // If you dont waht the variable to be chnaged you can make it a contant by placing Const before the variable type
    const int myNum = 15;
    
## Identifiers <a name="Identifiers"></a>

All C# variables must be identified with unique names.
These unique names are called identifiers.
Identifiers can be short names (like x and y) or more descriptive names (age, sum, totalVolume).

Note: It is recommended to use descriptive names in order to create understandable and maintainable code:

    // Good
    int minutesPerHour = 60;

    // OK, but not so easy to understand what m actually is
    int m = 60;
    
 ## Data Types <a name="Data-Types"></a>
 
 As explained in the variables chapter, a variable in C# must be a specified data type:
 
    Data Type       Size            Description
    int             4 bytes	        Stores whole numbers from -2,147,483,648 to 2,147,483,647
    long	        8 bytes	        Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807
    float	        4 bytes	        Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits
    double	        8 bytes	        Stores fractional numbers. Sufficient for storing 15 decimal digits
    bool	        1 bit	        Stores true or false values
    char	        2 bytes	        Stores a single character/letter, surrounded by single quotes
    string	        2 bytes char	Stores a sequence of characters, surrounded by double quotes
    
### Numbers <a name="Numbers"></a>

Number types are divided into two groups:

***Integer types*** stores whole numbers, positive or negative (such as 123 or -456), without decimals. Valid types are ***int*** and ***long***. Which type you should use, depends on the numeric value.

***Floating point types*** represents numbers with a fractional part, containing one or more decimals. Valid types are ***float*** and ***double***.

    The float data type can store fractional numbers from 3.4e−038 to 3.4e+038. 
    Note that you should end the value with an "F":

    The double data type can store fractional numbers from 1.7e−308 to 1.7e+308. 
    Note that you can end the value with a "D" (although not required):

    A floating point number can also be a scientific number with an "e" to indicate the power of 10:

    // float example
    float myNum = 5.75F;
    Console.WriteLine(myNum);
    
    // Double Example
    double myNum = 19.99D;
    Console.WriteLine(myNum);
    
    // scientific number Example
    float f1 = 35e3F;
    double d1 = 12E4D;
    Console.WriteLine(f1);
    Console.WriteLine(d1);
    
 ### Booleans <a name="Booleans"></a>
 
 A boolean data type is declared with the bool keyword and can only take the values ***true*** or ***false*** in lower case.
 
    bool isCSharpFun = true;
    bool isFishTasty = false;
    Console.WriteLine(isCSharpFun);   // Outputs True
    Console.WriteLine(isFishTasty);   // Outputs False

However, it is more common to return boolean values from boolean expressions, for conditional testing

You can use a comparison operator, such as the greater than (>) or the equal to (==) operator to find out if an expression (or a variable) is true:

    int x = 10;
    int y = 9;
    Console.WriteLine(x > y); // returns True, because 10 is higher than 9
    Console.WriteLine(10 > 9); // returns True, because 10 is higher than 9
    Console.WriteLine(x == 10); // returns True, because the value of x is equal to 10
    Console.WriteLine(10 == 15); // returns False, because 10 is not equal to 15
    
### Characters <a name="Characters"></a>

The char data type is used to store a single character. The character must be surrounded by ***single quotes***, like ***'A'*** or ***'c'***:

    char myGrade = 'B';
    Console.WriteLine(myGrade);
    
### Strings <a name="Strings"></a>

The string data type is used to store a sequence of characters (text). String values must be surrounded by ***double quotes*** like ***"hello"***.

    string greeting = "Hello World";
    Console.WriteLine(greeting);
    
A string in C# is actually an object, which contain properties and methods that can perform certain operations on strings. For example, 

The length of a string can be found with the Length property:

    string txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
    Console.WriteLine("The length of the txt string is: " + txt.Length);

There are many string methods available, for example ***ToUpper()*** and ***ToLower()***, which returns a copy of the string converted to uppercase or lowercase:

    string txt = "Hello World";
    Console.WriteLine(txt.ToUpper());   // Outputs "HELLO WORLD"
    Console.WriteLine(txt.ToLower());   // Outputs "hello world"

You can also use the ***string.Concat()*** method to concatenate two strings:

    string firstName = "John ";
    string lastName = "Doe";
    string name = string.Concat(firstName, lastName);
    Console.WriteLine(name);

or just use the + operator

    string name = firstName + lastName;
    
Another option of string concatenation, is string interpolation, which substitutes values of variables into placeholders in a string. 
Note that you do not have to worry about spaces, like with concatenation:

    string firstName = "John";
    string lastName = "Doe";
    string name = $"My full name is: {firstName} {lastName}";

You can access the characters in a string by referring to its index number inside square brackets [].

This example prints the first character in myString:

    // Note: String indexes start with 0: [0] is the first character. [1] is the second character, etc.
    string myString = "Hello";
    Console.WriteLine(myString[0]);  // Outputs "H"

Special Characters

Because strings must be written within quotes, C# will misunderstand this string, and generate an error:

    string txt = "We are the so-called "Vikings" from the north."; // error

The solution to avoid this problem, is to use the backslash escape character.

    string txt = "We are the so-called \"Vikings\" from the north."; // ok

The backslash (\) escape character turns special characters into string characters:

    Escape character       Result           Description
    \'                      '               Single quote
    \"                      "               Double quote
    \\                      \               Backslash

Other useful escape characters in C# are:

    Code        Result
    \n          New Line
    \t          Tab
    \b          Backspace

## Type Casting <a name="Type Casting"></a>
Type casting is when you assign a value of one data type to another type.

In C#, there are two types of casting:

***Implicit Casting*** (automatically) - converting a smaller type to a larger type size
char -> int -> long -> float -> double

***Explicit Casting*** (manually) - converting a larger type to a smaller size type
double -> float -> long -> int -> char

    //Implicit casting is done automatically when passing a smaller size type to a larger size type:
   
        int myInt = 9;
        double myDouble = myInt;       // Automatic casting: int to double

        Console.WriteLine(myInt);      // Outputs 9
        Console.WriteLine(myDouble);   // Outputs 9

    //Explicit casting must be done manually by placing the type in parentheses in front of the value:
   
        double myDouble = 9.78;
        int myInt = (int) myDouble;    // Manual casting: double to int

        Console.WriteLine(myDouble);   // Outputs 9.78
        Console.WriteLine(myInt);      // Outputs 9

    //It is also possible to convert data types explicitly by using built-in methods, such as 
    // Convert.ToBoolean, Convert.ToDouble, Convert.ToString, Convert.ToInt32 (int) and Convert.ToInt64 (long):
    
        int myInt = 10;
        double myDouble = 5.25;
        bool myBool = true;

        Console.WriteLine(Convert.ToString(myInt));    // convert int to string
        Console.WriteLine(Convert.ToDouble(myInt));    // convert int to double
        Console.WriteLine(Convert.ToInt32(myDouble));  // convert double to int
        Console.WriteLine(Convert.ToString(myBool));   // convert bool to string

## Output <a name="Output"></a>
    
    Console.WriteLine() // This will output on seperate lines 
    Console.Write() // This will output on the same line 

## User Input <a name="User Input"></a>

### Get User Input / Numbers
You have already learned that Console.WriteLine() is used to output (print) values. Now we will use Console.ReadLine() to get user input.

In the following example, the user can input his or hers username, which is stored in the variable userName. Then we print the value of userName:

    // Type your username and press enter
    Console.WriteLine("Enter username:");

    // Create a string variable and get user input from the keyboard and store it in the variable
    string userName = Console.ReadLine();

    // Print the value of the variable (userName), which will display the input value
    Console.WriteLine("Username is: " + userName);
    
User Input Numbers are handled diferantly, the Console.ReadLine() method returns a string.

Therefore, you cannot get information from another data type, such as int.

you need to convert using Type Casting. by using one of the Convert.To methods:


    Console.WriteLine("Enter your age:");
    int age = Convert.ToInt32(Console.ReadLine());
    Console.WriteLine("Your age is: " + age);
    
## Operators <a name="Operators"></a>

### Arithmetic Operators <a name="Arithmetic-Operators"></a>

Arithmetic operators are used to perform common mathematical operations:

    Operator                Name                                        Description	Example
    +   Addition            Adds together two values                    x + y	
    -   Subtraction         Subtracts one value from another            x - y	
    *   Multiplication      Multiplies two values                       x * y	
    /   Division            Divides one value by another                x / y	
    %   Modulus             Returns the division remainder              x % y	
    ++  Increment           Increases the value of a variable by 1      x++	
    --  Decrement           Decreases the value of a variable by 1      x--
    
### Assignment Operators <a name="Assignment-Operators"></a>

Assignment operators are used to assign values to variables.

    Operator            Example             Same As
    =                   x = 5               x = 5
    +=                  x += 3              x = x + 3
    -=                  x -= 3              x = x - 3
    *=                  x *= 3              x = x * 3
    /=                  x /= 3              x = x / 3
    %=                  x %= 3              x = x % 3
    &=                  x &= 3              x = x & 3
    |=                  x |= 3              x = x | 3
    ^=                  x ^= 3              x = x ^ 3
    >>=                 x >>= 3             x = x >> 3
    <<=                 x <<= 3             x = x << 3
    
### Comparison Operators <a name="Comparison-Operators"></a>

Comparison operators are used to compare two values:

    Operator        Name                            Example
    ==              Equal to                        x == y
    !=              Not equal                       x != y
    >               Greater than                    x > y
    <               Less than                       x < y
    >=              Greater than or equal to        x >= y
    <=              Less than or equal to           x <= y
    
    
### Logical Operators <a name="Logical-Operators"></a>

Logical operators are used to determine the logic between variables or values:

    Operator        Name                Description                                                 Example
    &&              Logical and         Returns true if both statements are true                    x < 5 &&  x < 10
    ||              Logical or          Returns true if one of the statements is true               x < 5 || x < 4
    !               Logical not         Reverse the result, returns false if the result is true     !(x < 5 && x < 10)
    
## Math <a name="Math"></a>

The C# Math class has many methods that allows you to perform mathematical tasks on numbers.

    Method              Description                                                     Example
    Math.Max(x,y)       method can be used to find the highest value of x and y:        Math.Max(5, 10);
    Math.Min(x,y)       method can be used to find the lowest value of of x and y:      Math.Min(5, 10);
    Math.Sqrt(x)        method returns the square root of x:                            Math.Sqrt(64);
    Math.Abs(x)         method returns the absolute (positive) value of x:              Math.Abs(-4.7);
    Math.Round()        rounds a number to the nearest whole number:                    Math.Round(9.99);
    
## Conditional Statements <a name="Conditional-Statements"></a>

C# has the following conditional statements:

Use ***if*** to specify a block of code to be executed, if a specified condition is true.   
Use ***else*** to specify a block of code to be executed, if the same condition is false.   
Use ***else if*** to specify a new condition to test, if the first condition is false.   
Use ***switch*** to specify many alternative blocks of code to be executed.   

***if*** (Case Sensative)

    if (condition1)
    {
      // block of code to be executed if condition1 is True
    } 
    else if (condition2) 
    {
      // block of code to be executed if the condition1 is false and condition2 is True
    } 
    else
    {
      // block of code to be executed if the condition1 is false and condition2 is False
    }
    
There is also a ***short-hand if else***, which is known as the ternary operator because it consists of three operands. It can be used to replace multiple lines of code with a single line. It is often used to replace simple if else statements:

    variable = (condition) ? expressionTrue :  expressionFalse;
    
    // example:
    int time = 20;
    string result = (time < 18) ? "Good day." : "Good evening.";
    Console.WriteLine(result);
    
Use the ***switch*** statement to select one of many code blocks to be executed.

This is how it works:

The ***switch*** expression is evaluated once     
The value of the expression is compared with the values of each ***case***   
If there is a match, the associated block of code is executed
Otherwise the ***default:*** code will execute  
When C# reaches a ***break*** keyword, it breaks out of the switch block.This will stop the execution of more code and case testing inside the block.

    switch(expression) 
    {
      case x:
        // code block
        break;
      case y:
        // code block
        break;
      default:
        // code block
        break;
    }

The example below uses the weekday number to calculate the weekday name:

    int day = 4;
    switch (day) 
    {
      case 1:
        Console.WriteLine("Monday");
        break;
      case 2:
        Console.WriteLine("Tuesday");
        break;
      case 3:
        Console.WriteLine("Wednesday");
        break;
      case 4:
        Console.WriteLine("Thursday");
        break;
      case 5:
        Console.WriteLine("Friday");
        break;
      case 6:
        Console.WriteLine("Saturday");
        break;
      case 7:
        Console.WriteLine("Sunday");
        break;
    }
    // Outputs "Thursday" (day 4)


## Loops <a name="Loops"></a>

***while loop***
The ***while loop*** loops through a block of code as long as a specified condition is True:

    while (condition) 
    {
      // code block to be executed
    }
    
In the example below, the code in the loop will run, over and over again, as long as a variable (i) is less than 5:

    int i = 0;
    while (i < 5) 
    {
      Console.WriteLine(i);
      i++;
    }

***do/while loop***
The ***do/while loop*** is a variant of the while loop. This loop will execute the code block once, before checking if the condition is true, then it will repeat the loop as long as the condition is true.

    do 
    {
      // code block to be executed
    }
    while (condition);

The example below uses a do/while loop. The loop will always be executed at least once, even if the condition is false, because the code block is executed before the condition is tested:

    int i = 0;
    do 
    {
      Console.WriteLine(i);
      i++;
    }
    while (i < 5);
    
***for loop***
When you know exactly how many times you want to loop through a block of code, use the ***for*** loop instead of a while loop:

    for (statement 1; statement 2; statement 3) 
    {
      // code block to be executed
    }
    
Statement 1 is executed (one time) before the execution of the code block.  
Statement 2 defines the condition for executing the code block.  
Statement 3 is executed (every time) after the code block has been executed.  

The example below will print the numbers 0 to 4:

    for (int i = 0; i < 5; i++) 
    {
      Console.WriteLine(i);
    }
    
***foreach loop***
There is also a ***foreach*** loop, which is used exclusively to loop through elements in an array:

    foreach (type variableName in arrayName) 
    {
      // code block to be executed
    }

The following example outputs all elements in the cars array, using a foreach loop:

    string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
    foreach (string i in cars) 
    {
      Console.WriteLine(i);
    }
    
### Break and Continue <a name="Break-and-Continue"></a>

***Break***  
You have already seen the break statement used in an earlier chapter of this tutorial. It was used to "jump out" of a switch statement.  
The break statement can be used to "jump out" of a switch statement but also to jump out of a loop.  

This example jumps out of the loop when i is equal to 4:

    for (int i = 0; i < 10; i++) 
    {
      if (i == 4) 
      {
        break;
      }
      Console.WriteLine(i);
    }


***Continue***  
The continue statement breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.

This example skips the value of 4:

    for (int i = 0; i < 10; i++) 
    {
      if (i == 4) 
      {
        continue;
      }
      Console.WriteLine(i);
    }
 

Break and Continue in While Loop
You can also use break and continue in while loops:

    //Break Example
    int i = 0;
    while (i < 10) 
    {
      Console.WriteLine(i);
      i++;
      if (i == 4) 
      {
        break;
      }
    }


    //Continue Example
    int i = 0;
    while (i < 10) 
    {
      if (i == 4) 
      {
        i++;
        continue;
      }
      Console.WriteLine(i);
      i++;
    }
    
### Arrays <a name="Arrays"></a>

***Create an Array***

Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value.

    // To declare an array, define the variable type with square brackets:
    string[] cars;

    //To insert values to it, we can use an array literal - place the values in a comma-separated list, inside curly braces:
    string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

    //To create an array of integers, you could write:
    int[] myNum = {10, 20, 30, 40};

***Access the Elements of an Array***

You access an array element by referring to the index number.   
This statement accesses the value of the first element in cars:

    string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
    Console.WriteLine(cars[0]);
    // Outputs Volvo

Note: Array indexes start with 0: [0] is the first element. [1] is the second element, etc.

***Change an Array Element***   
To change the value of a specific element, refer to the index number:

    cars[0] = "Opel";
    Example
    string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
    cars[0] = "Opel";
    Console.WriteLine(cars[0]);
    // Now outputs Opel instead of Volvo

***Array Length***   
To find out how many elements an array has, use the Length property:

    string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
    Console.WriteLine(cars.Length);
    // Outputs 4

***Loop Through an Array***   
You can loop through the array elements with the for loop, and use the Length property to specify how many times the loop should run.

The following example outputs all elements in the cars array:

    string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
    for (int i = 0; i < cars.Length; i++) 
    {
      Console.WriteLine(cars[i]);
    }
 
***The foreach Loop***   
There is also a foreach loop, which is used exclusively to loop through elements in an array:

    foreach (type variableName in arrayName) 
    {
      // code block to be executed
    }

The following example outputs all elements in the cars array, using a foreach loop:

    string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
    foreach (string i in cars) 
    {
      Console.WriteLine(i);
    }
 

The example above can be read like this: for each string element (called i - as in index) in cars, print out the value of i.

If you compare the for loop and foreach loop, you will see that the foreach method is easier to write, it does not require a counter (using the Length property), and it is more readable.

***Sort Arrays***   
There are many array methods available, for example Sort(), which sorts an array alphabetically or in an ascending order:


    // Sort a string
    string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
    Array.Sort(cars);
    foreach (string i in cars)
    {
      Console.WriteLine(i);
    }

    // Sort an int
    int[] myNumbers = {5, 1, 8, 9};
    Array.Sort(myNumbers);
    foreach (int i in myNumbers)
    {
      Console.WriteLine(i);
    } 

***System.Linq Namespace***   
Other useful array methods, such as Min, Max, and Sum, can be found in the System.Linq namespace:

    using System;
    using System.Linq;

    namespace MyApplication
    {
      class Program
      {
        static void Main(string[] args)
        {
          int[] myNumbers = {5, 1, 8, 9};
          Console.WriteLine(myNumbers.Max());  // returns the largest value
          Console.WriteLine(myNumbers.Min());  // returns the smallest value
          Console.WriteLine(myNumbers.Sum());  // returns the sum of elements
        }
      }
    }
 
***Other Ways to Create an Array***   
If you are familiar with C#, you might have seen arrays created with the new keyword, and perhaps you have seen arrays with a specified size as well. In C#, there are different ways to create an array:

    // Create an array of four elements, and add values later
    string[] cars = new string[4];

    // Create an array of four elements and add values right away 
    string[] cars = new string[4] {"Volvo", "BMW", "Ford", "Mazda"};

    // Create an array of four elements without specifying the size 
    string[] cars = new string[] {"Volvo", "BMW", "Ford", "Mazda"};

    // Create an array of four elements, omitting the new keyword, and without specifying the size
    string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

It is up to you which option you choose. In our tutorial, we will often use the last option, as it is faster and easier to read.

However, you should note that if you declare an array and initialize it later, you have to use the new keyword:

    // Declare an array
    string[] cars;

    // Add values, using new
    cars = new string[] {"Volvo", "BMW", "Ford"};

    // Add values without using new (this will cause an error)
    cars = {"Volvo", "BMW", "Ford"};

