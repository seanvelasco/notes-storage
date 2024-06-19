


### Date types

DateTime
DataTime someDate = DateTime.now

record

struct

class


**Access modifiers to classes**

public - visible everywhere
private - visible only within the scope
protected
internal
file

classes have methods and also have their access modifiers
- you can't have public methods on a public class

you can also inherit classes and there's a special keyword

abstract means the class is only for inheritance
```c#
public absrtract class BaseClass
{
	public abstract void MyMethod();
}

public class MyClass: BaseClass
{
	public override void MyMethod()
	{
		Console.WriteLine("Hello")
	}
}
```


interfaces
```c#
public interface IMyInterface
{
	void MyMethod();
}

public class MyClass: IMyInterface
{
	public void MyMethod()
	{
		Console.WriteLine("Hello");
	}
}
```

Properties
```c#
public class MyClass
{
	public string MyProperty { get; set; }
	public int OtherProperty { get; private set; }
}
```

readonly properties

```c#
public class MyClass
{
	public string MyProperty => "VALUE";
}
```


constructors and deconstructors
```c# 
public class MyClass
{
	public string ValueA { get; }
	public string ValueB { get; }

	public MyClass(string valueA, string ValueB)
	{
		ValueA = valueA;
		valueB = valueB;
	}

	public void Deconstruct(out string valueA, out string valueB)
	{
		valueA = this.valueA;
		valueB = this.valueB;
	}
}

var instance = new MyClass("one", "two");
var (one, two) = instance;
```

Constructing and deconstructing record types is more trivial

```c#
record MyRecord(string one, string two);

var instance MyRecord("one", "two");

var (one, two) = instance;
```

1. readonly and immutable types should be the default
2. use var to infer types
3. use `is not null` 
4. use pattern matching 
5. use tuples to return multiple values from a method
6. use the `using` statement to dispose of resources properly
7. use LINQ based expressions instead of loops
8. extension methods
9. generics
10. async await
11. 