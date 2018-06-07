---
layout: post
title: "Appearance Basics With Swift"
---
### Tidying the Landscape Orientation
Apps that are in landscape by default do not show the *status bar*. To ensure that the *status bar*
does not show up while the app is loading, go to **Project Settings**, scroll to **Deployment Info**,
find **Status Bar Deployment**, and check **Hide status bar**.

### Adding Images
**Assets.xcassets**, which can be found from the *Navigation area* is a folder that stores all
images that will be used in the app. Often, multiple copies of images are stored as **1x, 2x, and 3x
displays**, where
  * **1x** - low-resolution screens, have no special name
  * **2x** - high-resolution Retina screens (most modern iPhones, iPads, and iPod Touches), denoted
  by filename ending in **@2**
  * **3x** - super high-resolution Retina HD screens (iPhone Plus), denoted by filename ending in **@3**
To add wallpaper, do the following:
  * 
