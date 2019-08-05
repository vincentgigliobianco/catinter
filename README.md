# Objectif

Scikit-learn ne dispose pas de méthodes pour créer des intéractions de variables catégorielles. La fonction *catinter* prend en entrée un dataframe pandas et une liste de variables pour lesquelles on souhaite créer une variable intéraction.

# Arguments

 * dataframe : un dataframe pandas.
 * list_of_catvar : Liste de strings. une liste des colonnes du dataframe pour lesquelles on veut créer une colonne intéraction
 * ordre : Integer. le degré de l'intéraction. Ex : le degré d'ordre 2 créera les intéractions d'ordre 2, i.e. toutes les paires distinctes parmi la liste *list_of_var*. Si l'ordre vaut 3, on créera les intéractions issues de tout les triplets distincts de *list_of_var*
 * only_ordre : Booléen. Si True, alors seule les intéractions d'ordre *ordre* seront créées. Si False, les intéractions d'ordre *ordre* et toutes celles des niveaux inférieures seront créées.
 * dummy : Booléen. Si True, alors les nouvelles colonnes intéractions sont transformées en dummy variable. Si False, elles sont laissées tel quel.

# Exemple
```
import catinter
df = read.csv("data/df.csv")
df.head()
df = catinter.catinter(dataframe = df, list_of_var = ["color_eyes","color_hair","education","ville","salaire"], ordre = 2, only_ordre = True, dummy = True)

```