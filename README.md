# ChronoSport

Minuteur d'intervalles, minuteur à cadran et chronomètre pour l'entraînement.
Une seule page HTML, sans dépendance ni étape de compilation.

## Fonctions

- **Minuteurs d'intervalles** : préparation, effort, repos, séries, cycles, repos entre cycles et retour au calme. Six modèles fournis (Tabata, HIIT 40/20, Circuit training, Gainage, Boxe 3 min, Pomodoro), modifiables, duplicables et supprimables.
- **Séance plein écran** : grand décompte, anneau de progression coloré selon la phase, pause, phase précédente et suivante.
- **Chrono** : minuteur à cadran (de 1 à 60 minutes, réglage au doigt) et chronomètre avec aiguille des secondes et tours (le plus rapide en vert, le plus lent en rouge).
- **Alertes** : bips, compte à rebours sonore, annonce vocale en français, vibration, écran maintenu allumé.
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

Sur téléphone, ouvrez l'adresse du site puis utilisez « Ajouter à l'écran d'accueil » pour l'avoir comme une application.

## Structure

```
index.html                    toute l'application (HTML, CSS, JavaScript)
manifest.webmanifest          nom et icônes pour l'installation sur l'écran d'accueil
icons/                        icônes de l'application (180, 192 et 512 px, favicon)
.github/workflows/pages.yml   déploiement GitHub Pages
LICENSE                       licence MIT
```

## Licence

MIT, voir [LICENSE](LICENSE).
