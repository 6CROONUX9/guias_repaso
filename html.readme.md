### Guía detallada y didáctica de **HTML** para principiantes

¡Hola, chicos! En esta guía se les explicara todo lo que necesitan saber sobre HTML (**HyperText Markup Language**). No se preocupen si no saben nada de programación, ¡vamos a explicarlo paso a paso de manera simple!

---

### **1. ¿Qué es HTML?**

HTML es el lenguaje que se usa para crear páginas web. No es un lenguaje de programación, sino un **lenguaje de marcado**, lo que significa que usamos **etiquetas** para organizar el contenido de una página web, como texto, imágenes y enlaces.

---

### **2. Estructura básica de una página HTML**

Toda página web hecha con HTML tiene una estructura básica que debe seguir. Aquí se las muestro y luego la desglosamos:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Mi primera página web</title>
  </head>
  <body>
    <h1>¡Bienvenidos a mi página!</h1>
    <p>Esta es mi primera página web creada con HTML.</p>
  </body>
</html>
```

### Desglose:

1. **`<!DOCTYPE html>`**: Indica al navegador que estamos usando HTML5, la versión más actual de HTML.
  
2. **`<html>`**: Esta etiqueta le dice al navegador que todo lo que está dentro de ella es código HTML.

3. **`<head>`**: Contiene información **sobre la página** que no se muestra directamente, como el título de la pestaña en el navegador.
  
4. **`<title>`**: Define el título de la página, que aparece en la pestaña del navegador. Por ejemplo: "Mi primera página web".

5. **`<body>`**: Todo lo que va dentro de esta etiqueta es lo que veremos en la página web, como texto, imágenes, enlaces, etc.

6. **`<h1>`**: Es una cabecera (o título). El número indica su nivel de importancia. `<h1>` es el más importante y grande, y `<h6>` el más pequeño.

7. **`<p>`**: Representa un **párrafo** de texto.

---

### **3. Las etiquetas más comunes de HTML**

HTML usa muchas etiquetas para organizar el contenido. Aquí les explico algunas de las más importantes.

#### 3.1. **Encabezados o títulos**

Los encabezados sirven para dar títulos o subtítulos a tu página. Van del `<h1>` al `<h6>`.

```html
<h1>Este es el título principal</h1>
<h2>Este es un subtítulo</h2>
<h3>Este es un subtítulo más pequeño</h3>
```

#### 3.2. **Párrafos**

Para agregar texto en tu página, usamos la etiqueta `<p>`.

```html
<p>Este es un párrafo de texto. Puedes escribir todo lo que quieras aquí.</p>
```

#### 3.3. **Imágenes**

Para insertar imágenes, usamos la etiqueta `<img>`. **No necesita etiqueta de cierre**, pero tiene atributos que debemos definir, como `src` (la ubicación de la imagen) y `alt` (una descripción por si la imagen no carga).

```html
<img src="ruta/de/la/imagen.jpg" alt="Descripción de la imagen">
```

Ejemplo:

```html
<img src="gato.jpg" alt="Un lindo gatito">
```

#### 3.4. **Enlaces**

Si quieres agregar un enlace a otra página web, usas la etiqueta `<a>`. Debes especificar el atributo `href`, que contiene la dirección a la que se enlazará.

```html
<a href="https://www.google.com">Ir a Google</a>
```

#### 3.5. **Listas**

Hay dos tipos de listas en HTML:

- **Listas ordenadas** (`<ol>`): Se numeran automáticamente.
- **Listas desordenadas** (`<ul>`): Usan viñetas.

Dentro de estas listas, cada elemento usa la etiqueta `<li>`.

```html
<!-- Lista ordenada -->
<ol>
  <li>Primer elemento</li>
  <li>Segundo elemento</li>
  <li>Tercer elemento</li>
</ol>

<!-- Lista desordenada -->
<ul>
  <li>Elemento 1</li>
  <li>Elemento 2</li>
  <li>Elemento 3</li>
</ul>
```

#### 3.6. **Divisiones (div) y span**

Las etiquetas `<div>` y `<span>` se usan para agrupar partes del contenido.

- **`<div>`**: Se usa para agrupar bloques grandes de contenido (como secciones).
  
- **`<span>`**: Se usa para agrupar fragmentos pequeños de texto o contenido.

Ejemplo de uso de `<div>` y `<span>`:

```html
<div>
  <h2>Título de una sección</h2>
  <p>Este es un párrafo dentro de un div.</p>
</div>

