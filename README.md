
# 🐍 Multi-Style Snake Generator

[![Marketplace](https://img.shields.io/badge/Marketplace-Multi--Style--Snake-green?logo=github)](https://github.com/marketplace)
[![Build](https://github.com/Pro-Bandey/multi-style-snake-action/actions/workflows/snake.yml/badge.svg)](https://github.com/Pro-Bandey/multi-style-snake-action/actions)

Generate beautiful, highly customized GitHub contribution snakes with a single action. This action doesn't just make one snake; it generates **four distinct styles** featuring unique shapes, backgrounds, and **multi-snake effects**.

## 🌟 Features

- **Auto-Username Detection:** No need to hardcode your name; it automatically analyzes the repository owner.
- **Multiple Shapes:** Blocks (Squares), Rounds (Circles), Triangles, and 10-point Stars.
- **Multi-Snake Effects:** Uses CSS injection to create **Twin** and **Triple** snake visuals.
- **Enhanced Labels:** Month names are styled and clearly visible above the grid.
- **Theme Variety:** Includes Light, Dark, Ocean, and Dracula/Neon themes.

---

## 🖼️ Gallery (Styles Included)

| Style | Preview | Shape |
| :--- | :--- | :--- |
| **Twin Snakes** | ![Twin Snakes](https://raw.githubusercontent.com/Pro-Bandey/multi-style-snake-action/output/twin-snakes.svg) | Blocks + Shadow |
| **Triple Neon** | ![Triple Neon](https://raw.githubusercontent.com/Pro-Bandey/multi-style-snake-action/output/triple-snake.svg) | Blocks + Double Shadow |
| **Disco Rounds** | ![Disco Rounds](https://raw.githubusercontent.com/Pro-Bandey/multi-style-snake-action/output/disco-snake.svg) | Circles (Animated) |
| **Star Power** | ![Star Snake](https://raw.githubusercontent.com/Pro-Bandey/multi-style-snake-action/output/star-snake.svg) | 10-Point Stars |

---

## 🚀 Quick Start

1. Create a new repository (or use your Profile README repo).
2. Create a file at `.github/workflows/snake.yml`.
3. Paste the following code:

```yaml
name: Generate Snake

permissions:
  contents: write
  pages: write
  id-token: write

on:
  schedule:
    - cron: "0 */12 * * *" # Runs every 12 hours
  workflow_dispatch: # Allows manual trigger

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Generate Snakes
        uses: Pro-Bandey/multi-style-snake-action@v1 # Use the version you published
```

---

## 🛠️ How to Display on Your Profile

Once the action runs, it creates an `output` branch. Add the following Markdown to your `README.md` to show off your snakes:

```markdown
### My Contribution Snakes

#### Twin Style (The Shadow Follower)
![Snake](https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPO/output/twin-snakes.svg)

#### Neon Triple Style
![Snake](https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPO/output/triple-snake.svg)

#### Star Style
![Snake](https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPO/output/star-snake.svg)
```
*> Note: Replace `YOUR_USERNAME` and `YOUR_REPO` with your actual details.*

---

## 🎨 Style Breakdown

### 1. The Twin Snake
Features a primary green snake followed by a purple "ghost" snake using CSS filters.
- **Shapes:** Classic Blocks.
- **Best For:** Clean, minimal profiles with a twist.

### 2. Triple Neon
One main Cyan snake with Magenta and Yellow shadows, creating a "squad" effect.
- **Background:** Deep Black.
- **Best For:** Dark-themed profiles.

### 3. Disco Rounds
A circular snake that changes color dynamically using CSS keyframe animations.
- **Shape:** Perfect Circles.
- **Effect:** Color shifting.

### 4. Galactic Stars
The most complex style, turning every contribution block into a 10-point star.
- **Shape:** Star Polygons.
- **Colors:** Gold and Purple.

---

## 🤝 Contributing
Feel free to fork this repo and add more CSS shapes (like diamonds or hearts)! 

Created by [Pro-Bandey](https://github.com/Pro-Bandey).

---
*Based on the amazing [snk](https://github.com/Platane/snk) engine by Platane.*

***

### 💡 Pro-Tip for your Marketplace Page:
When you go to **Release** your action, GitHub will let you upload a "Social Preview" image. I recommend taking a screenshot of all four snakes together and using that as your banner so people see the variety immediately!
