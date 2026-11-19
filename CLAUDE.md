# Consignes pour Claude

## Le projet
- L'application est un seul fichier : `index.html` (suivi de séries, films, livres et BDs).
- Elle est publiée avec GitHub Pages : https://laspales87000.github.io/Yf/
- `yf.html` sert seulement à rediriger l'ancien lien vers `index.html`. Ne pas y mettre l'application.
- `fiche.html` est la page « fiche seule » (lecture seule, sans lien vers l'appli) ouverte par les fiches envoyées.
- `vendor/` contient des outils tiers rangés dans le dépôt pour la sécurité (lecture de texte Tesseract,
  lecture des PDF avec PDF.js 4.10.38 « legacy », toujours ouvert avec `isEvalSupported:false`,
  fabrication des QR codes avec qrcode-generator 2.0.4).
  Les outils chargés depuis Internet ont une empreinte de contrôle (SRI) dans `index.html` : si on change
  leur version, il faut recalculer l'empreinte.

## Façon de travailler
- Répondre en français, simplement, sans jargon technique.
- **Tout écrire en français**, sans exception : les petits messages pendant le travail, les messages
  d'enregistrement (commits) et les demandes de fusion (titre et description).
- Modifier directement `index.html` du dépôt. Ne pas demander de renvoyer le fichier.
- Tester chaque modification dans un navigateur, en taille téléphone, avant de l'envoyer.
- **Toujours illustrer les propositions avec des images** (maquettes ou captures en taille téléphone,
  une image par proposition), et pas seulement avec des descriptions, avant de demander un choix.
- Poser des questions avant de travailler quand quelque chose n'est pas clair.
- Commencer chaque réponse par l'heure de Paris : « 🕐 **JJ/MM/AAAA – HH h MM** ».
- **Fusionner soi-même** la demande de fusion (pull request) vers `main` dès que la modification
  est prête et testée, sans demander de validation. Ensuite, dire qu'il suffit de recharger
  https://laspales87000.github.io/Yf/ après une ou deux minutes.
- Les prix des services payants (voix, Gemini) sont des estimations écrites dans `index.html`
  (`PRICED`, `VPRICE`, `VPURL`, `vCost`) : quand on les vérifie, mettre à jour les chiffres et la date.
- Les données de chaque utilisateur restent sur son appareil : ne jamais casser la façon dont
  elles sont enregistrées, ni la synchronisation GitHub, ni les sauvegardes.
