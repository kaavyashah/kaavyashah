---
layout: post
title: "Xcode and Swift Introduction"
---
### Create a New App
Open `Xcode`, and decide the project template. Then follow instructions that lead to you choose
a project name, team, language (in most cases here `Swift`).  Select **Use Core Data**, **Include Unit Tests**,
and **Include UI Tests** accordingly. Then decide where to save the project folder, and if you want to create
a **Git repository** on your Mac. Click **Create** to finish creating.

### Run Project
Press the `Run` button in the top left corner (looks like a play button).
You can select which device you would like to work with by going to the bottom of the `Interface Builder`
and selecting **View as:** which will open up a panel with all other iOS device options
  * Make sure to press the **Stop** button to stop a simulation, before recompiling

### Important Parts of Xcode
* left pane of the window is **Navigator area**
  * row of icons lets you choose which navigator pane you are on
  * default is **Project navigator** - shows files in Project
* `Main.storyboard` is the original **Interface Builder**
  * where you add user interface objects that create the UI, the **storyboard**
* top right corner has 3 buttons with rectangles inside. each:
  1. hides or shows the **Navigator** (left panel)
  2. hides or shows the **Debug** area (bottom panel)
  3. hides or shows the **Utilities** (right panel)
* **Object Library**
  * located at bottom of **Utilities** pane, third button on the row
* **Document Outline** shows the components of the *storyboard*
  * to show the **Document Outline** next to the **Navigator area** select the toggle button in the bottom left
  corner of the **Interface Builder**
* **Connections inspector** shows all made connections
  * select the arrow-shaped button at the top left of the **Utilities** pane
* **Attributes inspector** controls the specifics of objects ex: color, values, etc.
  * icon that looks like a downwards arrow from the top of the **Utilities** pane
* **Project Settings** can be navigated to by clicking on the blue icon next to the app title at
the top of the **Navigator Area**

### Adding Buttons and Objects
* from the *storyboard* go to the **Object Library**
* click on the object desired, for example **Button**, and drag it onto the *storyboard*
* double click to edit the Text

### Make Connections
There are many different ways to make connections.
1. Method 1:
  * from the *storyboard*, click the desired object
  * hold the `Control` key and drag up to the desired **View Controller**. A blue line will drag through.
  * let go, and a menu will appear, containing **Action Segue** and **Sent Events**
      * **Sent Events** shows actions from source code that can be attached to the *storyboard*
  * click on the desired function
2. Method 2:
  * open the *storyboard*, hold `control` and click on object
  * from the pop-up menu that appears, find **Referencing Outlets**
  * click open circle next to **New Referencing Outlet** and drag to **View Controller**
  * select desired connection
3. Method 3:
  * open the *storyboard*, click on the object
  * go to the **Connections inspector**
  * drag from **New Referencing Outlet** to yellow circle at the top of the `storyboard`
  * choose the desired connection from the pop-up
* check that the connection was made by:
  * through the **Connections inspector** or by going to the source code and
  clicking on the shaded circle next to `@IBAction func ...`
  * open the *storyboard*, hold `control` and click on object, pop-up menu that appears shows all connections
* to see all made connections, right click on **View Inspector** from the *storyboard*

### Portrait vs. Landscape
* developers use *points*, designers use *pixels*
* **UIKit** works in *points*
* Switch from portrait to landscape
  1. change the view in the *storyboard*
  2. change the **Supported Device Orientations** setting
    * in the **View as:** panel, change the **Orientation**
    * in the Simulator menu bar, click **Hardware** which opens **Rotate Left** or **Rotate Right**
    * Click the blue app icon next to the app name from the top of the **Project navigator**.  Then select
    the **General** tab and locate **Deployment info** and select only the **Device Orientation**.  This prevents
    the screen from switching to the orientations that are not selected if the device is turned around.

### Objects, Data, and Methods
Swift is *object oriented*
* **Objects** - building blocks of program, each object is responsible for one part of the program
* **Data** - contains something, ex: button itself, color and size of button
* **Methods** - responsible for functionality, does something

All methods start with the word `func` and have parenthesis
```
@IBAction func showAlert() {
  ...
}
```
In order to have a function take in parameters, place the parameter inside of the parentheses.  If it will
always be a certain object, make the connection from the object to the method.
```
@IBAction func sliderMoved(_ slider: UISlider) {
  print("Slider value is \(slider.value)")
}
```

### Variables and Constants
**Variables** must have a specific data type and are created using `var`.
The scope of the variables determine where it can be accessed, and are the following:
  1. *Global scope* - accessible through  duration of app
  2. *Instance scope* - accessible through duration of object
  3. *Local scope* - accessible through duration of method
**Constants** are like variables, but can never change. They are created using `let`.
