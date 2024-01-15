---
layout: post
title: Tic-Tac-Toe with min max algorithm
date: 2019-08-31 09:56:00-0400
description: 
tags: project
categories: class-project
giscus_comments: false
related_posts: false
featured: false
---

# Ultimate Tic-Tac-Toe with Min-Max Algorithm

This is an implementation of the Tic-Tac-Toe game, where the player can play against the computer. The computer uses the minimax algorithm to make intelligent moves and challenge the player. Below is a brief explanation of the key components of the code:

1. **Constants and Macros:**
    - `COMPUTER`, `HUMAN`: Constants representing the player types.
    - `SIDE`: Length of the Tic-Tac-Toe board.
    - `COMPUTERMOVE`, `HUMANMOVE`: Characters representing moves for the computer and human, respectively.

2. **Function: `showBoard`**
    - Displays the current state of the Tic-Tac-Toe board.

3. **Function: `showInstructions`**
    - Displays instructions for the player to choose a cell numbered from 1 to 9.

4. **Function: `initialise`**
    - Initializes the Tic-Tac-Toe board with empty spaces.

5. **Function: `declareWinner`**
    - Declares the winner based on the current player.

6. **Functions: `rowCrossed`, `columnCrossed`, `diagonalCrossed`**
    - Check if any row, column, or diagonal is crossed by the same player.

7. **Function: `gameOver`**
    - Returns true if the game is over (any row, column, or diagonal is crossed).

8. **Function: `minimax`**
    - Implements the minimax algorithm to calculate the best score for the computer and human.

9. **Function: `bestMove`**
    - Determines the best move for the computer using the minimax algorithm.

10. **Function: `playTicTacToe`**
    - Handles the main game logic, taking turns between the player and the computer.

11. **Function: `main`**
    - The main function initiates the game, allowing the player to choose whether to start first. It then calls `playTicTacToe` accordingly.

**Note:** The program continues to run until the user decides to quit ('n'). The player can choose whether to start first, and the computer uses the minimax algorithm to make optimal moves. The game state is displayed after each move, and the winner or a draw is declared at the end. The user can choose to play again or quit after each game.

## 1. Introduction

Welcome to the Ultimate Tic-Tac-Toe with AI project documentation! This classic game has been given a strategic twist by incorporating the powerful minimax algorithm. Players can enjoy a challenging experience against the computer, where optimal moves are determined using sophisticated AI logic.

## 2. Game Overview

- **Players:** Two players, X and O.
- **Objective:** Align three marks in a horizontal, vertical, or diagonal row to win.
- **AI Enhancement:** Utilizes the minimax algorithm for intelligent decision-making by the computer.

## 3. Combinatorics Insights

Considering board state and accounting for symmetries, there are 138 distinct terminal positions. When "X" makes the first move:
- 91 distinct positions result in victory for "X."
- 44 distinct positions lead to victory for "O."
- 3 distinct positions end in a draw, often referred to as a "cat's game."

## 4. Minimax Algorithm

The minimax algorithm is a decision-making strategy that helps the computer determine optimal moves by evaluating possible outcomes. It explores the game tree and selects moves that maximize its chances of winning and minimize the chances of losing.

## 5. Pseudocode

```plaintext
function minimax(node, depth, isMaximizingPlayer, alpha, beta):
    if node is a leaf node:
        return value of the node
    
    if isMaximizingPlayer:
        bestVal = -INFINITY 
        for each child node:
            value = minimax(node, depth+1, false, alpha, beta)
            bestVal = max(bestVal, value) 
            alpha = max(alpha, bestVal)
            if beta <= alpha:
                break
        return bestVal

    else:
        bestVal = +INFINITY 
        for each child node:
            value = minimax(node, depth+1, true, alpha, beta)
            bestVal = min(bestVal, value) 
            beta = min(beta, bestVal)
            if beta <= alpha:
                break
        return bestVal
```

## 6. Minimax Algorithm Visualization

![Minimax Algorithm Visualization](MiniMax-algorithm.png)


In this Tic-Tac-Toe program, artificial intelligence (AI) is implemented using the minimax algorithm. The minimax algorithm is a decision-making algorithm that helps the computer player make optimal moves by exploring the entire game tree and choosing the move with the highest score. Here's how AI is used in the code:

1. **Function: `minimax`**
    - This function is the core of the AI implementation using the minimax algorithm.
    - It recursively explores all possible moves by simulating each move on a copy of the current board.
    - The function calculates a score for each possible move and returns the best score.
    - The algorithm assumes that the opponent (human player) will also play optimally.

2. **Function: `bestMove`**
    - This function determines the best move for the computer player by calling the `minimax` function for each available empty cell on the board.
    - It iterates over each empty cell, simulates placing the computer's move in that cell, and calculates the score using the minimax algorithm.
    - The move with the highest score is considered the best move, and its position (cell index) is returned.

3. **Main Game Loop: `playTicTacToe`**
    - Inside the main game loop, when it's the computer's turn (`COMPUTER`), the program calls the `bestMove` function to determine the optimal move.
    - The computer then places its move in the selected cell, and the game continues.

In summary, AI is used to enhance the computer player's decision-making in choosing the best move at each turn. The minimax algorithm ensures that the computer explores different possible moves, evaluates their outcomes, and selects the move that leads to the highest score, assuming optimal play from both players. This makes the computer a challenging opponent for the human player.


## 7. Instructions to Run

### Windows

1. Install a C++ compiler.
2. Open the command prompt in the folder where the program is saved.
3. Execute the following commands:
   ```bash
   g++ ai.cpp
   ./a
   ```

### Linux

1. Install a C++ compiler.
2. Open the terminal in the folder where the program is saved.
3. Execute the following commands:
   ```bash
   g++ ai.cpp
   ./a.out
   ```

## 8. Conclusion

Enjoy the strategic challenge of Ultimate Tic-Tac-Toe with AI! May the best player emerge victorious in this enhanced gaming experience. 🎮