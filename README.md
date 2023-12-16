import turtle
import random

def draw_colorful_pattern():
    # Set up the turtle screen
    turtle.bgcolor("black")
    turtle.title("Colorful Geometric Pattern")

    # Draw a colorful geometric pattern
    for _ in range(36):
        draw_random_shape()

    # Hide the turtle
    turtle.hideturtle()

    # Keep the window open
    turtle.mainloop()

def draw_random_shape():
    turtle.speed(2)
    turtle.pensize(2)
    turtle.color(get_random_color())

    shape_size = random.randint(50, 150)
    shape_type = random.choice(["square", "circle", "triangle"])

    if shape_type == "square":
        draw_square(shape_size)
    elif shape_type == "circle":
        draw_circle(shape_size)
    elif shape_type == "triangle":
        draw_triangle(shape_size)

def draw_square(size):
    for _ in range(4):
        turtle.forward(size)
        turtle.right(90)

def draw_circle(size):
    turtle.circle(size)

def draw_triangle(size):
    for _ in range(3):
        turtle.forward(size)
        turtle.left(120)

def get_random_color():
    colors = ["red", "orange", "yellow", "green", "blue", "purple"]
    return random.choice(colors)

# Call the function to draw the colorful geometric pattern
draw_colorful_pattern()
