# umr-1000.github.io

Personal academic profile for Umar Habib (B.S. Computer Science, LUMS), built to link from cold emails to professors. It is a single static HTML page with no build step and no framework.

Published with GitHub Pages at <https://umr-1000.github.io> (repository Settings > Pages > deploy from the `main` branch, root folder).

## What is on the page

Fixed profile column on the left (photo, contact links, light/dark switch) with the content on the right. On phones the profile column moves to the top of the page.

Sections, in order: About Me, Education, Research & Technical Interests, Publications, Experience, Projects, Relevant Coursework, Technical Skills, Achievements and Awards.

- **Publications** are numbered `[1]`, `[2]` and carry a venue line with an "Under review" badge, a key finding, and a collapsible figure (see below).
- **Light/dark mode** is a switch in the profile column. The page always opens in light mode; a visitor's choice is remembered in their browser (`localStorage`).
- **Coursework** shows four columns when there is room, a 2 x 2 grid when there is not, and one column on very narrow screens.
- Links to web pages open in a new tab. The email link does not.

## Files

| Path | What it is |
|---|---|
| `index.html` | The whole site: HTML, CSS and a few lines of JavaScript (only the theme switch) |
| `UmarHabib_CV.pdf` | The CV linked from the profile column |
| `profile.jpeg` | Profile photo (square, 400 x 400) |
| `fonts/` | Lora (the same font as the CV), Latin-only WOFF2 subsets, plus its licence (`OFL.txt`) |
| `icons/` | Browser tab icon: `favicon.svg`, `favicon-32.png`, `favicon.ico`, `apple-touch-icon.png` |

## Preview locally

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>. Use a local server rather than opening `index.html` directly, so the fonts, icons and figures load the same way as on GitHub Pages.

## Updating the site

- **Colours:** the sepia palette (and its dark counterpart) is defined as CSS variables at the top of the `<style>` block in `index.html`.
- **CV:** replace `UmarHabib_CV.pdf` with the newly compiled PDF, keeping the same filename so the link keeps working. Keep the CGPA / major GPA and other details on the page in step with the CV. The PDF is published as-is, so anything printed on it (including contact details) is public.
- **Paper status:** the "Under review" badges and venue lines are in the Publications section. Update them when a paper is accepted or published.
- **Fonts:** the Lora files only contain Latin characters (about 220 glyphs), which keeps them tiny (about 20 KB each). If you add text with characters outside that range, regenerate the subsets from the full font files.
- **Tab title and icon:** the `<title>` and the icon links are at the top of `index.html`.

## Figures

The two paper figures are inline SVG, so they follow the light/dark theme and add no image downloads. Each has a wide version (desktop) and a tall version (mobile); the page shows whichever fits the space available.

- **Made with AI?** pipeline: adapted from the figure on the co-author's own site (<https://abubakarmugha1.github.io>), re-coloured and re-typeset to match this site, with the user study replaced by the comment analysis.
- **Hive-Nav** system overview: a redrawing of Fig. 1 from the paper. The floor plan is traced from the paper's own map image, so it keeps the exact shape.

Please check with the co-authors before publishing changes to either figure.

## Credits and licences

- Font: [Lora](https://fonts.google.com/specimen/Lora), SIL Open Font License 1.1 (`fonts/OFL.txt`).
- Icon glyphs for GitHub and LinkedIn are simple inline SVG shapes; the YouTube mark on the "Video demos" link is likewise inline SVG.
