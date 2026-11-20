# ClozingSystem

Site vitrine construit avec Astro, rendu statiquement dans `dist/`.

## Développement

```sh
npm install
npm run dev
```

Vérifier une version de production avec `npm run build`.

## Déploiement continu Cloudflare Pages

Le dépôt est prêt pour Cloudflare Pages en mode **Git integration** (projet statique, sans adaptateur serveur).

1. Installer Git, puis initialiser ce dossier : `git init`.
2. Créer un dépôt GitHub vide et y pousser la branche principale (`main`).
3. Dans Cloudflare, aller dans **Workers & Pages → Create application → Pages → Connect to Git** et choisir le dépôt.
4. Paramètres de build : **Framework preset** `Astro`, **Build command** `npm run build`, **Build output directory** `dist`, **Root directory** `/`.
5. Enregistrer. Cloudflare construit et publie les pushes, et crée des prévisualisations pour les pull requests.

Les changements de la configuration Cloudflare nécessitent l’accès au compte et au dépôt GitHub concernés. Les appels à l’action renvoient vers l’adresse courriel et la page de contact ClozingSystem.

## Structure

- `src/layouts/SiteLayout.astro` : document HTML, métadonnées et polices.
- `src/components/` : navigation, hero, titres de sections, contenu et footer.
- `src/styles/global.css` : styles globaux et responsive.
- `DESIGN-SYSTEM.md` : guide pour garder une cohérence visuelle lors des prochaines pages.
