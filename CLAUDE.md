# villagomez.io — consignes pour Claude

Site de Villagomez Records : le label, les soirées LA VILLLA, le studio et l'artiste Villagomez. Fondateur : Samuel Villagomez. On travaille en français, au tutoiement.

## Le site

- Site statique, sans build : `index.html`, `styles.css`, `favicon.svg`. Polices locales dans `fonts/` (Big Shoulders Display, Instrument Serif, Hanken Grotesk, Archivo Black, licence OFL).
- Direction visuelle « Cinema » : fond noir, texte crème, vidéo plein écran à l'ouverture, grille de sets inspirée de Boiler Room. Ne pas changer de direction sans que Samuel le demande.
- Sections dans l'ordre (refonte du 20 octobre 2026, pour la candidature à la SAT) : hero, Le son spatial (`#recherche`), Villagomez et crédits (`#villagomez`), Musique (`#musique`), Le studio (`#studio`), LA VILLLA (`#soirees`), Les sets (`#sets`), Contact (`#contact`).
- Le site met de l'avant l'artiste et sa recherche en son spatial ; le label, le studio et les soirées suivent. Courriel de contact : info@villagomez.io.
- Les noms à respecter : **LA VILLLA** (trois L) pour le collectif et les soirées DISCO, VINYL, ROOFTOP et GOMEZ ; **Villagomez Records** pour le label.
- Aucune IA générative dans la musique : ne jamais écrire le contraire.

## Règles de contenu

- Le dépôt est **public**. N'ajouter aucun titre non sorti ni nom de collaborateur au site, ni dans ce dépôt, sans que Samuel le confirme dans la conversation.
- Les photos et vidéos à déposer dans `images/` sont listées dans `README.md`, avec leur format. Tant qu'un fichier manque, un dégradé prend sa place : ne pas retirer ce comportement.
- Préparation des photos : JPG, sRGB, environ 2400 px côté long, moins de 500 Ko, métadonnées GPS retirées et copyright conservé.

## Aperçu local

```
python3 -m http.server 8000
```

Puis ouvrir http://localhost:8000. Vérifier aussi à la largeur d'un téléphone (390 px).

## Mise en ligne

- Domaine villagomez.io chez GoDaddy. Les courriels Microsoft 365 passent par ce domaine : ne jamais toucher aux enregistrements MX, TXT (SPF, vérification) ni autodiscover.
- Hébergement : Cloudflare Workers (projet `villagomez-io`), déployé automatiquement à chaque push sur `main`. Réglages dans `wrangler.jsonc` ; `.assetsignore` liste les fichiers qui ne sont pas publiés (CLAUDE.md, README.md, etc.).
- DNS de villagomez.io gérés par Cloudflare depuis le 19 octobre 2026 (serveurs de noms changés chez GoDaddy ; l'ancien site Wix est abandonné). Le site est en ligne sur https://villagomez-io.villagomezrecords.workers.dev et branché sur villagomez.io et www.villagomez.io (onglet Domains du Worker).
- Le site est public même s'il manque encore des photos : les dégradés tiennent la place.

## Façon de travailler

- Une modification = un commit clair, en français.
- Montrer le résultat avant d'enchaîner les changements visuels.
