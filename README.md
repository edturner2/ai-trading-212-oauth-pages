# AI Trading 212 OAuth Information Site

Public informational pages for the **AI Trading 212** Desktop OAuth client used with the owner's market-data maintenance workflows.

## Website
- Homepage: https://ai212.missionplotter.com/
- Privacy policy: https://ai212.missionplotter.com/privacy/
- Terms: https://ai212.missionplotter.com/terms/

## Enable GitHub Pages
In repository **Settings → Pages**, choose **Deploy from a branch**, branch **main**, folder **/(root)** and save. Set the **Custom domain** to `ai212.missionplotter.com` if not already displayed. When DNS is configured, enable **Enforce HTTPS**.

## DNS configuration
In the DNS zone for `missionplotter.com`, add one CNAME:
- **Host/Name:** `ai212`
- **Points to/Target:** `edturner2.github.io`

Do not change any root/apex, `www`, email, or existing Mission Plotter deployment records.

## Google OAuth branding
Once all three pages are publicly accessible via HTTPS, set Google Auth Platform Branding:
- App: `AI Trading 212`
- Support and developer email: configured privately within Google Cloud, not displayed on these pages.
- Homepage: `https://ai212.missionplotter.com/`
- Privacy: `https://ai212.missionplotter.com/privacy/`
- Terms: `https://ai212.missionplotter.com/terms/`
- Authorized domain: `missionplotter.com` (not the subdomain)

Verify domain ownership in Google Search Console if required. Change **Audience** from **Testing** to **In production** after completing any Google requirements. Only then obtain a new refresh token for the existing OAuth **Desktop application** and update the GitHub Actions secret.

## Separation and security
This repository must contain **only public HTML/CSS and disclosure text**. Private database code, data, OAuth credentials and GitHub secrets stay in the existing private `AI-Trading-212` repository. This website is not an OAuth redirect handler, brokerage or execution endpoint.


