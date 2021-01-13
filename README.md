Ce fichier ne donne que des explications sommaires destinées à des personnes ayant suivi le projet. Pour de plus amples informations n'hésitez pas à me contacter.

Les path seront à redefinir

# ShroomeDex

L'extraction des données a été effectué depuis jupyter Notebook en local. 

Pour le training, l'utilisation d'un GPU a nécéssité l'utilisation de Google Colab

## Extraction des données 

Site source des champignons: https://www.wildfooduk.com/mushroom-guide/

Dans un premier temps il faut extraire les différents champignons ainsi que les labels possibles en utilisant "ExtractMushroom.ipynb"

## Data augmentation

Procéder à la data augmentation en 2 étapes

### Zoom et Rotation

dataAugmentation.ipynb pour transformer l'ensemble des images, augmentées par types.

Les labéliser sous le format necessaire pour Yolov4 en utilisant LabelImg

### Filtres

dataAugmentationFiltres.ipynb pour ajouter des images filtrées poivre ou sel.

Récupérer les memes labels que l'image de base.

## Configurer le model

En réutilisant le tutoriel https://github.com/AlexeyAB/darknet modifié le fichier darknet en prenant en compte la quantité de données utilisée.

## Train & Test le model

Lancer le fichier yolov4.ipynb

Attention: necessite l'utilisation d'un GPU!

## Résultat

Obtenu après 12h d'entrainement :
 - 23 classes
 - 350 images par classe environ
 
 mAP = 93 %

[![Watch the video](https://img.youtube.com/vi/Au9C15fEU8U/maxresdefault.jpg)](https://youtu.be/Au9C15fEU8U)

