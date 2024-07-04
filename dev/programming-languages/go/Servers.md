
`w.WriteHeader(http.StatusBadRequest)` only sets the status code of the response to 400. It does not write any content to the response body. If you want to include a response body, you need to manually do it after calling w.WriteHeader by w.Write()

```go
w.WriteHeader(http.StatusBadRequest)
w.Write([]byte("Invalid URL"))
```

`http.Erro(w, "Invalid URL", http.StatusBadRequest)`

This function sets ther status code of the reponse to 400 and writes the provided error mesage to the response body.

It is a convenience function that combines setting the status code and writing the error message in one call.

```go
http.Error(w, "Invalid URL", http.StatusBadRequest)
```

#### When to use each

Use `w.WriteHeader()` when you need to set the status code and then perform additonal actions before writing to ther response body

You want to write a custom response body in a more complex manner orformat.

Use `http.Error()` when you need a simpole way to respond with amn error message and sa status code.

You want to avoid writing adftioanl code to set thjr status code of the response body separately. 


```go

```