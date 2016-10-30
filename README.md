# dot

```
dot -Tpng arch.dot -o pouet.png
```

Les relations décrites dans le subgraph ne concerne que les objets du subgraph !!!

En dehors sont décrites :
- les relations hors subgraph
- les relations inter-subgraph


Exemple tiré du site graphviz

```
digraph G {

    subgraph cluster_0 {
        style=filled;
        color=lightgrey;
        node [style=filled,color=white];
        a0 -> a1 -> a2 -> a3; <-------------- relation entre objets d'un même subgraph
        label = "process #1";
    }

    subgraph cluster_1 {
        node [style=filled];
        b0 -> b1 -> b2 -> b3;  <-------------- relation entre objets d'un même subgraph
        label = "process #2";
        color=blue
    }
    a1 -> b3; <----------------- relation entre objets transverses 
    b2 -> a3; <--------------|
    a3 -> a0; <--------------|
}
```