<p>Este es un texto <span style="color: red;">con una palabra en rojo</span>.</p>
```

---

### **4. Atributos en HTML**

Las etiquetas HTML pueden tener **atributos**, que son características adicionales que modifican la funcionalidad o el estilo de las etiquetas. Los atributos van siempre **dentro de la etiqueta** y se escriben de la siguiente forma:

```html
<etiqueta atributo="valor">Contenido</etiqueta>
```

Algunos atributos comunes:

- **`src`**: Se usa para indicar la ubicación de una imagen o archivo multimedia (en etiquetas como `<img>`).
  
- **`href`**: Se usa en la etiqueta `<a>` para indicar la dirección de un enlace.
  
- **`alt`**: Atributo en imágenes para proporcionar una descripción alternativa.

- **`style`**: Se usa para agregar estilos en línea a una etiqueta, como cambiar colores, tamaños, etc. Ejemplo:

```html
<p style="color: blue;">Este es un texto azul.</p>
```

---

### **5. Estructurando una página web completa**

Vamos a juntar todo lo que hemos aprendido hasta ahora para crear una página web simple:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Mi página personal</title>
  </head>
  <body>
    <h1>¡Hola! Soy [Tu Nombre]</h1>
    <p>Bienvenidos a mi primera página web. Estoy aprendiendo HTML y me encanta.</p>

    <h2>Mis pasatiempos</h2>
    <ul>
      <li>Leer libros</li>
      <li>Jugar videojuegos</li>
      <li>Pasear a mi perro</li>
    </ul>

    <h2>Mi foto favorita</h2>
    <img src="mi_foto.jpg" alt="Una foto mía sonriendo">

    <h2>Enlaces útiles</h2>
    <p>Visita mis sitios web favoritos:</p>
    <ul>
      <li><a href="https://www.google.com">Google</a></li>
      <li><a href="https://www.youtube.com">YouTube</a></li>
    </ul>
  </body>
</html>
```

### Explicación del código:

- Tenemos un título que se verá en la pestaña del navegador: **Mi página personal**.
- Dentro del `<body>`, tenemos un **título principal** `<h1>`, un párrafo `<p>`, una **lista de pasatiempos** usando `<ul>` y `<li>`, y una **imagen**.
- También incluimos un par de **enlaces** usando la etiqueta `<a>`.

---

### **6. Buenas prácticas en HTML**

- **Usa etiquetas correctamente**: Cada etiqueta tiene un propósito. Por ejemplo, no uses `<h1>` si lo que quieres es un párrafo, usa `<p>`.
- **Cierra todas las etiquetas**: Algunas etiquetas, como `<img>`, no requieren cierre, pero otras sí, como `<p>`, `<div>`, etc.
- **Organiza tu código**: Deja espacio y usa sangría para que tu código sea más fácil de leer.

---

### **7. Práctica recomendada**

Crea un archivo en tu computadora llamado `mi_pagina.html` y pega el código de la sección "Estructurando una página web completa". Luego, ábrelo en tu navegador. Verás cómo todo lo que escribiste en HTML se convierte en una página web.

---

### **8. Siguientes pasos**

- Investiga más sobre **CSS** para darle estilos y colores a tu página web.
- Prueba agregar videos, mapas, y más a tu página.

Con esto, ya tienen una sólida base para empezar a crear páginas web sencillas. Siéntanse libres de experimentar y modificar el código. ¡El aprendizaje viene de la práctica!

--- 

### Resumen:

1. **HTML** es un lenguaje de marcado para crear páginas web.
2. La estructura básica tiene `<html>`, `<head>` y `<body>`.
3. Usamos etiquetas como `<h1>` a `<h6>`, `<p>`, `<a>`, `<img>`, entre otras, para organizar el contenido.
4. Atributos como `src`, `href` y `style` permiten ajustar el contenido.
5. ¡Prueba creando tu propia página y diviértete!

¡Me alegra que te haya gustado la guía! A continuación, te agrego algunas **referencias** para que tus alumnos puedan practicar, repasar conceptos y aprender HTML de manera didáctica, interactiva y divertida:

---

