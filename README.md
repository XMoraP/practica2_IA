# Practica 2 Inteligencia Aritificial - Busqueda Heuristica

## Respuestas: 

1. ¿Qué variable representa la lista ABIERTA?
    
    La variable que representa la lista Abierta es 'openSet', puesto que es una estructura de datos que contiene una serie de nodos que deben ser evaluados.

2. ¿Qué variable representa la función g?

    Esta representada por la variable gScore, puesto que es una estructura de datos (tipo map)  que recibe el nodo de inicio y el costo hasta el nodo n. 
    
    gScore.put(start, 0); ---> En este fragmento de código, start es el nodo inicial y como esta en ese nodo en un principio tiene coste 0.

3. ¿Qué variable representa la función f?

    Esta representada por la variable fScore, ya que es una estructura de datos que recibe el nodo inicial (g(n)) y la heuristica estimada (h(n)).
    
     fScore.put(start, heuristicCostEstimate(start,goal)); ---> En este fragmento de código, start representa el nodo inicial y el metodo heuristicCostEstimate( ) la heuristica estimada.
     
4. ¿Qué método habría que modificar para que la heurística representara
la distancia aérea entre vértices?

    Habría que modificar el método heuristicCostEstimate( ), ya que por defecto calcula la heuristica asignandole de coste 1 a cada vertica, entonces, habria implementar la fórmula de la distancia aérea dentro de dicho método.
    
5. ¿Realiza este método reevaluación de nudos cuando se encuentra una
nueva ruta a un determinado vértice?
