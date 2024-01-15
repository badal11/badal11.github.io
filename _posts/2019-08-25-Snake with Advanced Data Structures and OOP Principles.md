---
layout: post
title: Snake with Advanced Data Structures and OOP Principles
date: 2019-08-25 09:56:00-0400
description: 
tags: project
categories: class-project
giscus_comments: false
related_posts: false
featured: false
---

## Snake Game

### Game Overview
Assist the Snake in expanding its size and accumulating points by devouring apples. The game concludes when the Snake collides with the wall.

- Utilization of Canvas API for crafting an interactive UI design.
- Implementation of Arrays Data Structure & Object-Oriented Programming (OOP) principles to construct the Snake and game functions.
- Application of mathematical logic for tasks such as Snake movement, random apple generation, and score incrementation.


1. **Initialization (`init` function):**
   - Gets the canvas element and its context.
   - Sets up canvas width, height, and other variables.
   - Initializes the snake, food, game over flag, and score.
   - Loads images for food and trophy.

2. **Snake Object:**
   - The `snake` object represents the snake in the game.
   - It has properties like initial length, color, cells (body parts), and direction.
   - Methods include `createSnake` (to initialize the snake), `drawSnake` (to draw the snake on the canvas), and `updateSnake` (to update the snake's position).

3. **Key Event Listener:**
   - Listens for arrow key presses to change the snake's direction.

4. **Draw Function (`draw`):**
   - Clears the canvas.
   - Draws the snake and food on the canvas.
   - Displays the score using the trophy image.

5. **Update Function (`update`):**
   - Updates the snake's position based on its direction.
   - Checks if the snake has eaten the food, updates the score, and generates new food.

6. **Random Food Generation (`getrandomfood`):**
   - Generates random coordinates for the food.

7. **Game Loop (`gameloop`):**
   - Checks if the game is over, stops the game loop, and displays a game over alert.
   - Calls the `draw` and `update` functions.

8. **Game Initialization and Loop:**
   - Calls the `init` function to set up the game.
   - Sets up a game loop using `setInterval`, calling the `gameloop` function every 100 milliseconds.

### Conclusion:

This code creates a simple Snake game where the player controls the snake using arrow keys, and the goal is to eat the red food to grow longer. The game ends if the snake collides with the canvas boundaries. The score is displayed, and a trophy image is used for aesthetics.
