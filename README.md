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

2. **runner.py** – Pygame-based graphical interface:

    - Displays the board and moves.  
    - Handles user input via mouse clicks.  
    - Shows current game status and winner.  
    - Allows restarting the game after it ends.

## 🧩 File Structure
```text
tic-tac-toe-ai/
│
├── tictactoe.py         # Core game logic and Minimax AI
├── runner.py            # Pygame interface for playing
├── requirements.txt     # Dependencies
├── LICENSE              # MIT License
└── README.md            # Documentation (this file)

```
## 🧠 Algorithm Details

### Minimax Algorithm

The **Minimax algorithm** ensures the AI plays optimally:

- **Maximizing player (X)** tries to maximize the score.  
- **Minimizing player (O)** tries to minimize the score.  

---

### Utility Values

- **`+1`→ X wins**  
- **`−1` → O wins**  
- **`0` → Tie**
---
### Logic Flow

1. Check if the board is in a terminal state.  
2. Generate all possible moves.  
3. Recursively evaluate each move:  
   - Maximize the score if it's X's turn.  
   - Minimize the score if it's O's turn.  
4. Return the move that leads to the optimal outcome.

### 🧩 Board Representation

The board is represented as a **3x3 2D list** in Python:

```python
board = [
    [X, O, None],
    [None, X, O],
    [O, None, X]
]

```
- `X` and `O` represent players.
- `None` represents an empty cell.

### ▶️ Usage

**1. Clone the repository**
```python
git clone https://github.com/yourusername/tic-tac-toe-ai.git
cd tic-tac-toe-ai
```
**2. Install dependencies**
```python
pip install -r requirements.txt
```
**requirements.txt**
```python
pygame==2.6.0
```
**3. Run the game**
```python
python runner.py
```
**4. Gameplay**
- Choose your player: `X` or `O`.
- Click on an empty square to place your move.
- The AI responds automatically with the optimal move.
- When the game ends, you will see:
    "Game Over: X wins."
    "Game Over: O wins."
    "Game Over: Tie."
- Click **“Play Again”** to restart the game.

### 📊Example Gameplay
```python
Choose your player: X
You place X in the top-left corner
Computer places O in the center
You place X in the top-center
Computer places O in the bottom-right
...
Game Over: Tie
``` 
### 💡 Notes

- The AI cannot be beaten; it will always play optimally.
- The game handles full boards and detects ties automatically.
- Minimax uses deep copies to ensure the original board is not modified during recursion.
- You can test the logic without the GUI by using tictactoe.py functions directly.

### 🧩 Dependencies / Requirements

- Python 3.8 or higher
- Pygame (pip install pygame)
- No other external libraries required

### 🏁Credits

Inspired by CS50’s Introduction to Artificial Intelligence with Python (Project 0: Tic-Tac-Toe).
Adapted to include a Pygame graphical interface for interactive play.

### 📄 License
```text
MIT License

Copyright (c) 2025

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM,
DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```


