# MCQ Media website (draft)

Static site for mcqmediallc.com, built for GitHub Pages. No build step is needed: upload the files as they are.

## Pages
- `index.html`: studio home
- `beards-of-iron.html`: game page
- `support.html`: support email and FAQ (Apple requires a support URL)
- `privacy.html`: privacy policy (Apple and Google require a privacy policy URL)
- `style.css`, `img/`: shared styles and art taken from the game
- `CNAME`: tells GitHub Pages to serve the site at mcqmediallc.com

## Check before going live
- [ ] Fill in `[EFFECTIVE DATE]` in privacy.html.
- [ ] The privacy policy describes the planned launch setup: Google AdMob rewarded ads, the iPhone tracking prompt, and Apple in-app purchases. If the game launches without ads or purchases, remove those parts. Don't publish claims the game doesn't match yet.
- [ ] The support FAQ mentions a Restore Purchases button in the Shop. Add that button before launch, or edit the FAQ.
- [x] Age: Chris confirmed (2026-11-19) the game is not directed to children under 13. Pick a matching App Store age rating.
- [ ] Optional: have a lawyer look over the privacy policy.

## Putting it on GitHub Pages
1. Create a new **public** repository, for example `mcqmedia-site`, and upload everything in this folder to it.
2. In the repository, go to Settings, then Pages, choose "Deploy from a branch" with `main` and `/ (root)`, and set the custom domain to `mcqmediallc.com`.
3. In Porkbun DNS, replace the ALIAS record and the `*` CNAME record (both point at uixie.porkbun.com) with GitHub's records. Leave the iCloud email records (MX, TXT, DKIM) alone.
4. Once GitHub shows the domain as verified, tick "Enforce HTTPS".
