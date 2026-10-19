# ApnaTest Generator — SSC WARS Mini Web App

This is a static, installable web-app package based on the current ApnaTest Generator. The existing UI and generation logic are preserved; the package adds a web-app manifest, icons, and a service worker shell cache.

## Free shared URL

This ZIP is ready to publish as a static site using GitHub Pages. A public URL is not created automatically by making the ZIP; you must publish it to a hosting service.

1. Sign in to GitHub and create a new public repository (for example `apnatest-generator`).
2. Upload the files and folders in this package to the repository root (upload the contents, not the ZIP itself).
3. Open **Settings → Pages**. Under Build and deployment, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
4. Wait for GitHub Pages to publish and open the URL it shows. Share that URL with the team.
5. In Chrome or Edge, use the install icon in the address bar or the browser menu's **Install app** option.

## Local files and privacy

Each team member uses the app in their own browser/device. Files selected for OCR and generated pages are processed in that browser; they are not automatically shared between team members. The app itself is hosted at the shared URL.

## Important limitation

The service worker caches the app shell, but the OCR engine is loaded from an external CDN in the existing app. Therefore OCR may still require an internet connection. This package does not include a backend, user accounts, or shared cloud storage.
