# 🧩 Parametros, Funciones y SubAlgoritmos en Pseudocódigo

## 📘 ¿Qué son los parámetros?

Los **parámetros** son una forma de **pasar valores a una función o subproceso** desde el **algoritmo principal** o desde **otra función**.  

En otras palabras, permiten que una función **reciba valores**, los **use dentro de su propio bloque de código** y, según el **tipo de parámetro**, **pueda o no modificarlos**.

### 🧮 Tipos de Parámetros

En *PSeInt* existen **3 tipos de parámetros**:

---

1. **Parámetros normales:**

    Los parámetros sirven para **pasar valores a una función**, pero **no devuelven ningún valor** directamente.  
    Se usan generalmente en **funciones de retorno**, ya que se desea **usar los valores dentro de la función sin modificarlos**.

2. **Parámetros por Valor:**

    Con este tipo de parámetro podemos **pasar una variable** a una función y **modificarla dentro de la función**,  
    pero **sin afectar su valor fuera de ella**.

3. **Parámetros por Referencia:**

    Este tipo de parámetro permite **modificar directamente el valor** de una variable desde dentro de la función.  
    El cambio **se mantiene fuera de la función**, por lo que es útil cuando se necesita **actualizar valores globales** o **compartidos** entre varias funciones.

## 📘 ¿Qué son las funciones o subprocesos?

Las **funciones** (también llamadas **subalgoritmos** o **subprocesos** en *PSeInt*) son **bloques de código reutilizables** que realizan una tarea específica dentro de un programa.  
En pseudocódigo y en la mayoría de los lenguajes de programación, se usan para **organizar, simplificar y reutilizar** el código.

---

### 🧮 Tipos de Funciones

En *PSeInt* podemos clasificar las funciones en **2 tipos**:

---

1. **SubAlgoritmos:**

    Estas funciones **no deben retornar valores** y se usan principalmente para:

    - **Mostrar información**:

        ```pseudocodigo
        Algoritmo ejemplo

            subalgoritmo_ejemplo //entra en el SubAlgoritmo ejemplo

        FinAlgoritmo

        SubAlgoritmo subalgoritmo_ejemplo //se realizan las operaciones correspodientes

            Imprimir "Este subalgoritmo solo puede imprimir este mensaje"

        FinSubAlgoritmo //sale de el SubAlgoritmo
        ```

        >📘 **Ten en cuenta:** tambien puedes usar un parametro para mostrar una variable!

        ```pseudocodigo
        Algoritmo ejemplo
            Definir n1 Como Entero
            n1 = 4

            subalgoritmo_ejemplo(n1) //entra en el SubAlgoritmo ejemplo

        FinAlgoritmo

        SubAlgoritmo subalgoritmo_ejemplo(n1) //se realizan las operaciones correspodientes

            Imprimir "Este subalgoritmo solo puede imprimir este mensaje y escribir el numero ", n1

            // donde n1 = 4

        FinSubAlgoritmo //sale de el SubAlgoritmo
        ```

    - **Modificar un parametro por referencia:**

        ```pseudocodigo
        Algoritmo ejemplo
            Definir n1 Como Entero
            n1 = 4

            subalgoritmo_ejemplo(n1) //entra en el SubAlgoritmo ejemplo

            //despues de salir de el SubAlgoritmo, el algoritmo se sigue ejecutando desde este punto

            Imprimir n1 //esto va a imprimir el numero 5
        FinAlgoritmo

        SubAlgoritmo subalgoritmo_ejemplo(n1 Por Referencia) //se realizan las operaciones correspodientes

            Imprimir n1 //esto va a imprimir el numero 4
            n1 = n1 + 1
            Imprimir n1 //esto va a imprimir el numero 5

        FinSubAlgoritmo //sale de el SubAlgoritmo

2. **Funciones:**

    Estas funciones **deben retornar valores** y se usan principalmente para:

    - **Hacer operaciones:**

        ```pseudocodigo
        Algoritmo ejemplo
            Definir n1 Como Entero
            n1 = 4

            Imprimir funcion_ejemplo(n1) //entra en la funcion y retorna el resultado

        FinAlgoritmo

        Funcion resultado = funcion_ejemplo(n1) //se realizan las operaciones correspondientes

            resultado = n1 + 1

        FinFuncion //sale de la funcion

**como podemos diferenciar:**  
En los subalgoritmos, primero debemos llamarlos para que realicen su proceso y luego consultar o utilizar la variable donde se almacenó el resultado.
Esto se debe a que el subalgoritmo no devuelve directamente un valor, sino que modifica una variable externa o muestra información en pantalla.

Por otro lado, las funciones pueden llamarse directamente, ya que estas retornan un valor de forma inmediata.
De esta manera, el resultado de la función puede usarse directamente en expresiones, cálculos o asignaciones.

---
