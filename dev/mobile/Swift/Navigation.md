Answers the question: how to navigate between views?
### Hierarchical navigation

Example, navigating to a General in Settings

```swift
NavigationView {
	NavigationLink(destination: DetailView()) {
		Text("Go to Detail")
	}
}
```

### Tab-based navigation

This pattern is also called "view preferences"

```swift
TabView {
	HomeView()
		.tabItem {
			Label("Home", systemImage: "house")
		}
	ProfileView()
		.tabItem {
			Label("Profile", systemImage: "person")
		}
}
```

Notice how HomeView is front-and-center in this mode of navigation, and that the label is just a modifier to that view. `.tabItem()` is a modifier that's used within TabView.

This is me just thinking out loud - how is tabItem a modifier of HomeView when HomeView doesn't have the properties that enable navigation. How does TabView, HomeView, and .tabItem relate to each other?

`.tabItem()` is a special since it doesn't affect the presentation or content of the view it modifies. Instead, it tells the parent TabView how to present this view in the 


---

TabView
- container view that manages both the content and the navigation tab
- responsible for switching between different content views and rendering the tab bar
HomeView
- this is the content view
- doesn't know anything about navigation nor being part of a tab interface
.tabItem()
- a modifier, but a special modifier that doesn't affect the content or presentation of the HomeView
- provides metadata to the parent TabView about how to represent HomeView in the tab bar

the .tabItem() doesn't directly modify the view. it's a way of communicating with the TabView