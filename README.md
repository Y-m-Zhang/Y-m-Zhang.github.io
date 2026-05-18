# Personal Homepage

A minimal, single-file personal homepage. Pure HTML/CSS, no build step, deployed via GitHub Pages.

## Preview locally

Just open `index.html` in a browser, or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

1. Create a new repository on GitHub.
   - For a user/organization site at `https://<username>.github.io`, name the repo **`<username>.github.io`**.
   - For a project site at `https://<username>.github.io/<repo>/`, name it anything (e.g. `personal-homepage`).

2. Initialize and push:

   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin git@github.com:<username>/<repo>.git
   git push -u origin main
   ```

3. On GitHub, go to **Settings → Pages**:
   - Under **Build and deployment**, set **Source** to **GitHub Actions**.

4. Push to `main` — the included workflow (`.github/workflows/deploy.yml`) will deploy automatically. The site URL will appear on the Pages settings page once the first run succeeds.

## Customize

Edit [index.html](index.html) directly:

- `Your Name` and the tagline in the header
- `About` paragraph
- Three project cards under `Projects` (title, year, description, links)
- `Skills` grid rows
- `Contact` links (email, GitHub, X, LinkedIn)

That's it — one file, no dependencies.

## Custom domain (optional)

Add a `CNAME` file at the repo root containing your domain (e.g. `example.com`), then configure DNS:

- For an apex domain: A records to GitHub Pages IPs (see GitHub docs)
- For a subdomain: a CNAME record pointing to `<username>.github.io`

## License

Do whatever you want.
