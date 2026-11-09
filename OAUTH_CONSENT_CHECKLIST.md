# BusinessFlow – OAuth consent screen fill-in

Use these values in Google Cloud Console → **APIs & Services → OAuth consent screen**.

## Ready now (local files)

| Field | Value / file |
|---|---|
| **App name** | `Businessflow` |
| **User support email** | `mariusolsen13@gmail.com` |
| **App logo** | Upload `website/assets/businessflow-logo-120.png` (120×120 PNG, ~6 KB) |
| **Developer contact email** | `mariusolsen13@gmail.com` |

## Needs hosting first

Google requires public HTTPS URLs on an **Authorized domain** you verify in [Google Search Console](https://search.google.com/search-console).

| Field | After you host the `website/` folder |
|---|---|
| **Application home page** | `https://YOUR-DOMAIN/` or `https://YOUR-DOMAIN/index.html` |
| **Application privacy policy link** | `https://YOUR-DOMAIN/privacy.html` |
| **Application terms of service link** | `https://YOUR-DOMAIN/terms.html` |
| **Authorized domains** | the root domain only, e.g. `github.io` or `businessflow.app` |

### Fastest free option: GitHub Pages

1. Create a public GitHub repo (or a `docs`/`gh-pages` branch) and upload the contents of `website/`.
2. Enable **Settings → Pages → Deploy from branch**.
3. Your site will look like: `https://YOURUSER.github.io/REPONAME/`
4. In Search Console, add the property and verify ownership (HTML file or DNS).
5. In OAuth consent screen, add authorized domain: `github.io`
6. Paste:
   - Home: `https://YOURUSER.github.io/REPONAME/`
   - Privacy: `https://YOURUSER.github.io/REPONAME/privacy.html`
   - Terms: `https://YOURUSER.github.io/REPONAME/terms.html`

### Better long-term option: your own domain

Buy a domain (e.g. `businessflow.app`), point it at GitHub Pages / Netlify / Cloudflare Pages, verify that domain in Search Console, then use:

- Home: `https://businessflow.app/`
- Privacy: `https://businessflow.app/privacy.html`
- Terms: `https://businessflow.app/terms.html`
- Authorized domain: `businessflow.app`

## After URLs work

1. Switch Apps Script to a **standard** GCP project (not the default).
2. Add every Apps Script OAuth scope on the consent screen (manual add if needed).
3. Publish app status to **Production**.
4. Click **Prepare for verification** / **Submit for verification**.
5. Expect scope justifications + a short demo video for Drive / send-mail.

## Preview locally

```bash
cd website
python3 -m http.server 8080
```

Open http://localhost:8080
