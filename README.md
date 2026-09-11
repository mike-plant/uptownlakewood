# Uptown Lakewood Business Alliance

Single-page website for the Uptown Lakewood Business Alliance (ULBA), the west end of Madison Avenue in Lakewood, Ohio.

Pure HTML/CSS/JS in `index.html`. No build step.

## Local preview

Open `index.html` in a browser, or serve the folder:

```
python3 -m http.server 8000
```

## Deployment

Pushes to `main` deploy to GitHub Pages via `.github/workflows/deploy-pages.yml`.
The site is served at https://uptownlakewood.org (the `CNAME` file holds the domain).

### Custom domain setup (one time)

1. In the repo: Settings → Pages → Custom domain → enter `uptownlakewood.org`, save, and tick "Enforce HTTPS" once the check passes.
2. At the domain registrar, add these DNS records:

   | Type  | Host | Value                  |
   |-------|------|------------------------|
   | A     | @    | 185.199.108.153        |
   | A     | @    | 185.199.109.153        |
   | A     | @    | 185.199.110.153        |
   | A     | @    | 185.199.111.153        |
   | CNAME | www  | mike-plant.github.io   |

   Remove any existing A or CNAME records on `@` and `www` that point elsewhere (registrar parking pages, for example).
3. DNS can take up to an hour to propagate. GitHub issues the HTTPS certificate automatically after that.

## Hero photo

Place the Madison Avenue dusk photo at `images/madison-dusk.jpg`. Until it exists the hero shows a gradient sky.
