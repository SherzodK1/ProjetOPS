# TP DevOps Node.js

Petite application web Node.js/Express pour demontrer une chaine DevOps simple :

```text
Code
↓
GitHub
↓
GitHub Actions
↓
Build
↓
Render
↓
Production
```

## Lancer en local

```bash
npm install
npm start
```

Puis ouvrir :

```text
http://localhost:3000
```

## Deploiement Render

Creer un Web Service Render connecte au depot GitHub.

- Build command : `npm install`
- Start command : `node app.js`

Render utilise aussi la variable `PORT`, deja prise en compte dans `app.js`.

## Demonstration CI/CD

Modifier dans `app.js` :

```js
res.send("Bonjour DevOps !");
```

par :

```js
res.send("Bonjour DevOps 2026 !");
```

Puis pousser la modification :

```bash
git add .
git commit -m "update message"
git push
```

GitHub Actions lance automatiquement le build, puis Render redeploie le site.
