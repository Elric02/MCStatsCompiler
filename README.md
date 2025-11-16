# MCStatsCompiler – Mise à jour Cobblemon NBT (Fork non officiel) FRANÇAIS
Une mise à jour minimale pour restaurer la compatibilité avec les dernières versions de Cobblemon.

## Note sur le Fork

Depuis les dernières mises à jour de Cobblemon, les données de capture des joueurs ne sont plus stockées dans des fichiers JSON. Toutes les données Pokémon sont désormais sauvegardées au format NBT sous :

> world/pokedata/\<prefix>/\<UUID>.nbt

Le MCStatsCompiler original ne peut plus lire ce format.

Ce fork ajoute la prise en charge de la nouvelle structure NBT grâce à `nbtlib` et réorganise les données extraites afin que les classements Total, Shiny et Legendary fonctionnent à nouveau.  
Il est principalement conçu pour un usage personnel, certaines fonctionnalités peuvent donc ne pas se comporter exactement comme la version originale.

Mon hébergeur utilise un SFTP chrooté, ce qui a nécessité le passage complet à l’utilisation de chemins absolus. Les modifications internes ont été faites en conséquence et peuvent ne pas refléter tous les environnements.

Malgré tout, ce fork peut aider d’autres administrateurs de serveur à mettre à jour leurs scripts existants ou à comprendre comment adapter le projet original au nouveau format de données de Cobblemon.

## Objectif de ce Fork

Ce projet n’a pas pour vocation de remplacer le MCStatsCompiler original, ni d’être aussi complet ou abouti que d’autres forks.  
Ses principaux objectifs sont :

- Fournir un loader fonctionnel pour les nouvelles données joueurs `.nbt` de Cobblemon.
- Restaurer les classements liés aux captures avec les nouvelles clés Cobblemon.
- Servir de référence simple pour les utilisateurs souhaitant moderniser le script original.

Si votre serveur Cobblemon utilise des classements de captures, ce fork constitue un point de départ fonctionnel.

## Prérequis

Installez les packages Python requis listés ci-dessous. Ils sont nécessaires pour que le script fonctionne correctement :

- `pandas`
- `numpy`
- `openpyxl`
- `paramiko`
- `excel2img`
- `requests`
- `configparser`
- `nbtlib`

Vous pouvez les installer via :

>pip install -r requirements.txt

## Fonctionnalités ajoutées dans ce Fork

### Support des données joueurs Cobblemon NBT
- Lecture des fichiers de capture `.nbt` au lieu des fichiers JSON obsolètes.
- Extraction des espèces, statut de capture, informations shiny et flags pertinents.
- Gestion des clés mise à jour selon le format actuel de Cobblemon.

### Intégration SFTP/FTP mise à jour
En raison de l’environnement SFTP chrooté utilisé pour le développement :

- Seuls les chemins absolus sont supportés.
- La navigation dans les dossiers a été réécrite pour respecter cette contrainte.

### Logique d’auto-upload GitHub (partielle)
Les parties liées à GitHub sont basées sur le fork de floooz (MCStatsCompiler-autoupload).  
Toutes les fonctionnalités ne sont pas garanties d’être identiques.

## Limitations

- Certaines fonctionnalités du MCStatsCompiler original sont incomplètes ou non testées.
- L’upload GitHub peut nécessiter des ajustements manuels.
- Le comportement peut varier selon l’environnement serveur ou la configuration SFTP.
- Les futures mises à jour de Cobblemon peuvent nécessiter des modifications supplémentaires.

Cependant, les classements Total et Shiny fonctionnent de manière fiable dans les conditions actuelles.

## Crédits et Remerciements

Ce fork repose sur le code original des mainteneurs et contributeurs, dont une grande partie constitue toujours la base de ce projet.

- Elric02 — [MCStatsCompiler original](https://github.com/Elric02/MCStatsCompiler)  
- floooz — [Logique d’auto-upload GitHub](https://github.com/floooz/MCStatsCompiler-autoupload)


--------
# MCStatsCompiler – Cobblemon NBT Update (Unofficial Fork) ENGLISH
A minimal update to restore compatibility with recent Cobblemon versions.


## Fork Notice

Since the latest Cobblemon updates, player capture data is no longer stored in JSON files. All Pokémon data is now saved in NBT format under:

>world/pokedata/\<prefix>/\<UUID>.nbt


The original MCStatsCompiler cannot read this format anymore.

This fork adds support for the new NBT structure using `nbtlib`, and reorganizes the extracted data so that Total, Shiny, and Legendary leaderboards work again.  
It is primarily written for personal use, so certain features may not behave exactly like the original version.

My hosting provider uses a chrooted SFTP environment, which required switching fully to absolute path handling. Internal modifications were made accordingly and may not reflect all environments.

Even so, this fork may help other server owners update their existing scripts or understand how to adapt the original project to Cobblemon’s new data format.


## Purpose of This Fork

This project is not meant to replace the original MCStatsCompiler, nor is it as complete or polished as other forks.  
Its main goals are:

- Provide a working loader for the new Cobblemon `.nbt` player data.
- Restore capture-related leaderboards with updated Cobblemon keys.
- Offer a simple reference for users wanting to modernize the original script.

If your Cobblemon server uses capture leaderboards, this fork provides a functional starting point.

## Requirements

Install the required Python packages listed below. These are needed to run the script properly:

- `pandas`
- `numpy`
- `openpyxl`
- `paramiko`
- `excel2img`
- `requests`
- `configparser`
- `nbtlib`

You can install them via:

>pip install -r requirements.txt

## Features Added in This Fork

### Support for Cobblemon NBT Player Data
- Reads `.nbt` player capture files instead of deprecated JSON.
- Extracts species, capture status, shiny data, and relevant flags.
- Updated key handling based on the current Cobblemon format.

### Updated SFTP/FTP Integration
Because of the chrooted SFTP environment used for development:

- Only absolute paths are supported.
- Directory traversal was rewritten to match this constraint.

### GitHub Auto-upload Logic (Partial)
GitHub-related logic is based on the fork by floooz (MCStatsCompiler-autoupload).  
Not all features are guaranteed to work identically.


## Limitations

- Certain features from the original MCStatsCompiler are incomplete or not tested.
- GitHub upload functionality may require manual adjustments.
- Behavior may vary depending on server environments or SFTP setups.
- Future Cobblemon updates may require additional changes.

Still, Total, Shiny, and Legendary leaderboards operate reliably under current conditions.


## Credits and Acknowledgements

This fork builds upon the original code of the maintainers and contributors, with significant portions of their work still forming the foundation of this project.

- Elric02 — [original MCStatsCompiler](https://github.com/Elric02/MCStatsCompiler)
- floooz — [GitHub auto-upload logic](https://github.com/floooz/MCStatsCompiler-autoupload)






