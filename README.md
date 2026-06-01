# BOTTY website

Static, multi-language (10) landing page for the BOTTY project / BTY token.

## Edit before launch
Open `index.html` and edit the `CONFIG` block near the bottom:
- `presaleStart` / `presaleDays` — presale start (UTC) and length (2 weeks).
- `goal` — presale allocation in BTY.
- `raised` — set a **real sold number** for the bar; leave `null` for a time-based demo fill.
- `tokenPriceUsd` — real presale price.
- `buyUrl` — your presale/buy link.

## Run locally
Open `index.html` in a browser, or:
```
docker build -t botty-web . && docker run -p 8080:80 botty-web
```
Then visit http://localhost:8080

## Deploy on Coolify
1. Push this folder to a Git repo (GitHub).
2. Coolify → **New Resource → Public/Private Repository** → select the repo.
3. Build pack: **Dockerfile** (auto-detected). Port: **80**.
4. Add your domain (e.g. `botty.ubasoft.net`) → Coolify issues HTTPS automatically.
5. Deploy.
