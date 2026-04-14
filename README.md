# Nuojiji GitHub Pages Mirror

This directory is a static mirror of `https://nuojiji.pages.dev/`, adjusted to run on GitHub Pages.

## What was changed

- Root-relative asset links were converted to relative links.
- The runtime preload helper now resolves asset URLs from `document.baseURI`.
- Service worker auto-registration was disabled to avoid broken cache manifests from the original deployment.
- A minimal no-op `sw.js` was added so direct service worker requests stay harmless.
- A GitHub Pages Actions workflow was added at `.github/workflows/deploy.yml`.

## Deploy

1. Create a GitHub repository.
2. Upload the contents of this folder to the repository root.
3. Push to the `main` branch.
4. In GitHub, open `Settings -> Pages`.
5. Set `Build and deployment` to `GitHub Actions`.
6. Wait for the `Deploy to GitHub Pages` workflow to finish.

## Notes

- This is a mirrored production build, not the original source code.
- If the upstream site updates, you will need to mirror it again to stay in sync.
