

```go
bool

string

int  int8  int16  int32  int64
uint uint8 uint16 uint32 uint64 uintptr

byte // alias for uint8

rune // alias for int32
     // represents a Unicode code point

float32 float64

complex64 complex128
```


### Named return values

 >A return statement without arguments returns the named return values. This is known as a "naked" return. Naked return statements should be used only in short functions. They can harm readability in longer functions.
 Tour of Go

Note: always return named return values





## Structs

The order in which the members are defined do not matter. But it is good practice to be consistent to how the struct is defined.

### Anonymous structs in Go

An anonymous struct is just like a normal struct, but it is defined without a name and therefore cannot be referenced elsewhere.

```Go
car := struct {
	maker: string
	model: string
} {
	maker: "tesla",
	model: "model 3"
}

// a normal struct can contain an anonymous struct
type car struct {
	maker string
	model string
	wheel struct {
		radius int
		material string
	}
}
```

In general, named structs are preferred. Use anonymous structs if the struct is only used once and you don't see it being re-used in the future.

Example, an anonymous struct is useful when defining the shape of JSON data in an HTTP handler. This struct is not used elsewhere.

### Embedded structs

Go is not an OOP language. It doesn't support classes or inheritance. However, embedded structs are a way to share fields between struct definitions.

This is magic: unlike nested structs, embedded structs' fields can be accessed at the top-level.

Note: although the fields of the embedded struct are promoted to the top-level, they are still assigned in a *composite literal*. As a TypeScript example, the members can be accessed as if the members are unpacked `{ ...car, bedSize }`, but assigning the members requires you to define it as `{ car: { maker, model }, bedSize }` as if they are nested

```go
type car struct {
  maker string
  model string
}

// truck struct contains all the definitions of car struct
// car struct is embedded on truck struct
type truck struct {
  car
  bedSize int
}

// car is assigned in a composite literal
var personalCar = truck{
	bedSize: 10,
	car: car{
		maker: "toyota",
		model: "fortuner"
	}
}

// fields are promoted to the top-level
personalCar.bedSize
personalCar.maker
personalCar.model
```

### Struct methods in Go

Methods are just functions that have a receiver.

A receiver is a special function parameter. Syntactically, it goes before the name of the function.

Receivers are important because they allow us to define interfaces that our structs and other types can implement.

```Go
type rect struct {
	width int
	height int
}

// this is a method
// (r rect) is a receiver
func (r rect) area() int {
	return r.width * r.height
}

var r = rect{
	width: 5,
	height: 10
}

// rect implements area()
fmt.Println(r.area())
```