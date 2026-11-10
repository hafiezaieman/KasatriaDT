# 3D Tiles: Kasatria CSS3D Assessment

An interactive 3D visualization built with Three.js (CSS3DRenderer), adapted from the [css3d_periodictable](https://threejs.org/examples/#css3d_periodictable) demo. After signing in with Google, the page reads people data from a Google Sheet and shows each person as a tile in 3D.

**Live demo:** [https://hafiezaieman.github.io/KasatriaDT/](https://hafiezaieman.github.io/KasatriaDT/)

## Features

- **Google Sign-In** using Google Identity Services (OAuth 2.0)
- **Live data** loaded from a Google Sheet through the Google Sheets API
- **Tile content:** country, age, photo, name, interest and net worth
- **Colour by net worth:**
  | Colour | Net worth |
  |---|---|
  | Red | below $100K |
  | Orange / yellow | $100K to $200K |
  | Green | above $200K |
- **Four layouts**, switched with the buttons at the bottom:
  | Layout | Arrangement |
  |---|---|
  | Table | 20 x 10 |
  | Sphere | Tiles spread over a sphere |
  | Helix | Double helix (two strands, 180 degrees apart) |
  | Grid | 5 x 4 x 10 |
- Drag to rotate, scroll to zoom. A LOW to HIGH legend sits at the bottom right.

## Tech stack

- HTML, CSS and JavaScript (a single `index.html`)
- [Three.js](https://threejs.org/) r160 (CSS3DRenderer, TrackballControls)
- Google Identity Services and the Google Sheets API (read-only scope)
- Hosted on GitHub Pages

## Project structure

```
tiles-site/
├── index.html   # the whole app
└── README.md
```

## Notes

- The app requests **read-only** access to Google Sheets and stores nothing.
- Data is fetched on each sign-in, so edits to the Sheet show up after a page refresh and a new sign-in.
