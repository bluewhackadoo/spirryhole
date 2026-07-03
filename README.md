# spirryhole.com

Conspiracy theory catfish. Mix of real facts dressed as conspiracies and ridiculous spirries.

## Pages
- `index.html` — main feed (posts shuffle on every load)
- `about.html` — node dossier
- `submit.html` — tip submission (uses Formspree)

## Deploy to Azure Static Web Apps

### One-time setup

1. Push this repo to GitHub
2. In Azure Portal → **Create a resource** → search **Static Web App**
3. Link to your GitHub repo, branch `main`, app location `/`
4. Azure creates the `AZURE_STATIC_WEB_APPS_API_TOKEN` secret in your repo automatically
5. Point `spirryhole.com` DNS to the Azure SWA hostname (CNAME)

That's it. Every push to `main` auto-deploys.

### Contact form (optional)

1. Sign up at [formspree.io](https://formspree.io) (free tier = 50 submissions/month)
2. Create a form, grab the form ID
3. In `submit.html`, replace `YOUR_FORM_ID` in the form action URL
4. Uncomment the fetch block in the submit script

## Subtle color coding

- Blue tint + blue 3px dot = spirry (ridiculous)
- Rose tint + pink 3px dot = buried truth (documented fact)
- ~0.18 opacity — requires a color picker to notice
- Hover stamp reveals `UNCONFIRMED` (spirry) or `EVIDENCE FOUND` (truth)
