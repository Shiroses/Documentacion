# 🚀 Empezando con GitHub

## **Ramas y cómo usarlas**

Las ramas en Git son una característica fundamental que permite desarrollar diferentes versiones de un proyecto de una forma aislada y mantener un historial de los cambios. Es como una línea paralela de trabajo que parte de un punto específico en el historial del repositorio.

Cuando creas una rama nueva, estás copiando el estado actual del proyecto. Esto te permite trabajar en cambios sin afectar directamente al código principal. Esta práctica es útil para desarrollar nuevas funcionalidades, corregir errores, experimentar o trabajar en equipo sin interferir con el trabajo de los demás.

**Por ejemplo:** si estás trabajando en una nueva función para una aplicación o página web, puedes crear una rama llamada nueva-funcion, hacer todos los cambios ahí y luego, cuando esté lista y probada, unirla con la rama principal.

**En resumen:** las ramas sirven para:

- Aislar cambios del resto del proyecto.  
- Facilitar el trabajo en equipo.  
- Probar nuevas ideas sin riesgos.  
- Organizar mejor el desarrollo (por ejemplo, ramas para cada tarea, error o versión).

---

### **Creando ramas en la terminal**

Para crear una **nueva rama** además de la principal *(comúnmente llamada: `main` o `master`)* lo podemos hacer desde la terminal con `branch` y con `checkout`:

