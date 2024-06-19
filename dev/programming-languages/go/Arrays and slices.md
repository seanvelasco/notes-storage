Arrays are fixed-sized group of variables of the same type.

The type `[n]T` is an array of n values of the type `T`.

To declare an array of 10 integers:
```go
var myInts [10]int

// with an initialized literal
primes := [6]int{2, 3, 4, 5, 6, 11, 13}
```

Slices are dynamically-sized, flexible view of the elements of an array.

The zero value of slice is `nil`.

Slices always have an underlying array. To create a slice on top of an array we can:

```go
arrayname[lowIndex:highIndex]
arrayname[lowIndex:]
arrayname[:highIndex]
arrayname[:]
```

`lowIndex` is inclusive and `highInex` is exclusive.

```go
primes :- [6]int{2, 3, 5, 7, 11, 13}
firstThreePrimes := primes[1:4]
```

Slices hold references to the underlying array. If you take a slice argument, then change it, then the changes made to it will be reflected on the array. It's analogous to passing a pointer to the underlying array.

A Read function can therefore accept a slice argument rather than a pointer and a count. 

### make

Most of the time, we don't need to think about the underlying array of a slice. We can create a new slice using the make function.

```go
// func make([]T, len, cap) []T
mySlice := make([]int, 5, 10)

// the capacity can be omitted
mySlice := make([]int, 5)
```


### len

To ge the number of elements an array or slice contians
```
```

### cap

```
```

The capacity of a slice is the number of elements in the underlying array. Generally, we do not worry about the capacity of a slice because it will automatically grow as needed.



### Variadic functions

Functions can take an arbitrary number of arguments. A variadic function receives the variadic arguments as a slice.

The spread operator allows us to pass a slice into a variadic function.

```go
func concat(strs ...string) string {
	final := ''
	for _, str := range(strs) {
		final += str
	}
	return final
}
```


### append

append() is used to dynamically add elements to a slice.

If the underlying array is not large enough, append() will create a new underlying array and point the slice to it.

Notice that append() is variadic.

## Slice of slices

Slices can hold other slices, effectively creating a matrix, or a 2D slice

```go
rows := [][]int{}
```

### range

Go provides syntactic sugar to iterate easily over elements of a slice.

```go
for INDEX, ELEMENT range SLICE {

}
```


### contains

```go
import "slices"

slices.(badWords, "biatch")
```