To declare a class, use the `class` keyword, followed by the class name. Class names should be PascalCase.

```c#
// access modifier - classs - name
public class MyClass
{
	// fields, properties, methods
}
```

Properties define the attributes or data members of a class.

Methods are functions defined within the class that perform actions or operations. They can modify the class' state or provide functionality.

An access modifier precedes the `class`.

### Encapsulation

A class or struct can specify how accessible each its members is to code outside the class or struct. Methods and variables that aren't intended to be used from outside of the class can be hidden to limit the potential for coding errors or malicious exploits.
## Accessibility / access modifiers

Some methods and properties are meant to be called or accessed from code outside a class or struct. Other methods and properties might only be used in the class or struct internally. It's important to limit the accessibility of the code so that only the intended client code can reach it. 

C# provides access modifiers to control the visibility and accessibility of class members. 

**public** - members accessible from any code

**private** - members accessible from within the class

**protected** - members are accessibility within the class and derived classes

**internal** - members are accessible within the same assembly (a group of related classes in the same project)

**protected internal** - members are accessible within the same assemble and derived classes

**private protected** - members are only accessible only from derived classes within the current assembly

The default accessibility is `private`.

### Constructors and initialization

There are several ways to initialize values:
- accept default values
- field initializers
- constructor parameters
- object initliazers

#### Field initializers
```c#
public class Container
{
	private int _capacity = 10;
}
```

#### Constructors
```c#
public class Container
{
	private int _capacity;
	public Container(int capacity) => _capacity = capacity;
}
```
Require callers to provide an initial value


#### Primary constructors
```c#
public class Container(int capacity)
{
	private int _capacity = capacity;
}
```
Adding parameters to the class name defines the *primary constructor*. These parameters are available in the class body, which include its members. You can use them to initialize fields or anywhere else where they're needed.

#### Object initializers

You can also use the required modifier on a property and require callers to use an *object initializer* to set the initial value of the property.

```c#
public class Person
{
	public required string FirstName { get; set; }
	public required string LastName { get; set; }
}

// Notice how this is an object outside the parentheses ()
var p = new Person() { FirstName = "Grace", LastName = "Hopper" }
```

### Class inheritance

Classes fully support inheritance. When you create a class, you can inherit from any other class that isn't defined as sealed. Other classes can inherit from your class and override class virtual methods. Further, you can implement one or more interfaces.

```c#
// this is not a Manager of type type
// this is Manager inherits from Employee
public class Manager : Employee
{
// Employee members are inherited
// new Manager members go here...
}
```

#### Abstract

Classes may be declared abstract, which means that one or more of its methods have no implementation.  Abstract classes cannot be instantiated directly. They serve as base classes for other classes that provide the missing implementation. Classes can also be declared as sealed to prevent other classes from inheriting from them.
### Static

Classes (but not structs and records) can be declared `static`. A static class can only contain only static members. This class can't be instantiated with the `new` keyword.

One copy of the class is loaded into memory at runtime, and its members are accessed through the class name.

```c#
public static class Utilities
{
	public static void PrintMessage(string message)
	{
		Console.WriteLine(message);
	}
}

Utilities.PrintMessage("Hello world!!!");
```

Classes, structs, and records can contain static members. However, a static class cannot contain non-static members.