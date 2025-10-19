# 🚀 Empezando con GitHub

## **Ramas y como usarlas**

Las ramas en Git son una característica fundamental que now permite desarrollar diferentes versiones de un proyecto de una forma aislada y mantener un historial de los cambios. Es como una línea paralela de trabajo que parte de un punto específico en el historial del repositorio.

Cuando creas una rama nueva, estás copiando el **estado actual del proyecto** (normalmente desde la rama principal, llamada main o master) para trabajar en cambios **sin afectar directamente** al código principal. Esto es especialmente útil para desarrollar nuevas funcionalidades, corregir errores, experimentar con ideas o trabajar en equipo sin interferir con el trabajo de los demás.

**Por ejemplo:** si estás trabajando en una nueva función para una aplicación o pagina web, puedes crear una rama llamada nueva-funcion, hacer todos los cambios ahí, y luego, cuando esté lista y probada, unirla con la rama principal.

**En resumen:** las ramas sirven para:

- Aislar cambios del resto del proyecto
- Facilitar el trabajo en equipo
- Probar nuevas ideas sin riesgos
- Organizar mejor el desarrollo (por ejemplo, ramas para cada tarea, error o versión)

---

### **Creando ramas en la terminal**

Para crear una **nueva rama** ademas de la principal comunmente llamada: `main` o `master` lo podemos hacer desde la terminal con `branch` y con `checkout`:

> Recuerda que lo siguiente va a ser en la terminal puedes habrir una nueva con ``Ctrl + Shift + ` `` o  con `Ctrl + Shift + ñ` o en la pestaña `terminal` en la parte superior

1. Creandola y pasando directamente a la rama con `checkout`:

    ```bash
    git checkout -b <nombre-de-la-nueva-rama>
    ```

    esto va a tratar de cambiar a la rama `nombre-de-la-nueva-rama` y si no existe la va a crear **Y** va a cambiar a esa rama

    > `nombre-de-la-nueva-rama` se cambia por el nombre que deses usar!

2. Creandola **sin** cambiar directamente a la nueva rama con `branch`:

    ```bash
    git branch <nombre-de-la-nueva-rama>
    ```

    con esto vamos a crear la **nueva rama** sin cambiar a la misma, si queremos cambiar a esa rama usamos `checkout`para hacer el cambio:

    ```bash
    git checkout <nombre-de-la-nueva-rama>
    ```

asi podemos crear nuevas ramas **apartir de la principal** sin embargo de vez en cuando vamos a necesitar crear una nueva rama de una rama existente esto lo podemos hacer con `checkout` de la siguiente forma: 

1. Creando y pasando directamente a la rama con `checkout`:

    ```bash
    git checkout -b <nombre-de-la-nueva-rama> <nombre-de-la-rama-existente>
    ```

    esto va a tratar de cambiar a la rama `nombre-de-la-nueva-rama` que esta alojada en `nombre-de-la-rama-existente` y si no existe la va a crear **Y** va a cambiar a esa rama.

    