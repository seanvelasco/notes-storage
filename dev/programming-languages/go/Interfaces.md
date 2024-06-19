
Interfaces are just collections of method signatures.

Important: a type *implements* an interface if it has methods that match the interface's method signatures.

```go
// interface
type geometry interface {
	area() float64
	perimeter float64
}

// example
type rect struct {
	width, height float64
}

// example
type circle struct {
    radius float64
}

// method
func (r rect) area() float64 {
	return r.width * r.height
}

// method
func (r rect) perimeter() float64 {
    return 2*r.width + 2*r.height
}

// rect now has an area() method
// usage
func main() {
	r := rect{width: 3, height: 4}
	fmt.Println("rectangle area:", a.area())
}
```

Both `rect` and `circle` fulfill the `geometry` interface because both can perform `area` and `perimeter`. It can be said therefore that `rect` and `circle` implements `geometry`.

When a type implements an interface, the interface can be used as its type.

Because an empty interface doesn't require a type to have any methods at all, every type automatically implements the empty interface (`interface{}`)

```go 
func sendMessage(msg message) (string, int) {
	return msg, len(msg) * 3
}

type message interface {
	getMessage() string
}

type birthdayMessage struct {
	birthdayTime  time.Time
	recipientName string
}

func (bm birthdayMessage) getMessage() string {
	return fmt.Sprintf("Hi %s, it is your birthday on %s", bm.recipientName, bm.birthdayTime.Format(time.RFC3339))
}

type sendingReport struct {
	reportName    string
	numberOfSends int
}

func (sr sendingReport) getMessage() string {
	return fmt.Sprintf(`Your "%s" report is ready. You've sent %v messages.`, sr.reportName, sr.numberOfSends)
}
```

#### Interfaces are implemented implicitly

A type implements an interface by implementing *all* of its methods.

Unlike in many other programing languages, there is no explicit declaration of intent. There is not `implements` keyword.

Implicit interfaces decouple the definitions of an interface from its implementation. You may add methods to a type and in the process be unknowingly implementing various interfaces.

In Go:
```go
type shape interface {
	area() float64
}

type circle struct{
	radius int
}

func (c *circle) area() float64 {
	return 3.14 * c.radius * c.radius
}

// circle implements area
// circle implicitly implements shape
```

In other programming langauges:
```ts
class Circle implements Shape
```

### Type assertion
### Type switches


Interfaces are not classes. They don't have constructors and deconstructors. Interfaces are not hierarchical.

Interfaces define function signatures, but not underlying behavior.

Interfaces should not have knowledge about the underlying types at design time.
















A value of interface type can hold any value that implements those methods.
