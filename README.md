
<!-- TOC -->autoauto- [Python](#python)auto    - [Actions de base](#actions-de-base)auto        - [Lire un fichier de données](#lire-un-fichier-de-données)auto            - [Avec le module pandas](#avec-le-module-pandas)auto        - [Matplotlib](#matplotlib)auto        - [Les différentes approches de Matplotlib](#les-différentes-approches-de-matplotlib)auto            - [La plus simple (et la moins recommandée)](#la-plus-simple-et-la-moins-recommandée)auto            - [La plus complète (recommandée)](#la-plus-complète-recommandée)auto        - [La fonction plot()](#la-fonction-plot)auto    - [Flask](#flask)auto- [DOCKER](#docker)auto    - [Commandes de bases](#commandes-de-bases)auto- [UNIX](#unix)auto- [JAVASCRIPT](#javascript)autoauto<!-- /TOC -->

# Python

## Actions de base

### Lire un fichier de données avec le module `pandas`



Si on a un fichier de données `exemple.txt` (ou `exemple.csv`, tant qu'il est composé de colonnes) dans le même dossier que le fichier python. 


On utilise la fonction `read_csv()` pour importer les données:

```py
import pandas as pd #  On importe le module pandas (et on le renomme localement pd)

data = pd.read_csv("exemple.txt")
```
Pour accéder aux données de `data` : `data["nom_de_la_colonne"]`.

`read_csv()` prend plusieurs paramètres supplémentaires, dont :

* `sep` = "<caractère>" : précise le caractère qui sépare les colonnes du fichier : `\t` pour une tabulation (par défaut)
* `header= None` : va charger les données sans les noms des colonnes



### Matplotlib
Dans matplotlib, il y a deux "objets" principaux:

* Les figures: on peut les considérer comme les "fenêtres"
* Les axes: ils vont contenir les courbes

Chaque figure peut contenir un ou plusieurs axes.

Pour utiliser matplotlib, il suffit la plupart du temps d'importer la partie "pyplot" de matplotlib.

```PYTHON
import matplotlib.pyplot as plt
```

### Les différentes approches de Matplotlib

Matplotlib permet plusieurs approches pour créer des graphiques. 

#### La plus simple (et la moins recommandée)

Cette approche est utile si l'on n'a qu'une seule figure avec qu'un seul axe.

```PYTHON
import matplotlib.pyplot as plt
 

## On crée nos données
x =[1,2,3,4,5,6,7,8,9,10]
y =[2,6,3,7,1,4,6,8,3,11]

plt.plot(x,y) # plt.plot() utilisé pour nuages de points (reliés ou pas) 
plt.show()
```
#### La plus complète (recommandée)

avec cette technique on utilise les figures et les axes.

```python
import matplotlib.pyplot as plt

# On crée nos données
x =[1,2,3,4,5,6,7,8,9,10]
y =[2,6,3,7,1,4,6,8,3,11]

fig,ax = plt.subplots() # on crée une figure et un axe
#une autre manière:

fig = plt.figure(figsize=(10,9)) # dimension de la figure
ax1 = fig.add_subplot(111)

ax.plot(x,y) # on plot sur cet axe en particulier

plt.show()
```
Cette technique permet de configurer indépendemment les axes (par exemple mettre en échelle logarithmique)

C'est aussi possible d'utiliser la forme:

```python
fig = plt.figure(figsize=(10,9)) # dimension de la figure
ax1 = fig.add_subplot(221) 
ax2 = fig.add_subplot(222)
ax3 = fig.add_subplot(223)
ax4 = fig.add_subplot(224)
```
Les axes sont numérotés de droite à gauche et de haut en bas.

Par exemple, `221` signifie "créer un axe à la première place dans une disposition 2 ligne, 2 colonnes" (donc en haut à gauche )

### La fonction plot()

plt.plot() prends plusieurs arguments: <br>
`color = "blue"`

## Flask

# DOCKER

## Commandes de bases

Créer un nouveau container:

View all containers: 
`docker ps -a`

Rename container: 
`docker rename CONTAINER NEW_NAME`

Start container and link bash
`docker start -i NAME_CONTAINER_OR_ID`

Run another terminal in a container:
`docker exec -it <container> bash`




# UNIX

Compresser un fichier:  `tar -zcvf <nom>.tar.gz <nomDossier>`

Trouver les fichiers et supprimer dans sous-dossiers : `find . -name \*.png -type f -delete`


# JAVASCRIPT

fonction isolée (sont exécutées directement):
```JAVASCRIPT
(function(){})();
```

Sans déclaration de type, variable est globale !

Exemple récupérer donnée d'un dom:

```javascript
<div id="myDiv">
    <p>Un peu de texte <a>et un lien</a></p>
</div>

<script>
    var div = document.getElementById('myDiv');
    alert(div);
</script>
```






























