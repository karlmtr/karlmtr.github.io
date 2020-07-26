* TOC {:toc}

# Pour commencer
Dans matplotlib, il y a deux "objets" principaux:

* Les figures: on peut les considérer comme les "fenêtres"
* Les axes: ils vont contenir les courbes

Chaque figure peut contenir un ou plusieurs axes.

Pour utiliser matplotlib, il suffit la plupart du temps d'importer la partie "pyplot" de matplotlib.

```PYTHON
import matplotlib.pyplot as plt
```

# Les dfférentes approches de Matplotlib

Matplotlib permet plusieurs approches pour créer des graphiques. 

## La plus simple (et la moins recommandée)

Cette approche est utile si l'on n'a qu'une seule figure avec qu'un seul axe.

```PyTHON
 import matplotlib.pyplot as plt
 

## On crée nos données
x =[1,2,3,4,5,6,7,8,9,10]
y =[2,6,3,7,1,4,6,8,3,11]

plt.plot(x,y) # plt.plot() utilisé pour 
plt.show()
```







## Matplotlib et LaTeX




