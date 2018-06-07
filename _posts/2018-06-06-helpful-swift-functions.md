---
layout: post
title: "Helpful Swift Functions"
---
This is just a page where I am going to store Swift functions that I have come across,
and think I may use in the future.  Kind of just a personal cheat sheet.

```
print()
```
Prints string parameters

```
let alert = UIAlertController(title: "An Alert", message: "Alert message", preferredStyle: .alert)
let action = UIAlertAction(title: "OK", style: .default, handler: nil)
alert.addAction(action)
present(alert, animated: true, completion: nil)
```
`UIAlertController` sets up an alert with the according title, message, and style.  The `UIAlertAction` determines what the
button in the alert says(`title`), the style(`style`), and what should happen after the button is
pressed(`handler`).  `addAction` connects the alert to the action and then presents the alert.

```
arc4random_uniform(100)
```
Selects random integer between 0 and 99, non-inclusive of the 100
