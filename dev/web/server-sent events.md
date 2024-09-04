Client-side implementation for server-sent events are almost identical to websockets. However, unlike websockets, server-sent events are a one-way connection.

### Server

### Client

To open a connection to the server to begin receiving recents, create an EventSource object

```javascript
const sse = new EventSource("https://api.sean.app", {
	withCredentials: false
})

// listen to message events
sse.onmessage = (event) => {
	console.log(event.data)
}

// listen to custom events
// event with field set to "notification"
sse.addEventListener("notification", (event) => {
	console.log(event.event)

	const payload = JSON.parse(event.data)
})

// error handling
sse.onerror = (error) => {
	console.error(error)
}
```

### Event Stream format

The event stream is a simple stream of text data which must be encoded using UTF-8.

Messages in the event stream are separated by a pair of newline characters.

A colon as the first character of a line is a comment and is ignored.

### Fields

-   event - string key used for dispatching events
-   data
-   id
-   retry

links

-   AI

Back-pressure and cancellation with streams
