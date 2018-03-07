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
- C# is a strongly-typed language, meaning a few things, including how once a variable's data type is declared, it can't be changed
- Variables are typed in camel-case in C#.
- In C#, everything is an instance of a class or structure, and therefore every variable is an instance of some class or structure that has properties and methods
- You can use `StringBuilder()` to append strings together. For instance, you can instantiate one like
  - ```C#
StringBuilder builder = new StringBuilder();
builder.Append("Hello");
``` 
```C#
StringBuilder builder = new StringBuilder();
builder.Append("Hello");
```
- You can convert a string to an int using the `.Parse` method
- With variables, there's such a thing called "implicit" and "explicit" typing. 
  - Implicit typing means you can use the `var` keyword, and the C# compiler will figure out what type you mean based on the assignment.
    - EX: `var name = "David";`
  - Explicit means


