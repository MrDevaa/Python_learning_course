# Travailler avec des données dans Python Cheat Sheet

## Lecture et écriture de fichiers

### Modes d'ouverture de fichiers
- Différents modes pour ouvrir des fichiers pour des opérations spécifiques.

| Mode | Description |
|------|-------------|
| `r`  | Lecture uniquement |
| `w`  | Écriture uniquement (écrase le fichier) |
| `a`  | Ajout (écriture à la fin du fichier) |
| `+`  | Mise à jour (lecture et écriture) |
| `b`  | Mode binaire (par défaut, texte) |

#### Exemples :
```python
with open("data.txt", "r") as file:
    content = file.read()
    print(content)

with open("output.txt", "w") as file:
    file.write("Hello, world!")

with open("log.txt", "a") as file:
    file.write("Log entry: Something happened.")

with open("data.txt", "r+") as file:
    content = file.read()
    file.write("Contenu mis à jour : " + content)
```

### Méthodes de lecture de fichiers
- Différentes méthodes pour lire le contenu d'un fichier.

| Méthode            | Description                                   |
|--------------------|-----------------------------------------------|
| `file.readlines()` | Lit toutes les lignes sous forme de liste    |
| `file.readline()`  | Lit la ligne suivante sous forme de chaîne   |
| `file.read()`      | Lit tout le contenu sous forme de chaîne     |

#### Exemple :
```python
with open("data.txt", "r") as file:
    lines = file.readlines()
    next_line = file.readline()
    content = file.read()
```

### Méthodes d'écriture de fichiers
- Différentes méthodes pour écrire du contenu dans un fichier.

| Méthode             | Description                                |
|---------------------|--------------------------------------------|
| `file.write(str)`   | Écrit une chaîne dans le fichier           |
| `file.writelines(list)` | Écrit une liste de chaînes dans le fichier |

#### Exemple :
```python
lines = ["Hello\n", "World\n"]
with open("output.txt", "w") as file:
    file.writelines(lines)
```

### Itération sur les lignes
- Itère à travers chaque ligne d'un fichier.

#### Exemple :
```python
with open("data.txt", "r") as file:
    for line in file:
        print(line)
```

### `open()` et `close()`
- Ouvre un fichier, effectue des opérations, et le ferme explicitement.

#### Exemple :
```python
file = open("data.txt", "r")
content = file.read()
file.close()
```

### `with open()`
- Ouvre un fichier avec un bloc `with`, garantissant une fermeture automatique.

#### Exemple :
```python
with open("data.txt", "r") as file:
    content = file.read()
```

---

## Pandas

### Importer Pandas
```python
import pandas as pd
```

### Lecture et écriture de fichiers

#### Lire un fichier CSV
```python
df = pd.read_csv("data.csv")
```

#### Lire un fichier Excel
```python
df = pd.read_excel("data.xlsx")
```

#### Écrire dans un fichier CSV
```python
df.to_csv("output.csv", index=False)
```

### Accéder aux colonnes
```python
# Une seule colonne
col = df["column_name"]

# Plusieurs colonnes
cols = df[["column1", "column2"]]
```

### Résumé statistique
```python
df.describe()
```

### Supprimer des colonnes ou lignes
```python
# Supprimer des colonnes
df.drop(["column1", "column2"], axis=1, inplace=True)

# Supprimer des lignes
df.drop(index=[row1, row2], axis=0, inplace=True)
```

### Gérer les valeurs manquantes
```python
# Supprimer les lignes avec des valeurs NaN
df.dropna(axis=0, inplace=True)
```

### Identifier les doublons
```python
duplicate_rows = df[df.duplicated()]
```

### Filtrer les lignes
```python
filtered_df = df[(df["age"] > 30) & (df["salary"] < 50000)]
```

### Groupby et agrégation
```python
grouped = df.groupby(["category", "region"]).agg({"sales": "sum"})
```

### Afficher le début ou la fin du DataFrame
```python
# Premières n lignes
df.head(n)

# Dernières n lignes
df.tail(n)
```

### Informations sur le DataFrame
```python
df.info()
```

### Fusionner deux DataFrames
```python
merged_df = pd.merge(df1, df2, on=["column1", "column2"])
```

### Remplacer des valeurs
```python
df["status"].replace("In Progress", "Active", inplace=True)
```

---

## NumPy

### Importer NumPy
```python
import numpy as np
```

### Créer un tableau NumPy
```python
# Tableau 1D
array_1d = np.array([1, 2, 3])

# Tableau 2D
array_2d = np.array([[1, 2], [3, 4]])
```

### Attributs et opérations sur les tableaux
```python
# Moyenne
np.mean(array)

# Somme
np.sum(array)

# Minimum et maximum
np.min(array)
np.max(array)

# Produit scalaire
np.dot(array_1, array_2)
