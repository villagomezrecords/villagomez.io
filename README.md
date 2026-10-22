# villagomez.io

Site web de Villagomez (recherche en son spatial, label Villagomez Records, studio, soirées LA VILLLA), en ligne sur villagomez.io via Cloudflare Workers. Consignes de travail dans `CLAUDE.md`.

Site statique : `index.html`, `styles.css`, polices locales dans `fonts/` (Big Shoulders Display, Instrument Serif, Hanken Grotesk, licence OFL).

## Photos et vidéos à déposer dans `images/`

Photos : JPG, sRGB, ~2400 px côté long, < 500 Ko. Tant qu'un fichier manque, un dégradé prend sa place.

| Fichier | Où | Format |
|---|---|---|
| `hero.mp4` (+ `hero.webm`) | Vidéo plein écran d'ouverture | 1080p, 10-20 s en boucle, sans son, < 10 Mo |
| `hero.jpg` | Image d'ouverture (avant la vidéo) | horizontal 16:9 |
| `collectif.jpg` | Grande photo du collectif sous le titre LA VILLLA | horizontal 3:2 |
| `disco.jpg`, `vinyl.jpg`, `rooftop.jpg`, `gomez.jpg` | Les quatre soirées LA VILLLA | vertical 4:5 |
| `soiree-01.jpg` à `-05` | Bande photo sous les soirées (LA VILLLA ROOFTOP) | vertical 4:5 |
| `soiree-07.jpg` | Bande photo : grande photo à côté de `soiree-05` | horizontal 3:2 |
| `set-rooftop-2021.jpg`, `set-vinyl-01.jpg`, `set-03.jpg` | Vignettes des sets filmés | carré |
| `sessions-01.jpg` à `sessions-06.jpg` | Studio : sessions d'enregistrement (une seule série) | 01 et 02-03 en haut, 04-06 en rangée | 
| `studio-01.jpg` à `-03` | Studio : Studio Villagomez | 01 large, 02-03 libres |
| `live-360-*.jpg` | Live 360 : photos 360° équirectangulaires (rapport 2:1) | 2:1, environ 2500-4000 px de large |
| `portrait.jpg` | Section Villagomez | vertical 4:5 |
| `recherche-spatialisation.jpg` | Le son spatial : grande photo (studio de Huddersfield) | horizontal |
| `recherche-captation.jpg` | Le son spatial : à côté des quatre piliers | vertical 3:4 |
| `parcours-hacienda.jpg` | Section Villagomez : grande photo au-dessus des crédits | horizontal |

## Extraits vidéo de sessions

La rangée du bas de la série sessions accepte des extraits vidéo : `sessions-04.mp4`, `sessions-05.mp4`, `sessions-06.mp4`.
Ils jouent en boucle sans son quand ils sont à l'écran ; un bouton « Activer le son » permet d'écouter (un seul à la fois).
Format : MP4 (H.264 + AAC), 8 à 15 s, 1080p ou 720p, 3 à 8 Mo. Optionnel : une image `sessions-0X.jpg` affichée avant la lecture.

Le clip complet va sur YouTube ; il sera intégré dans la section Musique.
