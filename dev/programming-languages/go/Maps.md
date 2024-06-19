Maps are similar to JavaScript objects, Python dictionaries, and Ruby hashes. Maps are a data structure that provide key->value mapping.

Th zero value of a map is `nil`.

We can create a map by using a literal or by using a `make()` function.

```go
ages := make(map[string]int)
ages["John"] = 30

ages = map[string]int{
 "John": 37,
  "Mary": 21,
}
```

`len()` works on a map.

```go
ages = map[string]int{
  "John": 37,
  "Mary": 21,
}
fmt.Println(len(ages)) // 2
```


### Higher order functions

A programming language is said to have "first-class functions" when functions in that language are treated like any other variable. For example, a function can be passed as an argument to other functions, and can be returned by another function and can be assigned as a value to a variable.

A function that returns a function or accepts a function as input is called a Higher-Order Function.

```go
func add (x, y int) int {
	return x + y
}

func mul (x, y int) int {
	return x * y
}

func aggregate(a, b, c int, arithmetic func(int, int) int) int {
  return arithmetic(arithmetic(a, b), c)
}

func main() {
  fmt.Println(aggregate(2,3,4, add))
  // prints 9
  fmt.Println(aggregate(2,3,4, mul))
  // prints 24
}
```


