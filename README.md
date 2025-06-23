# 🎯 Balloon Shooting Game 🎈

A fun, interactive balloon-shooting game developed using **Processing (Java-based language)**. The game challenges players to pop balloons across multiple levels using arrows, with limited ammo, score tracking, and dynamic visuals.

---

## 📌 Overview

This game features:
- Two engaging levels
- Mouse and keyboard interactions
- Score-based progression
- Game over and restart mechanics
- Clean object-oriented structure using multiple classes

> 🔧 Built entirely in **Processing**, a flexible graphical framework for visual arts and simulations.

---

## 🛠️ Core Components

### ✅ `Main` Class

Handles the overall setup, game state management, input control, and rendering:

- **Initialization**: Loads images, sounds, canvas, and game objects.
- **Resetting**: 
  - `resetSketch()`: Resets balloons and scores.
  - `resetArrows()`: Resets player arrows.
- **Game Loop (`draw()`)**:
  - Renders scenes and controls level switching.
  - Calls level-specific logic like `level1()`.
- **Input**: 
  - Mouse: `mousePressed()`, `mouseReleased()`, `mouseClicked()`, `mouseDragged()`
  - Keyboard: `keyPressed()`
- **Exit**:
  - `ex()`: Displays exit button
  - `mouseClicked()`: Detects click on exit to quit

---

### 🏹 `Arrow` Class

Represents the arrow shot by the player:

- **Fields**:
  - `x`, `y`: Coordinates
  - `PApplet part`: Link to main Processing app
- **Functions**:
  - `update()`: Moves the arrow
  - `display()`: Draws the arrow
  - `stop()`: Detects when arrow leaves the screen
  - `getX()`, `getY()`: Accessor methods

---

### 🎈 `Balloon` Class

Handles creation, movement, and popping of balloons:

- **Fields**:
  - Position: `x`, `y`
  - Motion: `yspeed`, `acc`
  - State: `popped`, `level`
  - Images: `photo`, `pop`, `popy`
- **Functions**:
  - `show()`, `showp()`, `showpy()`: Display visuals
  - `moveup()`, `movedown()`, `up()`: Control movement
  - `pop()`, `isPopped()`: Manage state

---

### 🖼️ `Introduction` Class

Controls scene rendering like intro screen, backgrounds, and game over screen.

- **Fields**:
  - Backgrounds: `BG`, `BG_level1`, `BG_level2`, `game_over`
  - `PApplet parent`: Main canvas
- **Functions**:
  - `show()`: Intro screen
  - `show_level1()`, `show_level2()`: Level backgrounds
  - `game_over()`: Game over screen

---

## 🎮 Game Flow

### ▶️ Start
- Intro screen (level `== 0`)
- Press `space` to start

### 🏆 Winning
- **Level 1** complete: `bbscore == 15` → proceed to Level 2
- **Level 2** complete: Final score shown → `levels == 3` (game ends)

### ❌ Losing
- Arrows run out (`ascore == 0`) and not all balloons popped → “Game Over”
- Press `space` to retry the level

### 🚪 Exit
- Click "Exit" button → game closes

---

## 📸 Screenshots

> Add your images here

| Level 1  | Level 2 | 
|----------|---------|
| ![Start](Screenshots/Screenshot%202025-06-23%20051139.png) | ![Level1](Screenshots/Screenshot%202025-06-23%20051253.png)  |


---

*Enjoy the game and happy popping! 🎯🎈*