# AnyPS5 Library

Une bibliothèque façon console pour tes jeux PS5 sous Windows. Elle importe tes dumps, les convertit avec [AnyPS5](https://github.com/boykopovar/AnyPS5) et les lance depuis un écran d'accueil qui se pilote à la manette.

**[Télécharger la dernière version](https://github.com/Sharpeer/AnyPS5-Library/releases/latest)** · Windows 10 ou 11, 64 bits · interface en français · gratuit

> AnyPS5 Library est un projet indépendant. Il n'est affilié ni à Sony Interactive Entertainment ni aux auteurs d'AnyPS5. Il fonctionne avec les jeux que tu possèdes : aucun jeu, aucune clé et aucun firmware n'est fourni.

## Sommaire

- [Fonctions](#fonctions)
- [Installer](#installer)
- [Mettre à jour](#mettre-à-jour)
- [Premiers pas](#premiers-pas)
- [À la manette](#à-la-manette)
- [En ligne de commande](#en-ligne-de-commande)
- [Questions fréquentes](#questions-fréquentes)
- [Aide et signalements](#aide-et-signalements)
- [Licence](#licence)

## Fonctions

**Importer**

- Une image `.ffpfsc` ou `.exfat`, une archive `.zip`, `.7z` ou `.rar`, ou le dossier d'un jeu déjà extrait.
- Un lien magnet, un fichier `.torrent` ou un lien de téléchargement direct.
- Un dossier surveillé : ce qui y arrive est importé tout seul.
- Plusieurs jeux à la suite : ils sont traités un par un, avec leur avancement.

**Convertir**

- AnyPS5 est installé et mis à jour par la bibliothèque. Tu peux aussi choisir une version précise.
- Un jeu converti avec une ancienne version d'AnyPS5 est signalé « À reconvertir ».
- Quand une conversion échoue, l'erreur est affichée en entier et un rapport de diagnostic se copie en un clic.

**Jouer**

- Un écran d'accueil et une bibliothèque, à la manette, au clavier ou à la souris.
- Le jeu s'affiche dans la fenêtre de la bibliothèque. Le bouton PS le met en pause et ouvre le menu PS.
- Captures d'écran avec le bouton Create, puis un écran pour les revoir.
- Trophées : la progression, la liste, et un message quand un trophée est obtenu.
- Temps de jeu, dernière partie, favoris, recherche, tri et filtres.
- Logo, description et genres de chaque jeu, lus une fois en ligne.
- Mode télé : plein écran, clavier virtuel, ouverture au démarrage de Windows.

## Installer

1. Télécharge `AnyPS5-Library-Setup-<version>.exe` dans les [versions](https://github.com/Sharpeer/AnyPS5-Library/releases/latest).
2. Lance-le. Il ne demande pas les droits d'administrateur.
3. Au premier démarrage, la bibliothèque télécharge AnyPS5.

**Avertissement de Windows.** L'installateur n'est pas signé : Windows SmartScreen peut afficher « Windows a protégé votre ordinateur ». Choisis « Informations complémentaires », puis « Exécuter quand même ».

**Contrôler le téléchargement.** Chaque version publie l'empreinte SHA-256 de son installateur, dans le fichier `.sha256`. Dans PowerShell :

```powershell
Get-FileHash .\AnyPS5-Library-Setup-0.1.0.exe -Algorithm SHA256
```

L'empreinte affichée doit être celle du fichier `.sha256`.

**Désinstaller.** Par « Applications installées » de Windows. Ton dossier de jeux n'est pas supprimé.

## Mettre à jour

La bibliothèque cherche ses nouvelles versions au démarrage. Quand il y en a une, un bandeau la propose, et la ligne « Mettre à jour AnyPS5 Library » apparaît dans Paramètres › Avancé. Elle télécharge l'installateur, contrôle son empreinte, l'installe, puis se relance.

Le moteur AnyPS5 se met à jour à part, dans Paramètres › Moteur AnyPS5.

## Premiers pas

1. Ouvre la bibliothèque et choisis « Ajouter un jeu ».
2. Donne un fichier, un dossier ou un lien. Tu peux aussi glisser un fichier dans la fenêtre.
3. Attends la fin de l'import et de la conversion : le panneau « Tâches » montre l'avancement.
4. Choisis le jeu, puis « Jouer ».

Il te faut tes propres dumps de jeux, déjà déchiffrés.

## À la manette

La bibliothèque est faite pour une manette DualSense ou DualShock 4.

| Bouton | Action |
|---|---|
| ✕ | Valider, jouer |
| ○ | Retour |
| △ | Options du jeu |
| □ | Favori |
| L1 · R1 | Changer d'écran |
| PS | Mettre le jeu en pause et ouvrir le menu PS, puis y revenir |
| Create | Prendre une capture d'écran pendant le jeu |

Au clavier : les flèches, Entrée, Échap, F11 pour le plein écran, Ctrl+F pour chercher.

## En ligne de commande

```text
--add <fichier|dossier|lien>   importe un jeu
--convert <ID|dossier>         reconvertit un jeu de la bibliothèque
--play <ID|dossier>            lance un jeu
--list                         liste les jeux de la bibliothèque
--update [version]             installe la dernière version d'AnyPS5, ou celle indiquée
--clean                        supprime les fichiers temporaires d'un import interrompu
--inspect <image>              analyse une image sans rien extraire
--library <dossier>            utilise une autre bibliothèque pour cette commande
```

## Questions fréquentes

**Où trouver des jeux ?**
Nulle part ici. La bibliothèque fonctionne avec les dumps des jeux que tu possèdes.

**Un jeu se convertit mais plante une fois lancé.**
C'est le plus souvent AnyPS5, le moteur, et pas la bibliothèque. Regarde le [suivi d'AnyPS5](https://github.com/boykopovar/AnyPS5/issues). Essaie aussi une autre version d'AnyPS5 dans Paramètres › Avancé › « Installer une autre version ».

**La bibliothèque marche-t-elle sans connexion ?**
Oui, une fois AnyPS5 installé. Sans connexion, elle ne cherche ni mises à jour ni fiches de jeux.

**Que lit-elle en ligne ?**
Les versions d'AnyPS5 et les siennes sur GitHub. Le logo des jeux sur SteamGridDB, avec ta clé. La description et les genres sur la boutique Steam. Un réglage de Paramètres › Affichage éteint les fiches en ligne. Elle n'envoie aucune statistique. Un lien magnet ou un fichier `.torrent` utilise le réseau BitTorrent : ton adresse IP y est visible des autres participants.

**Le code source est-il disponible ?**
Non. AnyPS5 Library est gratuit, mais son code n'est pas publié.

## Aide et signalements

- [Signaler un problème](https://github.com/Sharpeer/AnyPS5-Library/issues/new/choose) : un problème de la bibliothèque, un jeu qui ne s'importe pas ou ne se convertit pas, une idée.
- Une faille de sécurité : voir [SECURITY.md](SECURITY.md).
- L'historique des versions : [CHANGELOG.md](CHANGELOG.md).

Ne joins jamais un fichier de jeu ni un lien de téléchargement à un ticket.

## Licence

AnyPS5 Library est un logiciel gratuit, non libre. Son utilisation est régie par la [licence d'utilisation](LICENSE.md). Les composants tiers sont listés dans [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

« PlayStation », « PS5 », « DualSense » et « DualShock » sont des marques de Sony Interactive Entertainment. « Steam » est une marque de Valve Corporation.

Copyright © 2026 Sharpeer. Tous droits réservés.
