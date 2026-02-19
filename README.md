# REFLECT

REFLECT est une web app statique (HTML/CSS/JS) prête à être déployée sur Cloudflare Pages, Vercel, Netlify ou GitHub Pages.

## Préparer la publication

1. Définir une clé API côté client **au runtime** (ne jamais la commiter) :

```html
<script>
  window.REFLECT_API_KEY = "sk-...";
</script>
```

2. Servir le dossier en statique.
3. Vérifier le mode PWA (`manifest.json` + `service-worker.js`).

## Développement local

```bash
python -m http.server 4173
```

Puis ouvrir `http://localhost:4173`.

## Sécurité

- La clé API est lue depuis `window.REFLECT_API_KEY` ou `localStorage["REFLECT_API_KEY"]`.
- Aucune clé secrète n'est embarquée dans le code source.

