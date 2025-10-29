# Validaciones y Ciclos

## Estructuras en Programación (Pseudocódigo)

Las **estructuras** en programación son **bloques o formas organizadas de instrucciones** que permiten **controlar el flujo** del programa.  
Sirven para **tomar decisiones**, **repetir acciones** o **organizar datos** de forma lógica.

### Estructuras Secuenciales

Son las más básicas: las instrucciones se ejecutan **una tras otra**, en el **orden en que aparecen**.

```pseudocodigo
Escribir "Ingrese su nombre:"
Leer nombre
Escribir "Hola ", nombre
```

> La estructura secuencial no toma decisiones ni repite acciones.

### Estructuras Condicionales (de decisión)

Permiten tomar decisiones dependiendo de una condición lógica (verdadero o falso).

1. **Simple**

    ```pseudocodigo
    Si edad >= 18 Entonces
        Escribir "Eres mayor de edad."
    FinSi
    ```

2. **Doble**

    ```pseudocodigo
    Si edad >= 18 Entonces
        Escribir "Eres mayor de edad."
    Sino
        Escribir "Eres menor de edad."
    FinSi
    ```

3. **Múltiple (según)**

    ```pseudocodigo
    Segun opcion Hacer
        1: Escribir "Has elegido opción 1"
        2: Escribir "Has elegido opción 2"
        De Otro Modo:
            Escribir "Opción no válida"
    FinSegun
    ```

## Estructuras Repetitivas (ciclos o bucles)

Las **estructuras repetitivas** son aquellas que permiten **ejecutar un bloque de instrucciones varias veces** mientras se cumpla una **condición lógica** o hasta que se alcance un **límite definido**.  
Son útiles para **automatizar tareas repetitivas** sin necesidad de escribir las mismas instrucciones múltiples veces.

1. **Mientras (While)**

    ```pseudocodigo
    Mientras contador <= 10 Hacer
        Escribir contador
        contador = contador + 1
    FinMientras
    ```

    > Repite mientras la condición sea verdadera.

2. **Repetir...Hasta Que (Do...While)**

    ```pseudocodigo
    Repetir
        Escribir contador
        contador = contador + 1
    Hasta Que contador > 10
    ```

    > Se ejecuta al menos una vez, incluso si la condición no se cumple al inicio.

3. **Para (For)**

    ```pseudocodigo
    Para i = 1 Hasta 5 Con Paso 1 Hacer
        Escribir "Número ", i
    FinPara
    ```

    > Repite un número definido de veces.

## Estructuras de Datos (agrupan información)

Las **estructuras de datos** son **formas organizadas de almacenar y gestionar información**  

Estas permiten **guardar varios valores** bajo un mismo nombre, lo que hace más fácil el manejo y procesamiento de grandes cantidades de datos.

1. **Arreglos (Vectores)**

    Un conjunto de datos del mismo tipo, almacenados en una sola variable con posiciones (índices).

    **Ejemplo:**

    ```pseudocodigo
    Definir notas Como Real  

    Dimencionar notas[5]

    Para i = 1 Hasta 5 Hacer
        Escribir "Ingrese la nota ", i, ":"
        Leer notas[i]
    FinPara

    Escribir "Primera nota: ", notas[1]
    Escribir "Segunda nota: ", notas[2]
    Escribir "Tercera nota: ", notas[3]
    Escribir "Cuarta nota: ", notas[4]
    Escribir "Quinta nota: ", notas[5]
    ```

    > Cada posición del arreglo guarda un valor diferente del mismo tipo.

2. **Matrices (Arreglos bidimensionales)**

    Son tablas con filas y columnas, útiles para organizar datos en dos dimensiones.

    **Ejemplo:**

    ```pseudocodigo
    Definir notas Como Real

    Dimencionar notas[3, 4]

    Para i = 1 Hasta 3 Hacer
        Para j = 1 Hasta 4 Hacer
            Escribir "Ingrese nota del estudiante ", i, " en materia ", j, ":"
            Leer notas[i, j]
        FinPara
    FinPara
    ```

    > Una matriz puede representar tablas, planillas o tableros.
