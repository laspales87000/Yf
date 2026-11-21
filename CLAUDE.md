# Consignes pour Claude

## Le projet
- L'application est un seul fichier : `index.html` (suivi de séries, films, livres et BDs).
- Elle est publiée avec GitHub Pages : https://laspales87000.github.io/Yf/
- `yf.html` sert seulement à rediriger l'ancien lien vers `index.html`. Ne pas y mettre l'application.
- Le geste retour (glisser vers la droite) et le bouton retour du téléphone doivent toujours faire
  exactement comme le bouton « ← Retour » de l'écran : revenir à l'écran ou au menu d'avant.
- `fiche.html` est la page « fiche seule » (lecture seule, sans lien vers l'appli) ouverte par les fiches envoyées.
- `acces.html` est la page publique « Accès réservé » (montrée aux personnes non autorisées par Cloudflare) :
  elle ne doit jamais contenir de lien vers l'application.
- `wrangler.jsonc` et `.assetsignore` servent à la mise en ligne chez Cloudflare (site fait seulement de fichiers) :
  `.assetsignore` liste les fichiers du dépôt à ne jamais publier (CLAUDE.md, LICENSE…).
- `vendor/` contient des outils tiers rangés dans le dépôt pour la sécurité (lecture de texte Tesseract,
  lecture des PDF avec PDF.js 4.10.38 « legacy », toujours ouvert avec `isEvalSupported:false`,
  fabrication des QR codes avec qrcode-generator 2.0.4).
  Les outils chargés depuis Internet ont une empreinte de contrôle (SRI) dans `index.html` : si on change
  leur version, il faut recalculer l'empreinte.

## Façon de travailler
- Répondre en français, simplement, sans jargon technique.
- **Tout écrire en français, en permanence et sans exception** : chaque phrase affichée à l'écran
  (y compris les petits messages pendant le travail), les messages d'enregistrement (commits)
  et les demandes de fusion (titre et description).
- Modifier directement `index.html` du dépôt. Ne pas demander de renvoyer le fichier.
- Tester chaque modification dans un navigateur, en taille téléphone, avant de l'envoyer.
- **Toujours illustrer les propositions avec des images** (maquettes ou captures en taille téléphone,
  une image par proposition), et pas seulement avec des descriptions, avant de demander un choix.
- **Si une demande n'est pas logique, imprécise ou peut se comprendre de plusieurs façons : toujours poser
  des questions avant de commencer**, sans rien modifier.
- Commencer chaque réponse par l'heure de Paris : « 🕐 **JJ/MM/AAAA – HH h MM** ».
- **Fusionner soi-même** la demande de fusion (pull request) vers `main` dès que la modification
  est prête et testée, sans demander de validation. Ensuite, dire qu'il suffit de recharger
  https://laspales87000.github.io/Yf/ après une ou deux minutes.
- Les prix des services payants (voix, Gemini) sont des estimations écrites dans `index.html`
  (`PRICED`, `VPRICE`, `VPURL`, `vCost`) : quand on les vérifie, mettre à jour les chiffres et la date.
- Les données de chaque utilisateur restent sur son appareil : ne jamais casser la façon dont
  elles sont enregistrées, ni la synchronisation GitHub, ni les sauvegardes.
