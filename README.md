# Projet 6: Classifiez automatiquement des biens de consommations
## Présentation:
Je suis Data Scientist au sein de l’entreprise "Place de marché”, qui souhaite lancer une marketplace e-commerce.
Sur la place de marché, des vendeurs proposent des articles à des acheteurs en postant une photo et une description.
Pour l'instant, l'attribution de la catégorie d'un article est effectuée manuellement par les vendeurs, et est donc peu fiable. De plus, le volume des articles est pour l’instant très petit.

Pour rendre l’expérience utilisateur des vendeurs (faciliter la mise en ligne de nouveaux articles) et des acheteurs (faciliter la recherche de produits) la plus fluide possible, et dans l'optique d'un passage à l'échelle, il devient nécessaire d'automatiser cette tâche.
## Mission:
Linda, Lead Data Scientist, me demande donc d'étudier la faisabilité d'un moteur de classification des articles en différentes catégories, avec un niveau de précision suffisant.

Voici le mail qu’elle m'a envoyé: "Bonjour,
Merci pour ton aide sur ce projet !
Ta mission est de réaliser, dans une première itération, une étude de faisabilité d'un moteur de classification d'articles, basé sur une image et une description, pour l'automatisation de l'attribution de la catégorie de l'article.
Tu dois analyser les descriptions textuelles et les images des produits, au travers des étapes suivantes :

- Un prétraitement des données texte ou image suivant le cas ;
- Une extraction de features ;
- Une réduction en 2 dimensions, afin de projeter les produits sur un graphique 2D, sous la forme de points dont la couleur correspondra à la catégorie réelle ;
- Analyse du graphique afin d’en déduire ou pas, à l’aide des descriptions ou des images, la faisabilité de regrouper automatiquement des produits de même catégorie ;
- Réalisation d’une mesure pour confirmer ton analyse visuelle, en calculant la similarité entre les catégories réelles et les catégories issues d’une segmentation en clusters.

Pourrais-tu nous démontrer, par cette approche, la faisabilité de regrouper automatiquement des produits de même catégorie ?

Voici les contraintes :
Afin d’extraire les features texte, il sera nécessaire de mettre en œuvre : 

- deux approches de type “bag-of-words”, comptage simple de mots et Tf-idf ;
- une approche de type word/sentence embedding classique avec Word2Vec (ou Glove ou FastText) ;
- une approche de type word/sentence embedding avec BERT ;
- une approche de type word/sentence embedding avec USE (Universal Sentence Encoder). 

En pièce jointe, tu trouveras un exemple de mise en œuvre de ces approches d’extraction de features texte sur un autre dataset. Je t’invite à l’utiliser comme point de départ, cela va te faire gagner beaucoup de temps !
Afin d’extraire les features image, il sera nécessaire de mettre en œuvre :

- un algorithme de type SIFT / ORB / SURF ;
- un algorithme de type CNN Transfer Learning"
## Données:
Jeu de données d'articles avec le lien pour télécharger la photo et une description associée: https://s3-eu-west-1.amazonaws.com/static.oc-static.com/prod/courses/files/Parcours_data_scientist/Projet+-+Textimage+DAS+V2/Dataset+projet+pre%CC%81traitement+textes+images.zip
## Construction:
Dans ce dépôt, vous trouverez un fichier:

- "notebook.ipynb" : notebook  contenant les fonctions permettant le prétraitement, la feature extraction des données textes et images, la réduction en 2 dimensions ainsi que les résultats de l’étude de faisabilité (graphiques, mesure de similarité).

## Packages:
Différents packages Python ont été utilisés:

- pandas 1.4.4
- numpy 1.23.5
- matplotlib 3.5.2
- scikit-learn 1.0.2
- nltk 3.7
- tensorflow 2.13.0
- seaborn 0.11.2
- keras 2.13.1
- transformers 4.31.0
- pathlib 1.0.1

## Compétences:
- Prétraiter des données image pour obtenir un jeu de données exploitable
- Prétraiter des données texte pour obtenir un jeu de données exploitable
- Représenter graphiquement des données à grandes dimensions
- Mettre en œuvre des techniques de réduction de dimension