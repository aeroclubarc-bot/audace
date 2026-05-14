# AUDACE Chavenay — Site web

**Association des Usagers De l'Aérodrome de Chavenay et de son Environnement**

Site vitrine de l'AUDACE, association représentant les usagers de l'aérodrome de Chavenay-Villepreux (LFPX).

## 🚀 Déploiement

### Railway (recommandé)

1. Créer un compte sur [railway.app](https://railway.app)
2. New Project → Deploy from GitHub repo
3. Sélectionner ce repo → Railway détecte automatiquement Node.js
4. Variables d'environnement : aucune requise
5. Deploy → le site est en ligne en 2 minutes

URL automatique : `audace-chavenay.up.railway.app`  
Pour un domaine custom : Settings → Custom Domain → `audace-chavenay.fr`

### GitHub Pages (alternative statique)

1. Push sur GitHub
2. Settings → Pages → Source: `main` branch → `/public` folder
3. URL : `https://[username].github.io/audace-chavenay`

> ⚠️ GitHub Pages ne supporte que les sites statiques. Railway est recommandé pour la flexibilité future (formulaire de contact, newsletter, etc.)

## 📁 Structure

```
audace-chavenay/
├── public/
│   ├── index.html        ← Site principal (tout-en-un)
│   └── audace-logo.png   ← Logo PNG transparent
├── server.js             ← Serveur Express (Railway)
├── package.json
├── railway.toml          ← Config Railway
└── .gitignore
```

## 🛠 Développement local

```bash
npm install
npm start
# → http://localhost:3000
```

## ✏️ Modifier le contenu

Tout le contenu est dans `public/index.html`.  
Sections principales :
- `#missions` — Les 4 piliers
- `#charte` — La Charte de Chavenay + articles
- `#ou-voler` — Les clubs + infos pistes
- `#jeunes` — Jeunes & Métiers
- `#communes` — Communes partenaires
- `#contact` — Formulaire de contact

## 📧 Formulaire de contact

Le formulaire est actuellement en mode démo (pas d'envoi réel).  
Pour activer l'envoi d'emails, ajouter [Resend](https://resend.com) :

```bash
npm install resend
```

Puis ajouter la variable `RESEND_API_KEY` dans Railway.

---

*AUDACE · Association loi 1901 · N° W78000748 · Aérodrome de Chavenay 78450 Villepreux*
