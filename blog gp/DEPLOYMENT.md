# Guide de Déploiement Vercel - Résolution 404

## Problème : Erreur 404 NOT_FOUND

Si vous obtenez une erreur 404, voici les étapes à suivre :

### 1. Vérification dans le Dashboard Vercel

1. Allez sur https://vercel.com/dashboard
2. Sélectionnez votre projet
3. Allez dans **Settings** > **General**
4. Vérifiez les paramètres suivants :
   - **Framework Preset** : `Other` ou `None`
   - **Build Command** : (laisser vide)
   - **Output Directory** : (laisser vide ou `.`)
   - **Install Command** : (laisser vide)

### 2. Configuration du Projet

Le projet doit être configuré comme suit :
- **Framework Preset** : `Other`
- **Root Directory** : (laisser vide si tous les fichiers sont à la racine)
- **Build Command** : (vide - site statique)
- **Output Directory** : (vide)

### 3. Structure des Fichiers

Assurez-vous que `index.html` est bien à la racine du projet :
```
/
├── index.html          ← Doit être à la racine
├── styles.css
├── images/
├── blog/
├── vercel.json
└── package.json
```

### 4. Redéploiement

1. Dans Vercel Dashboard, allez dans **Deployments**
2. Cliquez sur les 3 points (...) du dernier déploiement
3. Sélectionnez **Redeploy**
4. Ou faites un nouveau commit et push

### 5. Vérification des Logs

1. Dans Vercel Dashboard, ouvrez le dernier déploiement
2. Cliquez sur **View Function Logs**
3. Vérifiez s'il y a des erreurs

### 6. Test Local avec Vercel CLI (optionnel)

```bash
npm i -g vercel
vercel
```

### Solution Alternative

Si le problème persiste, essayez de :
1. Supprimer le projet sur Vercel
2. Le recréer en important depuis GitHub
3. Lors de la configuration, sélectionner **"Other"** comme Framework Preset
4. Laisser tous les champs de build vides

