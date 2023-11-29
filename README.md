# Practica 2 Inteligencia Aritificial - Busqueda Heuristica

## Descripción:

Esta práctica consiste en analizar código del algoritmo A* y proporcionar respuestas a preguntas específicas relacionadas con las definiciones del algoritmo A*.

## Como utilizarlo:

1. Clonar el repositorio.

    ```
    https://github.com/XMoraP/practica2_IA.git
    ```
   
2. Modificar el método main para indicar el nodo origen y el nodo destino, el cual proporciona el camino mejor basandose en el algoritmo A*.
3. Ejecutar el comando:

    ```
    ant run_main
    ```

## Respuestas: 

1. ¿Qué variable representa la lista ABIERTA?

    La variable designada para representar la lista Abierta es 'openSet', ya que esta variable se refiere a una estructura de datos que alberga un conjunto de nodos que requieren evaluación.

3. ¿Qué variable representa la función g?

    Esta representada por la variable gScore, la cual se elige como una estructura de datos, específicamente un mapa. Este mapa almacena la información relacionada con el nodo de inicio y los costos asociados hasta alcanzar el nodo específico 'n'.
   
    ```
    gScore.put(start, 0);
    ```
    En este fragmento de código se puede apreciar el uso de gScore, recibiendo como parámetros el nodo inicial y el coste.

4. ¿Qué variable representa la función f?

    Esta representada por la variable fScore, en este caso, 'fScore' recibe la contribución del costo acumulado desde el nodo inicial, expresado como 'g(n)', y la estimación heurística, denotada como 'h(n)'. 
    
    ```
     fScore.put(start, heuristicCostEstimate(start,goal));
    ```
     
5. ¿Qué método habría que modificar para que la heurística representara
la distancia aérea entre vértices?

    Habría que modificar el método: 
    ```
    heuristicCostEstimate( )
    ```
   Dado que, por defecto, se calcula la heurística asignándole un costo de 1 a cada vertice, entonces, será necesario implementar la fórmula de la distancia aérea dentro de dicho método. En otras palabras, para ajustar el cálculo heurístico y considerar las distancias diagonales de manera precisa, se debe incorporar la fórmula que calcula la distancia aérea en la lógica del método correspondiente. 
    
6. ¿Realiza este método reevaluación de nudos cuando se encuentra una
nueva ruta a un determinado vértice?

    ```
    private List<Graph.Edge<T>> reconstructPath(Map<Graph.Vertex<T>,Graph.Vertex<T>> cameFrom, Graph.Vertex<T> current)
    ```
   Sí, este método realiza una reevaluación. Para explicarlo de manera más detallada, recibe un mapa que contiene nodos, y a partir del nodo objetivo llamado 'current', procede a reconstruir el camino. La reconstrucción del camino implica una reevaluación minuciosa del mismo, y si logra identificar una ruta más óptima, se realizará la actualización correspondiente. 
