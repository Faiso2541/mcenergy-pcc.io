# McEnergy Project Control Center (PCC)

Single-file web app (`index.html`) for tracking projects: customers, documents and approvals,
PR/PO and deliveries, WBS and daily site updates, action center, contract countdown and cost.

## Run locally
Open `index.html` in Microsoft Edge or Google Chrome. No install or build step.

## Deploy on Vercel
1. Push this folder to a GitHub repository.
2. In Vercel: **Add New → Project → Import** the repository.
3. Framework preset: **Other** · Build command: *(empty)* · Output directory: *(empty / root)*.
4. Deploy. Every push to `main` redeploys automatically.

## Where data is stored
- Data is saved in the **browser** of each user (localStorage), per website address.
  The Vercel site and a local `index.html` file keep **separate** data.
- **Settings → Data**: export / import a backup (`.json`), or download `index.html` with the data inside.
- **💾 Save to index.html** (Edge / Chrome) writes the data into a local `index.html` file.

> ⚠️ Do **not** commit backups or an `index.html` that has data saved inside it — they contain
> contract values and customer contacts. The `index.html` in this repo must stay empty
> (`<script id="pcc-data" type="application/json">null</script>`).
> If the repo is public, anyone can open the site — keep the repo **private** and use Vercel
> Deployment Protection if needed.

## Limits (current version)
- No shared database yet: each user sees only the data in their own browser.
- Roles are selected in the app (no login) — not a security control.
- Files and photos are stored as links (OneDrive / SharePoint).
