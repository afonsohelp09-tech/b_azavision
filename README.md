# Vitrine boutique — GitHub Pages

## Fichiers à la racine du dépôt

Placez **le contenu de ce dossier** à la racine du dépôt GitHub de la vitrine.

| Fichier | Description |
|---------|-------------|
| **`index.html`** | **Vitrine complète** (tout le HTML, CSS et JS embarqués) — **c’est le fichier principal** pour GitHub Pages. |
| `boutique_client.html` | Même application que `index.html` (copie pour compatibilité / liens existants). Vous pouvez ne versionner que `index.html` si vous préférez un seul fichier. |
| `.nojekyll` | Évite que Jekyll casse des fichiers sur GitHub Pages |
| `.gitignore` | Fichiers à ne pas versionner |

`window.ERP_BOUTIQUE_URL` pointe vers `index.html` pour que la boutique s’affiche correctement à la racine du site (`https://…github.io/nom-du-depot/`).

## Avant la mise en ligne obligatoire

1. Ouvrir **`index.html`** (ou `boutique_client.html` — même contenu) et configurer l’**URL du Web App** Google Apps Script :
   - `window.ERP_API_URL_DEFAULT = 'https://script.google.com/macros/s/.../exec'`
   - et/ou la ligne `var API_URL = '...'` dans le bloc « COLAR ».
2. Si l’**admin** est hébergé ailleurs, définir une URL **HTTPS absolue** vers sa page (idéalement `…/index.html`) :
   - `window.ERP_ADMIN_URL = 'https://VOTRE-USER.github.io/VOTRE-REPO-ADMIN/index.html';`
3. Ne pas ouvrir la page en `file://` : tester via l’URL GitHub Pages (`https://...`).

## Activer GitHub Pages

Dépôt → **Settings** → **Pages** → Source : branche `main` (ou `master`), dossier `/ (root)`.

## Optionnel

- Images / logo : ajoutez un dossier (ex. `images/`) et référencez les chemins dans l’HTML ou les paramètres boutique côté admin.