### **1. W3Schools (HTML Tutorial)**
- **URL**: [https://www.w3schools.com/html/](https://www.w3schools.com/html/)
- **Descripción**: W3Schools es una plataforma excelente para aprender HTML de forma interactiva. Cada tema incluye ejemplos prácticos que los alumnos pueden probar directamente en su navegador usando el editor en línea. Es una de las mejores herramientas para principiantes.
- **Características destacadas**:
  - Ejercicios prácticos interactivos.
  - Explicaciones simples y ejemplos claros.
  - Puedes modificar y ejecutar código en tiempo real.
  
### **2. FreeCodeCamp**
- **URL**: [https://www.freecodecamp.org/espanol/news/tag/html/](https://www.freecodecamp.org/espanol/news/tag/html/)
- **Descripción**: FreeCodeCamp ofrece un curso completo y gratuito sobre HTML y diseño web responsivo. Los alumnos pueden aprender desde lo más básico hasta temas más avanzados, siguiendo un enfoque práctico con desafíos que deben resolver.
- **Características destacadas**:
  - Lecciones progresivas y detalladas.
  - Desafíos prácticos que ayudan a consolidar el conocimiento.
  - Enfocado en el aprendizaje práctico.

### **3. MDN Web Docs (Guía de HTML)**
- **URL**: [https://developer.mozilla.org/es/docs/Learn/HTML](https://developer.mozilla.org/es/docs/Learn/HTML)
- **Descripción**: Mozilla Developer Network (MDN) ofrece una guía completa de HTML. Es ideal para aquellos que deseen profundizar más en los conceptos fundamentales del lenguaje y obtener información detallada. Aunque es un poco más técnica, es un excelente recurso para complementar el aprendizaje.
- **Características destacadas**:
  - Explicaciones detalladas y técnicas.
  - Ejemplos avanzados.
  - Excelente referencia a largo plazo.

### **4. CodePen (Editor en línea para practicar)**
- **URL**: [https://codepen.io/pen/](https://codepen.io/pen/)
- **Descripción**: CodePen es una plataforma donde los alumnos pueden crear proyectos de HTML, CSS y JavaScript en línea. Pueden ver el resultado de su código en tiempo real y explorar proyectos de otros usuarios para inspirarse.
- **Características destacadas**:
  - Ideal para experimentar y practicar HTML.
  - Ver el resultado del código inmediatamente.
  - Explora trabajos de otros para aprender más.

### **5. HTML Dog**
- **URL**: [https://htmldog.com/guides/html/](https://htmldog.com/guides/html/)
- **Descripción**: HTML Dog es una página con tutoriales claros y bien estructurados para aprender HTML desde lo más básico hasta lo avanzado. Está dividida en secciones y permite avanzar a su propio ritmo.
- **Características destacadas**:
  - Explicaciones simples con muchos ejemplos.
  - Ejercicios prácticos para cada sección.
  - Ideal para quienes prefieren leer y practicar a su propio ritmo.

### **8. Codecademy (Curso de Introducción a HTML)**
- **URL**: [https://www.codecademy.com/learn/learn-html](https://www.codecademy.com/learn/learn-html)
- **Descripción**: Codecademy es otra plataforma interactiva de aprendizaje que permite practicar HTML de forma progresiva. Cada lección incluye ejemplos prácticos que los alumnos deben resolver antes de avanzar al siguiente tema.
- **Características destacadas**:
  - Lecciones paso a paso con ejercicios.
  - Sistema de aprendizaje interactivo y seguimiento de progreso.
  - Ideal para principiantes que buscan aprender a través de la práctica.

### **9. Proyectos y desafíos prácticos:**
- **URL**: [https://frontendmentor.io](https://frontendmentor.io)
- **Descripción**: En Frontend Mentor, los alumnos pueden acceder a desafíos prácticos de diseño web utilizando HTML y CSS. Estos desafíos permiten mejorar sus habilidades y ver el progreso con proyectos reales.
- **Características destacadas**:
  - Proyectos reales y desafiantes.
  - Práctica con proyectos visualmente atractivos.
  - Permite ver cómo otros resolvieron el mismo proyecto.

### **10. Tutoriales en YouTube**

YouTube es un excelente recurso para aprender HTML de manera visual. Aquí les dejo un par de canales recomendados:

- **Código Facilito**: [https://www.youtube.com/c/CodigoFacilito](https://www.youtube.com/c/CodigoFacilito)
  - Ofrece tutoriales claros y en español sobre HTML, CSS, y otros lenguajes.
  
- **Fazt Code**: [https://www.youtube.com/c/FaztCode](https://www.youtube.com/c/FaztCode)
  - Canal con tutoriales sencillos para aprender HTML y otros temas de desarrollo web.
- **Soy Dalto**: [https://www.youtube.com/@soydalto](https://www.youtube.com/@soydalto)
  - Canal con tutoriales sencillos para aprender HTML y otros temas de desarrollo web.

---

### **Recomendaciones**:

1. **Practica todos los días**: La clave para aprender HTML (y cualquier lenguaje) es la práctica. Dedica unos minutos al día para escribir código.
   
2. **Explora código de otras personas**: Usa plataformas como CodePen o Frontend Mentor para ver cómo otros resuelven problemas. Así aprenderás nuevas formas de usar etiquetas y organizar el código.

3. **Juega y experimenta**: No tengas miedo de cambiar cosas en tu código. Prueba diferentes combinaciones de etiquetas, estilos y contenido.

4. **Haz pequeños proyectos**: Intenta crear cosas sencillas como una página de presentación personal, una galería de fotos o una lista de tus libros favoritos. Los proyectos prácticos te ayudarán a consolidar los conceptos aprendidos.

Con estas referencias y un poco de dedicación, tus alumnos podrán dominar HTML rápidamente. ¡Les abrirá la puerta al fascinante mundo del desarrollo web!