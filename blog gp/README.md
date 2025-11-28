# GP Explorer 3 - Guide Merchandising

Site statique HTML/CSS dédié au merchandising du GP Explorer 3.

## Structure

- `index.html` - Page d'accueil
- `where-to-buy.html` - Liste des boutiques officielles
- `faq.html` - FAQ sur le merchandising
- `about.html` - À propos du GP Explorer 3
- `privacy-policy.html` - Politique de confidentialité
- `blog/` - Articles de blog sur le merchandising
- `images/` - Images et logo
- `styles.css` - Feuille de style principale

## Déploiement sur Vercel

1. Connectez votre repository GitHub à Vercel
2. Vercel détectera automatiquement que c'est un site statique
3. Le fichier `vercel.json` configure les headers de sécurité et le cache
4. Le site sera déployé automatiquement à chaque push

## Configuration

- **Framework Preset**: Other
- **Build Command**: (aucun - site statique)
- **Output Directory**: (racine)

## Notes

- Tous les chemins sont relatifs
- Les images sont dans `/images/`
- Le logo est en format AVIF pour une meilleure performance
- Le site est entièrement en français

