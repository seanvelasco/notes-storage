
Go enables two styles of concurrent programming - goroutines and channels, which support communicating sequential process (CSP), a model of concurrency in which values are passed between independent activities (goroutines) but variables are for the most part confined to a single activity.

Shared memory multithreading.

### Goroutines

Each concurrently executing activity is called a goroutine.

Consider a program that has two functions - one that does some computation and another that writes some output. Assume neither function calls the other.

A sequential program may call one function and then call the other. But in a concurrent program with two or more goroutines, calls to both functions can be active at the same time.

When a program starts, its only goroutine is the one that calls `main()`. We call it the main goroutine, New goroutiens are created by the `go` statement. Syntactinally, a go statement is an ordinary function or method call prefixed by the keyword go.

A go statement causes the function to be called in a newly created goroutine. The go statement itself completes immediately.

```
f() // call f() and wait for it to return

go f() // create a new goroutine that calls f(); dont wait
```

### Channels

Create a channel
```go
ch := make(chan int)
```

Send data to a channel
```go
ch <- 69
```

Receive data from a channel
```go
v := <- ch
```


A deadlock is when a group of goroutines are all blocking so none of them can continue. This is a common bug we need to watch out for in concurrent programming.


Empty structs are ofen used as tokens. In t his context, a token is a unary value. We do not care what is passed through the channel. We only care when and if it is passed.

We can block and wait until something is sent on a channel using the following syntax.

```go
<- ch
```
This will block until it pops a single item off the channel, then continue, discarding the item.



