# 🚀 Guide de Déploiement sur GitHub Pages

## Avant de commencer
- Avoir un compte GitHub : https://github.com
- Avoir Git installé sur votre PC : https://git-scm.com
- Avoir Node.js installé : https://nodejs.org

---

## ÉTAPE 1 — Modifier le package.json

Ouvrez `package.json` et remplacez :
```
"homepage": "https://VOTRE_USERNAME.github.io/NOM_DU_REPO",
```
Par votre vrai nom d'utilisateur GitHub et le nom que vous donnerez au dépôt.

**Exemple :**
```
"homepage": "https://jean123.github.io/mon-app",
```

---

## ÉTAPE 2 — Créer un dépôt GitHub

1. Allez sur https://github.com/new
2. Donnez un nom au dépôt (ex: `mon-app`)
3. Laissez-le **Public**
4. Cliquez **Create repository**
5. Copiez l'URL du dépôt (ex: `https://github.com/jean123/mon-app.git`)

---

## ÉTAPE 3 — Pousser le code

Ouvrez un terminal dans le dossier du projet et tapez :

```bash
git init
git add .
git commit -m "Premier commit"
git branch -M main
git remote add origin https://github.com/Dipongui237/CASA_PUPPIES.git
git push -u origin main
```

---

## ÉTAPE 4 — Installer les dépendances et déployer

```bash
npm install
npm run deploy
```

Cette commande va :
1. Builder l'application (optimiser les animations Framer Motion, CSS, etc.)
2. Créer une branche `gh-pages` sur GitHub
3. Y pousser le dossier `dist/`

---

## ÉTAPE 5 — Activer GitHub Pages

1. Allez dans votre dépôt GitHub
2. Cliquez **Settings** → **Pages**
3. Dans **Branch**, sélectionnez `gh-pages` → `/ (root)`
4. Cliquez **Save**

⏳ Attendez 2-3 minutes, puis visitez :
**https://VOTRE_USERNAME.github.io/NOM_DU_REPO**

---

## ✅ Ce qui a été configuré pour vous

| Fichier | Modification |
|--------|-------------|
| `vite.config.ts` | `base: './'` ajouté → les animations et assets se chargent correctement |
| `package.json` | Scripts `predeploy` et `deploy` ajoutés |
| `gh-pages` | Package installé dans les devDependencies |

---

## 🔄 Pour mettre à jour l'app plus tard

```bash
git add .
git commit -m "Mise à jour"
git push
npm run deploy
```

