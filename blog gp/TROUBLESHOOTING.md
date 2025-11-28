# Résolution Erreur 404 Vercel

## Problème
Erreur 404 NOT_FOUND sur Vercel

## Solutions à essayer (dans l'ordre)

### Solution 1 : Vérifier les paramètres dans Vercel Dashboard

1. Allez sur https://vercel.com/dashboard
2. Sélectionnez votre projet
3. **Settings** > **General**
4. Configurez EXACTEMENT comme suit :
   - **Framework Preset** : `Other`
   - **Root Directory** : (LAISSER VIDE - pas de `/` ni `.`)
   - **Build Command** : (LAISSER VIDE)
   - **Output Directory** : (LAISSER VIDE)
   - **Install Command** : (LAISSER VIDE)
5. **SAUVEZ** les changements
6. Allez dans **Deployments**
7. Cliquez sur les **3 points** du dernier déploiement
8. **Redeploy**

### Solution 2 : Supprimer et recréer le projet

1. Dans Vercel Dashboard, supprimez le projet
2. Cliquez sur **Add New Project**
3. Importez depuis GitHub
4. Lors de la configuration :
   - **Framework Preset** : `Other`
   - **Root Directory** : (vide)
   - **Build Command** : (vide)
   - **Output Directory** : (vide)
5. Cliquez sur **Deploy**

### Solution 3 : Vérifier que index.html est bien commité

```bash
git status
git add index.html
git commit -m "Ensure index.html is tracked"
git push
```

### Solution 4 : Vérifier les logs de déploiement

1. Dans Vercel Dashboard > votre projet
2. Cliquez sur le dernier déploiement
3. Regardez les **Build Logs**
4. Cherchez des erreurs ou warnings

### Solution 5 : Test avec Vercel CLI

```bash
npm i -g vercel
cd "/Users/xd/Downloads/Work/wimbledon/site/blog gp"
vercel
```

Cela vous permettra de voir les erreurs en temps réel.

## Vérifications importantes

- [ ] `index.html` est à la racine du repository
- [ ] `vercel.json` est à la racine
- [ ] Tous les fichiers sont commités et pushés
- [ ] Framework Preset est sur "Other"
- [ ] Aucun build command n'est défini

## Si rien ne fonctionne

Contactez le support Vercel avec :
- L'URL de votre projet
- Les logs de déploiement
- Une capture d'écran des paramètres du projet

