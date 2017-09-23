# Librería Arduino Median Filter
La librería median Filter implementa un filtro de mediana móvil. La librería almacena los N últimos elementos de la ventana y calcula la mediana. La clase emplea templates para permitir funcionar con distintos tipos (int, long, float,…). <br />
Más información https://www.luisllamas.es/libreria-arduino-median-filter/

## Instrucciones de uso
La clase median Filter sigue el algoritmo propuesto por Phil Ekstrom para el cálculo rápido del filtro mediana. Emplea un buffer circular para almacenar los valores por antigüedad junto con una linkedlist para mantener el orden de los elementos. <br />
La clase median Filter emplea una excepción en el caso de que el tamaño de la ventana sea igual a 3, empleando una implementación directa para mejorar la eficiencia. Para tamaño de ventana distinto de 3 se emplea el algoritmo genérico.

### Constructor
El filtro de mediana móvil se instancia a través de su constructor que recibe el tamaño de la ventana como único parámetro.
```c++
medianFilter<T> medianFilter(windowSize);
```

### Uso del filtro
```c++
// Añadir un nuevo valor al filtro y devolver el valor filtrado
medianFilter.AddValue(value);
 
//Obtiene el ultimo valor filtrado (el mismo que el devuelto al añadir el valor al filtro)
medianFilter.GetFiltered();
```


## Ejemplos
La librería Median Filter incluye los siguientes ejemplos para ilustrar su uso.
* MedianFilterInt: Ejemplo de filtrado para variables integer.
* MedianFilterInt: Ejemplo de filtrado para variables integer.
