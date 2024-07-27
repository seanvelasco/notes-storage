
q: What's the recommended project structure for a .NET project?

a: 

---

q: Is it common for classes to implement `IAsyncDisposable`?

a:

---

q: Why should there be a separate `Init()` or `Initialize()` method on a class? Why can't we but the `Init()` code in the constructor?

a: Because the constructor is not async, it only runs synchronously.

---

q: Aren't abstract classes just interfaces?

a:

Abstract classes can have both abstract and concrete / implemented methods.

Interfaces only declare method signatures.

Abstract classes have fields. Interfaces do not have fields, but can have static fields or constants

A class can implement multiple interfaces. A class can only inherit from one abstract class.


