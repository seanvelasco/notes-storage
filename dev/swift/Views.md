
### ForEach
```swift
ForEach(1...10, id: \.self) {
	Text("Item \($0)")
}

var items = []

ForEach(items.indices, id: \.self) { item in
	Text(items[item])
}
```

