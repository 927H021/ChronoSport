# ChronoSport

Minuteur d'intervalles, minuteur à cadran et chronomètre pour l'entraînement.
Une seule page HTML, sans dépendance ni étape de compilation.

## Fonctions

- **Minuteurs d'intervalles** : préparation, effort, repos, séries, cycles, repos entre cycles et retour au calme. Quatre modèles fournis (HIIT 40/20, Circuit training, Gainage, Boxe 3 min), modifiables, duplicables et supprimables.
- **Séance plein écran** : grand décompte, anneau de progression coloré selon la phase, pause, phase précédente et suivante.
- **Chrono** : minuteur à cadran (de 1 à 60 minutes, réglage au doigt) et chronomètre avec aiguille des secondes et tours (le plus rapide en vert, le plus lent en rouge).
- **Alertes** : sept sons au choix (gong, ring de boxe, klaxon de stade, sifflet de coach, montre sport, marimba, synthwave), compte à rebours sonore, voix d'annonceur en français qui crie le nom du minuteur (style et voix au choix), vibration, écran maintenu allumé.
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
