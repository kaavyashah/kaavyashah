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

### Adding Buttons and Objects
* from the *storyboard* go to the **Object Library**
* click on the object desired, for example **Button**, and drag it onto the *storyboard*
* double click to edit the Text

### Make Connections
* from the *storyboard*, click the desired object
* hold the `Control` key and drag up to the desired **View Controller**. A blue line will drag through.
* let go, and a menu will appear, containing **Action Segue** and **Sent Events**
      * **Sent Events** shows actions from source code that can be attached to the *storyboard*
* click on the desired function
* check that the connection was made through the **Connections inspector** or by going to the source code and
clicking on the shaded circle next to `@IBAction func ...`

### Portrait vs. Landscape
* developers use *points*, designers use *pixels*
* **UIKit** works in *points*
* Switch from portrait to landscape
  1. change the view in the *storyboard*
  2. change the **Supported Device Orientations** setting
    * in the **View as:** panel, change the **Orientation**
    * in the Simulator menu bar, click **Hardware** &rightarrow **Rotate Left** or **Rotate Right**
    * Click the blue app icon next to the app name from the top of the **Project navigator**.  Then select
    the **General** tab and locate **Deployment info** and select only the **Device Orientation**.  This prevents
    the screen from switching to the orientations that are not selected if the device is turned around.
