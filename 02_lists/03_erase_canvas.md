<!-- Problem Statement
Implement an 'eraser' on a canvas.

The canvas consists of a grid of blue 'cells' which are drawn as rectangles on the screen. We then create an eraser rectangle which, when dragged around the canvas, sets all of the rectangles it is in contact with to white. -->

import tkinter as tk

# Set up the main window
root = tk.Tk()
root.title("Eraser Tool on Canvas")

# Constants for the grid size
CELL_SIZE = 30
GRID_WIDTH = 10
GRID_HEIGHT = 10

# Create a canvas widget
canvas = tk.Canvas(root, width=GRID_WIDTH * CELL_SIZE, height=GRID_HEIGHT * CELL_SIZE, bg="white")
canvas.pack()

# Create a grid of blue cells
cells = []
for i in range(GRID_WIDTH):
    row = []
    for j in range(GRID_HEIGHT):
        x1 = i * CELL_SIZE
        y1 = j * CELL_SIZE
        x2 = x1 + CELL_SIZE
        y2 = y1 + CELL_SIZE
        rect = canvas.create_rectangle(x1, y1, x2, y2, fill="blue", outline="black")
        row.append(rect)
    cells.append(row)

# Create the eraser rectangle
eraser_size = 3 * CELL_SIZE  # Size of the eraser (3 cells wide)
eraser = canvas.create_rectangle(0, 0, eraser_size, eraser_size, fill="red", outline="black", width=2)

# Function to move the eraser and erase cells
def move_eraser(event):
    # Move the eraser based on mouse coordinates
    x = event.x // CELL_SIZE * CELL_SIZE
    y = event.y // CELL_SIZE * CELL_SIZE
    
    # Update eraser position
    canvas.coords(eraser, x, y, x + eraser_size, y + eraser_size)
    
    # Erase cells that the eraser touches
    for i in range(GRID_WIDTH):
        for j in range(GRID_HEIGHT):
            cell_coords = canvas.coords(cells[i][j])
            if (cell_coords[0] < x + eraser_size and cell_coords[2] > x and 
                cell_coords[1] < y + eraser_size and cell_coords[3] > y):
                canvas.itemconfig(cells[i][j], fill="white")  # Set the cell to white

# Bind the mouse drag event to move the eraser
canvas.bind("<B1-Motion>", move_eraser)

# Start the Tkinter event loop
root.mainloop()
