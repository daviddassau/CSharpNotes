# C Sharp Notes

## This is where I will keep my general notes on C#

#### Getting Started
- Each class in C# is a member of what's called a "namespace"
- When writing `Console.Write();` and `Console.WriteLine();` the difference is simple:
  - `Console.Write();` will display whatever is in the parenthesis
  - `Console.WriteLine();` will do the same, but will also append a new line at the end of the text

#### Language Fundamentals
- C# is a strict object-oriented language
- All values are stored as objects, and an object is an area of memory that stores data and behaviors
- Objects in C# are instances of things called `classes` and `structures`
- A `method` is just like a function in a non-object-oriented language. It's a member of a classes and structures.

#### Declaring Variables
- Each variable has a data type, and that data type dictates what you can put in that variable
- There are different types of variables, including: `string`, `int`, `double`, and `bool`.
  - `string`s handle basically anything that's not strictly always going to be a number. 
  - `int`s are always going to be a number. However, you can use the `.Parse` method to convert a number into a string.
  - `double`s are going to be numbers with decimal places.
  - `bool`s are going to be true/false variables.
- C# is a strongly-typed language, meaning a few things, including how once a variable's data type is declared, it can't be changed
- Variables are typed in camel-case in C#.
- In C#, everything is an instance of a class or structure, and therefore every variable is an instance of some class or structure that has properties and methods
- You can use `StringBuilder()` to append strings together. For instance, you can instantiate one like
```C#
StringBuilder builder = new StringBuilder();
builder.Append("Hello");
```
- You can convert a string to an int using the `.Parse` method.
  - EX: `int.Parse("15")` will convert the string "15" to the number 15.
- With variables, there's such a thing called "implicit" and "explicit" typing. 
  - Implicit typing means you can use the `var` keyword, and the C# compiler will figure out what type you mean based on the assignment.
    - EX: `var name = "David";`
  - Explicit means

#### Working with Strings
- You can convert a string to all uppercase or lowercase, which comes in handy with working with passwords. For example, you can declare `var password = "Password";`, and then do `password.ToUpper();` and it will convert the string Password to PASSWORD. You can obviously do the opposite with `ToLower()`.
- Another important part of strings is the `Substring()`. You can declare a variable like `var dickens = "It was the best of times, it was the worst of times.";` and then do `dickens.Substring(4, 8)`. This will return `as the b`. So basically you're saying that you want everything in between the 4th character and 8th character.
- You can also use the `.Length()` method to get back the total amount of characters in that string.

#### String Building
- String building comes in handy because instead of using concatenation, you can declare something like 
```C#
var sb = new StringBuilder();
sb.Append("David");
sb.Append("Dassau");
sb.ToString();
```
- This will take the two strings I "appended" and print them out.
- In addition, you can use `.AppendLine()` if you want the two things that you appended to show up on different lines, instead of next to each other.

#### Parsing Strings as Numbers
- You can use the `.TryParse()` method, which takes in two parameters, to test and see if you can indeed parse the string you give it.
  - For instance, you can do `int.TryParse("12345", out result)`, which will return true, because you can in fact parse out that number. However, if you were to throw a comma in the middle of the string you pass in, it will give you false.
  
#### Constants and Enumerators
- You can use enumerators if you want to use numbers to represent values in your program
```C#
enum weekDays { Monday, Tuesday, Wednesday, Thursday, Friday }
var someday = weekDays.Monday;
```
- For the enum `weekDay` Monday will be represented by 0. However, you can actually assign it a specific number, like this:
```C#
enum weekDays { Monday = 1, Tuesday, Wednesday, Thursday, Friday }
```

#### Dates and Times
- `DateTime.Now` will give you the time right now.
- You can assign any specific date, like your birthday, to a variable:
```C#
var birthday = new DateTime(1986, 01, 02);
```

#### Working with Classes
- Inside a class, you can create a `field`, which is an instance variable
```C#
string SchoolName;
```
- If you want, you can go ahead and "initialize" it by adding a getter and setter. When you do this, you're saying that your field has an auto-property, meaning that it's set but it has no particular value.
```C#
string SchoolName { get; set; }
```
- An Access Modifier is designed to limit the visibility of properties, methods, fields, and anything else so you can't accidentally or unintentionally change something. There are 4 types of access modifiers:
  - Public: this means that the variable can be seen outside of the class it belongs to
  - Private: this means that the variable can only be seen inside of its class
  - Protected
  - Internal
- A Constructor is something that will run immediately when an object is instantiated. A contructor can look something like this:
```C#
public School()
{
  Name = "Untitled School";
  PhoneNumber = "555-1234";
}

public School(string SchoolName, string SchoolPhoneNumber)
{
  Name = SchoolName;
  PhoneNumber = SchoolPhoneNumber
}
```
- **Methods**, sometimes called functions in other languages, are used to manipulate data from your properties, fields, variables, etc.
```C#
public float AverageThreeScores(float a, float b, float c)
{
  var result = (a + b + c) / 3;
  return result;
}
```
- This method is going to take in three float variables. Then, inside the method, we create a variable called `result` and assign the math operation to it. Nothing will happen and the name of the method will remain red-lined until you `return` something. In this case, we just return the variable `result`. In addition, if you don't necessarily need to return something, you can use the return type `void` instead of float/int/string/etc.
- **Function Bodied Expressions** is a new feature to C#, and it's just a different, shorter way of writing things such as methods. You should really only use them to return simple things; you wouldn't want to use them for executing loops or anything too complicated. For instance, you can re-write the method from above like this:
```C#
public float AverageThreeScores(float a, float b, float c) => (a + b + c) / 3;
```
- **Static methods** are methods that you can call without instantiating the class. These can be convienient if you just need to do a quick computation or expose something that can be used without instantiation.
