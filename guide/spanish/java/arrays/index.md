---
title: Arrays
localeTitle: Arrays
---
# Formación

Un Array es una colección de valores (u objetos) de tipos de datos similares (se permiten las formas de tipos de datos primitivas y de referencia) mantenidas en direcciones de memoria secuenciales. Una matriz se utiliza para almacenar una colección de tipos de datos similares. Las matrices siempre comienzan con el índice de 0 y se crean instancias de un número determinado de índices. Todas las variables de la matriz deben ser del mismo tipo, declaradas en la instanciación.

**Sintaxis:**

```java
dataType[] arrayName;   // forma prefereida 
```

Aquí, el `datatype[]` describe que todas las variables indicadas después de que se crearán una instancia como matrices del tipo de datos especificado. Por lo tanto, si queremos crear una instancia de más matrices del tipo de datos similar, solo tenemos que agregarlas después del nombre de `java arrayName` especificado (no olvide separarlas solo con comas). Un ejemplo se da a continuación en la siguiente sección para referencia.

```java
dataType arrayName[];  //  funciona también, pero no es la forma preferida de escritura 
```

Aquí, el `datatype` solo describe que las variables indicadas después de que pertenecen a ese tipo de datos. Además, `[]` después del nombre de la variable describe que la variable es un arreglo del tipo de datos especificado (no solo un solo valor u objeto de ese tipo de datos). Entonces, si queremos instanciar más matrices del tipo de datos similar, agregaremos los nombres de las variables justo después del ya especificado, separados por comas y cada vez tendremos que agregar `[]` después del nombre de la variable, de lo contrario la variable será instanciado como una variable de almacenamiento de valor ordinario (no una matriz). Para una mejor comprensión se da un ejemplo en la siguiente sección.

## Fragmentos de código de la sintaxis anterior:

```java
double[] list1, list2; // forma preferida 
```

El fragmento de código anterior crea una instancia de 2 matrices de nombres de tipo doble list1 y list2.

```java
double list1[], list2; // funciona pero no es la forma preferida 
```

En el fragmento de código anterior, una matriz de tipo doble de nombre list1 y una variable simple de tipo doble nombre list2 (No debe confundirse con el nombre **list2** . Los nombres de variables no tienen nada que ver con el tipo de variable).

Nota: El estilo de escritura `double list[]` no se prefiere, ya que proviene del lenguaje C/C++ y se adoptó en Java para dar cabida a los programadores de C/C++. Además, es más fácil de entender: se puede interpretar que se trata de un "arreglo (array) doble de nombre list" y no "un doble llamado list que es un arreglo (array)"

## Creando Arrays:

```java
dataType[] arrayName = new dataType[arraySize]; //Donde 'arraySize' representa cualquier valor entero mayor o igual a cero
```

## Fragmentos de código de la sintaxis anterior:

```java
double[] List = new double[10]; 
```

## Otra forma de crear un Array:

```java
dataType[] arrayName = {value_0, value_1, ..., value_k}; 
```

## Fragmentos de código de la sintaxis anterior:

```java
double[] lista = {1, 2, 3, 4}; 
 
 El código anterior es equivalente a: 
 double[] list = new double[4]; 
/**NOTA IMPORTANTE: Por favor nota la diferencia entre los tipos de corchetes y llaves que son usados para representar arreglos(arrays) en dos diferentes formas. 
*/
```

## Accediendo a Arrays:

```java
arrayName[index]; // se obtiene el valor en el indice (index) especificado. 
```

## Fragmentos de código de la sintaxis anterior:

```java
System.out.println(list[1]); 
```

Salida:
```
2.0 
```

## Modificación de matrices:

```java
arrayName[index] = value; 
```

Nota: No puedes cambiar el tamaño o el tipo de una matriz después de inicializarla. Nota: Sin embargo, puedes restablecer la matriz como sigue:

```java
arrayName = new dataType[] {value1, value2, value3}; 
```

## Tamaño de las matrices:

Es posible encontrar el número de elementos en una matriz utilizando el "atributo _length_". Debe notarse aquí que `length` es un **atributo** de cada arreglo, es decir, un nombre de variable que almacena la longitud del arreglo. No debe confundirse como un **método** de arreglo, ya que el nombre es el mismo que el método de `length()` correspondiente a la clase _String_.

```java
int[] a = {4, 5, 6, 7, 8}; // declaramos un array 
 System.out.println(a.length); //imprime 5 
```

## Fragmentos de código de la sintaxis anterior:

```java
list[1] = 3; // ahora, si accedemos al arreglo como antes, ahora arrojará 3 en lugar de 2 
```

_Ejemplo de código:_

```java
int[] a = {4, 5, 6, 7, 8}; // declaramos el arreglo 
 for (int i = 0; i < a.length; i++){ // ciclo que pasa por cada índice del arreglo
    System.out.println(a[i]); // imprime el arreglo. 
 } 
```

Salida:

```java
    4 
    5 
    6 
    7 
    8 
```

### Matrices multidimensionales

Las matrices bidimensionales (matrices 2D) se pueden considerar como una tabla con filas y columnas. Aunque esta representación es solo una forma de visualizar la matriz para una mejor resolución de problemas. Los valores se almacenan realmente en direcciones de memoria secuenciales solamente.

```java
int M = 5; 
 int N = 5; 
 double[][] a = new double [M][N]; //M = filas N = columnas 
 for(int i = 0; i < M; i++) { 
    for (int j = 0; j < N; j++) { 
        //Hacer algo aquí, en este índice
    } 
 } 
```

Este bucle ejecutará M ^ N veces y construirá esto:

\[0 | 1 | 2 | 3 | 4\]  
\[0 | 1 | 2 | 3 | 4\]  
\[0 | 1 | 2 | 3 | 4\]  
\[0 | 1 | 2 | 3 | 4\]  
\[0 | 1 | 2 | 3 | 4\]

Del mismo modo también se puede hacer una matriz 3D. Se puede visualizar como un cuboide en lugar de un rectángulo (como arriba), dividido en cubos más pequeños con cada cubo almacenando algún valor. Se puede inicializar a continuación:

```java
int a=2, b=3, c=4; 
 int[][][] a=new int[a][b][c]; //es como un cubo de 2x3x4
```

De manera similar, uno puede tener una serie de tantas dimensiones como desee, pero visualizar una matriz de más de 3 dimensiones es difícil de visualizar.

### Matrices dentadas

Las matrices dentadas son matrices multidimensionales que tienen un número determinado de filas pero un número variable de columnas. Las matrices dentadas se utilizan para conservar el uso de memoria de la matriz. Aquí hay un ejemplo de código:

```java
int[][] array = new int[5][]; //inicializa un arreglo 2D con 5 filas 
 array[0] = new int[1]; //crea 1 columna para la primer fila 
 array[1] = new int[2]; //crea 2 culumnas para la segunda fila 
 array[2] = new int[5]; //crea 5 culumnas para la tercera fila 
 array[3] = new int[5]; //crea 5 culumnas para la cuarta fila 
 array[4] = new int[5]; //crea 5 culumnas para la quinta fila 
```

Salida:

\[0\]  
\[0 | 1\]  
\[0 | 1 | 2 | 3 | 4\]  
\[0 | 1 | 2 | 3 | 4\]  
\[0 | 1 | 2 | 3 | 4\]

#### Más información:

*   Fuente: [Java Arrays](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/arrays.html)
