# Objectif

Dans cette lecture, vous apprendrez :

- Les bases de NumPy
- Comment créer des tableaux NumPy
- Attributs et indexation des tableaux
- Opérations de base comme l’addition et la multiplication

## Qu’est-ce que NumPy ?

NumPy, abréviation de Numérique Python, est une bibliothèque fondamentale pour le calcul numérique et scientifique en Python. Elle fournit un support pour de grands tableaux et matrices multidimensionnels, ainsi qu’une collection de fonctions mathématiques de haut niveau pour opérer sur ces tableaux. NumPy sert de base à de nombreuses bibliothèques de science des données et d’apprentissage automatique, en faisant un outil essentiel pour l’analyse de données et la recherche scientifique en Python.

### Aspects clés de NumPy en Python :

- **Structures de données efficaces** : NumPy introduit des structures de tableaux efficaces, qui sont plus rapides et consomment moins de mémoire que les listes Python. Cela est crucial pour gérer de grands ensembles de données.
- **Tableaux multi-dimensionnels** : NumPy vous permet de travailler avec des tableaux multi-dimensionnels, facilitant la représentation de matrices et de tenseurs. Cela est particulièrement utile en calcul scientifique.
- **Opérations élément par élément** : NumPy simplifie les opérations mathématiques élément par élément sur les tableaux, rendant facile l’exécution de calculs sur l’ensemble des ensembles de données en une seule fois.
- **Génération de nombres aléatoires** : Il fournit une large gamme de fonctions pour générer des nombres aléatoires et des données aléatoires, ce qui est utile pour les simulations et l’analyse statistique.
- **Intégration avec d’autres bibliothèques** : NumPy s’intègre parfaitement avec d’autres bibliothèques de science des données comme SciPy, Pandas et Matplotlib, augmentant son utilité dans divers domaines.
- **Optimisation des performances** : Les fonctions NumPy sont implémentées dans des langages de bas niveau comme C et Fortran, ce qui améliore considérablement leurs performances. C’est un choix privilégié lorsque la vitesse est essentielle.

---

## Installation

Si vous n’avez pas encore installé NumPy, vous pouvez le faire en utilisant pip :

```bash
pip install numpy
```

---

## Création de tableaux NumPy

Vous pouvez créer des tableaux NumPy à partir de listes Python. Ces tableaux peuvent être unidimensionnels ou multidimensionnels.

### Création d’un tableau 1D

```python
import numpy as np

# Creating a 1D array
arr_1d = np.array([1, 2, 3, 4, 5])
```

### Création d’un tableau 2D

```python
import numpy as np

# Creating a 2D array
arr_2d = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
```

---

## Attributs des tableaux

Les tableaux NumPy ont plusieurs attributs utiles :

```python
# Array attributes
print(arr_2d.ndim)  # Nombre de dimensions
# Output: 2

print(arr_2d.shape)  # Forme (nombre de lignes et de colonnes)
# Output: (3, 3)

print(arr_2d.size)  # Nombre total d'éléments
# Output: 9
```

---

## Indexation et découpage

Vous pouvez accéder aux éléments d’un tableau NumPy en utilisant l’indexation et le découpage :

### Exemple 1 : Accès à un élément dans un tableau 1D

```python
print(arr_1d[2])  # Accède au 3ème élément
# Output: 3
```

### Exemple 2 : Accès à un élément dans un tableau 2D

```python
print(arr_2d[1, 2])  # Accède à l'élément (2ème ligne, 3ème colonne)
# Output: 6

print(arr_2d[1])  # Accède à une ligne complète (2ème ligne)
# Output: [4, 5, 6]

print(arr_2d[:, 1])  # Accède à une colonne complète (2ème colonne)
# Output: [2, 5, 8]
```

---

## Opérations de base

NumPy simplifie les opérations de base sur les tableaux :

### Addition de tableaux

```python
# Array addition
array1 = np.array([1, 2, 3])
array2 = np.array([4, 5, 6])
result = array1 + array2
print(result)  # Output: [5, 7, 9]
```

### Multiplication scalaire

```python
# Scalar multiplication
array = np.array([1, 2, 3])
result = array * 2
print(result)  # Output: [2, 4, 6]
```

### Multiplication élément par élément (Produit de Hadamard)

```python
# Element-wise multiplication
array1 = np.array([1, 2, 3])
array2 = np.array([4, 5, 6])
result = array1 * array2
print(result)  # Output: [4, 10, 18]
```

### Multiplication de matrices

```python
# Matrix multiplication
matrix1 = np.array([[1, 2], [3, 4]])
matrix2 = np.array([[5, 6], [7, 8]])
result = np.dot(matrix1, matrix2)
print(result)
# Output:
# [[19 22]
#  [43 50]]
```

---

## Tableau des opérations avec NumPy

| Opération                        | Description                                     | Exemple                                       |
|----------------------------------|-------------------------------------------------|-----------------------------------------------|
| Création de tableau              | Création d’un tableau NumPy.                  | `arr = np.array([1, 2, 3, 4, 5])`            |
| Arithmétique élément par élément | Addition, soustraction, etc. élément par élément. | `result = arr1 + arr2`                       |
| Arithmétique scalaire            | Addition, soustraction, etc. scalaire.          | `result = arr * 2`                           |
| Fonctions élément par élément    | Application de fonctions à chaque élément.      | `result = np.sqrt(arr)`                      |
| Somme et Moyenne                 | Calculer la somme et la moyenne d’un tableau.  | `total = np.sum(arr)`<br>`average = np.mean(arr)` |
| Valeurs maximales et minimales   | Trouver les valeurs maximales et minimales.     | `max_val = np.max(arr)`<br>`min_val = np.min(arr)` |
| Restructuration                  | Changer la forme d’un tableau.                 | `reshaped_arr = arr.reshape(2, 3)`           |
| Transposition                    | Transposer un tableau multidimensionnel.        | `transposed_arr = arr.T`                     |
| Multiplication de matrices       | Effectuer une multiplication de matrices.       | `result = np.dot(matrix1, matrix2)`          |

---

## Conclusion

NumPy est une bibliothèque fondamentale pour la science des données et les calculs numériques. Ce guide couvre les bases de NumPy, et il y a encore beaucoup plus à explorer. Visitez [numpy.org](https://numpy.org) pour plus d’informations et d’exemples.
