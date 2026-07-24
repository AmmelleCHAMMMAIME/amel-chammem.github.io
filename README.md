# Portfolio

Site statique (HTML/CSS/JS, aucune étape de build) déployé gratuitement sur
**GitHub Pages** via **GitHub Actions**.

## 1. Contenu déjà personnalisé

Le site est rempli avec le contenu réel du CV (profil, parcours, stack,
projets, contact). Avant de publier, vérifie/ajuste :

- **Téléphone public** : le numéro apparaît dans la section Contact
  (`href="tel:..."`). Un site GitHub Pages est public — supprime cette ligne
  dans `index.html` si tu préfères ne partager que l'email et LinkedIn.
- **Dates de parcours** : certaines dates ont été reconstituées à partir du
  CV (mise en page complexe) — vérifie-les avant publication.
- `style.css` : les couleurs sont centralisées en haut du fichier dans `:root`
  si tu veux changer la palette (`--accent`, `--accent-2`, etc.).
- Ajoute une photo/CV en PDF dans le dossier `assets/` et référence-la depuis
  `index.html` (ex: `<img src="assets/photo.jpg">`).

## 2. Créer le dépôt GitHub

```bash
cd portfolio
git init
git add .
git commit -m "Portfolio initial"
git branch -M main
git remote add origin https://github.com/<ton-utilisateur>/<ton-repo>.git
git push -u origin main
```

## 3. Activer GitHub Pages via Actions

Sur GitHub :

1. Va dans **Settings → Pages**.
2. Sous **Build and deployment → Source**, choisis **GitHub Actions**.
3. Fais un push (ou relance le workflow depuis l'onglet **Actions**) : le
   workflow `.github/workflows/deploy.yml` se déclenche automatiquement à
   chaque push sur `main`.

Une fois le déploiement terminé (onglet **Actions** → coche verte), ton site
est en ligne à l'adresse :

```
https://<ton-utilisateur>.github.io/<ton-repo>/
```

## 4. Domaine personnalisé (optionnel)

Si tu as un nom de domaine, ajoute un fichier `CNAME` à la racine contenant
ton domaine (ex: `portfolio.mondomaine.com`), puis configure un enregistrement
DNS CNAME pointant vers `<ton-utilisateur>.github.io`.

## Structure du projet

```
portfolio/
├── index.html
├── style.css
├── script.js
├── assets/                  # images, CV, etc.
└── .github/
    └── workflows/
        └── deploy.yml       # déploiement automatique
```
"# amel-chammem.github.io" 
"# amel-chammem.github.io" 
