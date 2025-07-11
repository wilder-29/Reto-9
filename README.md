Reto 9
Desarrolle la mayoría de ejercicios en clase. Para cada punto cree un programa individual. Al finalizar suba todo a un repo y subalo al canal reto_9 en slack.
1. Desarrollar un algoritmo que calcule el promedio de un arreglo de reales.

       def calcular_promedio(arreglo):
           if len(arreglo) == 0:
               return 0
           return sum(arreglo) / len(arreglo)
       arreglo = [3.5, 4.0, 5.2, 2.8, 3.9]
       promedio = calcular_promedio(arreglo)
       print(f"El promedio del arreglo {arreglo} es: {promedio}")

2. Desarrollar un algoritmo que calcule el producto punto de dos arreglos de números enteros (reales) de igual tamaño.

       def producto_punto(v1, v2):
           if len(v1) != len(v2):
               raise ValueError("Los arreglos deben tener el mismo tamaño.")
           return sum(v1[i] * v2[i] for i in range(len(v1)))
    
       a = [1, 2, 3]
       b = [4, 5, 6]
       resultado = producto_punto(a, b)
       print(f"El producto punto de {a} y {b} es: {resultado}")

3. Hacer un algoritmo que deje al final de un arreglo de números todos los ceros que aparezcan en dicho arreglo.

       def mover_ceros_al_final(lista):
           sin_ceros = [x for x in lista if x != 0]
           cantidad_ceros = lista.count(0)
           return sin_ceros + [0] * cantidad_ceros

       arreglo = [1, 0, 2, 0, 4, 5, 0, 3]
       resultado = mover_ceros_al_final(arreglo)
       print(f"Arreglo original: {arreglo}")
       print(f"Arreglo modificado: {resultado}")

4. Revisar que son los algoritmos de sorting, entender bubble-sort (enlace a implementación).
Bubble Sort (ordenamiento de burbuja) es un algoritmo de ordenamiento simple pero ineficiente, que funciona intercambiando pares de elementos adyacentes si están en el orden incorrecto.
Se realizan múltiples pasadas (ciclos) sobre el arreglo.
En cada pasada:
- Se compara cada par de elementos adyacentes.
- Si el primero es mayor que el segundo, se intercambian.

Después de cada pasada, el elemento más grande de los no ordenados "sube" (como una burbuja) hasta su posición correcta.
El proceso se repite hasta que en una pasada no se realice ningún intercambio (lo que indica que la lista ya está ordenada).
Ventajas
    Fácil de entender e implementar.
    No requiere memoria adicional (ordenamiento in-place).
    Es estable (conserva el orden de elementos iguales).

Desventajas
    Su complejidad es O(n²) → muy lento para listas grandes.
    Casi no se usa en aplicaciones reales; se usa sobre todo en la enseñanza.
