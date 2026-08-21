# Site web Mindflow Budget

Site vitrine statique de l'application Mindflow Budget — https://mindflow-budget.app

## Contenu

| Fichier | Rôle | URL publique |
|---|---|---|
| `index.html` | Page d'accueil (SEO + redirection vers la page principale) | `/` |
| `Mindflow Budget Site.dc.html` | Page principale du site | `/` |
| `Support.dc.html` | Formulaire de contact (mailto pré-rempli) | `/support` |
| `Confidentialite.dc.html` | Politique de confidentialité | `/confidentialite` |
| `Conditions.dc.html` | Conditions d'utilisation | `/conditions` |
| `support.js` | Runtime nécessaire aux pages `.dc.html` | — |
| `assets/` | Icône de l'app et captures d'écran iPhone / Android | — |
| `netlify.toml` | Configuration Netlify (URLs propres, cache, en-têtes) | — |

Aucune étape de build : ce sont des fichiers statiques, servis tels quels.

## Déploiement

1. Netlify → **Add new site → Import an existing project → GitHub** → choisir ce dépôt.
2. Build command : *(vide)* — Publish directory : `.`
3. **Domain management → Add custom domain** → `mindflow-budget.app`, puis suivre les enregistrements DNS.
   Le `.app` impose HTTPS ; le certificat est généré automatiquement par Netlify.

Chaque `git push` sur la branche principale redéploie le site automatiquement.

## Mise à jour du contenu

- **Textes FR/EN** : dictionnaire `dict` dans le bloc de logique en bas de chaque `.dc.html`.
- **Captures d'écran** : remplacer les fichiers dans `assets/` en gardant les mêmes noms
  (`ip-*.jpeg` pour iPhone, `ga-*.jpeg` pour Android).
- **Liens des stores** : rechercher `apps.apple.com` et `play.google.com` dans
  `Mindflow Budget Site.dc.html`.
- **Intensité des animations** : propriété `motionIntensity` (0 = statique, 1 = défaut, 1.6 = marqué).

## À faire

- [ ] Remplacer les 3 témoignages (actuellement fictifs) par de vrais avis App Store.
- [ ] Faire relire les Conditions d'utilisation par un juriste.
- [ ] Remplacer le lien Google Play par l'URL directe de la fiche une fois la version publique validée.
