# Tablas de Verdad

## Que son y para que sirven las Tablas de Verdad?

Una **tabla de verdad** es una herramienta que se utiliza para **analizar expresiones lógicas** y **determinar sus posibles resultados** (Verdadero o Falso) según los valores de entrada.

Se usa principalmente en **lógica booleana**, **programación** y **algoritmos de decisión**.

### Valores lógicos básicos

- **Verdadero (V)** → Representa una condición que se cumple.
- **Falso (F)** → Representa una condición que no se cumple.

### Operadores lógicos más comunes

| Operador | Nombre | Símbolo alternativo | Descripción |
|-----------|----------|---------------------|--------------|
| `Y` | Conjunción | `AND` | Es Verdadero solo si **ambas condiciones** son verdaderas. |
| `O` | Disyunción | `OR` | Es Verdadero si **al menos una condición** es verdadera. |
| `NO` | Negación | `NOT` | Invierte el valor lógico (de V a F o de F a V). |

---

### Tabla de verdad del operador **Y (AND):**

| A | B | A Y B |
|---|---|--------|
| V | V | V |
| V | F | F |
| F | V | F |
| F | F | F |

>*Solo es Verdadero cuando ambas condiciones son Verdaderas.*

---

### Tabla de verdad del operador **O (OR):**

| A | B | A O B |
|---|---|--------|
| V | V | V |
| V | F | V |
| F | V | V |
| F | F | F |

>*Es Verdadero si al menos una de las condiciones es Verdadera.*

---

### Tabla de verdad del operador **NO (NOT):**

| A | NO A |
|---|------|
| V | F |
| F | V |

>*Invierte el valor lógico.*

---
