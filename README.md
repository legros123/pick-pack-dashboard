# Pick & Pack · Suivi Performance Opérateurs

Dashboard individuel accessible par QR code pour les opérateurs Pick & Pack.  
**Rexel Champigneulles · CLR**

## Fonctionnement

Chaque opérateur scanne son QR code personnel → il accède à **ses stats uniquement** sur son téléphone :
- Score global + classement
- Production, quota, heures, erreurs
- Comparaison vs moyenne équipe
- Évolution mensuelle (Jan/Fév/Mars)

**Aucun opérateur ne peut voir les données individuelles des autres.**

## Déploiement sur GitHub Pages

### 1. Créer le repo
```
1. Va sur github.com → "New repository"
2. Nom : pick-pack-dashboard (ou ce que tu veux)
3. Public (obligatoire pour GitHub Pages gratuit)
4. Clique "Create repository"
```

### 2. Uploader le fichier
```
1. Clique "uploading an existing file"
2. Glisse le fichier index.html
3. Clique "Commit changes"
```

### 3. Activer GitHub Pages
```
1. Va dans Settings → Pages
2. Source : "Deploy from a branch"
3. Branch : main → / (root)
4. Clique Save
5. Attends 1-2 min → ton site est live !
```

### 4. URL du site
```
https://TON-USERNAME.github.io/pick-pack-dashboard/
```

Les QR codes se génèrent automatiquement avec cette URL.

## Mise à jour des données

Pour mettre à jour les données (chaque mois par exemple) :

1. Ouvre `index.html` dans un éditeur de texte
2. Cherche la ligne `const DATA = {`
3. Remplace le bloc JSON par les nouvelles données exportées
4. Commit sur GitHub → le site se met à jour automatiquement

## Structure des QR codes

| Opérateur | URL |
|-----------|-----|
| MESSAOUDI Kahin | `?op=MESSAOUDI` |
| MATHIEU Allan | `?op=MATHIEU` |
| STARCK Nicolas | `?op=STARCK` |
| ... | `?op=NOM` |

Page admin (sans paramètre) : affiche tous les QR codes, imprimable.

## Confidentialité

- Chaque opérateur ne voit que ses propres données
- Les stats équipe sont agrégées (moyennes globales uniquement)
- Aucune donnée nominative tierce n'est accessible
