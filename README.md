# GMC Audit Report Builder

Offline-capable PWA for HSE operational-control audits. Choose controls once, fill the checklist, generate the audit report as a Word (.docx) file.

No build step, no dependencies to install. Plain static site.

## Files
- `index.html` the app
- `vendor/docx.umd.js` docx 8.5.0 (bundled so Word export works offline)
- `sw.js`, `manifest.webmanifest`, `icons/` PWA install and offline support
- `vercel.json` optional Vercel headers

## Deploy
**GitHub:** create a repo, upload all files keeping the folder structure, commit to `main`.

**Vercel:** Add New Project, import the repo, Framework Preset "Other", leave build command and output directory empty, Deploy.

**GitHub Pages (alternative):** Settings, Pages, deploy from `main` / root.

## Install on a phone
Open the deployed URL in Chrome or Safari, then Add to Home Screen / Install app. After the first load it works offline. Answers are stored in the browser (localStorage) on that device.

## Updating
Edit `index.html`, then bump `V` in `sw.js` (e.g. `gmc-audit-v2`) so installed copies refresh.