> *Recuerda:*  
> *Vamos a escribir en la terminal; puedes abrir una nueva con* ``Ctrl + Shift + ` `` *o con* `Ctrl + Shift + ñ`, *o en la pestaña* `Terminal` *en la parte superior.*

1. Creando la rama **y cambiando** inmediatamente con `checkout`:

    ```bash
    git checkout -b nombre-de-la-nueva-rama
    ```

    Esto va a crear la rama `nombre-de-la-nueva-rama` **Y** va a cambiar a la misma.

> *Recuerda:*  
> `nombre-de-la-nueva-rama` *se cambia por el nombre que desees usar.*

2. Creando la rama **sin cambiar** inmediatamente a la nueva rama con `branch`:

    ```bash
    git branch nombre-de-la-nueva-rama
    ```

    Con esto vamos a crear la **nueva rama** sin cambiar a la misma. Si queremos cambiar a esa rama usamos `switch` para hacer el cambio:

    ```bash
    git switch nombre-de-la-nueva-rama
    ```

Así podemos crear nuevas ramas **a partir de la principal**. Sin embargo, de vez en cuando vamos a necesitar crear una **nueva rama** de una **rama existente**. Esto lo podemos hacer con `branch` y `checkout` de la siguiente forma:

1. Creando la nueva rama a partir de una existente **y cambiando** inmediatamente con `checkout`:

    ```bash
    git checkout -b nombre-de-la-nueva-rama nombre-de-la-rama-existente
    ```

    Esto va a crear la rama `nombre-de-la-nueva-rama` que tomará el estado más reciente de `nombre-de-la-rama-existente` **Y** va a cambiar a esa rama.

> También podemos crear una rama desde un commit si se necesita con
>
> ```bash
> git checkout -b nombre-de-la-rama hash-del-commit
> ```
>
> El `hash-del-commit` se puede obtener con `git log`.

2. Creando la nueva rama **sin** cambiar directamente con `branch`:

    ```bash
    git branch nombre-de-la-nueva-rama nombre-de-la-rama-existente
    ```

    > Al igual que con `checkout`, podemos crear una rama desde un commit con
    >
    > ```bash
    > git branch nombre-de-la-nueva-rama hash-del-commit
    > ```
    >
    > Con esto creamos la nueva rama en el commit que deseemos, sin cambiar a ella.  
    > Recuerda que el `hash-del-commit` se puede obtener con `git log`.

    Con esto vamos a crear la **nueva rama** sin cambiar a la misma. Si queremos cambiar a esa rama usamos `switch` para hacer el cambio:

    ```bash
    git switch nombre-de-la-nueva-rama
    ```

Y asi de rapido se pueden crear nuevas ramas apartir de ramas o commits ya existentes desde la terminal.

---

### **Creando ramas en VS Code**

Para crear ramas desde VS Code vamos a trabajar desde la página de control de versiones y nos vamos a enfocar en la *`pestaña de gráfica`* y *`cambios`*:

![Inicio VS Code](<../Resources/Git, Github y VS Code/Images/ComVSCodePag1.png>)

- **En el panel de Cambios:**

  - Le damos a los tres puntos.  
  - En el menú seleccionamos `Rama...`.  
  - En el submenú seleccionamos `Crear Rama...`.  
  - En la `toolbar` le ponemos un nuevo nombre y confirmamos.

    <video controls src="../Resources/Git, Github y VS Code/Videos/NRama.mp4" title="Title"></video>

    Así quedaría la pestaña de gráfico. Como podemos ver, cambia de una vez a la nueva rama como si de `git checkout -b` se tratase.

También podemos crearla desde una rama existente:

- **En el panel de Cambios:**

  - En el menú seleccionamos `Rama...`
  - En el submenú seleccionamos `Crear de Rama...`
  - En la `toolbar` seleccionamos la rama de la que vamos a sacar la nueva.  
  - Le ponemos un nuevo nombre y confirmamos.

    <video controls src="../Resources/Git, Github y VS Code/Videos/CRRama.mp4" title="Title"></video>

O incluso desde un commit:

- **En el panel de gráfica:**

  - Seleccionamos el commit y le damos clic derecho.  
  - En el menú seleccionamos `Crear rama...`
  - En la `toolba`

    <video controls src="../Resources/Git, Github y VS Code/Videos/CCRama.mp4" title="Title"></video>

Terminada la creación de rama, vamos a mirar cómo cambiar de ramas en VS Code:

- **En el panel de Cambios:**

  - Le damos a los tres puntos.  
  - En el menú seleccionamos `Checkout a...`
  - En la `toolbar` seleccionamos la rama a la que queremos cambiar.

    <video controls src="../Resources/Git, Github y VS Code/Videos/SRama.mp4" title="Title"></video>

Y así de sencillo podemos crear y cambiar de ramas en VS Code.

---

### **Borrando ramas en la terminal y VS Code**

En esta pequeña sección vamos a revisar las raras ocasiones en las que es necesario eliminar ramas y cómo hacerlo. Esto puede suceder por varias razones:

- La rama ya no se utiliza.  
- Los cambios realizados no convencen o no son lo que se buscaba.  
- Se utilizó la rama para hacer pruebas temporales y no se desea hacer `merge` con una rama oficial.  
- Es una rama antigua que quedó olvidada en el proyecto.  

> Eliminar ramas innecesarias ayuda a mantener el repositorio **limpio** y **organizado**.

⚠️⚠️**TEN EN CUENTA QUE ELIMINAR UNA RAMA NO NECESITA CONFIRMACION. USAR CON PRECAUCION**⚠️⚠️

1. **Borrando desde la terminal**

    > Antes de seguir, recuerda que **NO** debes estar en la rama que vas a eliminar. Puedes revisar en qué rama estás con `git status`.
  
    Para borrar una rama desde la terminal usamos el comando `branch`:

    ```bash
    git branch -d nombre-de-la-rama
    ```

    Esto va a borrar la rama si los cambios se ha hecho `merge` en otra rama. Si quieres forzar el borrado puedes cambiarlo a:

    ```bash
    git branch -D nombre-de-la-rama
    ```

2. **Borrando desde VS Code**

    En VS Code tenemos que hacer lo siguiente:

- **En el panel de gráfica:**

  - Seleccionamos un commit que tenga una rama.

    > Si el commit no tiene rama no se puede eliminar.
  
  - Le damos clic derecho y seleccionamos `Eliminar rama...`
  - Seleccionamos la rama a eliminar para confirmar.

    > No se puede eliminar la rama si estamos en la misma, asegúrate de estar en otra.

    <video controls src="../Resources/Git, Github y VS Code/Videos/DRama.mp4" title="Title"></video>

> En el video no se mostró, pero como la rama no ha hecho `merge` con otra rama, me pidió confirmación; solo deben darle a aceptar.
