# villagomez.io — consignes pour Claude

villagomez.io regroupe trois sites distincts, chacun avec sa propre direction visuelle. Fondateur : Samuel Villagomez. On travaille en français, au tutoiement.

## Les trois sites (depuis le 12 novembre 2026)

- `/` : page d'accueil à trois portes vers les sites ci-dessous (`index.html`, styles intégrés).
- `/records/` : **Villagomez Records**, le label (son spatial, musique, collaborateurs, studio, Villagomez, Live 360, contact). C'est l'adresse à mettre dans la fiche Google Maps du label. Fichier `records/index.html` + `styles.css` à la racine.
- `/lavillla/` : **la viLLLa**, la communauté (Samuel : « la viLLLa, c'est la communauté » ; ne pas écrire « de la nuit ») (agenda façon Resident Advisor, soirées, fiches d'artistes façon ADE, sets, contact lavillla.club@gmail.com). Fichier `lavillla/index.html`, styles intégrés. Deux modes : nuit (le noir domine, rose #FF2E93 et lime #C6DD36), automatique de 18 h à 6 h, et jour façon Piknic Électronik (fond lime #DCF14A, texte noir, rose ; « Latin Lime Lovers »), avec un bouton Jour / Nuit. Ouverture : carte Air Villagomez (destinations des départs gardées secrètes jusqu'à l'annonce). la viLLLa Radio façon GTA. Pas d'appel ouvert aux artistes : Samuel choisit qui joue. Agenda : la date la plus proche en premier ; les fiches d'artistes ne nomment que des personnes confirmées par Samuel.
- `/sanfronteras/` : **San Fronteras**, le média Sound & Mindset (FR/EN/ES, jour/nuit). Styles intégrés.
- Chaque site garde des liens vers les deux autres (pied de page). Dans les sous-dossiers, toujours des chemins absolus (`/images/...`, `/fonts/...`).

## Le site du label (`/records/`)

- Site statique, sans build : `records/index.html`, `styles.css`, `favicon.svg`. Polices locales dans `fonts/` (Big Shoulders Display, Instrument Serif, Hanken Grotesk, Archivo Black, licence OFL).
- Direction visuelle « Cinema » : fond noir, texte crème, vidéo plein écran à l'ouverture, grille de sets inspirée de Boiler Room. Ne pas changer de direction sans que Samuel le demande.
- Sections dans l'ordre : hero, renvoi vers la viLLLa (`#soirees`), Le son spatial (`#recherche`), Musique (`#musique`), Les collaborateurs (`#collaborateurs` ; on ne nomme que les personnes que Samuel a confirmées), Le studio (`#studio`), Villagomez et crédits (`#villagomez`), Live 360 (`#live`), Contact (`#contact`). Les soirées et les sets sont passés sur `/lavillla/`.
- Courriel de contact : info@villagomez.io.
- Les noms à respecter : **la viLLLa** (« la » en minuscules, trois L majuscules) pour le collectif et ses soirées Disco, Vinyl, Rooftop et Gomez ; **Villagomez Records** pour le label (Villagomez en un mot) ; **San Fronteras** pour le média.
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
