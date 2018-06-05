---
layout: post
title: "WWDC18 I Have This Idea For an App"
---
### View Controller
* use helper methods!
* Variables in the storyboard that have not been connected have an open circle next
to them.
* Closed circles indicate that a connection has been made
* Action method
* to see what a function does, hold down on the `option` key and hover over the function
for a more detailed description
* Xcode has autocomplete
* `Navigation Controller` added on the main `View Controller` allows for the user
to navigate between pages
* `Segues` connect 2 View Controllers
* connect the `View Controller` to a different class with the `Identity Inspector`
  * then, you can connect `@IBOutlet` to the corresponding values

---
### Object Library
* stores all different objects that can be placed in the App
* use the search bar to find objects
* static cells store static data
* create a new `View Controller` for each new display, ex: Leaderboards, Profiles

---
### Connections Inspector
* specific actions, including touch down
  * make connections as one would normally

---
* `SpriteKit` gives more life to buttons
* `MusicKit` incorporates sound into games

---
### Model-View-Controller
* Data represented as Model
* UI represented as View
* UIViewController represented as Controller
* Think about data as a separate entity, separate it away from UI
  * Core Data for storage
  * NSURLSession for web-based data

---
### Auto Layout
##### Make the app be centered vertically and horizontally
* Bottom right of the story board, icon with two horizontal rectangles
  * center the object
* Select multiple labels and apply layout restrictions to all at once
