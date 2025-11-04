# Baseball Stats Website (GitHub Pages)

This package contains a small static site that loads `Baseball.xlsx` in the browser (using SheetJS) and displays **only** the `Sheet1` worksheet as a read-only table. The `Players` worksheet is loaded into memory for lookup/reference and is not displayed.

## Files
- `index.html` — The single-page site (HTML + JS). Fetches `Baseball.xlsx` from the same folder.
- `Baseball.xlsx` — **(You must upload this file yourself)** Place it alongside `index.html` in the repository root.

## How to publish on GitHub Pages
1. Create a new GitHub repository (e.g. `baseball-stats-site`).
2. Upload `index.html` and your `Baseball.xlsx` to the repository root (`/`).
3. In the repo, go to **Settings → Pages** (or **Settings → Pages & GitHub Pages**).
4. Under "Build and deployment", set the branch to `main` (or `master`) and folder to `/ (root)`, then save.
5. GitHub will publish your site at: `https://YOURUSERNAME.github.io/REPONAME/`
6. Visit that URL. The page will fetch `Baseball.xlsx` and display `Sheet1`.

## Notes & Troubleshooting
- The site expects the Excel file to be at `https://.../REPO/.../Baseball.xlsx` (same folder as `index.html`). If you rename the file, update the fetch path in `index.html`.
- When you update `Baseball.xlsx`, re-upload it to the repo (overwrite the old file). Visitors should refresh the page (or you can press the "Reload Data" button on the page).
- If your Excel file has a different sheet name than `Sheet1`, edit the `sheetShown` variable near the top of the `<script>` tag in `index.html`.

If you'd like, I can also:
- Add column sorting, search, or filters.
- Generate the repo and ZIP everything for you.
