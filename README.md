# CSS Grid - Wes Bos

## Course Notes 

## 3: CSS Grid Fundamentals
'Grid' allows for you to split up a div into a literal Grid. This allows for you to position items within this area in the specified row and column.

### Getting Started
You must start off with a parent div with the class **container**. 
Any items which belong to the Grid must then be placed as child elements of the parent element, with the class name of **item**.

### CSS Grid Properties

- **grid-template-columns** - define the size and number of columns in the grid.
- **grid-template-rows** - define the size and number of rows in the grid.
- **grid-gap** - adds some margin around each grid element.

## 4: CSS Grid Dev Tools - Mozilla Firefox

- Solid Line: Explicit Grid Edge
- Lighter Dotted Line: Implicit Track
- Dashed Line: Explicit Track
- Diagonal Dashed Line: Gap

## 5: CSS Grid Implicit vs. Explicit Tracks
- Implicit: A row or column that is not specifically defined, created automatically.
- Explicit: A row or column that is specifically defined using one of the properties such as grid-template-columns

### Properties
For the following properties, the number of values entered correspond to the number of rows or columns that a size is being defined for.
- **grid-auto-rows**: Defines the size of implicitly created rows
- **grid-auto-columns**: Defines the size of implicitly created columns

## 6: CSS grid-auto-flow Explained
**grid-auto-flow** allows for you to define exactly what happens when **extra rows or columns are added**, outside of our explicitly defined sizes (using grid-template-columns/rows).

By default, if we have defined 2 columns, any extra elements will start on a **new row**. However, if we wanted to create a new column instead, we can set **grid-auto-flow** to '**column**' which will ensure that any new item is always placed in a brand new column.

## 7: Sizing tracks in CSS Grid

The fr unit is a great unit to use, because it dictates what the Grid should do with the **excess remaining space** of the given elements. This allows for an even distribution of Grid elements, e.g:

```css
.container {
    grid-template-columns: 1fr 1fr 1fr 1fr;
}
```

This will create 4 evenly distributed columns with the contents of your grid.

## 8: CSS Grid Repeat Function

Looking back at the previous example, it can be written in a better way to save typing:

```css
.container {
    grid-template-columns: repeat(4, 1fr);
}
```

## 9: Sizing Grid Items
After selecting a particular grid element via ID/Class, the following properties can be used in relation to the item size:

- **grid-column**
- **grid-row**

We can have an element take up two columns in the grid, making it wider, and also take up two rows, making it longer, with the following code:

```css
.item9 {
    /* 'span' followed by a number tells the grid element how much Grid space it should take relative to it's initial position in the Grid. This follows the Grid Track values which can be seen in the Dev Tools. */
    grid-column: span 2;
    grid-row: span 2;
}
```

## 10: Placing Grid Items

- **grid-column**:
  - grid-column-start: You can specify a track value here to specify where to start at.
  - grid-column-end: You can specify a track value here to specify where to start at.


```css
.class{
    /* Span the item three spaces across the grid, starting at track value 2 and ending at 5. */
    grid-column-start: 2;
    grid-column-end: 5;

    /* Shorthand */
    grid-column: 2 / 5;

    /* Tell the element where to start, and then how large it should be. These can be used together if you only want to define the start OR end point, exclusively. */
    grid-column: 1 / span 2;

    /* Position element to start at the beginning, 1, and end at the last track, which can be picked up as -1.
    This is like 'width: 100%' */
    grid-column: 1 / -1;

    /* Note: To use the above technique, the row or column must be explicitly defined using grid-template-rows/columns - it does not work with implicitly created areas of the grid. */
}
```


```css

```

## Extra Notes
Notes in this section may be from other sources, such as Mozilla Developer Network or CSS-Tricks.


