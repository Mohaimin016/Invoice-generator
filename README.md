# Invoice Portal

Commercial Invoice maker. Load the **Dplus excel** export, pick an AWB, check the fields, and **Print / Save PDF** (one A4 page). Works offline and can be installed as an app (PWA).

Contact & Support: Mohaimin Al Islam Siddike

## Files

| File | Purpose |
|---|---|
| `index.html` | The app (sign-in, invoice, Excel import, print) |
| `manifest.webmanifest` | App name, colours and icons for installing |
| `service-worker.js` | Offline support (caches the app) |
| `icons/` | App icons (192, 512, maskable, Apple, favicon) |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

## Publish on GitHub Pages

1. Create a new repository on GitHub (for example `invoice-portal`).
2. Upload **all** files and the `icons` folder to the root of the repository (Add file → Upload files → drag the whole folder contents → Commit).
3. Go to **Settings → Pages**. Under *Build and deployment* choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
4. After 1–2 minutes the site is live at `https://<your-username>.github.io/invoice-portal/`.

## Install as an app

- **Chrome / Edge (PC or Android):** open the site and click **Install app** in the toolbar, or the install icon in the address bar.
- **iPhone / iPad (Safari):** Share → **Add to Home Screen**.

## Updating

After changing any file, open `service-worker.js` and raise the version, for example `invoice-portal-v1` → `invoice-portal-v2`. Users then get the new version the next time they open the app.

## Notes

- The Excel file is read inside the browser. Nothing is uploaded to a server.
- Draft invoices are saved in each user's own browser only.
- The sign-in runs inside the page, so it keeps casual visitors out but is not real security. Keep the repository **private** if you can (GitHub Pages on private repositories needs a paid plan), and don't treat the page as protected.
