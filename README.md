# Conways-Life-Skeleton
An incomplete framework for teaching coding of Conway's Life


This file creates a window and suitable function stubs for creating a game of life.
To see the rules of Life, check the Wiki page:
https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life

Some background info.
The program uses an object called Cell to represent a single square on the board
Values are either 0 (dead) or 1 (alive)

The main app window has a 2D array called cells[][] which contains individual Cell objects.
The cells can be changed by using either Cell.flip() or Cell.setValue()

Students have to complete two functions:

countNeighbours()

    This will receive cells (the 2D array) as a parameter.
    It should use its own position ( held in self.row and self,col ) to find its neighbours
    it should return a count of the number of live cells (Cells where the .value is 1)
    This will test 2D indexing methods and iteration.
    Look out for Index Errors when dealing with cells at the edges!
    
simulate()

    This will require a new grid to hold the temporary values, calculating every one before updating the cells
    This is important, because if they change each cells immediately after calculating the new value
    they will get a different type of action.
    Use the countNeighbours to get the number of neighbours, then apply the rules as follows:
    
* Any live cell with fewer than two live neighbours dies, as if by underpopulation.
* Any live cell with two or three live neighbours lives on to the next generation.
* Any live cell with more than three live neighbours dies, as if by overpopulation.
* Any dead cell with exactly three live neighbours becomes a live cell, as if by reproduction.

    The Simulate function contains a callback which will make the function repeat until the Stop button is pressed.
    
Possible Extensions:
* Create a Clear All Button
* Create a Save State / Load state button
