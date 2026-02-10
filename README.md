# EVera — Your Guide to the Electric Future

EVera is a static informational website that provides users with guides, comparisons and educational material about electric vehicles (EVs), plug-in hybrids (PHEVs), hybrids (HEVs) and fuel-cell EVs (FCEVs). The project is a client-side website built with plain HTML, CSS and static assets (images and video). It is intended for learning, demonstration and documentation purposes.

## Table of contents

- Project overview
- Features
- Tech stack
- Repository structure
- Getting started (run locally)
- Development notes
- Deployment
- Contributing
- License
- Credits

## Project overview

This project was created as part of an Internet Technologies course. It aggregates pages and resources about electric vehicle technologies, maintenance, buying guides, and comparisons. The site is organized into several pages under the `pages/` folder and styled with CSS in the `style/` folder. Static images and media are stored in `assets/`.

## Features

- Multi-page static site with separate pages for BEVs, PHEVs, HEVs, FCEVs and general EV topics
- Dedicated buying guide and care/maintenance guides
- Image and video assets to support content
- Simple responsive layout via CSS files (see `style/main-layout.css` and per-page styles)
- 404 page for hosting fallback

## Tech stack

- HTML5 (static pages)
- CSS3 (separate stylesheets for layout and articles)
- Static assets: PNG/JPEG images and a video
- Optional: Firebase Hosting configuration present (firebase.json)

## Repository structure

Top-level files
- index.html — Homepage
- 404.html — Not found page
- firebase.json — Firebase Hosting configuration (if used)
- README.md — This file

Directories
- assets/
  - image/ — collection of vehicle and structure images used by pages
  - video/ — site videos used in content
- pages/ — separate content pages (about.html, bev-cars.html, ev-buying-guide.html, ev-care.html, ev-topics.html, battery-ev.html, fuel-cell-ev.html, hybrid-ev.html, plug-in-ev.html)
- style/ — CSS stylesheets (main-layout.css, article.css and per-page CSS)

## Getting started (run locally)

Because the project is a static website, you can view it directly by opening `index.html` in a browser. For a local development server (recommended to avoid cross-file restrictions and to preview routing), use one of the following methods.

Using Python 3 (works on Windows):
- Open a terminal in the project root (where index.html is located).
- Run:
  - For Python 3.10+ or Windows default: python -m http.server 8000
- Open http://localhost:8000 in your browser.

Using Node (http-server):
- Install http-server globally if not present: npm install -g http-server
- Run: http-server -p 8000
- Open http://localhost:8000

Using Visual Studio Code Live Server extension:
- Install Live Server extension and click "Go Live" while the workspace is open.

## Development notes

- The site is purely static; no build step is required.
- Styles are split into a main layout and page-specific CSS files in `style/`.
- To add or update pages, create an HTML file in `pages/` and link it from navigation in `index.html` or site header/footer.
- Keep images inside `assets/image/` and reference with relative paths (e.g. `assets/image/tesla-model-3.png`).
- If adding JavaScript, create a new `js/` directory and reference scripts in the appropriate pages.

## Deployment

Firebase hosting configuration exists in `firebase.json`. To deploy the site to Firebase Hosting:

1. Install Firebase CLI (if not installed): npm install -g firebase-tools
2. Authenticate: firebase login
3. Initialize hosting (only needed once per project): firebase init hosting
   - When prompted, choose the existing project or create a new one.
   - Set the public directory to the repo root (or the folder that contains index.html).
   - Configure as a single-page app? Choose no if you want normal multi-page routing.
4. Deploy: firebase deploy --only hosting

Alternatively, host on any static hosting provider (GitHub Pages, Netlify, Vercel, or a static file server). For GitHub Pages, push the repository and enable GitHub Pages from the repository settings (use the root or docs folder as source as appropriate).

## Contributing

Contributions are welcome for fixing typos, improving content, adding images, or enhancing styles.

Suggested workflow:
- Fork the repo
- Create a feature branch: git checkout -b fix/your-change
- Make changes, commit, and push
- Open a pull request with a clear description of the change

Please keep changes focused and include screenshots for UI updates where appropriate.

## License

This project contains educational content and static assets. If you own the images or they are from public domain / allowed usage, ensure you have the right to distribute them. The repository itself can be licensed under the MIT License for the website code. Add a LICENSE file if you want to use MIT or another license.

Example short license notice you can add below or in a LICENSE file:

MIT License
Copyright (c) 2026 [Your Name]

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions: (See full MIT text in LICENSE file.)

## Credits and resources

- Project created for an Internet Technologies course (2nd semester)
- Images and other assets included in `assets/image/`
- If using external images, ensure attribution and license compliance where required

## Contact

For questions about this project, update the README with contact details or link to a course page or repository issues.

---

Thank you for using EVera — Your Guide to the Electric Future.

