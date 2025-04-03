# 🎨 **Etch-A-Sketch App (Python Turtle Graphics)**  

This project is a **Python-based Etch-A-Sketch App** that allows users to **draw on the screen using keyboard controls**. It is built using the **Turtle module** in Python, which provides simple tools for creating graphics.  

---

## 🚀 **How It Works**  
- **Control a Turtle (Pen) using Keyboard Keys** to move forward, backward, and rotate.  
- **Press "C" to clear the screen and reset the turtle to the center**.  
- The turtle moves **like an Etch-A-Sketch**, drawing lines as it moves.  

---

## 🖥 **Controls**  
| Key | Action |
|-----|--------|
| `W` | Move **forward** |
| `S` | Move **backward** |
| `A` | Turn **left** (counterclockwise) |
| `D` | Turn **right** (clockwise) |
| `C` | **Clear** the screen and reset |

---

## 📜 **Code Explanation (Step-by-Step)**  

### 📌 **1. Importing Required Modules**  
```python
from turtle import Turtle, Screen
```
- **Turtle module** is imported to create the drawing canvas and control movements.  
- **Screen module** is used to listen for key presses.  

---

### 🐢 **2. Creating the Turtle and Screen**  
```python
timmy = Turtle()  # Creates a turtle object named 'timmy'
screen = Screen()  # Creates a screen object
```
- `Turtle()` creates the **pen (turtle)** that will be controlled.  
- `Screen()` sets up the **window where drawing will happen**.  

---

### 🎮 **3. Defining Movement Functions**  

```python
def move_forwards():
    timmy.forward(10)
```
- Moves the turtle **forward by 10 pixels** when called.

```python
def move_backwards():
    timmy.backward(10)
```
- Moves the turtle **backward by 10 pixels**.

```python
def turn_left():
    timmy.left(10)
```
- Rotates the turtle **left (counterclockwise) by 10 degrees**.

```python
def turn_right():
    timmy.right(10)
```
- Rotates the turtle **right (clockwise) by 10 degrees**.

```python
def clear():
    timmy.clear()  # Clears all drawings on the screen
    timmy.penup()  # Lifts the pen to avoid drawing while moving to home
    timmy.home()  # Resets the turtle back to the center (0,0)
    timmy.pendown()  # Puts the pen back down
```
- **Clears the screen** and **resets the turtle position** to the center.

---

### ⌨️ **4. Assigning Key Bindings**  

```python
screen.listen()  # Start listening for key presses
screen.onkey(move_forwards, "w")  # Calls move_forwards() when 'w' is pressed
screen.onkey(move_backwards, "s")  # Calls move_backwards() when 's' is pressed
screen.onkey(turn_left, "a")  # Calls turn_left() when 'a' is pressed
screen.onkey(turn_right, "d")  # Calls turn_right() when 'd' is pressed
screen.onkey(clear, "c")  # Calls clear() when 'c' is pressed
```
- **`screen.listen()`** → Activates the screen’s ability to detect key presses.  
- **`screen.onkey(function, "key")`** → Binds a function to a specific key.  

---

### 🖥 **5. Keeping the Window Open**  
```python
screen.exitonclick()
```
- Waits for the **user to click on the screen** before closing the window.  
- Prevents the program from exiting immediately after running.  

---

## 📚 **Python Concepts Used in This Code**  
✅ **Turtle Graphics** → Used to control the turtle’s movement and draw on the screen.  
✅ **Functions (`def`)** → Encapsulates movement logic in separate reusable functions.  
✅ **Event Listeners (`screen.onkey()`)** → Detects keypress events and triggers actions.  
✅ **Conditional Execution** → Clears the screen and resets the position when the user presses "C".  

---

## 🎯 **Conclusion**  
This **Etch-A-Sketch App** is a fun way to practice **event handling, functions, and Turtle graphics** in Python!  
You can enhance it by:  
- **Changing movement distance** (increase/decrease `timmy.forward(10)`).  
- **Adding more controls** (e.g., change color, increase/decrease pen size).  
- **Allowing user-defined drawing styles** (e.g., dashed lines, different shapes).  

👉 **Fork the repo and experiment with new features!** 🚀
