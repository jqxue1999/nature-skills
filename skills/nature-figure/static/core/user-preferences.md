# The user's own plotting habits (always on)

Learned while redrawing every results figure of one of the user's papers (2026-10). These
rules apply to every data figure for this user. Where they conflict with the defaults in `stance.md`, these win.

## Look

- **Two spines (left and bottom) only.** The user tried a four-sided frame and went back: on a four-sided frame,
  annotations such as "n=1, σ=2" covered the top edge.
- Spine width 0.8 pt, dark ink (`#1A1A1A`). Ticks point outward, about 2.2 pt long. Light grid (`#E6E6E6`,
  0.5 pt) behind the data.
- Font: Nimbus Sans (a Helvetica clone, sans-serif). 8 pt for axis labels, 7.5 pt for ticks and the legend.
  Small panels may drop to about 7/6.8 pt. Embed it as Type 42 (`pdf.fonttype: 42`). No text, annotation or
  legend may cover an axis line.
- Our method is the hero series: solid line, filled star marker, thicker (1.4 pt), drawn on top. Baselines are
  dashed and thinner, with hollow markers. The legend has no frame edge and a white, almost opaque background.
- Muted palette, the same in every figure of the paper. One paper used crimson `#B5303F` for the method, and
  `#4C72B0` blue, `#D9A441` ochre and `#5E9C88` sage for the others. Make the LaTeX colour macros of the text
  match these values.

## Layout

- **Compact, little white space.** Keep the figure's footprint in the paper (`\includegraphics` width) and the
  original aspect ratio, then trim the margins until the content sits about 1 pt inside the canvas
  (move the subplot edges until the tight bounding box sits 1 pt inside).
- Panels side by side have the same plot height. A legend that describes only one panel stays with that panel.
  Do not put it where it seems to describe the other panel too, and do not push one panel down with it.
- The user asks for a whole-paper pass: check every results figure for loose white space and for font sizes
  that differ between figures.

## Consistency

- When some figures are redrawn, redraw all of them, including ones whose content did not change. Mixed styles
  look worse than an old style everywhere.
- After renaming the method, search every figure (legends, labels, file names) for the old name.

## Tables or charts

- Do not force a small results table into a chart. The user tried a results table as a bar chart, both full-width and
  half-width, and went back to the table. Offer a chart only when the trend is the message, and keep the table
  if the user prefers it.

## Working with this user

- Show the rendered PNG of each change. Ask decisions with AskUserQuestion, in Chinese.
