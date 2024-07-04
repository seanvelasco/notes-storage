

not all the time do we import swiftui. we only import swiftui when dealing with UI.

for backend code, we dont import swiftui, we use `Foundation`

for things that access the database, we use ``

everything is a struct swiftui

"view" = "behaves like a view"

a view is just a rectangular area on screen that draws something and can get events

view is not a struct. view is something you behave, like a protocol 


confusing -

`some` keyword
https://stackoverflow.com/questions/56433665/what-is-the-some-keyword-in-swiftui

opaque return type

for example, `Collection` can only be used as a generic constraint, not a return type

therefore, we should use `some Collection`

---

thins inside a View, such as body, are called properties

computed property. meaning, these values aren't stored somewhere, these are computed.

---

`VStack` is a struct with parameters

```swift
// normally it appears like VStack is an object
VStack {
	Image(systemName: "globe")
	Text("Hello world")
}

// however, VStack can also have parameters
VStack (...) {
	Image(systemName: "globe")
	Text("Hello world")
}

// the above can be writted like below also
VStack (content: {
	Image(systemName: "globe")
	Text("Hello world")
})
```


----

Functions are also called View modifiers

----

Why do some values start with a dot ?

When working with enums, you can use a dot to refer to a case without repeating the enum name if the type is already known. For example:

```swift
enum Direction {
    case north, south, east, west
}

let direction: Direction = .north
```

Swift allows the use of implicit member expressions to refer to static members of a type when the type context is already clear. This is often used with types like `UIColor` in UIKit:

```swift
let color: UIColor = .red
```

### Closures

Closures in Swift are similar to lambas or anonymous functions.

---

### Trailing closure syntax

You can't delete the parentheses of a function call or a creation of a struct unless you've got a trailing closure syntax

Rather than pass in the closure as a parameter, it can be passed directly after the function inside braces.


```Swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        VStack(alignment: .center, spacing: 10, content: {})
    }
}
```

Because the parameter content is










---

views are just structs, so you can

```swift

```

