### Guía detallada y didáctica de **Git y GitHub**

¡Hola chicos! Ahora que ya tienen una base sólida en HTML, CSS y JavaScript, es momento de aprender a utilizar **Git** y **GitHub**, dos herramientas fundamentales para cualquier desarrollador. Git es un **sistema de control de versiones**, mientras que GitHub es una plataforma en la nube que permite almacenar tus proyectos Git y colaborar con otros desarrolladores. En esta guía les enseñaré cómo usarlos y cómo conectarse a través de **SSH** para trabajar de manera eficiente.

---

## **1. ¿Qué es Git?**

**Git** es un sistema de control de versiones distribuido que te permite llevar un historial de los cambios realizados en tus archivos y proyectos. Con Git puedes:

- **Registrar cambios** en tu código.
- **Volver atrás** en el tiempo si algo sale mal.
- Trabajar en **diferentes versiones** (ramas) de un proyecto sin interferir en el código principal.
- **Colaborar** con otros desarrolladores de manera eficiente.

---

## **2. ¿Qué es GitHub?**

**GitHub** es una plataforma que te permite almacenar tus proyectos Git en la nube y compartirlos con otros. Además, ofrece funcionalidades adicionales como la colaboración en proyectos, seguimiento de errores, y mucho más. Piensa en GitHub como una "nube" para tus repositorios Git.

---

## **3. Instalación de Git**

Antes de comenzar, necesitas tener Git instalado en tu computadora. Aquí te muestro cómo hacerlo dependiendo de tu sistema operativo:

