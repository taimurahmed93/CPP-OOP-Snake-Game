# CPP-OOP-Snake-Game

A classic **Snake** game implemented in **C++ using Object-Oriented Design (OOD)**.  
Built with a bottom-up OOD approach using reusable building blocks for board positions and list-based snake movement.

> Course Project: COMPENG 2SH4 (McMaster University)

---

## Features
- Classic Snake gameplay:
  - 4-direction movement
  - boundary **wraparound**
  - random food generation
  - snake **growth** on food consumption
  - **self-collision** detection (game over)
  - score tracking
  - **Multi-food support** (multiple food items active at once)
  - **Special food effects** (e.g., bonus score, speed changes, temporary effects)
- Clean OOD architecture (no procedural-style implementation)
- Clean OOD architecture (no procedural-style implementation)
- Dynamic memory handled safely (Rule of 3/5/6 considerations for heap members)

---

## Architecture (OOD)
This project is built around a few core classes required by the project design:

- `objPos`  
  Represents a single “cell” on the game board: (x, y) + ASCII symbol.
- `objPosArrayList`  
  Custom array-list of `objPos`. Used to track the snake body as an ordered list.
- `GameMechs`  
  Container for game state: board size, input buffer, score, exit/lose flags, etc.
- `Player`  
  Snake logic: movement FSM, list-based body movement, food collision, self-collision.

The snake body movement uses a list trick:
- insert new head at the next position
- remove tail (unless food was eaten)

(Design workflow and class responsibilities are outlined in the project manual.)

---
