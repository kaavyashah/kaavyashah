---
layout: post
title: "Table Views in Swift"
---
To make it simple, a **table view** is something that shows a list of things.  
Often, table views are used with **navigation controllers**, which allows for multiple,
but ordered and connected screens.  One distinction to make is that a **UITableView**
has only rows, whereas a **UICollectionView** can have multiple rows and multiple
columns.  Additionally, there are two different types of tables - *plain* and *grouped*;
plain tables usually represent objects that are related whereas grouped represent
information that isn't necessarily related, on a grey background.  Do the following to make a table view:
  1. If selected "Single View" when making the app, go to the storyboard and delete
  the View Controller, as it needs to be replaced with a Table View Controller.  
  2. Go to the source code file, and change the first line of actual code so that it
  reads `class ...ViewController: UITableViewController {` because the storyboard and the
  source code must match.  Make sure to change the filename to match the class name.
  3. Drag a Table View Controller onto the storyboard.  Then go to the identity inspector and
  change the **Class** to match your new source code filename.
  4. If the Table View Controller is the first one, make sure to check **Is Initial View Controller**
  from the Attribute Inspector.

Make sure to add prototype cells to the table, and if you want a checklist, select **Checkmark** from
the **Accessory** section from the **Table View Cell**'s attribute inspector.  

###Table View Protocols
Two methods to override are the following:
```
override func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
        return 5
    }

override func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
        let cell = tableView.dequeueReusableCell(withIdentifier: "ChecklistItem", for: indexPath)
        return cell
    }
```
The `tableView(_:numberOfRowsInSection)` determines how many cells are present, while `tableView(_:cellForRowAt)`
is responsible for the ability for cells to be reused, rather than creating new cells each time. The
`dequeueReusableCell` will get a copy of the prototype cell, either new or recycled, and the `indexPath` is
responsible for where the cell is placed.  Using **tags** is a good way to keep track of cells without using
**@IBOutlets** because you want to keep track of multiple cells.
