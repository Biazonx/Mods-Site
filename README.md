# Biazon Mods Site

Static website for my modding projects, built with [Zola](https://www.getzola.org/) and published on GitHub Pages.

🌐 Live site: <https://biazonx.github.io/Mods-Site/>

## Tech Stack

- **Generator:** Zola
- **Hosting:** GitHub Pages
- **Auto deploy:** GitHub Actions via `.github/workflows/deploy.yml`

## Run Locally

1. Install Zola:
   - Windows: `winget install getzola.zola`
   - Or download it from the Zola website.
2. Start the local server:

```bash
zola serve
```

3. Open the preview at `http://127.0.0.1:1111`.

## Build the Site

```bash
zola build
```

The generated static files will be created in `public/`.

## Publish on GitHub

This repository is already set up to deploy automatically.

### 1) Push your changes to `main`

```bash
git add .
git commit -m "Update site"
git push origin main
```

### 2) Enable GitHub Pages

In your GitHub repository:

- Go to **Settings** → **Pages**
- Under **Build and deployment**, choose **Source: GitHub Actions**

### 3) Wait for deployment

After each push to `main`, the workflow in `.github/workflows/deploy.yml` will:

- install Zola
- build the site
- upload `public/`
- deploy to GitHub Pages

## Project Structure

```text
content/     Site pages and sections
static/      CSS, icons, and static assets
templates/   Zola templates and partials
zola.toml    Site configuration
```

## Important Note

The site URL is configured in `zola.toml`:

```toml
base_url = "https://biazonx.github.io/Mods-Site"
```

Keep this value correct so asset paths and page links work properly on GitHub Pages.
