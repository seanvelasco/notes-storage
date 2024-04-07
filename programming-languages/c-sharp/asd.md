
### Conventions

##### Naming convention

For namespaces, classes, methods, and properties, use `PascalCase`.

For local variables and function parameters, use `camelCase`.

#### Braces

Braces should be placed on new lines for control flow structures.

if (condition) 
{

}
else
{

}

One class per file, with the filename matching the class name.

##### Constants

Constants should be in uppercase.

const GRAVITY = 9.8

Enums should be PascalCase and enum values should be UPPER_CASE.

#### Access modifiers

Use appropriate access modifiers (public, private, protected, internal) for class members based on their visibility and accessibility requirements.




### Namespaces

Namespaces are purely code organization tools but they are valuable when dealing with numerous classes.

For example, the Console class lives in the System namespace

```c#
using System;

// Console becomes available
Console.WriteLine("Hello World");
```

```c#
System.Console.WriteLine("Hello World");
```


Unlike JS where semicolons `;` are optional, they are required in C#. It indicates the end of a statement.

Whitespaces (spaces, tabs, newlines) are ignored in C#. Hence the importance of the semicolon, to determine where statements start and end.

### Variables

To declare a variable, a variable name and a type are needed.

A variable is a named location in memory for staring data. It has three parts: type, name, and value.

```C#
// Declare and assign later:
// decalres the variable name
string name;
name = "Sean";

// Declare and assign in the same line
// decalres the variable name and assigns a value
string name = "Sean";

string motto;
motto = Console.ReadLine();
```

### Compiler errors and debugging





When you read the contents of a variable, the variable's value are copied. They do not share the same reference.






### Types

For integers:
int
short
long
byte
sbyte
uint
ushort
ulong

For single characters:
char

For text:
string

For real numbers:
float
double
decimal

For truth values:
bool

Using `var` for a variable's type tells the compiler to infer its type from the surrounding code.

The Convert() class helps convert one type to another.


### Representing data in binary

### Integer types
the digit separator
choosing between integer types
binary and hexadecimal literals


### Text

### Floating point types
Scientific Notation

### Math and MathF


