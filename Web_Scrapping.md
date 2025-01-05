# Introduction au web scraping

Le web scraping, également connu sous le nom de collecte de données web ou d’extraction de données web, est le processus d’extraction d’informations à partir de sites web ou de pages web. Il implique la récupération automatisée de données à partir de sources web. Les gens l’utilisent pour diverses applications telles que l’analyse de données, le data mining, la comparaison de prix, l’agrégation de contenu, et plus encore.

## Comment fonctionne le web scraping

### Requête HTTP
Le processus commence généralement par une requête HTTP. Un web scraper envoie une requête HTTP à une URL spécifique, de la même manière qu’un navigateur web le ferait lorsque vous visitez un site web. La requête est généralement une requête HTTP GET, qui récupère le contenu de la page web.

### Récupération de page web
Le serveur web hébergeant le site répond à la demande en renvoyant le contenu HTML de la page web demandée. Ce contenu inclut le texte visible et les éléments médiatiques ainsi que la structure HTML sous-jacente qui définit la mise en page de la page.

### Analyse HTML
Une fois le contenu HTML reçu, vous devez analyser le contenu. L’analyse consiste à décomposer la structure HTML en composants, tels que les balises, les attributs et le contenu textuel. Vous pouvez utiliser **BeautifulSoup** en Python. Cela crée une représentation structurée du contenu HTML qui peut être facilement parcourue et manipulée.

### Extraction de données
Avec le contenu HTML analysé, les extracteurs de données peuvent désormais identifier et extraire les données spécifiques dont ils ont besoin. Ces données peuvent inclure du texte, des liens, des images, des tableaux, des prix de produits, des articles de presse, et plus encore. Les extracteurs localisent les données en recherchant des balises HTML, des attributs et des motifs pertinents dans la structure HTML.

### Transformation des données
Les données extraites peuvent nécessiter un traitement et une transformation supplémentaires. Par exemple, vous pouvez supprimer les balises HTML du texte, convertir des formats de données ou nettoyer des données désordonnées. Cette étape garantit que les données sont prêtes pour l’analyse ou d’autres cas d’utilisation.

### Stockage
Après l’extraction et la transformation, vous pouvez stocker les données récupérées dans divers formats, tels que des bases de données, des feuilles de calcul, JSON ou des fichiers CSV. Le choix du format de stockage dépend des exigences spécifiques du projet.

### Automatisation
Dans de nombreux cas, des scripts ou des programmes automatisent le web scraping. Ces outils d’automatisation permettent l’extraction récurrente de données à partir de plusieurs pages web ou sites internet. Le scraping automatisé est particulièrement utile pour collecter des données à partir de sites web dynamiques qui mettent régulièrement à jour leur contenu.

![Exemple de page web](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%205/images/Webpage.png)

## Document Tree

### Structure HTML
Le langage de balisage hypertexte (HTML) sert de fondation aux pages web. Comprendre sa structure est essentiel pour le web scraping.

- `<html>` est l’élément racine d’une page HTML.
- `<head>` contient des méta-informations sur la page HTML.
- `<body>` affiche le contenu de la page web, souvent les données d’intérêt.
- Les balises `<h3>` sont des titres de type 3, rendant le texte plus grand et en gras, généralement utilisées pour les noms des joueurs.
- Les balises `<p>` représentent des paragraphes et contiennent des informations sur les salaires des joueurs.

### Composition d’une balise HTML
Les balises HTML définissent la structure du contenu web et peuvent contenir des attributs.

- Une balise HTML se compose d’une balise d’ouverture (début) et d’une balise de fermeture (fin).
- Les balises ont des noms (`<a>` pour une balise d’ancrage).
- Les balises peuvent contenir des attributs avec un nom d’attribut et une valeur, fournissant des informations supplémentaires à la balise.

### Arbre de document HTML
Vous pouvez visualiser les documents HTML comme des arbres avec des balises comme nœuds.

