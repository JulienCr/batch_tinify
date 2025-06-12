# Documentation de Batch Tinify

Batch Tinify est un petit outil en ligne de commande permettant de redimensionner et compresser un ensemble d'images à l'aide de l'API [Tinify](https://tinypng.com/). Le script accepte un dossier en entrée et génère les fichiers optimisés dans un dossier de sortie.

## Installation

1. Assurez-vous d'avoir Python 3.8 ou plus installé sur votre système.
2. Clonez ce dépôt puis installez les dépendances :

```bash
pip install -r requirements.txt
```

## Utilisation

Par défaut, `main.py` traite les images du dossier `input` et place les fichiers optimisés dans le dossier `output`.

```bash
python main.py [dossier_source] [dossier_destination]
```

- `dossier_source` : chemin du dossier contenant les images à optimiser ("input" si non renseigné).
- `dossier_destination` : chemin du dossier où enregistrer les images optimisées ("output" si non renseigné).

Seuls les fichiers `jpg`, `jpeg` et `png` sont pris en charge. Les images sont redimensionnées pour que la plus grande dimension n'excède pas `800` pixels avant d'être compressées via l'API Tinify.

## Exemple

```bash
python main.py images_a_compresser images_optimisees
```

## Licence

Ce projet est distribué sous la licence CC0. Consultez le fichier `LICENSE` pour plus d'informations.