### 3.1. **Windows**
1. Descarga Git desde [https://git-scm.com/](https://git-scm.com/).
2. Sigue el asistente de instalación (deja las opciones predeterminadas).

### 3.2. **Mac**
Abre la terminal y ejecuta el siguiente comando:

```bash
brew install git
```

Si no tienes Homebrew instalado, sigue las instrucciones en [https://brew.sh/](https://brew.sh/).

### 3.3. **Linux**
En la mayoría de las distribuciones de Linux, puedes instalar Git con este comando:

```bash
sudo apt-get install git
```

---

## **4. Configuración inicial de Git**

Después de instalar Git, necesitas configurarlo con tu nombre y correo electrónico (el mismo que usarás en GitHub).

Abre la terminal y ejecuta los siguientes comandos:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@example.com"
```

Esto configurará Git para que registre quién realiza los cambios en tus proyectos.

---

## **5. Conceptos básicos de Git**

Antes de empezar a trabajar, es importante entender algunos conceptos clave de Git.

- **Repositorio**: Es una carpeta que Git está siguiendo. Puede ser local (en tu computadora) o remoto (en GitHub).
- **Commit**: Es un "snapshot" o captura de los cambios que has hecho en los archivos.
- **Rama (branch)**: Es una versión independiente de tu proyecto. La rama principal suele llamarse `main` o `master`.
- **Push**: Enviar tus cambios locales a un repositorio remoto (en GitHub).
- **Pull**: Traer los cambios del repositorio remoto a tu máquina local.
- **Clone**: Descargar un repositorio remoto a tu computadora.

---

## **6. Crear un nuevo repositorio en GitHub**

1. Inicia sesión en [GitHub](https://github.com/).
2. Haz clic en el botón "New" para crear un nuevo repositorio.
3. Asigna un nombre a tu repositorio y selecciona si quieres que sea público o privado.
4. No olvides inicializar el repositorio con un archivo `README` y (opcionalmente) un archivo `.gitignore`.
5. Haz clic en "Create Repository".

Ahora tienes un repositorio vacío en GitHub listo para usarse.

---

## **7. Inicializar un repositorio Git local**

Si tienes una carpeta con un proyecto en tu computadora que quieres gestionar con Git, debes inicializarla como un repositorio:

1. Abre la terminal y navega a la carpeta de tu proyecto.
2. Ejecuta el siguiente comando para inicializar el repositorio:

```bash
git init
```

Esto crea una carpeta oculta `.git` que Git usará para seguir los cambios en tu proyecto.

---

## **8. Conectar un repositorio local con GitHub (SSH)**

Para conectar tu repositorio local con GitHub, puedes usar **SSH** (Secure Shell). SSH es una forma segura de conectar tu computadora con GitHub, sin necesidad de ingresar tu usuario y contraseña cada vez que haces `push` o `pull`.

### 8.1. **Conectar tu repositorio local con GitHub usando SSH**

En tu terminal, usa el siguiente comando para conectar tu repositorio local con el remoto en GitHub:

```bash
git remote add origin git@github.com:tuusuario/tu-repositorio.git
```

Esto crea un alias llamado `origin` que apunta a tu repositorio en GitHub.

---

## **9. Comandos esenciales de Git**

### 9.1. **Verificar el estado de tu repositorio**

Para ver el estado actual de tu repositorio (qué archivos han cambiado, cuáles están listos para commit, etc.), usa:

```bash
git status
```

### 9.2. **Agregar archivos al "stage" (preparar archivos para el commit)**

Para agregar un archivo específico al "stage", usa:

```bash
git add nombre_del_archivo
```

Para agregar todos los archivos que hayan cambiado, usa:

```bash
git add .
```

### 9.3. **Hacer un commit**

Cuando ya tengas archivos listos para ser guardados en el historial, puedes hacer un **commit**. Esto guardará los cambios en tu repositorio local:

```bash
git commit -m "Mensaje descriptivo del cambio"
```

Asegúrate de usar un mensaje claro que explique qué cambios hiciste.

### 9.4. **Enviar los cambios a GitHub (Push)**

Una vez que hayas hecho un commit, puedes enviar tus cambios al repositorio remoto en GitHub con el siguiente comando:

```bash
git push origin main
```

- **`origin`** es el nombre del repositorio remoto.
- **`main`** es el nombre de la rama donde estás trabajando (puede ser `master` si usas esa convención).

### 9.5. **Descargar cambios del repositorio remoto (Pull)**

Si alguien más ha hecho cambios en el repositorio remoto, puedes descargarlos a tu máquina local con:

```bash
git pull origin main
```

Esto traerá los cambios que estén en la rama `main` en GitHub a tu máquina local.

---

## **10. Clonar un repositorio**

Si quieres descargar un repositorio que ya está en GitHub a tu computadora, puedes usar el comando `git clone`.

1. Ve a GitHub, navega al repositorio que deseas clonar, y copia la URL SSH del repositorio.
2. En tu terminal, ejecuta:

```bash
git clone git@github.com:usuario/repo.git
```

Esto descargará el repositorio completo en tu máquina.

---

## **11. Crear y cambiar de rama (Branch)**

Las **ramas** permiten trabajar en diferentes versiones de un proyecto sin afectar la rama principal.

### 11.1. **Crear una nueva rama**

Para crear una nueva rama, usa el siguiente comando:

```bash
git checkout -b nombre_de_rama
```

Esto creará una nueva rama y cambiará a ella.

### 11.2. **Cambiar de rama**

Para cambiar a otra rama, usa:

```bash
git checkout nombre_de_rama
```

### 11.3. **Fusionar una rama (Merge)**

Cuando hayas terminado de trabajar en una rama y quieras fusionar tus cambios con la rama principal (`main`), sigue estos pasos:

1. Cambia a la rama `main`:

   ```bash
   git checkout main
   ```

2. Fusiona la rama con los cambios:

   ```bash
   git merge nombre_de_rama
   ```

---

## **12. Referencias para aprender más**

1. **Pro Git Book (libro gratuito y completo sobre Git)**: [https://git-scm.com/book/en/v2](https

://git-scm.com/book/en/v2)
2. **GitHub Docs**: [https://docs.github.com/](https://docs.github.com/)
3. **Git Cheat Sheet (hoja de trucos)**: [https://education.github.com/git-cheat-sheet-education.pdf](https://education.github.com/git-cheat-sheet-education.pdf)
4. **Try Git (interactivo para aprender Git)**: [https://try.github.io/](https://try.github.io/)
5. **Learn Git Branching (simulador visual para entender las ramas en Git)**: [https://learngitbranching.js.org/](https://learngitbranching.js.org/)
6. **Moure Dev (Canal De YouTube)**: [https://www.youtube.com/@mouredev](https://www.youtube.com/@mouredev)

---

### **Resumen**

1. **Git** es un sistema de control de versiones que te permite llevar un historial de los cambios en tus proyectos.
2. **GitHub** es una plataforma para almacenar y compartir tus repositorios Git en la nube.
3. Usa **SSH** para conectarte de manera segura a GitHub y evitar ingresar tu usuario y contraseña repetidamente.
4. Los comandos esenciales de Git incluyen `git add`, `git commit`, `git push`, `git pull`, y `git clone`.
5. Las **ramas** te permiten trabajar en versiones separadas de tu proyecto, y puedes fusionarlas más tarde.

