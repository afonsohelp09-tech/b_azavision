# VENTE EN LIGNE TPE

Lot **ERP e‑commerce** (vêtements & accessoires) prêt pour **Google Apps Script** + pages **HTML** autonomes : URL de l’API Web App documentée **dans les fichiers** (variables `ERP_API_URL_DEFAULT` et bloc COLAR), sans `config.js`.

## Contenu du dépôt

| Fichier | Rôle |
|--------|------|
| `api_apps_script.gs` | Backend à coller dans le projet Apps Script lié à la feuille Google Sheets |
| `admin_erp.html` | Panneau d’administration (responsive, menu mobile) |
| `boutique_client.html` | Vitrine client (responsive, tiroir navigation) |
| `INSTRUCTIONS_INSTALLATION.txt` | Guide d’installation détaillé (FR) |

## Installation rapide

1. Ouvrez **Google Sheets** + **Extensions** → **Apps Script**, remplacez tout le code par `api_apps_script.gs`, enregistrez.
2. **Déployer** → **Application Web** → exécuter en tant que vous, accès **Toute personne** ; copiez l’URL se terminant par **`/exec`**.
3. Dans **`admin_erp.html`** et **`boutique_client.html`**, renseignez la même URL dans `window.ERP_API_URL_DEFAULT` et/ou la ligne marquée **COLAR** (voir commentaires dans les fichiers).
4. Hébergez les HTML en **HTTPS** (Google Sites, Netlify, GitHub Pages *avec la bonne config*, etc.). Évitez `file://` pour les appels `fetch` vers Apps Script.

Détails : lisez **`INSTRUCTIONS_INSTALLATION.txt`**.

## Publier sur GitHub

Dans un terminal, à la racine **de ce dossier** (`VENTE EN LIGNE TPE`) :

```bash
git init
git add .
git commit -m "Initial import: VENTE EN LIGNE TPE (ERP + vitrine)"
```

Sur GitHub : créez un **nouveau dépôt** vide, puis :

```bash
git remote add origin https://github.com/VOTRE_USER/VOTRE_REPO.git
git branch -M main
git push -u origin main
```

*(Remplacez l’URL par celle de votre repo.)*

## Sécurité

- Ne commitez pas de **clés secrètes** (Stripe, etc.) : utilisez les **propriétés du script** côté Apps Script si votre code les prévoit.
- L’URL `/exec` du Web App est en général **publique** une fois déployée ; la protection repose sur la logique du script (tokens, rôles, etc.).

## Licence

À définir par le détenteur du projet (ce dépôt ne impose pas de licence par défaut).
