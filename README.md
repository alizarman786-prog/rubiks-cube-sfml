## Why I Built This Project

I built this Rubik’s Cube simulator for my CS100 course, but the idea came from my own interest rather than just an assignment requirement. I have always been curious about how a Rubik’s Cube works behind the scenes, especially how each move affects multiple parts of the cube at the same time.

When I started the project, I thought it would be a simple graphics task, but I quickly realized the real challenge was in the logic. Every rotation changes several faces, and keeping everything consistent made me think more deeply about data structures and how to manage state properly.

I also wanted to go beyond basic C++ assignments and build something that combined logic with graphics. Using SFML helped me see my work visually, which made the learning process more engaging.

In the end, this project helped me improve my problem solving skills and gave me a better understanding of how complex systems can be designed and implemented from scratch.

# Rubik's Cube Simulator

A Rubik's Cube Simulator developed in C++ using the SFML graphics library as a CS100 semester project.

## Project Overview

This project simulates the behavior of a standard 3×3 Rubik's Cube and allows users to perform rotations on any face of the cube in real time. The goal was to recreate the mechanics of a physical Rubik's Cube while providing a simple graphical interface for interaction and visualization.

The cube is displayed as an unfolded cube net. If you imagine holding a real Rubik's Cube with the Green face facing you and the White face on top, the simulator presents the cube as if it has been unfolded onto a flat surface, making it easier to visualize rotations and color movements.

## Features

* Interactive Rubik's Cube simulation
* Clockwise and counterclockwise face rotations
* Real-time graphical rendering using SFML
* Random cube scrambling
* Instant cube reset to solved state
* Keyboard-controlled gameplay
* Accurate edge and face transformation logic

## How It Works

The cube is represented internally using a three-dimensional character array:

```cpp
char cube[6][3][3];
```

Each of the six faces is stored as a 3×3 matrix:

| Face   | Color |
| ------ | ----- |
| White  | W     |
| Green  | G     |
| Red    | R     |
| Blue   | B     |
| Orange | O     |
| Yellow | Y     |

When the program starts, every face is initialized with a single color, representing a solved Rubik's Cube.

### Rotation Logic

The most important part of the project is the rotation system.

Whenever a user rotates a face:

1. The selected face's 3×3 matrix is rotated.
2. The corresponding rows and columns of neighboring faces are updated.
3. The cube state is refreshed and rendered again.

Separate functions were implemented for:

* Clockwise face rotation
* Counterclockwise face rotation
* Adjacent edge movement
* Complete face transformations

This ensures that every move behaves exactly like it would on a real Rubik's Cube.

## Controls

| Key                   | Action                                |
| --------------------- | ------------------------------------- |
| W                     | Rotate White face clockwise           |
| G                     | Rotate Green face clockwise           |
| R                     | Rotate Red face clockwise             |
| B                     | Rotate Blue face clockwise            |
| O                     | Rotate Orange face clockwise          |
| Y                     | Rotate Yellow face clockwise          |
| Left Shift + Face Key | Rotate selected face counterclockwise |
| S                     | Scramble cube                         |
| Space                 | Reset cube                            |
| Esc                   | Exit program                          |

## Technologies Used

* C++
* SFML (Simple and Fast Multimedia Library)
* Object-Oriented Programming Concepts
* Matrix Manipulation Algorithms

## Challenges Faced

One of the biggest challenges during development was implementing the rotation logic correctly.

Rotating a face does not only affect the selected face itself—it also changes specific rows and columns on four adjacent faces. Ensuring that every edge moved correctly while preserving the cube's state required careful planning, testing, and debugging.

Another challenge was creating a visual representation that clearly displayed the cube's current state while remaining intuitive for users.

## What I Learned

Through this project I gained hands-on experience with:

* Multi-dimensional arrays
* Matrix transformations
* Graphics programming with SFML
* Event-driven programming
* Algorithm design
* Debugging complex state-based systems
* Problem-solving using object-oriented principles

This project helped me understand how data structures and graphical applications can work together to simulate real-world objects.

## Future Improvements

Potential enhancements include:

* Animated face rotations
* Mouse-based controls
* Cube-solving algorithms
* Move history tracking
* Timer and statistics system
* Different cube sizes (2×2, 4×4, etc.)
* Improved 3D visualization


## Author

Developed as a CS100 Semester Project using C++ and SFML.

Thank you for checking out this project.
