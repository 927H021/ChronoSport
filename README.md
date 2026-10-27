# ChronoSport

Minuteur d'intervalles, minuteur à cadran et chronomètre pour l'entraînement.
Une seule page HTML, sans dépendance ni étape de compilation.

## Fonctions

- **Minuteurs d'intervalles** : préparation, effort, repos, séries, cycles, repos entre cycles et retour au calme. Quatre modèles fournis (HIIT 40/20, Circuit training, Gainage, Boxe 3 min), modifiables, duplicables et supprimables. Dans l'éditeur, chaque réglage se fait à la molette verticale (minutes et secondes, à la seconde près ; nombre simple pour les séries et les cycles), avec un cliquet sonore à chaque cran (une molette ne se règle qu'après l'avoir touchée, y compris « Toutes les (secondes) », pour ne pas la tourner en faisant défiler l'éditeur), comme pour « Son répété pendant l'effort ».
- **Actions seconde par seconde** (affichées dans l'éditeur seulement si l'interrupteur **Réglages > Actions rapides** est activé) : dans l'éditeur, un tableau permet d'associer une action à chaque seconde de l'effort (« Jab » à la 1<sup>re</sup> seconde, « Jab & crochet » à la 3<sup>e</sup>…), avec des actions rapides à toucher pour enchaîner les coups. Les boutons d'actions rapides restent affichés en haut de l'éditeur pendant le défilement du tableau ; ils s'activent et se personnalisent dans **Réglages > Actions rapides** (interrupteur, puis ajouter, modifier, réordonner, supprimer, rétablir). Les blocs de secondes se sélectionnent (touchez le numéro de la première puis de la dernière seconde), se copient, se collent à une autre seconde ou dans une autre série, se répètent en boucle jusqu'à la fin de l'effort ou s'effacent. « Insérer » ajoute des secondes vides avant la sélection (autant que la sélection en compte) : les actions suivantes sont décalées et l'effort s'allonge d'autant. Le programme peut être commun à toutes les séries ou différent pour chacune (copie d'une série vers toutes les autres). Pendant la séance, l'action en cours et la suivante s'affichent sous le cadran, et elles sont lues à voix haute quand l'annonce vocale est active. 
- **Séance plein écran** : grand décompte, anneau de progression coloré selon la phase, pause, phase précédente et suivante.
- **Chrono** : minuteur à cadran (de 1 à 60 minutes, réglage au doigt) et chronomètre avec aiguille des secondes et tours (le plus rapide en vert, le plus lent en rouge).
- **Sons d'horlogerie** : un « clic-clac » de poussoir de chronographe au lancement, à la pause, au tour et à la remise à zéro du chronomètre, du minuteur à cadran et des minuteurs d'intervalles, et un cran de lunette à chaque minute lorsqu'on règle l'aiguille du minuteur (actifs avec l'option de son).
- **Alertes** : sept sons au choix (gong, ring de boxe, klaxon de stade, sifflet de coach, montre sport, marimba, synthwave), compte à rebours sonore, annonce vocale en français ou, avec l'option **Voix anglaise**, en anglais américain (en-US) (nom de la phase, le nom du minuteur remplaçant « Effort », et les actions programmées seconde par seconde), vibration, écran maintenu allumé.
- **Historique** des séances avec bilan de la semaine.
- Thème sombre par défaut, thème clair en option.

Les minuteurs, les réglages et l'historique sont enregistrés dans le navigateur (`localStorage`). Rien n'est envoyé à un serveur.

## Utilisation en local

Ouvrez `index.html` dans un navigateur. Pour tester sur téléphone, servez le dossier :

```sh
python3 -m http.server 8000
```

Les polices Barlow et Barlow Condensed sont chargées depuis Google Fonts. Hors connexion, la page utilise des polices système de remplacement.

## Publication sur GitHub Pages

1. Poussez ce dossier dans un dépôt GitHub.
2. Dans **Settings > Pages**, choisissez **GitHub Actions** comme source.
3. Chaque push sur la branche `main` déclenche `.github/workflows/pages.yml` et met le site en ligne.

## Installer l'application

ChronoSport est une application web installable (PWA) : plein écran, icône sur l'écran d'accueil, fonctionnement hors connexion.

- **iPhone / iPad** : ouvrez https://927h021.github.io/ChronoSport/ dans **Safari**, touchez le bouton Partager, puis **Sur l'écran d'accueil**.
- **Android** : ouvrez l'adresse dans Chrome, menu ⋮, puis **Installer l'application**.
- **Ordinateur** : dans Chrome ou Edge, icône d'installation dans la barre d'adresse.

L'application se met à jour toute seule à l'ouverture quand une nouvelle version est publiée.

## Structure

```
index.html                    toute l'application (HTML, CSS, JavaScript)
manifest.webmanifest          nom et icônes pour l'installation sur l'écran d'accueil
sw.js                         service worker : mode hors connexion et mises à jour
icons/                        icônes de l'application (180, 192 et 512 px, favicon)
.github/workflows/pages.yml   déploiement GitHub Pages
LICENSE                       licence MIT
```

## Licence

MIT, voir [LICENSE](LICENSE).
