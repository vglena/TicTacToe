## 🎮 Tic-Tac-Toe AI (Minimax Implementation)

This project allows you to play Tic-Tac-Toe against an unbeatable AI using the Minimax algorithm.
The AI always plays optimally, so if both you and the AI play perfectly, the game will always end in a tie.

##  📖 Overview

This program implements a fully functional Tic-Tac-Toe game with AI:

Players take turns placing their symbol (X or O) on a 3x3 grid.

The first player to align three symbols horizontally, vertically, or diagonally wins.

The game ends in a tie if all cells are filled without a winner.

The AI uses Minimax, a recursive decision-making algorithm, to determine the optimal move.

## ⚙️ How It Works

The project contains two main Python files:

1. **tictactoe.py** – Core game logic and AI:

    - `player(board)`: Determines whose turn it is (`X` or `O`).  
    - `actions(board)`: Returns a set of all possible moves `(i, j)` on the board.  
    - `result(board, action)`: Returns a new board after making a move.  
    - `winner(board)`: Returns the winner (`X`, `O`, or `None`).  
    - `terminal(board)`: Returns `True` if the game is over.  
    - `utility(board)`: Returns `1` if X wins, `-1` if O wins, `0` for a tie.  
    - `minimax(board)`: Returns the optimal action `(i, j)` for the current player.


2. runner.py – Pygame-based graphical interface:

Displays the board and moves.

Handles user input via mouse clicks.

Shows current game status and winner.

Allows restarting the game after it ends.
