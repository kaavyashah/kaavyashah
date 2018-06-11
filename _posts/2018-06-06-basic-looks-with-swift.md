---
layout: post
title: "Appearance Basics With Swift"
---
### Tidying the Landscape Orientation
Apps that are in landscape by default do not show the *status bar*. To ensure that the *status bar*
does not show up while the app is loading, go to **Project Settings**, scroll to **Deployment Info**,
find **Status Bar Deployment**, and check **Hide status bar**.

### Images
**Assets.xcassets**, which can be found from the *Navigation area* is a folder that stores all
images that will be used in the app. Often, multiple copies of images are stored as **1x, 2x, and 3x
displays**, where
  * **1x** - low-resolution screens, have no special name
  * **2x** - high-resolution Retina screens (most modern iPhones, iPads, and iPod Touches), denoted
  by filename ending in **@2**
  * **3x** - super high-resolution Retina HD screens (iPhone Plus), denoted by filename ending in **@3**

### Adding a Wallpaper
* open the *storyboard*
* from the **Object Library**, select **Image View** and drag it on the **View Controller**
* in the **Size Inspector**, change X and Y to equal 0, and width to 568 and height to 320 to fit the screen
* from **Attributes Inspector** select the drop down titled **Image** and pick the desired image
* from the **Document Outline**, drag the image title to the top
  * furthest back item is at the top of the list, furthest front item is at the bottom

### Change Label Looks
* select the label from the *storyboard*, go to the **Attributes Inspector** and click on `Color` and
choose the color you want
* `Shadow` from the **Attributes Inspector** determines the shadow
  * ex: set red, green, and blue = 0, opacity 50%, **Shadow Offset** width = 0 and height = 1
* change fonts by clicking the **T** icon next to the **Font** bar
* **Autoshrink** changes the size of the font to fit the label size
* to change the label size to fit around the text, press `Command` and `=` on the keyboard or
go to the **Editor Menu** and click **Size to fit Content**

### Changing Button Looks
* very similar to labels
* **system** button only has label and no border, **custom** button can be styled in any way
* to select an image as the background of the button, from the **Attributes Inspector** find the
**Background** drop down menu and select the desired image
* anything with an **opacity** of less than 100% has transparence
* buttons can have multiple states
  1. default state
  2. highlighted state - while the button is tapped and held down
    * go to **State Config** and selected **Highlighted**
    * change the **Background** field, **Text Color**, and **Shadow Color** if desired
    * select **Reverses on Highlight** to make sure that the effects are present when the label is tapped
    > if unspecified, UIKit will darken a button indicating that it is pressed

### Changing Slider Looks
Though everything above was done with the Interface Builder, the same could be done using source code.  For example,
to set the color of a button one could use `setTitleColor` in `viewDidLoad`.  To change a majority of components of the **slider**
you have to use source code. 
