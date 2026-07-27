# Task 3: CSS - Units, Box Model, Fonts

A simple responsive page displaying an image inside a styled container with a gradient "Click Me" button, built using pure CSS box-model and viewport units — no Flexbox, no `overflow: hidden`, and no `position: relative/absolute`.

## Preview

A centered image section with 25% horizontal spacing and 10% vertical spacing from the screen edges, followed by a gradient-styled button below the image.

## Project Structure

```
task3/
├── index.html
├── style.css
└── README.md
```

## Features

- **HTML Structure**: Semantic setup with a linked external stylesheet, a container `div` holding an image and button.
- **Spacing (Box Model)**:
  - 25% spacing from left and right of the screen.
  - 10% spacing from top and bottom of the screen.
- **Viewport Units**: All dimensions use `vw` / `vh` instead of fixed pixels, so the layout scales with screen size.
- **No Scroll**: Achieved by using `box-sizing: border-box` with `padding` on `body` (instead of `margin` on the child), avoiding margin-collapse issues that would otherwise push content past `100vh`.
- **Button Styling**: Gradient background, custom font size/weight/letter-spacing, no default border/outline.
- **Constraints followed**:
  -  No `flex`
  -  No `overflow: hidden`
  -  No `position: relative` or `position: absolute`
  -  Proper HTML tag closure
  - `box-sizing` used correctly throughout

## How It Works

| Requirement | Implementation |
|---|---|
| 25% left/right spacing | `body { padding: 10vh 25vw; }` |
| 10% top/bottom spacing | Same padding rule (top/bottom values) |
| No page scroll | `body { height: 100vh; box-sizing: border-box; }` — padding is included in the 100vh instead of adding to it |
| Image display | `.image-section img { width: 100%; height: 85%; object-fit: cover; }` |
| Button styling | `linear-gradient()` background + `vw`-based font sizing |

## How to Run

1. Keep `index.html` and `style.css` in the same folder.
2. Open `index.html` in any web browser.
3. (Optional) Replace the image `src` in `index.html` with your own local image path.

## Tech Used

- HTML5
- CSS3 (Box Model, Viewport Units, Linear Gradients)