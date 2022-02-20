# Analyse Semantique Latente

Cet article passe en revue l'analyse sémantique latente (LSA), une théorie de la signification ainsi qu'une méthode pour extraire ce sens de passages de texte, basée sur des statistiques calculs sur un ensemble de documents. LSA comme théorie du sens définit un espace sémantique latent où les documents et les mots individuels sont représentés sous forme de vecteurs. LSA en tant que technique de calcul utilise l'algèbre linéaire pour extraire les dimensions qui représentent cet espace. Cette représentation permet le calcul de la similarité entre les termes et les documents, la catégorisation des termes et documents, et résumé de grandes collections de documents en utilisant procédures automatisées qui imitent la façon dont les humains effectuent des tâches cognitives similaires. Nous présentons quelques détails techniques, divers exemples illustratifs et discutons d'un nombre de candidatures en linguistique, psychologie, sciences cognitives, éducation, sciences de l'information et analyse de données textuelles en général. 

## Objectif de Notre Analyse

Dans ce projet, nous allons voir comment « extraire » des concepts à partir d'un corpus (collection) de documents textuels.

Je vais vous montrer comment extraire mathématiquement des "concepts" de ce corpus. La technique que nous allons utiliser s'appelle "l'analyse sémantique latente".

## Les Packages Utilisés

![image](images/1.png)

* **BeautifulSoup**: Je vais utiliser ce package pour le webscraping c'est à dire l'extraction des information à travers l'internet.
  
* **nltk**: ce package pour les manipulations l'inguistique et nettoyage des textes à analyser.
  
* **TruncatedSVD**: pour la reduction de la dimensionnalité des matrices creuses.
  
* **TfidfVectorizer**: pour  le calcule ses fréquence des mots et termes dans les documents

## Web Scraping

dans ce tutoriel je vais scrapé cet article sur le Deep Learning à travers le **site CNRS** Le Journal.
[https://lejournal.cnrs.fr/billets/letonnante-acceptabilite-des-deep-fake](https://lejournal.cnrs.fr/billets/letonnante-acceptabilite-des-deep-fake)

## Le Code du Web Scraping En Python

![image](images/2.png)

## Quelques Data Préprocessing

### Suppression des Nombres

![image](images/3.png)

### Suppression des Entités

![images](images/4.png)

## Les Stopwords

Les **Les Stopwords** sont des mots que je ne veux pas convertir en **features** ou variables, car ils ne sont pas particulièrement utiles. Des mots comme **a**, **et** et **le** sont de bons **Stopwords** en français. Je peux utiliser une liste intégrée de **Stopwords** de **nltk** pour commencer. 

### Création des Stopwords

![image](images/5.png)

## TF-IDF Vectorizing

Je vais utiliser le vectoriseur TF-IDF de scikit-learn pour prendre mon corpus et convertir chaque document en une matrice creuse de fonctionnalités TFIDF...

![image](images/6.png)