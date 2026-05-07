# Felix's Portfolio

A simple, dark-mode developer portfolio built with plain HTML, CSS, and JavaScript. No build step required — it's ready to deploy to GitHub Pages as-is.

## Project structure

```
.
├── index.html              # Home / hero page
├── about.html              # About + tech stack
├── projects.html           # Project grid
├── contact.html            # Contact / socials
├── projects/
│   ├── ecommerce.html
│   ├── warehouse.html
│   ├── database.html
│   └── ship-monitoring.html
├── css/
│   └── styles.css          # All styles
├── js/
│   └── main.js             # Mobile nav + active link highlight
├── .nojekyll               # Tells GitHub Pages to skip Jekyll
└── README.md
```

## Deploying to GitHub Pages

There are two common patterns. Pick whichever you prefer.

### Option A — User site (recommended): `username.github.io`

This gives you a clean URL like `https://your-username.github.io`.

1. On GitHub, create a new public repo named **exactly** `your-username.github.io` (replace `your-username` with your actual GitHub username).
2. Push the contents of this folder to the `main` branch:
   ```bash
   cd /path/to/this/folder
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/your-username/your-username.github.io.git
   git push -u origin main
   ```
3. In the repo's **Settings → Pages**, confirm the source is set to `main` branch, root folder.
4. Wait ~1 minute, then visit `https://your-username.github.io`.

### Option B — Project site: `username.github.io/portfolio`

Use this if you'd rather keep the repo under a project name.

1. Create a public repo named e.g. `portfolio`.
2. Push the files the same way as Option A.
3. In **Settings → Pages**, set source to `main` branch, `/ (root)`.
4. Visit `https://your-username.github.io/portfolio`.

> **Note:** All internal links in this site use **relative paths** (e.g. `about.html`, `css/styles.css`) so it works under both patterns without any code changes.

## Customizing — what to fill in

Everywhere you see `// edit me` or `// TODO` comments in the HTML, that's a spot to replace with your real content. The most important things to update:

- **`about.html`** — your bio, location, and tech stack
- **`contact.html`** — your real GitHub and LinkedIn URLs
- **`projects/*.html`** — for each project: overview, features, role, tech, and a screenshot
- **Project screenshots** — drop image files into a new `projects/img/` folder and replace each `.placeholder-img` div with `<img src="img/your-screenshot.png" class="project-screenshot" alt="..." />`

## Testing locally

Just open `index.html` in a browser, or run a tiny static server:

```bash
# Python
python -m http.server 8000
# then visit http://localhost:8000

# Or with Node
npx serve .
```

## License

Personal portfolio — feel free to fork as a starting point.
