# Odyssée Égypte au Canada
Site vitrine du mini-festival **« Égypte au-delà du Temps »** — un seul fichier
HTML, sans dépendance ni build.
Trilingue : **français par défaut**, arabe (mise en page RTL) et anglais.
Les traductions vivent dans l'objet `I18N`, en bas de `index.html`.
Le français n'est écrit qu'une fois : il est lu directement dans le HTML au
chargement, donc pour modifier un texte français il suffit de modifier le HTML.
## Les médias à déposer dans `assets/`
| Fichier | Rôle | Format conseillé |
|---|---|---|
| `video.mp4` | la vidéo de la section « Le festival en vidéo », juste sous la bannière | MP4 H.264 |
| `hero.mp4` | vidéo de repli pour cette section | MP4 H.264 |
| `hero-poster.jpg` | la bannière : fond du hero | **1920 × 1080** (la version actuelle ne fait que 960 × 479 : à remplacer) |
|  `logo.jpg` | logo rond du festival (en-tête + hero + favicon) | PNG carré, 1000 × 1000 |
| `gallery/1.jpg` … `6.jpg` | galerie | ~1200 × 900 |
| `partners/acmc.png`, `partners/mascan.png` | logos partenaires | PNG fond transparent |
Rien n'est obligatoire : tant qu'un fichier est absent, le site le remplace
proprement (scène animée en CSS pour le hero, hiéroglyphe pour la galerie,
sigle texte pour les partenaires). Aucune image cassée n'apparaît jamais.
## Lancer en local
    npx serve .
## Ajouter une langue
1. Ajouter une entrée dans `I18N` (avec `_dir` et `_title`).
2. Ajouter un bouton `<button data-lang="xx">` dans `.langs`.
