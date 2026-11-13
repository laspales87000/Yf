# Consignes pour Claude

## Le projet
- L'application est un seul fichier : `index.html` (suivi de séries, films, livres et BDs).
- Elle est publiée avec GitHub Pages : https://laspales87000.github.io/Yf/
- `yf.html` sert seulement à rediriger l'ancien lien vers `index.html`. Ne pas y mettre l'application.
- `vendor/` contient des outils tiers rangés dans le dépôt pour la sécurité (lecture de texte Tesseract,
  lecture des PDF avec PDF.js 4.10.38 « legacy », toujours ouvert avec `isEvalSupported:false`).
  Les outils chargés depuis Internet ont une empreinte de contrôle (SRI) dans `index.html` : si on change
  leur version, il faut recalculer l'empreinte.

## Façon de travailler
- Répondre en français, simplement, sans jargon technique.
- Modifier directement `index.html` du dépôt. Ne pas demander de renvoyer le fichier.
- Tester chaque modification dans un navigateur, en taille téléphone, avant de l'envoyer.
- **Fusionner soi-même** la demande de fusion (pull request) vers `main` dès que la modification
  est prête et testée, sans demander de validation. Ensuite, dire qu'il suffit de recharger
  https://laspales87000.github.io/Yf/ après une ou deux minutes.
- Les données de chaque utilisateur restent sur son appareil : ne jamais casser la façon dont
  elles sont enregistrées, ni la synchronisation GitHub, ni les sauvegardes.
