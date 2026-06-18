# 🌿 ArboPest v2 — Plateforme IPM

> Livrable 1 — Design System CSS + Layout B

## Stack
- HTML + CSS + Vanilla JS (fichier unique)
- Open-Meteo API (météo gratuite)
- Notion API (bases de données)
- Lucide Icons CDN

## Livrable 1 — Ce qui est inclus

| Composant | Statut |
|---|---|
| Reset CSS + Variables `:root` complètes | ✅ |
| Layout B : Sidebar PC verte + Bottom Nav mobile | ✅ |
| Responsive 430px / 768px / 1200px | ✅ |
| Typographie Inter Tight + Inter | ✅ |
| Lucide Icons CDN | ✅ |
| Animations hover CSS (GPU) | ✅ |
| 4 boutons couleurs hover distinctes (GPS/Biofix/Réglages/Alerte) | ✅ |
| 3 types cards (safe / warn / danger) | ✅ |
| Badges de statut (6 variantes) | ✅ |
| DD Progress Bar avec milestones | ✅ |
| Toast notifications | ✅ |
| Connexion Notion (placeholder + live) | ✅ |

## Décisions design validées

- **Fond** : `#F5F0E8` blanc cassé chaud
- **Sidebar** : `#1A3A1A` vert très foncé
- **Accent logo** : `#7BC67E`
- **Transitions** : `cubic-bezier(0.16, 1, 0.3, 1)`
- **Hover cards** : `translateY(-3px)`
- **Hover boutons** : `translateY(-2px)`
- **Icônes hover** : `scale(1.15)`

## Variables CSS clés

```css
--bg:       #F5F0E8
--green:    #1A3A1A
--orange:   #FF4D00
--red:      #CC0000
--blue:     #4A90D9
--t-fast:   150ms cubic-bezier(0.16,1,0.3,1)
--t-smooth: 220ms cubic-bezier(0.16,1,0.3,1)
--t-spring: 350ms cubic-bezier(0.34,1.56,0.64,1)
--sidebar-w: 220px
```

## Configuration Notion

Dans `index.html`, remplir `NOTION_CONFIG.db` avec les IDs des bases Notion :

```js
const NOTION_CONFIG = {
  apiBase: 'https://votre-proxy.vercel.app/api',
  db: {
    cultures:  'VOTRE_DB_ID',
    ravageurs: 'VOTRE_DB_ID',
    meteo:     'VOTRE_DB_ID',
    produits:  'VOTRE_DB_ID',
    alertes:   'VOTRE_DB_ID'
  }
};
```

> ⚠️ Ne jamais exposer la clé API Notion directement côté client. Utiliser un proxy CORS (Vercel/Netlify Function).

## GitHub Pages

Activé sur `main` → accessible sur : `https://omarmfl-cmyk.github.io/arbopest-v2/`

---
*IAV Hassan II — MPVE 4e année — Omar Mouflih*
