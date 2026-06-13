# pragma-web

Static site for **Pragma** — performance marketing studio.
No build step. Plain HTML + CSS. Deploys to GitHub Pages as-is.

## Structure

```
pragma-web/
├─ index.html        → Pragma corporate home (general marketing landing)
├─ audit/
│  └─ index.html     → AI Visibility Audit (the money page / lead magnet)
├─ styles.css        → shared brand stylesheet (Brand v0.1)
└─ README.md
```

- Home: `https://<user>.github.io/pragma-web/`
- Money page: `https://<user>.github.io/pragma-web/audit/`  ← send outreach/ad traffic here

## Before going live — 3 things to connect

1. **Stripe Payment Link (USD).** Create a $299 USD Payment Link in Stripe → in `audit/index.html` replace `PASTE_STRIPE_LINK`.
2. **Mercado Pago link (MXN).** Create a $4,900 MXN payment link → replace `PASTE_MERCADOPAGO_LINK`.
3. **Formspree (lead form).** Create a free form at formspree.io routing to `jackdaniel@happiier.studio` → replace `YOUR_FORMSPREE_ID` in both `index.html` and `audit/index.html`.

## Deploy (GitHub Pages)

```bash
# from this folder
git init
git add .
git commit -m "Pragma site v0.1: home + AI Visibility Audit money page"
git branch -M main
git remote add origin https://github.com/<user>/pragma-web.git
git push -u origin main
```

Then on GitHub: **Settings → Pages → Source: `main` / root**. Live in ~1 minute.

## Brand source of truth

`../Pragma — INFO.md` (OneDrive). Colors, voice, offer ladder, pending items.

## TODO (v0.1 → v1)

- [ ] Embed real **Smile Human** sample audit in the `#sample` slot.
- [ ] Paste Stripe + Mercado Pago links.
- [ ] Connect Formspree.
- [ ] Add client results / testimonials (trust load — no faces yet).
- [ ] Custom domain when ready (replaces github.io).
