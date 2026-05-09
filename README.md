# Vitrine boutique — GitHub Pages

Alias : **BOUTIQUE** ou **BOUTIQUE_CLIENT** (même paquet que ce dossier).

## Fichiers à la racine du dépôt

Placez **le contenu de ce dossier** à la racine du dépôt GitHub de la vitrine.

| Fichier | Description |
|---------|-------------|
| **`index.html`** | **Vitrine complète** (tout le HTML, CSS et JS embarqués) — **c’est le fichier principal** pour GitHub Pages. |
| `boutique_client.html` | Même application que `index.html` (copie pour compatibilité / liens existants). Vous pouvez ne versionner que `index.html` si vous préférez un seul fichier. |
| `.nojekyll` | Évite que Jekyll casse des fichiers sur GitHub Pages |
| `.gitignore` | Fichiers à ne pas versionner |

`window.ERP_BOUTIQUE_URL` vaut `index.html` pour la racine GitHub Pages. Dans les fichiers livrés ici, `window.ERP_ADMIN_URL` est un **exemple** (`https://VOTRE-USER.github.io/VOTRE-REPO-ADMIN/index.html`) : remplacez-le par votre URL admin réelle.

## Avant la mise en ligne obligatoire

1. Ouvrir **`index.html`** (ou `boutique_client.html` — même contenu) et configurer l’**URL du Web App** Google Apps Script :
   - `window.ERP_API_URL_DEFAULT = 'https://script.google.com/macros/s/.../exec'`
   - et/ou la ligne `var API_URL = '...'` dans le bloc « COLAR ».
2. Remplacer **`window.ERP_ADMIN_URL`** par l’URL **HTTPS** de votre dépôt **ADMIN** (souvent `…/index.html`).
3. Ne pas ouvrir la page en `file://` : tester via l’URL GitHub Pages (`https://...`).

## Activer GitHub Pages

Dépôt → **Settings** → **Pages** → Source : branche `main` (ou `master`), dossier `/ (root)`.

## Optionnel

- Images / logo : ajoutez un dossier (ex. `images/`) et référencez les chemins dans l’HTML ou les paramètres boutique côté admin.
