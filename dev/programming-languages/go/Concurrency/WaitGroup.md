


We first initialize an instance of WaitGroup wg.

Then we add 1 to wg to wait for one goroutine to finish.

We then run the goroutine. Inside the goroutine, we make a defer call to wg.Done() to decrement the number of goroutines to wait on.

After the goroutine call, we make sure to block the code execution until WaitGroup is empty by calling wg.Wait()

### Why use WaitGroups over channels?

Using waitgroup is clearer. Using channels is clever.

There are instances when we don't need to use a channel.

```go
  var wg sync.WaitGroup

  for i := 0; i < 5; i++ {
      wg.Add(1)
      go func() {
          defer wg.Done()

          fmt.Println(time.Now(), "start")
          time.Sleep(time.Second)
          fmt.Println(time.Now(), "done")
      }()
  }

  wg.Wait()
  fmt.Println(time.Now(), "exiting...")
```

If the goroutine isn't communicating data to other goroutines (if the goroutines are one-off jobs), using a WaitGroup is desirable.

```go
  ch := make(chan int)

  for i := 0; i < 5; i++ {
      go func() {
          randomInt := rand.Intn(10)
          ch <- randomInt
      }()
  }

  for i := 0; i < 5; i++ {
      fmt.Println(<-ch)
  }
```

The goroutine is sending data back to the channel. In these cases, we don't need to use a WaitGroup because it would be reduntant as receiving already does enough blocking.


----

We typically need to access the WaitGroup inside a goroutine. We pass its pointer because Go is a pass-by-value language.


---

Buffered vs unbuffered channels? Usage