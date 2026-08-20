# Your website — how to edit it

Plain HTML/CSS, no build step. Open any `.html` file in a text editor and
change the text — that's it.

## Files

- `index.html` — homepage (photo, bio, links)
- `news.html` — timeline of updates
- `publications.html` — papers, grouped by year
- `projects.html` — project cards
- `style.css` — all styling and colors, in one place

## Content status

The site is now populated from your CV (name, bio, education, news
timeline, patents, publications, and projects). A few things the CV
didn't give me, so they still need your input:

1. **Google Scholar link** — the PDF only showed the text "Google
   Scholar," not the actual URL. Search each file for `href="#"` next
   to `Google Scholar` and paste in your real profile link (2 spots:
   `index.html` and `publications.html`).
2. **Co-authors** — the CV lists paper titles and venues but not full
   author lists, so each publication currently shows "Vijay Kumar
   Singh, et al." Search `publications.html` for `et al.` and replace
   with the full author list per paper.
3. **Project/paper links** — a few `View project →` links in
   `projects.html` point to `#` because there's no public link yet
   (WiLight, the gesture-tracking work, WiProctor). Swap in a real
   link once one exists.
4. **Photo (optional)** — in `index.html`, find:
   ```html
   <div class="avatar-wrap">
     <div class="avatar avatar-lg">V</div>
   </div>
   ```
   Replace the inner `<div>` with:
   ```html
   <img src="images/your-photo.jpg" alt="Vijay Kumar Singh">
   ```
   and put a square-ish photo at `images/your-photo.jpg`.
5. **CV** — add a `cv.pdf` file next to `index.html` (the "CV" nav link
   already points to it).
6. **Adding more entries** — each entry is one HTML block
   (`<article class="pub">...`, `<article class="project-card">...`,
   `<li>...</li>`). Copy a block and edit the text to add more.

## Deploying to GitHub Pages (free hosting)

1. Create a new GitHub repo named exactly `<your-github-username>.github.io`.
2. Push these files to the repo's root (not a subfolder).
3. In the repo's Settings → Pages, set the source to the `main` branch, root.
4. Your site will be live at `https://<your-github-username>.github.io/`
   within a few minutes.

## Notes

- Fonts (Space Grotesk, Inter, IBM Plex Mono) load from Google Fonts via
  the `<link>` tags in each page's `<head>` — no local files needed.
- Colors, spacing, and fonts are all controlled by the CSS variables at
  the top of `style.css` if you want to retheme later.

  cd ~/Videos/vijay-website
   git add .
   git commit -m "Add new publication"
   git push
