# GitHub Pages deployment notes

1. Upload **all files in this folder** to the same GitHub repository folder (not just `index.html`).
2. In GitHub: Settings → Pages → Deploy from a branch → choose your branch and `/ (root)` (or the folder containing these files).
3. Wait for the Pages deployment to finish, then open the URL shown under Settings → Pages.
4. The original `index.html` is preserved byte-for-byte. This bundle only supplies the missing PWA support files referenced by the HTML (`manifest.json`, icons, and `sw.js`).

Important:
- A working GitHub Pages URL does not automatically authorize Google sign-in. Add the exact Pages hostname to the Google OAuth client's Authorized JavaScript origins, if Google sign-in is used.
- Firebase Realtime Database rules and allowed domains must also permit the deployed origin. Do not make database rules public just to make the page load.
- Images/scripts still referenced from third-party domains require those domains to remain online and allow browser access. This bundle cannot guarantee those external services.
- This is a static-hosting support bundle only; it does not repair or validate account, payment, betting, or other server-side workflows.
