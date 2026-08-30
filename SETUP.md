# How to publish this profile

1. Create (or open) the special repo named exactly after your GitHub username:
   https://github.com/mmubeenkhatri/mmubeenkhatri  — tick "Add a README file" if it doesn't exist.
2. Copy `README.md` and the whole `assets/` folder into the root of that repo.
3. Commit and push:

   git add README.md assets/
   git commit -m "Refresh profile README with branded header"
   git push

4. Open https://github.com/mmubeenkhatri and confirm the banner renders in both light and dark mode
   (GitHub → Settings → Appearance to toggle).

Notes
- The banner and stack card are plain SVG files in `assets/` — no external services, nothing to break.
- To edit the wording on the banner, open `assets/banner-dark.svg` / `banner-light.svg` in any text
  editor; the text lives in plain <text> elements near the bottom of the file.
- The two GitHub stats cards at the bottom are the only third-party images. Delete that block if you
  prefer zero external dependencies.
