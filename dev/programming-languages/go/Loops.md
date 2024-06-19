
```go
for INITIAL; CONDITION; AFTER {

}
```

`INITIAL` is run once and can create variables used within the scope of the loop

`CONDITION` is checked before each iteration. If the condition doesn't pass then the loop breaks

`AFTER` is run after each iteration

```go
for i := 0; i < 10; i++ {
	fmt.Println(i)
}
```


