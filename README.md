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