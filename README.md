# Memory Game (Nand2Tetris - Jack)
A two-player Memory Matching Game built using the Jack programming language as part of the Nand2Tetris project. The game features multiple difficulty levels, interactive keyboard input handling, dynamic board rendering, and score tracking for competitive gameplay.

## Overview
This project is a **two-player Memory Matching Game** developed using the **Jack programming language** as part of the **Nand2Tetris course**.

The game challenges players to find matching pairs of cards on a grid. It demonstrates core concepts of **Object-Oriented Programming**, **memory management**, and **low-level system interaction** in a constrained environment.

---

## Features

* Two-player gameplay
* Multiple difficulty levels:

  * Level 1 → 2×4 grid (4 pairs)
  * Level 2 → 3×4 grid (6 pairs)
  * Level 3 → 4×4 grid (8 pairs)
* Keyboard-based input system
* Card reveal and matching logic
* Real-time score tracking
* Turn-based gameplay
* Exit option using ESC key
* Game over screen with winner display

---

## Project Structure

```
MemoryGame/
│
├── Main.jack        # Entry point
├── Game.jack        # Core game logic and flow
├── Board.jack       # Grid and card management
├── Card.jack        # Individual card behavior
├── Input.jack       # Keyboard input handling
├── UI.jack          # Display and user interface
```

---

## How It Works

### 1. Game Initialization

* The game starts in `Main.jack`
* A `Game` object is created and executed

### 2. Level Selection

* User selects difficulty using keyboard:

  * `1`, `2`, `3` → Select level
  * `ESC` → Exit

### 3. Board Setup

* Cards are generated in pairs
* Symbols are shuffled using a custom algorithm
* Grid is created based on selected level

### 4. Gameplay Loop

* Players take turns:

  1. Select first card
  2. Select second card
* If cards match:

  * Player earns a point
* Else:

  * Cards are hidden again
  * Turn switches

### 5. Game End

* Game ends when all pairs are matched
* Winner is displayed based on scores

---

## Key Concepts Used

* Object-Oriented Programming (Classes, Methods, Fields)
* Arrays and Memory Allocation
* Keyboard Input Handling (`Keyboard.keyPressed()`)
* Screen Rendering (`Screen`, `Output`)
* Game Loop Design
* State Management
* Basic Randomization (Fisher-Yates Shuffle)

---

## Controls

| Key       | Action            |
| --------- | ----------------- |
| 1 / 2 / 3 | Select level      |
| 0–9       | Enter card number |
| Enter     | Confirm input     |
| Backspace | Delete input      |
| ESC       | Exit game         |

---

## How to Run

1. Open the project in the **Nand2Tetris VM Emulator**
2. Load all `.jack` files
3. Compile the project
4. Run `Main.vm`

---

## Gameplay Preview

* Grid-based card layout
* Player scores displayed at top
* Interactive input for selecting cards

---

## Highlights

* Designed without high-level libraries (pure Jack)
* Manual input handling and validation
* Custom shuffle implementation
* Clean modular architecture

---

## Future Improvements

* Add animations for card flipping
* Add timer-based scoring
* Single-player mode with AI
* Better randomization using improved seed logic

---

## Author

Developed as part of the **Nand2Tetris course project**

---
