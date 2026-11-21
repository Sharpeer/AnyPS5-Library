# Historique des versions

Toutes les versions d'AnyPS5 Library sont listées ici, la plus récente d'abord. Les numéros suivent le [versionnage sémantique](https://semver.org/lang/fr/).

## 0.1.1 — 21 novembre 2026

### Accueil et interface

- Musique du jeu choisi sur l'accueil, quand le jeu en a une.
- Parcours guidé au premier démarrage, et panneau « Quoi de neuf » après une mise à jour.
- Animation d'ouverture, et couleur d'accent au choix ou tirée du jeu.
- La molette ouvre et ferme les détails du jeu.
- Paramètres ouverts depuis un onglet du menu du haut, navigation par niveaux.

### Manette

- Centre des manettes : test des boutons, vibrations, zone morte et barre lumineuse.
- Vibrations dans l'interface.

### Import et conversion

- Import d'un dossier de jeu sans recopier ses données quand il est sur le même disque que la bibliothèque.
- Reconversion automatique des jeux après une mise à jour d'AnyPS5 (interrupteur dans Moteur AnyPS5).
- Une conversion déjà faite est réutilisée quand rien n'a changé.
- Une conversion interrompue repart seule, une fois par session.
- Changer le dossier de la bibliothèque propose d'y déplacer les jeux.

### Trophées et diagnostic

- Pourcentage pondéré par le grade des trophées.
- Trophées cachés révélés tous d'un coup, ou un par un avec « Afficher » et « Masquer ».
- Une phrase en clair dit pourquoi un jeu s'est arrêté ; avertissement quand le processeur est trop ancien.

### Corrections

- Les musiques ATRAC9 à débit réduit sont lues.
- Les paramètres ne figent plus l'écran pendant leurs vérifications.
- L'animation de lancement d'un jeu n'est plus finie avant que l'écran n'apparaisse.
- Un dossier de jeu est refusé comme dossier de bibliothèque.
- Un rapport d'AnyPS5 plus ancien que le dernier lancement est ignoré.
- Les barres d'avancement restent bleues, quelle que soit la couleur d'accent.

## 0.1.0 — 20 novembre 2026

Première version publiée.

### Import et conversion

- Import d'une image `.ffpfsc` ou `.exfat`, d'une archive `.zip`, `.7z` ou `.rar`, d'un dossier, d'un lien magnet, d'un fichier `.torrent` ou d'un lien direct.
- Dossier surveillé, file de tâches avec avancement, vitesse et temps restant.
- Installation et mise à jour d'AnyPS5 par la bibliothèque ; choix d'une version précise.
- État « À reconvertir » pour un jeu converti avec une autre version d'AnyPS5.

### Interface

- Écran d'accueil, bibliothèque avec recherche, tri et filtres, favoris.
- Détails du jeu : captures, fiche, temps de jeu, dernière session.
- Options du jeu dans un panneau : images, dépannage, suppression.
- Paramètres en quatre catégories : Affichage, Manette, Moteur AnyPS5, Avancé.
- Clavier virtuel, mode plein écran, ouverture au démarrage de Windows.
- Logo, description et genres des jeux, lus une fois en ligne.

### En jeu

- Jeu affiché dans la fenêtre de la bibliothèque.
- Menu PS : pause du jeu, reprise, changement de jeu, fermeture.
- Écran de lancement, et écran de retour quand un jeu s'arrête sur une erreur.
- Captures d'écran avec le bouton Create.
- Trophées : progression, liste, message à l'obtention.

### Mise à jour

- La bibliothèque propose ses nouvelles versions, les télécharge, contrôle leur empreinte et les installe.
