🐢 Turtle Crossing
A Python arcade game built with the turtle module where you guide a turtle across a road full of oncoming cars. Survive the traffic, reach the finish line, and advance through increasingly difficult levels.
Demo
╔══════════════════════╗
║     LEVEL: 3         ║
║                      ║
║  ←←←  ←←  ←←←←←    ║
║       🐢             ║
║  ←←←←   ←←   ←←    ║
╚══════════════════════╝
Features

Player-controlled turtle navigating upward across a 600×600 screen
Randomly spawning cars moving left at increasing speeds
Level progression — each time you reach the top, speed increases
Collision detection — game ends on contact with any car
Live scoreboard displaying current level and game over screen

Project Structure
turtle-crossing/
├── main.py          # Game loop and event handling
├── player.py        # Player movement and finish line detection
├── car_manager.py   # Car spawning, movement, and level scaling
└── scoreboard.py    # Level display and game over text
Requirements

Python 3.x (standard library only — no external dependencies)

How to Run
bashpython main.py

Make sure all four .py files are in the same directory.

Controls
KeyAction↑Move turtle up
How It Works
The game loop runs at 10 FPS (time.sleep(0.1)). Each tick:

New cars are randomly spawned on the right edge
All cars move left across the screen
Collision is checked between the player and every car
If the player reaches the top, level increases and cars speed up

Modules
player.py
Handles turtle spawn position, upward movement, finish line detection, and reset to start.
car_manager.py
Manages a list of all active cars, handles random car creation, moves all cars each frame, and increases car speed on level_up().
scoreboard.py
Displays the current level in the top-left corner and renders a centered "GAME OVER" message on collision.
Built With

turtle — Python's built-in graphics module
time — for controlling frame rate

Acknowledgements
Built as part of the 100 Days of Code: The Complete Python Pro Bootcamp by Dr. Angela Yu.
