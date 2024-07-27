
*Some noob questions I asked while learning Swift*

--- 

Q: I have a list item on a list, and when I tap on that list item, I want to navigate to a certain view. How to I navigate to that view? The list item must also have an arrow indicating navigation.

A: Wrap the list item with NavigationLink(). This can also be used for when you want to navigate to another view on a button click.

---

Q: Why doesn't List appear when inside ScrollView?

A: Because both are supposed to be used as a root view that wraps other views. So we either use only a ScrollView or a List - never together.

---

Q: Why does ScrollView take up the whole screen while VStack only take up a portion of the screen?

A: Because ScrollView is **expanding**, while VStack is **hugging**. Expanding views always use 100% of the width and height, unless they are constrained. Hugging views just take up the width and height of the content, unless we use a frame modifier that explicitly sets their width and height.

--- 

Q: How to conditionally add a modifier to a view?

A: We can't. In this case, we create a custom modifier. Or if possible, we can do `.modifier(isDisabled ? doThis : orElseThis)`

---

Q: When should we `.clipShape(.rect(cornerSize: 12))` or just `.cornerSize(12)`? They appear identical, but what is the difference?

A: ...

---
Q: ScrollView starts with 100% of the width. The moment we introduce Text, the ScrollView width shrinks to the width of the Text. When Text is wrapped with a VStack, the width stays the same. When it is wrapped with a LazyVStack, the width becomes 100%. What is the explanation for this behavior?