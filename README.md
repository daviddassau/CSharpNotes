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

#### String building
- String building comes in handy because instead of using concatenation, you can declare something like 
```C#
var sb = new StringBuilder();
sb.Append("David");
sb.Append("Dassau");
sb.ToString();
```
- This will take the two strings I "appended" and print them out.
- In addition, you can use `.AppendLine()` if you want the two things that you appended to show up on different lines, instead of next to each other.




