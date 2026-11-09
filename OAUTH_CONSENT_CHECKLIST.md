# BusinessFlow – OAuth consent screen fill-in

Use these values in Google Cloud Console → **APIs & Services → OAuth consent screen**.

## Ready now (local files)

| Field | Value / file |
|---|---|
| **App name** | `Businessflow` |
| **User support email** | `mariusolsen13@gmail.com` |
| **App logo** | Upload `website/assets/businessflow-logo-120.png` (120×120 PNG, ~6 KB) |
| **Developer contact email** | `mariusolsen13@gmail.com` |

## Live GitHub Pages URLs (paste into Cloud Console)

Site repo: https://github.com/MariusBosnes/businessflow  
Live site: https://mariusbosnes.github.io/businessflow/

| Field | Value |
|---|---|
| **Application home page** | `https://mariusbosnes.github.io/businessflow/` |
| **Application privacy policy link** | `https://mariusbosnes.github.io/businessflow/privacy.html` |
| **Application terms of service link** | `https://mariusbosnes.github.io/businessflow/terms.html` |
| **Authorized domains** | `github.io` |

### Search Console (required before Google verifies)

1. Open [Google Search Console](https://search.google.com/search-console)
2. Add property → URL prefix: `https://mariusbosnes.github.io/businessflow/`
3. Verify ownership (HTML file upload into this repo, or Google Analytics / DNS if you use a custom domain)
4. Same Google account must be owner/editor on the Cloud / Apps Script project

### Optional later: custom domain

Buy a domain (e.g. `businessflow.app`), point it at this Pages site, verify that domain in Search Console, then swap the three URLs and set Authorized domain to `businessflow.app`.

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
