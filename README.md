# Classification des Fleurs Iris avec un Arbre de Décision

Ce projet implémente un modèle de classification utilisant un **arbre de décision** pour prédire la classe d'une fleur en fonction de ses caractéristiques. L'objectif est de s'entraîner sur le célèbre **jeu de données Iris** afin de classer correctement les différentes espèces de fleurs.

## Jeu de Données : Iris

Le jeu de données **Iris** est un ensemble de données classique utilisé pour la classification. Il contient 150 observations de fleurs de 3 espèces différentes (Setosa, Versicolour, et Virginica) avec les caractéristiques suivantes :

- **Sepal Length** : Longueur du sépale en cm.
- **Sepal Width** : Largeur du sépale en cm.
- **Petal Length** : Longueur du pétale en cm.
- **Petal Width** : Largeur du pétale en cm.
- **Target** : Espèce de la fleur (0 : Setosa, 1 : Versicolour, 2 : Virginica)

## Objectif

L’objectif de ce projet est de :
1. Construire un modèle de classification basé sur un arbre de décision.
2. Entraîner ce modèle pour prédire la classe d'une fleur en fonction de ses caractéristiques.
3. Évaluer la performance du modèle.

## Bibliothèques Utilisées

- **sklearn.datasets** : Permet de charger des jeux de données intégrés comme le jeu de données Iris.
- **sklearn.model_selection** : Fournit des outils pour diviser le jeu de données en ensembles d’entraînement et de test.
- **sklearn.tree** : Contient l’implémentation des arbres de décision.
- **sklearn.metrics** : Permet d’évaluer la précision du modèle avec des métriques telles que la précision et le rapport de classification.
- **matplotlib.pyplot** : Utilisé pour visualiser l’arbre de décision, facilitant l'interprétation du modèle.

## Structure du Projet

- **iris_decision_tree.ipynb** : Notebook Jupyter contenant le code pour le chargement des données, la construction, l'entraînement, et l'évaluation du modèle, ainsi que la visualisation de l’arbre de décision.

## Explication du Code

1. **Chargement des Données** : Utilisation de `load_iris()` depuis `sklearn.datasets` pour charger le jeu de données Iris.

2. **Division des Données** :
   - Séparation des données en **ensemble d'entraînement** et **ensemble de test** avec `train_test_split()` depuis `sklearn.model_selection`.
   - Cela permet d’évaluer la performance du modèle sur des données non vues lors de l’entraînement.

3. **Construction de l’Arbre de Décision** :
   - Création d’un classificateur d’arbre de décision avec `DecisionTreeClassifier` depuis `sklearn.tree`.
   - Entraînement du modèle avec l’ensemble de données d’entraînement.

4. **Évaluation du Modèle** :
   - Utilisation de `accuracy_score` depuis `sklearn.metrics` pour calculer la précision sur l'ensemble de test.
   - Affichage du **rapport de classification** pour comprendre la performance sur chaque classe.

5. **Visualisation de l'Arbre** :
   - Utilisation de `plot_tree()` depuis `sklearn.tree` pour afficher l'arbre de décision et visualiser les règles de décision.

## Exécution du Projet

1. Clonez ce dépôt et ouvrez le fichier `iris_decision_tree.ipynb` dans Jupyter Notebook.
2. Exécutez chaque cellule pour charger les données, entraîner le modèle, et visualiser les résultats.

## Exemple de Résultat

Le modèle fournit un arbre de décision structuré, facile à interpréter, qui sépare les données en fonction des caractéristiques des fleurs pour prédire leur espèce. Une matrice de confusion ou un rapport de classification est aussi fourni pour évaluer la précision de la classification.

## Conclusion

Ce projet utilise un arbre de décision pour effectuer une **classification supervisée** sur le jeu de données Iris. Le modèle d'arbre de décision est un algorithme performant pour les tâches de classification simples et peut être facilement interprété grâce aux visualisations, ce qui est un avantage pour la compréhension des décisions prises par le modèle.
