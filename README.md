# B.A. Hons Psychology — Syllabus Site (Invertis University)

A static, multi-page site covering the 4-year B.A. Hons Psychology programme:

- `index.html` — Overview of the programme
- `syllabus.html` — Year-by-year, semester-by-semester syllabus
- `readings.html` — Subject-wise suggested reading lists
- `career.html` — "Career Compass": pick up to 5 subjects, get a suggested specialisation
- `css/style.css` — Shared styling
- `js/data.js` — All syllabus data, book lists, and career-mapping logic

No build step, no dependencies — plain HTML/CSS/JS.

## Run locally

Just open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

1. Create a new GitHub repository and push these files to the `main` branch
   (keep this folder structure — `index.html` should sit at the repo root,
   or inside a `/docs` folder if you prefer).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Pick branch `main` and folder `/ (root)` (or `/docs` if you used that).
5. Save — GitHub will publish the site at
   `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## Updating content

All syllabus data lives in `js/data.js`:

- `SYLLABUS` — course tables per year/semester
- `BOOKS` — reading lists keyed by course code
- `CAREER_SUBJECTS` / `SPECIALISATIONS` — the Career Compass tagging and copy

Edit that file and refresh — no rebuild needed.
