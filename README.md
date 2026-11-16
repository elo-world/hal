# hal – Landing page

Static landing page for **hal – Your Helper to Automate Your Life**, a connected tablet and smartwatch that helps elderly people live independently while staying close to their families.

Plain HTML, CSS and a little JavaScript. No build step, no dependencies.

## Structure

```
hal/
├── index.html        Page markup
├── css/
│   └── style.css     All styles (design tokens at the top, in :root)
├── js/
│   └── script.js     Mobile menu and footer year
├── assets/
│   └── favicon.svg
├── .gitignore
└── README.md
```

Fonts: [Instrument Serif](https://fonts.google.com/specimen/Instrument+Serif) and [Inter](https://fonts.google.com/specimen/Inter), loaded from Google Fonts.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Before you publish

Search the project for `TODO` and replace the placeholders:

- **Contact email** in the footer (`[YOUR CONTACT EMAIL]`).
- **"Order your hal" button** in the pricing section: point it at your checkout, shop page or waitlist form.
- **"Request a demo" buttons**: currently jump to the footer contact block; link them to a form or `mailto:` address.
- Optionally add an `og:image` meta tag in `index.html` for link previews.

## Push to GitHub

```bash
cd hal-landing
git init
git add .
git commit -m "Add hal landing page"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

## Deploy with GitHub Pages

1. In your repository, go to **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select the `main` branch and the `/ (root)` folder, then save.
4. The site will be available at `https://<your-username>.github.io/<your-repo>/` after a minute or two.

All asset paths are relative, so it works both on a project URL and on a custom domain.

## Customize

- **Colors, fonts, container width:** edit the variables in `:root` at the top of `css/style.css`.
- **Copy:** edit the text directly in `index.html`.
- **Icons:** defined once in the SVG sprite at the top of `index.html` and reused with `<use href="#i-…">`.
- **Breakpoint:** the mobile layout and menu switch at 700px.
