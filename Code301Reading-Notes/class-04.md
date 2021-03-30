# CSS GRID
## Grid properties
### Properties for the Parent(Grid Container)
* display : Defines the element as a grid container and establishes a new grid formatting context for its contents.
* grid-template-columns ,
grid-template-rows : Defines the columns and rows of the grid with a space-separated list of values. The values represent the track size, and the space between them represents the grid line.
* grid-template-areas : Repeating the name of a grid area causes the content to span those cells.
* grid-template : A shorthand for setting grid-template-rows, grid-template-columns, and grid-template-areas in a single declaration.
* column-gap
row-gap
grid-column-gap
grid-row-gap :
Specifies the size of the grid lines. You can think of it like setting the width of the gutters between the columns/rows.
* gap
grid-gap :
A shorthand for row-gap and column-gap
* justify-items :
Aligns grid items along the inline (row) axis , This value applies to all grid items inside the container.
* align-items :
Aligns grid items along the block (column) axis , This value applies to all grid items inside the container.
* place-items :
place-items sets both the align-items and justify-items properties in a single declaration.
* justify-content : This property aligns the grid along the inline (row) axis (as opposed to align-content which aligns the grid along the block (column) axis)
* align-content : This property aligns the grid along the block (column) axis (as opposed to justify-content which aligns the grid along the inline (row) axis).
* place-content : place-content sets both the align-content and justify-content properties in a single declaration.
* grid-auto-columns
grid-auto-rows :  Implicit tracks get created when there are more grid items than cells in the grid or when a grid item is placed outside of the explicit grid.
* grid-auto-flow :
If you have grid items that you don’t explicitly place on the grid, the auto-placement algorithm kicks in to automatically place the items. This property controls how the auto-placement algorithm works.
* grid :
A shorthand for setting all of the following properties in a single declaration: grid-template-rows, grid-template-columns, grid-template-areas, grid-auto-rows, grid-auto-columns, and grid-auto-flow
### Properties for the Children (Grid Items)
* grid-column-start
grid-column-end
grid-row-start
grid-row-end : Determines a grid item’s location within the grid by referring to specific grid lines. grid-column-start/grid-row-start is the line where the item begins, and grid-column-end/grid-row-end is the line where the item ends.
* grid-column
grid-row :
Shorthand for grid-column-start + grid-column-end, and grid-row-start + grid-row-end, respectively.
* justify-self :
Aligns a grid item inside a cell along the inline (row) axis (as opposed to align-self which aligns along the block (column) axis)
* align-self :
Aligns a grid item inside a cell along the block (column) axis (as opposed to justify-self which aligns along the inline (row) axis). This value applies to the content inside a single grid item.
* place-self :
place-self sets both the align-self and justify-self properties in a single declaration.