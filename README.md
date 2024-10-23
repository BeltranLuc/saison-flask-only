
# README

## Description

Ce projet est une **application web** qui permet de vérifier si un fruit ou un légume est de saison en fonction du pays et du mois spécifiés. Vous pouvez prendre une photo ou utiliser une vidéo en direct pour identifier l'aliment. Une fois l'aliment reconnu, l'application vous indique s'il est de saison ou non.

Le but de cette application est de promouvoir la consommation de produits de saison, en rendant cette information facilement accessible via un simple clic ou une photo.

Le projet a été réalisé en équipe de 4 personnes sur une période de **10 jours**.

## Fonctionnalités

- **Reconnaissance d'image** : Utilisation de modèles de classification et de segmentation (VGG et YOLO) pour identifier le fruit ou légume à partir d'une image/photo ou d'une vidéo en temps réel.
- **Vérification de la saisonnalité** : Basée sur un fichier `season.json` qui contient les données de saisonnalité des fruits et légumes par pays et par mois.
- **Interface utilisateur intuitive** : Permet de télécharger une image ou d'activer la webcam pour analyser les produits.
- **Choix du pays et du mois** : L'utilisateur peut sélectionner le pays et le mois pour lequel il souhaite vérifier la saisonnalité.

## Architecture du projet

Le projet est structuré comme suit :

```
├── data
│   └── season.json                 # Contient les données de saisonnalité
├── Dockerfile                      # Fichier pour la conteneurisation de l'application avec Docker
├── models                          # Modèles de reconnaissance d'image
├── README.md                       
├── requirements.txt                # Dépendances Python nécessaires
├── setup.py                        # Script d'installation du projet
└── src
    ├── app.py                      # Script principal pour lancer l'application web
    ├── custom_function.py          # Fonctions utilitaires pour le traitement des données
    ├── model.py                    # Chargement et gestion des modèles de machine learning
    ├── static                      # Fichiers CSS pour le style de l'application
    ├── templates                   # Fichiers HTML de l'application
```

## Prérequis

- **Python 3.x**
- Les dépendances listées dans le fichier `requirements.txt`
- Un modèle pré-entraîné de classification et segmentation (inclus dans le dossier `models`)

## Installation

1. Clonez le projet :

   ```bash
   git clone git@github.com:BeltranLuc/saison-flask-only.git
   ```

2. Accédez au répertoire du projet :

   ```bash
   cd saison-flask-only
   ```

3. Créez un environnement virtuel et activez-le :

   ```bash
   python -m venv .venv
   source .venv/bin/activate   # Pour Linux/MacOS
   # ou
   .venv\Scripts\activate    # Pour Windows
   ```

4. Installez les dépendances nécessaires :

   ```bash
   pip install -r requirements.txt
   ```

5. Lancez l'application en local :

   ```bash
   python src/app.py
   ```

6. Ouvrez votre navigateur à l'adresse suivante :

   ```
   http://localhost:5000
   ```

## Utilisation

1. **Choisissez une image** ou **activez la webcam** pour capturer l'image d'un fruit ou légume.
2. **Sélectionnez le pays** et **le mois**.
3. L'application identifiera le produit et indiquera s'il est de saison.

## Technologies utilisées

- **Python** pour le backend
- **Flask** pour la gestion du serveur web
- **HTML/CSS** pour le frontend
- **Modèles de deep learning** pour la classification et la segmentation d'image (VGG, YOLO)
- **OpenCV** pour la gestion de la webcam et le traitement d'image
- **Docker** pour la conteneurisation de l'application

## Contributeurs

Le projet a été développé par une équipe de 4 personnes :

- Luc Beltran (https://www.linkedin.com/in/lucbeltran)
- Joffrey Elis
- Eric Hu
- Jean-Philippe Meline

## Liens

Le dépôt original du projet, incluant le traitement des données, le paramétrage GCP et plus encore, est disponible à l'adresse suivante :
[repo du projet](git@github.com:M4DMojO/saison.git)


## Licence

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0).

---

Pour toute question, vous pouvez me contacter via [LinkedIn](https://www.linkedin.com/in/lucbeltran)