- Les balises peuvent contenir des chaînes de caractères et d’autres balises, faisant d’elles les enfants de la balise.
- Les balises au sein de la même balise parente sont considérées comme des sœurs.
- Par exemple, la balise `<html>` contient à la fois les balises `<head>` et `<body>`, les rendant descendants de `<html>` mais enfants de `<html>`. `<head>` et `<body>` sont des sœurs.

![Arbre de document HTML](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%205/images/DOM_structure.png)

### Tables HTML
Les tables HTML sont essentielles pour présenter des données structurées.

- Définissez une table HTML en utilisant la balise `<table>`.
- Chaque ligne de table est définie avec une balise `<tr>`.
- La première ligne utilise souvent la balise d’en-tête de table, généralement `<th>`.
- La cellule de la table est représentée par des balises `<td>`, définissant des cellules individuelles dans une ligne.

## Extraction de données web

L’extraction de données web consiste à extraire des informations à partir de pages web en utilisant Python. Cela peut faire gagner du temps et automatiser la collecte de données.

### Outils requis
Le web scraping nécessite du code Python et deux modules essentiels : **Requests** et **Beautiful Soup**. Assurez-vous d’avoir installé les deux modules dans votre environnement Python.

```python
# Import Beautiful Soup to parse the web page content
from bs4 import BeautifulSoup
```

### Récupération et analyse HTML
Pour commencer le web scraping, vous devez récupérer le contenu HTML d’une page web et l’analyser à l’aide de Beautiful Soup. Voici un exemple étape par étape :

```python
import requests
from bs4 import BeautifulSoup

# Specify the URL of the webpage you want to scrape
url = 'https://en.wikipedia.org/wiki/IBM'

# Send an HTTP GET request to the webpage
response = requests.get(url)

# Store the HTML content in a variable
html_content = response.text

# Create a BeautifulSoup object to parse the HTML
soup = BeautifulSoup(html_content, 'html.parser')

# Display a snippet of the HTML content
print(html_content[:500])
```

### Naviguer dans la structure HTML
BeautifulSoup représente le contenu HTML sous forme de structure arborescente, ce qui permet une navigation facile. Vous pouvez utiliser des méthodes comme `find_all` pour filtrer et extraire des éléments HTML spécifiques. Par exemple, pour trouver toutes les balises d’ancrage (`<a>`) et imprimer leur texte :

```python
# Find all <a> tags (anchor tags) in the HTML
links = soup.find_all('a')

# Iterate through the list of links and print their text
for link in links:
    print(link.text)
```

### Extraction de données personnalisée
Le web scraping vous permet de naviguer dans la structure HTML et d’extraire des informations spécifiques en fonction de vos besoins. Ce processus peut impliquer la recherche de balises, d’attributs ou de contenus textuels spécifiques dans le document HTML.

### Utilisation de BeautifulSoup pour l’analyse HTML
Beautiful Soup est un outil puissant pour naviguer et extraire des parties spécifiques des pages web. Il vous permet de trouver des éléments en fonction de leurs balises, attributs ou texte, facilitant ainsi l’extraction des informations qui vous intéressent.

### Utilisation de pandas `read_html` pour l’extraction de tableaux
Pandas, une bibliothèque Python, fournit une fonction appelée `read_html`, qui peut extraire automatiquement des données des tableaux des sites web et les présenter dans un format adapté à l’analyse. C’est similaire à prendre un tableau d’une page web et à l’importer dans une feuille de calcul pour une analyse plus approfondie.

## Conclusion

Dans cette lecture, vous avez appris à réaliser du web scraping avec **BeautifulSoup** et **Pandas**, en mettant l’accent sur l’extraction d’éléments et de tables. BeautifulSoup facilite l’analyse HTML, tandis que la fonction `read_html` de Pandas simplifie l’extraction de tables. La lecture a également souligné l’importance d’un web scraping responsable, garantissant le respect des conditions des sites web. Armé de ces connaissances, vous pouvez vous engager en toute confiance dans une extraction de données précise.
