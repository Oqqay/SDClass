import turtle
import random

who = turtle.Turtle()

def leaf():
  setposition(random.randint(-300, 0), random.randint(75, 225))
  who.dot(20, "green")

def ground():
  who.pendown()
  who.seth(0)
  who.color("black", "lightgreen")
  who.begin_fill()
  who.forward(900)
  who.right(90)
  who.forward(450)
  who.right(90)
  who.forward(900)
  who.right(90)
  who.forward(450)
  who.end_fill()




def tree(height, width, leafFromTree):
  who.seth(90)
  who.color("black", "brown")
  who.begin_fill()
  who.pendown()
  who.forward(height)
  who.right(90)
  who.forward(width)
  who.right(90)
  who.forward(height)
  who.right(90)
  who.forward(width)
  who.end_fill()
  who.penup()
  who.right(90)
  who.forward(leafFromTree)


def square(length, angle, move):
  who.forward(length)
  who.right(angle)
  who.forward(length)
  who.right(angle)
  who.forward(length)
  who.right(angle)
  who.forward(length)
  who.right(move)


who.speed(20)
who.setposition(-450,0)
ground()
who.penup()
who.setpos(-225, -225)
tree(300,50, 300)
who.right(90)
who.forward(25)
who.pendown()

for i in range(10):
  who.begin_fill()
  who.color(255, 150, 0)
  square(120, 90, 50)
  who.end_fill()
  who.color(200, 255, 100)
  who.begin_fill()
  square(120, 90, 50)
  who.end_fill()

who.color("black")
for i in range(2):
    who.setpos(50, 0)
    square(120, 90, 50)
#turtle.setpos(50, y=None)
#turtle.color("black", "red")
#turtle.begin_fill()
#turtle.circle(50)
#turtle.end_fill()
