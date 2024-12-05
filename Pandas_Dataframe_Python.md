Qu’est-ce que Pandas ?
Pandas est une bibliothèque populaire open-source de manipulation et d’analyse de données pour le langage de programmation Python. Elle offre un ensemble d’outils puissants et flexibles pour travailler avec des données structurées, ce qui en fait un outil fondamental pour les scientifiques des données, les analystes et les ingénieurs.
Pandas est conçu pour gérer des données dans divers formats, tels que les données tabulaires, les séries temporelles, et plus encore, ce qui en fait une partie essentielle du flux de traitement des données dans de nombreuses industries.

Voici quelques caractéristiques et fonctionnalités clés de Pandas :

Structures de Données : Pandas propose deux structures de données principales - DataFrame et Series.

Un DataFrame est une structure de données tabulaire bidimensionnelle, de taille mutable et potentiellement hétérogène avec des axes étiquetés (lignes et colonnes).
Une Series est un tableau étiqueté unidimensionnel, essentiellement une seule colonne ou ligne de données.
Importation et Exportation de Données : Pandas facilite la lecture de données provenant de diverses sources, y compris les fichiers CSV, les feuilles de calcul Excel, les bases de données SQL, et plus encore. Il peut également exporter des données vers ces formats, permettant un échange de données fluide.

Fusion et Jointure de Données : Vous pouvez combiner plusieurs DataFrames en utilisant des méthodes comme merge et join, similaires aux opérations SQL, pour créer des ensembles de données plus complexes à partir de différentes sources.

Indexation Efficace : Pandas fournit des méthodes d’indexation et de sélection efficaces, vous permettant d’accéder rapidement à des lignes et colonnes spécifiques de données.

Structures de Données Personnalisées : Vous pouvez créer des structures de données personnalisées et manipuler les données de manière à répondre à vos besoins spécifiques, étendant ainsi les capacités de Pandas.

Importation de Pandas :
Importez Pandas en utilisant la commande d’importation, suivie du nom de la bibliothèque.
Généralement, Pandas est importé en tant que pd pour plus de concision dans le code.

1
import pandas as pd
Copied!
Chargement des données :
Pandas peut être utilisé pour charger des données à partir de diverses sources, telles que des fichiers CSV et Excel.
La fonction read_csv est utilisée pour charger des données à partir d’un fichier CSV dans un DataFrame Pandas.
Pour lire un fichier CSV (Comma-Separated Values) en Python en utilisant la bibliothèque Pandas, vous pouvez utiliser la fonction pd.read_csv(). Voici la syntaxe pour lire un fichier CSV :

1
2
3
4
import pandas as pd
# Read the CSV file into a DataFrame
df = pd.read_csv('your_file.csv')
Copied!
Remplacez 'your_file.csv' par le chemin réel de votre fichier CSV. Assurez-vous que le fichier se trouve dans le même répertoire que votre script Python, ou que vous fournissez le chemin de fichier correct.

Qu’est-ce qu’une Série ?
Une Série est un tableau unidimensionnel étiqueté dans Pandas. On peut la considérer comme une seule colonne de données avec des étiquettes ou des indices pour chaque élément. Vous pouvez créer une Série à partir de diverses sources de données, telles que des listes, des tableaux NumPy ou des dictionnaires.
Voici un exemple de base de création d’une Série dans Pandas :

  import pandas as pd
  # Create a Series from a list
  data = [10, 20, 30, 40, 50]
  s = pd.Series(data)
  print(s)

Dans cet exemple, nous avons créé une Série nommée s avec des données numériques. Remarquez que Pandas a automatiquement attribué des indices numériques (0, 1, 2, 3, 4) à chaque élément, mais vous pouvez également spécifier des étiquettes personnalisées si nécessaire.

Accéder aux éléments dans une série
Vous pouvez accéder aux éléments d’une série en utilisant les étiquettes d’index ou les positions entières. Voici quelques méthodes courantes pour accéder aux données d’une série :

Accès par étiquette

print(s[2])     # Access the element with label 2 (value 30)

Accéder par position

print(s.iloc[3]) # Access the element at position 3 (value 40)

Accéder à plusieurs éléments

print(s[1:4])   # Access a range of elements by label

Attributs et Méthodes de la Série
Les Séries Pandas sont accompagnées de divers attributs et méthodes pour vous aider à manipuler et analyser les données efficacement. Voici quelques-uns des essentiels :

values : Renvoie les données de la Série sous forme de tableau NumPy.
index : Renvoie l’index (étiquettes) de la Série.
shape : Renvoie un tuple représentant les dimensions de la Série.
size : Renvoie le nombre d’éléments dans la Série.
mean(), sum(), min(), max() : Calcule des statistiques sommaires des données.
unique(), nunique() : Obtenez des valeurs uniques ou le nombre de valeurs uniques.
sort_values(), sort_index() : Trie la Série par valeurs ou étiquettes d’index.
isnull(), notnull() : Vérifie les valeurs manquantes (NaN) ou non manquantes.
apply() : Applique une fonction personnalisée à chaque élément de la Série.

Qu’est-ce qu’un DataFrame ?
Un DataFrame est une structure de données bidimensionnelle étiquetée avec des colonnes de types de données potentiellement différents.
Pensez-y comme à une table où chaque colonne représente une variable et chaque ligne représente une observation ou un point de données. 
Les DataFrames sont adaptés à une large gamme de données, y compris les données structurées provenant de fichiers CSV, de feuilles de calcul Excel, de bases de données SQL, et plus encore.

Création de DataFrames à partir de dictionnaires :
Les DataFrames peuvent être créés à partir de dictionnaires, avec les clés comme étiquettes de colonnes et les valeurs comme listes représentant des lignes.

import pandas as pd
# Creating a DataFrame from a dictionary
data = {'Name': ['Alice', 'Bob', 'Charlie', 'David'],
        'Age': [25, 30, 35, 28],
        'City': ['New York', 'San Francisco', 'Los Angeles', 'Chicago']}
df = pd.DataFrame(data)
print(df)
