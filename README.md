# Git Client Website

This repository contains the static homepage for **Git Client**, an Android application for authenticating with GitHub and working with repositories locally. It is intentionally framework-free and can be published directly with GitHub Pages.

## Project structure

- `index.html` — product homepage
- `privacy.html` — practical privacy notice
- `terms.html` — concise terms of use
- `404.html` — GitHub Pages custom not-found page
- `css/styles.css` — shared responsive design system and dark-mode styles
- `js/site.js` — small progressive-enhancement script for the mobile menu and copyright year
- `assets/logo.svg` — original code-bracket mark
- `assets/social-preview.svg` — lightweight social preview asset

## Preview locally

From the repository root, run:

```text
python -m http.server 8000
```

Then open `http://localhost:8000/`. Opening `index.html` directly also works for basic inspection, although a local server is closer to GitHub Pages behavior.

## Required before publishing

The GitHub release link is `https://github.com/AggiaBintangRH/GitClonePush/releases/tag/Git`, privacy or terms questions can be sent to `aggiaramadhan@gmail.com`, and the legal pages were last updated on 5 October 2026.

## GitHub Pages deployment

1. Push this repository to GitHub.
2. Open the repository's **Settings**.
3. Open **Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`.
6. Save.
7. Wait for the deployment to complete.
8. Visit the generated GitHub Pages URL.

The site uses relative asset and internal page paths, so it works when hosted beneath a project subpath such as `https://USERNAME.github.io/git-client-homepage/`.

## OAuth homepage documentation

Once deployed, the public GitHub Pages URL can be used as the **Homepage URL** for a GitHub OAuth App. For example:

```text
https://USERNAME.github.io/git-client-homepage/
```

The Homepage URL and callback URL are different concepts. The Homepage URL is the public website describing the application. The callback URL is the URI GitHub uses to return authorization results to the Android application. This repository does not change Android OAuth configuration and does not implement an OAuth callback.

## Scope and privacy

This is a static website only. It has no backend, database, GitHub API integration, authentication flow, analytics, advertising, tracking scripts, or cookies. The terms page uses an explicit date placeholder where the developer-specific revision date is still required.
