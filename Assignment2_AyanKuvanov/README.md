# Assignment #2 — Advanced CSS (Flexbox & Grid)

Three tasks built with plain HTML/CSS only — no Bootstrap, no JavaScript, no media queries.

## Structure

```
shared.css          Design tokens (color, type, spacing) shared by every page
index.html           Landing page linking to the three tasks

task1/               Geometric composition — a single 6x6 CSS Grid
  index.html
  grid.css

task2/               Component library — five components, Flexbox only
  index.html
  components.css

task3/               Three layouts, one markup — CSS Grid + Flexbox
  index.html
  layouts.css
```

## Running it

No build step. Open `index.html` in a browser, or serve the folder with any static
file server, e.g.:

```
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Notes

- **Task 1** places every block with `grid-column` / `grid-row` line numbers on a
  `repeat(6, 1fr)` grid. The black lines are the grid `gap`, not borders.
- **Task 2**'s five components (navbar, card row, pagination, comment, pricing) all
  share `shared.css`'s color/spacing/font variables and use Flexbox exclusively.
- **Task 3** keeps one HTML markup for all twelve articles. Because the assignment
  disallows JavaScript, the "single class on the container" mode switch is implemented
  with three CSS-only radio inputs and the `~` sibling selector
  (`#mode-list:checked ~ .gallery`), which is the CSS-only equivalent of toggling one
  class name on the container.
