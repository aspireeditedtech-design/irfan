# Video Editing Portfolio — V3 GitHub Pages fix

The cinematic V2 layout and 30%-opacity hero portrait are retained, with a responsive headline fix and smaller poster images. All 5 hero reels (silent hover previews + audible click-to-watch) and the standalone Work Payoff video are included.

## IMPORTANT: How to upload without the GitHub loading/404 error

**This ZIP deliberately has `index.html` at the ZIP ROOT, not inside a nested `video-editor-portfolio-v3-fixed/` folder.**

1. Download ZIP and extract it to your computer. **Do not upload the ZIP itself to the GitHub repository.**
2. Open the *contents* of the extracted folder, select `index.html`, `styles.css`, `script.js`, `site-config.js`, `.nojekyll` and the whole `assets` folder; upload them into the **repository root** (top level). In GitHub's file list, you should see `index.html` directly, not inside another folder. Some systems hide `.nojekyll`; its absence is usually fine for this site.
3. If updating an older V2 version, **replace existing files** (do not add a second V3 subfolder). Keep the `assets/images/`, `assets/videos/`, and `assets/previews/` directory names unchanged. Delete obsolete `chandrasekhar-preview.png` and `vegetables-preview.png` if desired; V3 uses WebP.
4. Go to **Settings > Pages > Build and deployment**. Select **Deploy from a branch**, choose the publishing branch (`main` if that is your default branch), and **/(root)**, then Save. If GitHub Pages is configured to use a different branch, upload the files there or update the Pages setting accordingly.
5. Find the **Visit site** link on the Pages settings page. A project repository usually publishes at `https://USERNAME.github.io/REPOSITORY-NAME/`, not just `https://USERNAME.github.io/`. Wait for GitHub's Pages deployment to finish, then force-refresh (Ctrl+Shift+R / Cmd+Shift+R).

**If the page is blank / says 404:** check `index.html` is at the root, Pages points to the uploaded branch + root, the repository is public if your GitHub plan requires it, and the browser URL includes the repository name. GitHub filename case matters: `assets/videos/...` is not the same as `Assets/Videos/...`. **If just the videos show load errors:** verify that all six MP4s and all five silent previews were uploaded, not just the top-level HTML files. Individual files are below 6 MB.

**If you still get an error:** send the actual GitHub Pages URL or the full error screenshot so the exact deployment issue can be identified; a ZIP fix cannot resolve a misconfigured or incomplete remote upload by itself.

## Files

- `index.html` main site
- `styles.css` cinematic look, reel wobble and clipping fix
- `script.js` interaction, silent hover preview and modal player
- `site-config.js` update contact/video links
- `assets/images/`, `assets/videos/`, `assets/previews/` all media
- `.nojekyll` keeps Pages from processing the static site with Jekyll

**Local test:** open `index.html` directly or run `python -m http.server 8000` from this directory and visit `http://localhost:8000/`.
