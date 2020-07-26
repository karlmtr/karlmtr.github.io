- [Python](#python)
	- [Matplotlib](#matplotlib)
		- [Les différentes approches de Matplotlib](#les-différentes-approches-de-matplotlib)
			- [La plus simple (et la moins recommandée)](#la-plus-simple-et-la-moins-recommandée)
				- [La plus complète (recommandée)](#la-plus-complète-recommandée)
		- [La fonction plot()](#la-fonction-plot)
- [Docker](#docker)

# Python
## Matplotlib
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
##### La plus complète (recommandée)

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

plt.plot() prends plusieurs arguments:
`color = "blue,`



# Docker 





















