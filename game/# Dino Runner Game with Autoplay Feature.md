 # Dino Runner Game with Autoplay Feature

This repository contains the code for a Dino Runner game with an autoplay feature. The game is inspired by the popular Chrome dinosaur game and is implemented using an Arduino Uno board and an LCD display.

## Prerequisites

To run this code, you will need the following:

* Arduino Uno board
* LCD display (16x2 character display)
* Breadboard
* Jumper wires
* Resistor (10kΩ)
* Potentiometer (10kΩ)
* Push button

## Setup

1. Connect the LCD display to the Arduino Uno board as follows:

* VCC to 5V
* GND to GND
* SDA to A4
* SCL to A5
`

2. Connect the push button to digital pin 2 of the Arduino Uno board.

3. Connect the autoplay pin to digital pin 1 of the Arduino Uno board.

## Code Overview

The code for the Dino Runner game is written in Arduino C++ and consists of the following main components:

* **Initialization:** The `initializeGraphics()` function initializes the LCD display and creates custom characters for the sprites.
* **Terrain Generation:** The `advanceTerrain()` function shifts the terrain to the left and generates new terrain.
* **Hero Drawing:** The `drawHero()` function draws the hero sprite on the LCD display and checks for collisions.
* **Button Handling:** The `buttonPush()` function is called when the button is pressed and sets the `buttonPushed` flag to `true`.
* **Main Loop:** The `loop()` function is the main game loop and controls the game logic, including hero movement, terrain generation, and collision detection.

## Game Logic

The game logic is relatively simple. The hero can run, jump, and duck to avoid obstacles. The player controls the hero by pressing the button. When the button is pressed, the hero jumps. If the hero is already in the air, pressing the button again will make the hero jump higher.

The terrain is generated randomly and consists of two layers: an upper layer and a lower layer. The hero can run on either layer, but he can only jump from the lower layer. If the

