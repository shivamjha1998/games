# Game Arcade

A collection of 10 hyper-casual browser games built with vanilla HTML5, CSS3, and JavaScript. No frameworks, no dependencies — each game is a single self-contained `.html` file.

## Play

Open `games/index.html` in any modern browser, or serve locally:

```bash
cd games
python3 -m http.server 8000
# open http://localhost:8000
```

## Games

| # | Game | Description | Controls |
|---|------|-------------|----------|
| 01 | **Stack Tower** | Tap to stack blocks — align them perfectly to keep building | Tap / Space |
| 02 | **Color Switch** | Jump through spinning color rings — match your color to pass | Tap / Space |
| 03 | **Flappy Clone** | Tap to flap through pipe gaps without crashing | Tap / Space |
| 04 | **Zigzag Path** | Tap to switch direction on an isometric zigzag path | Tap / Space |
| 05 | **Ball Bounce** | Bounce upward through platforms — don't fall! | Left/Right or touch sides |
| 06 | **Fruit Slice** | Swipe to slice fruits, avoid bombs | Swipe / mouse drag |
| 07 | **2048 Puzzle** | Slide and merge tiles to reach 2048 | Swipe / Arrow keys |
| 08 | **Tap Speed** | Tap as fast as you can in 10 seconds | Tap / Space |
| 09 | **Snake** | Classic snake — eat, grow, don't hit walls or yourself | Swipe / Arrow keys / WASD |
| 10 | **Endless Runner** | Run, jump, and duck past obstacles | Tap/Space = jump, Down = duck |

## Features

- **Zero dependencies** — pure HTML/CSS/JS, no build step
- **Mobile-friendly** — touch controls, responsive scaling, no pinch-zoom
- **Persistent high scores** — saved to localStorage per game
- **60fps animations** — requestAnimationFrame with delta-time
- **Consistent design** — shared color palette and UI patterns across all games

## Technical Details

- 9 games use **Canvas 2D** rendering; 2048 uses **DOM + CSS transitions**
- Internal resolution of 400x700 (portrait), CSS-scaled to fit any screen
- Each game follows a 3-state machine: `title` → `playing` → `gameover`
- Touch events use `preventDefault` with `passive: false` to prevent scroll/zoom interference

## Project Structure

```
games/
  index.html            # Launcher gallery
  01-stack-tower.html
  02-color-switch.html
  03-flappy-clone.html
  04-zigzag-path.html
  05-ball-bounce.html
  06-fruit-slice.html
  07-2048-puzzle.html
  08-tap-speed.html
  09-snake-game.html
  10-endless-runner.html
```
