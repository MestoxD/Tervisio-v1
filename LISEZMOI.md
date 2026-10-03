# Landing page TERVISIO, version animée

Site statique (HTML, CSS, JavaScript), prêt à déployer sur Vercel : glisser le dossier, ou passer par GitHub.

## Structure

```
index.html                 la page
assets/img/                images (WebP) et logos
assets/js/                 GSAP 3.15, ScrollTrigger, Lenis (fichiers locaux, sans CDN)
assets/fonts/              police Archivo variable et sa licence (SIL OFL)
```

## Images et emplacements

| Fichier | Emplacement |
|---|---|
| tervisio-mockup.webp | Hero : ordinateur incliné qui se redresse au défilement |
| tervisio-mobile.webp | Bloc « Un dossier qui se perd en chemin » |
| ecran-activite.webp, ecran-stocks.webp, ecran-rendez-vous.webp | Carrousel de « Ce que TERVISIO remplace » |
| dashboard-ecran.webp | Onglets des fonctionnalités : écran extrait du mockup, la caméra zoome sur le module choisi |
| medecin.webp | Bloc Tarifs |

Pour remplacer une image, garder le même nom de fichier. Les zones de zoom des onglets sont réglées par l'attribut `data-focus` de chaque onglet (x, y, largeur, hauteur en pixels sur l'écran de 1317 × 874).

## Animations

Entrée orchestrée du hero, fond WebGL animé (hero et contact), bordure lumineuse (onglets et tarifs), défilement fluide, barre de progression, en-tête qui se masque à la descente, bandeau défilant des modules, titres révélés mot à mot, téléphone en parallaxe, caméra sur le tableau de bord, ligne du parcours qui se dessine, icônes tracées, ancien usage barré puis nouveau révélé, carrousel 3D, FAQ animée, boutons magnétiques, signature TERVISIO dans le pied de page.

Toutes les animations s'arrêtent si le visiteur a activé « réduire les animations » dans son système. Les fonds WebGL se mettent en pause hors de l'écran.

## Formulaire

En haut du dernier script de index.html :

- `FORM_ENDPOINT` : adresse du webhook qui reçoit les demandes (par exemple n8n). Vide, le formulaire ouvre la messagerie du visiteur avec la demande pré-remplie.
- `CONTACT_EMAIL` : adresse de destination en mode messagerie.

## Reste à fournir

- Les réponses des six questions marquées « À compléter » dans la FAQ.
- Les pages mentions-legales.html et confidentialite.html, liées dans le pied de page.
- Un écran du dossier patient, pour le premier onglet.
- Une image de partage (og:image).
