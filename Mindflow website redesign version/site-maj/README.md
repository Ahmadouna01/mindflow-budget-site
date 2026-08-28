# Mindflow Budget — site web

Site statique (HTML/CSS/JS natif, aucun build).

## Pages
- `index.html` — accueil
- `support.html` — support et contact
- `confidentialite.html` — politique de confidentialite
- `conditions.html` — conditions d'utilisation
- `assets/` — icone et captures d'ecran

## Deploiement Netlify
Publish directory : `.` — aucune commande de build.
Les anciennes URL (`/Support.dc.html`, etc.) sont redirigees en 301 dans `netlify.toml`.

## Mise a jour
Remplacer les fichiers a la racine du depot, commit, push : Netlify redeploie automatiquement.
