# Virtual Golf Ball Rack

A digital replica of a physical golf ball display case — every logo ball from every
course played, rendered as an interactive web page with a course list and a map.

## Features

- **The rack** — a faithful recreation of the mahogany 9×13 display case, including
  the black felt shelves, brass hinges, and the empty drilled slots at the bottom.
  Each ball carries its course's logo mark and colors.
- **Interactive map** — every identified course is pinned on a map (Leaflet +
  OpenStreetMap/CARTO tiles). Click a ball to fly to its course; click a pin to find
  its ball in the rack.
- **Courses played** — the full list, grouped by state, with per-course ball counts.
- **Best guesses** — balls whose logos couldn't be fully read from the photo are
  flagged with an amber dot. Edit `data.js` to correct or fill in any of them.

## Running it

No build step — it's a static page:

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

Or just open `index.html` in a browser (an internet connection is needed for map
tiles and fonts).

## Editing the collection

All ball data lives in `data.js`. Each entry has the rack position (`row`, `col`),
the text stamped on the ball (`mark`, `color`), the course name and location, and
optional flags (`uncertain`, `special`). Add, correct, or move balls there and
refresh the page.
