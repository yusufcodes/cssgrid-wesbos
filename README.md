# CSS Grid - Wes Bos

## Course Notes 

## 3: CSS Grid Fundamentals
'Grid' allows for you to split up a div into a literal Grid. This allows for you to position items within this area in the specified row and column.

### Getting Started
You must start off with a parent div with the class **container**. 
Any items which belong to the Grid must then be placed as child elements of the parent element, with the class name of **item**.

### CSS Grid Properties
grid-template-columns - define the size and number of columns in the grid.
grid-template-rows - define the size and number of rows in the grid.
grid-gap - adds some margin around each grid element.

## 4: CSS Grid Dev Tools
Solid Line: Explicit Grid Edge
Lighter Dotted Line: Implicit Track
Dashed Line: Explicit Track
Diagonal Dashed Line: Gap

## 5: CSS Grid Implicit vs. Explicit Tracks
Implicit: A row or column that is not specifically defined, created automatically.
Explicit: A row or column that is specifically defined using one of the properties such as grid-template-columns

### Properties
For the following properties, the number of values entered correspond to the number of rows or columns that a size is being defined for.
grid-auto-rows: Defines the size of implicitly created rows
grid-auto-columns: Defines the size of implicitly created columns

## 6: CSS grid-auto-flow Explained
grid-auto-flow allows for you to define exactly what happens when extra rows or columns are added, outside of our explicitly defined sizes (using grid-template-columns/rows).

By default, if we have defined 2 columns for instance, any extra elements will start on a new row. However, if we wanted to create a new column instead, we can set grid-auto-flow to 'column' which will ensure that any new item is always placed in a brand new column.

## Extra Notes
Notes in this section may be from other sources, such as Mozilla Developer Network or CSS-Tricks.


