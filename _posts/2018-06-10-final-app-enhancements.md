---
layout: post
title: "Final App Enhancements"
---
### Support All Screens
In order to make sure that everything stays constant between the many different iOS devices,
it is important to use the *Auto Layout* UIKit.  First make sure that the **Use Safe Area Layout Guides** is
selected to be true in the **File Inspector** for the selected **View Controller**.

For the background, do the following:
  * go to the *storyboard* and select the background **Image View** from the main **View Controller**
  * click the **Add Constraints** button from the bottom of the Xcode window
  * set the top, bottom, left, and right spacing values to equal `0`, and make sure that
  all of the red ticks are enabled
  * select `Add 4 Restraints`

For buttons, do the following:
  * set the button in a general area where you would like it to remain
  * then, select the **Align** menu, and select **Horizontally in Container**, then click
  **Add 1 Restraint**
  * if there are all blue lines around the button, you are good to go. if not, add more restraints by going
  to **Add New Restraints** and make sure they are enabled
  * if the lines around the button are orange, click on the button and then click **Update Frames** from the
  bottom of the **Interface Builder** (in line with **Align** and **Add Constraints**)

For the actual main screen, or a page with many buttons:
  * go to **Add Constraints** and check the boxes next to height and width, and then select
  `Add 2 Restraints`
  * go to **Align** and check **Horizontally in Container** and **Vertically in Container**, then
  `Add 2 Restraints`
  * make the background transparent
