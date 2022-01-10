# Implémentation de l'algorithme kmeans de zéro
## Linda Belkessa (2CS SIQ3) : Ecole Nationale Supérieure d'Inforamtique - Alger
### Introduction 

Plusieurs algorithmes pour éffectuer la classification automatique des données, le plus simple à mettre en oeuvre voir le plus connu c'est l'algorithme des kmeans qui est une variante de "l'algorithme des centres mobiles" inventé en 1965 par Foggy.

Dans ce qui suit, j'implémente le processus sans utiliser la fonction de sci-kit learn.


### Principe et étapes :
> #### Etape 01 : Initialisation des centroids :
> En premier, nous initialisons en utilisant une fonction pseudo-aléatoire les centroids à des k points du jeu de données, k étant fixé au départ
> #### Etape 02 : Affectation des points du jeu de données
> Chaque centroid définit à priori une classe, chaque point sera associé au centroid le plus proche i.e dont la distance Euclidienne est minimale
> #### Etape 03 : Mise à jour des centroids
> après chaque affectation on recalcule les centroids qui sont pris comme étant la moyenne des éléments d'une meme classe, on réitère le processus N fois, ce dernier est le nombre d'itérations et est figé au départ aussi


#### Remarque :
> Il existe plusieurs critères de séléction du k (nombre de partitions), on peut se contenter de mesurer l'inértie totale en fonction de ce dernier pout le fixer 
> Il est aussi à noter que l'algorithme des kmeans cherche plutot à maximiser l'inértie intra-classe et minimiser au mieux l'inértie inter-classe 
