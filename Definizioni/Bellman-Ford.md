Formula che enuncia che per trovare il percorso a costo minimo tra un nodo sorgente $x$ e un nodo destinazione $y$, tramite nodi intermedi vicini $v$ supponendo che:
- Costo $c(x,y)$ tra nodo sorgente $x$ e il vicino $z$ sia noto
- Distanza minima tra vicino $z$ e destinazione $y$ sia nota ($d_{zy}$)

L'equazione è:
se $d_{xy}$ := costo del cammino a costo minimo da $x$ a $y$ allora 

$$d_{xy}=min_v\{c(x,v)+d_{vy}\}$$