
```
print("Hello, world!")
```
In Swift, this is a complete program.

There is no need to import a library for functionality like outputting text.

There is no main() function because code written at a global scope is used as the entry point for the program.

There's also no need for a semicolon at the end of each statement.


### Variables

Use `let` to make a constant. Use `var` to make a variable.

There is implicit typing. Explicitly typing is optional.

```swift
let name = "Sean" // constant
var score = 10 // variable

let followers = 50 // implicitly typed
let following: Int = 25 // explicitly typed

let availableBalance = 500.0 // implicit double
let availableCredit: Double = 1000 // explicit double
```

Values are never `implicitly` converted to another type

Values can be casted to another type
```swift
let label = "follows " + String(following)
```


Use `""""` for multi-line strings
```swift
let greeting = """
We extend our best wishes to you, inhabitants of another world.
	
With the best of intentions, we look forward to establishing contact with other civilized societies in the universe. We look forward to working together with you to build a better life in this vast universe.
"""
```

Create arrays and dictionaries using brackets `[]` and access their elements by writing the index or key in the brackets.

```swift
var study = ["Jeff", "Pierce", "Shirley", "Britta", "Annie", "Abed", "Troy"]

studyGroup[1] = "Chang"

var occupations = [
	"Michael Scott": "Manager",
	"Dwight Schrute": "Assistant Regional Manager",
	"Angela Martin": "Head of Accounting",
	"Toby Flenderson": "Head of Human Resources"
]

occupations["Dwight Schrute"] = "Assistant to the Regional Manager"
```

Create an empty array or dictionary
```swift
study = []
occupations = [:]

study: [String] = []
occupations: [String: String] = [:]
```

Control flow
```swift
let scores = [75,90,100]
var totalScores = 0

for score in scores {
	if score > 50 {
		totalScores += 3
	} else {
		totalScores += 1
	}
}
```

In an if statement, the conditional must be a Boolean expression

You can write if statement or switch after the equal sign of an assignment or after return, to choose a value based on the condition

```swift
let emoji = if totalScore > 90 {
	"happy"
} else {
	"sad"
}

print("I am", emoji)
```



Functions and closures

Objects and classes

Enumerations and structures

Concurrency


Generics





