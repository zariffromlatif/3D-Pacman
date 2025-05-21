# CSE423 Lab Project: 3D Pacman Game
This project is a lab assignment for CSE423: Computer Graphics, implementing a 3D Pacman-style game using Python and OpenGL. The game demonstrates core computer graphics concepts such as 3D rendering, camera perspectives, collision detection, and real-time interaction. Players control a Pacman-inspired character to navigate a maze, avoid enemies, collect power-ups, and shoot bullets to score points, supporting both first-person and third-person camera modes.
Project Objectives

Apply OpenGL for 3D rendering and scene management.
Implement player movement, enemy AI, and collision detection in a 3D environment.
Demonstrate camera control with first-person and third-person perspectives.
Showcase real-time game mechanics, including scoring, lives, and game-over conditions.

# Features

3D Maze Navigation: A 600x600 unit maze with blue walls (50 units high) for exploration.
Player Mechanics: Move Pacman, shoot bullets, and collect power-ups to restore lives.
Enemies: Four red spherical enemies chase the player, respawning at random valid positions.
Power-Ups: Two green cubes restore lives when collected, with a pulsing visual effect.
Camera Modes: Toggle between first-person and third-person views using the mouse.
Game State: Track lives, score, and missed bullets, with game-over triggered by losing all lives or missing 10 bullets.
Animations: Pacman’s mouth animates, and power-ups and bullets pulse for visual feedback.

# Prerequisites
To run the game, ensure the following are installed:

Python 3.x
PyOpenGL (pip install PyOpenGL PyOpenGL_accelerate)
PyOpenGL GLUT (pip install PyOpenGL-GLUT) or system-installed GLUT
A system with OpenGL support

# Installation

Clone the Repository:
git clone https://github.com/zariffromlatif/3D-Pacman.git
cd 3D-Pacman


Install Dependencies: Install required Python packages:
pip install PyOpenGL PyOpenGL_accelerate


Install GLUT (if not already installed):

Windows: GLUT is typically included with PyOpenGL.
macOS: Install FreeGLUT via Homebrew:brew install freeglut


Linux: Install FreeGLUT via your package manager, e.g., for Ubuntu:sudo apt-get install freeglut3 freeglut3-dev





Usage

Run the Game: Execute the main script:
python 3DPacman.py


Game Objective:

Navigate the 3D maze as Pacman.
Shoot enemies (red spheres) with bullets to earn 10 points per hit.
Collect power-ups (green cubes) to restore lives (max 5).
Avoid enemies to prevent losing lives.
The game ends if all lives are lost or 10 bullets miss.
Press 'R' to restart after game over.



Controls

Keyboard:
W: Move Pacman forward
S: Move Pacman backward
A: Turn Pacman left
D: Turn Pacman right
R: Restart the game (when game over)


Arrow Keys (Third-person mode only):
Up: Increase camera height
Down: Decrease camera height
Left: Rotate camera left
Right: Rotate camera right


Mouse:
Left Click: Fire a bullet
Right Click: Toggle between first-person and third-person camera modes



Game Elements

Maze: Defined by outer and inner blue walls, 50 units high.
Player (Pacman): A yellow sphere with an animated mouth, controlled by the player.
Enemies: Four red spheres chasing the player at 0.5 units per frame.
Power-Ups: Two green cubes that pulse and restore one life when collected.
Bullets: White cubes fired by the player, moving at 3 units per frame.
HUD: Displays lives, score, missed bullets, and camera mode.

Technical Details

Libraries: PyOpenGL for rendering, GLUT for window and input handling, and Python’s math, random, and time modules.
Camera:
First-person: Positioned slightly behind Pacman, aligned with its direction.
Third-person: Orbits Pacman at a 200-unit distance, with adjustable height (100–600 units).


Collision Detection: Prevents player, enemies, and bullets from passing through walls.
Game Loop: Updates game state (bullets, enemies, collisions) in an idle function and redraws the scene.

Known Issues

Performance depends on system hardware and OpenGL support.
Simplified collision detection may allow minor overlaps near wall edges.
No sound effects or advanced lighting (lighting disabled for simplicity).

Contributing
This is a lab project for CSE423. Contributions are welcome for academic purposes:

Fork the repository.
Create a feature branch (git checkout -b feature-name).
Commit changes (git commit -m "Add feature").
Push to the branch (git push origin feature-name).
Open a pull request for review.

License
This project is licensed under the MIT License. See the LICENSE file for details.
Acknowledgments

Developed as part of the CSE423: Computer Graphics course.
Inspired by the classic Pacman game.
Built using PyOpenGL and GLUT for 3D rendering and interaction.

