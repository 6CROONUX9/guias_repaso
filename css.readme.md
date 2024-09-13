### Guía detallada y didáctica de **CSS**

¡Hola de nuevo, chicos! Ahora que ya tienen una buena base de HTML, vamos a continuar con **CSS** (**Cascading Style Sheets**), que se utiliza para dar estilo a las páginas web. Así que si quieren hacer que sus páginas web se vean más bonitas con colores, fuentes y diseños atractivos, ¡este es el camino!

---

### **1. ¿Qué es CSS?**

CSS es el lenguaje utilizado para describir la apariencia de un documento HTML. Mientras HTML se enfoca en el contenido y la estructura de la página, CSS se encarga de todo lo visual, como colores, tipografías, márgenes, y posicionamiento de los elementos en la página.

---

### **2. ¿Cómo se usa CSS con HTML?**

CSS se puede usar de **tres maneras principales** en una página web:

1. **CSS en línea (Inline CSS)**: Escribir los estilos directamente dentro de la etiqueta HTML.
2. **CSS interno (Internal CSS)**: Escribir los estilos dentro de la misma página HTML, en la sección `<head>`.
3. **CSS externo (External CSS)**: Colocar los estilos en un archivo separado con extensión `.css` y vincularlo a la página HTML.

### Ejemplos:

#### 2.1. **CSS en línea (Inline CSS)**

Este es el método menos recomendado, pero se usa cuando solo queremos aplicar un estilo específico a un elemento individual.

```html
<p style="color: red;">Este párrafo es rojo gracias al CSS en línea.</p>
```

#### 2.2. **CSS interno (Internal CSS)**

Los estilos se colocan dentro de la etiqueta `<style>` en el `<head>` del documento HTML.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      p {
        color: blue;
        font-size: 18px;
      }
    </style>
  </head>
  <body>
    <p>Este párrafo es azul y tiene un tamaño de fuente de 18px.</p>
  </body>
</html>
```

#### 2.3. **CSS externo (External CSS)**

El método más recomendado es tener los estilos en un archivo CSS separado. Se vincula usando la etiqueta `<link>` en el `<head>` del HTML.

**HTML:**

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <p>Este párrafo será estilizado desde un archivo CSS externo.</p>
  </body>
</html>
```

**Archivo CSS (`styles.css`):**

```css
p {
  color: green;
  font-size: 20px;
}
```

---

### **3. Selectores en CSS**

Los **selectores** en CSS determinan a qué elementos HTML se le aplicarán los estilos. Aquí te explico los más importantes:

#### 3.1. **Selector de elementos**

Selecciona todas las etiquetas de un tipo. Por ejemplo, este código aplicará el mismo estilo a todos los elementos `<h1>` de la página.

```css
h1 {
  color: blue;
  text-align: center;
}
```

#### 3.2. **Selector de clase**

Una clase permite aplicar estilos a elementos específicos usando el atributo `class` en HTML. Las clases se definen en CSS con un punto (`.`) antes del nombre de la clase.

**HTML:**

```html
<p class="importante">Este es un párrafo importante.</p>
<p>Este es un párrafo normal.</p>
```

**CSS:**

```css
.importante {
  color: red;
  font-weight: bold;
}
```

#### 3.3. **Selector de ID**

Un ID es único y se usa para un solo elemento en una página. En HTML, se define con el atributo `id`, y en CSS se usa el símbolo `#` para seleccionarlo.

**HTML:**

```html
<p id="principal">Este es el párrafo principal de la página.</p>
```

**CSS:**

```css
#principal {
  color: blue;
  font-size: 24px;
}
```

#### 3.4. **Selectores combinados**

Puedes combinar selectores para aplicar estilos a elementos específicos dentro de otros.

**HTML:**

```html
<div class="contenedor">
  <p>Este párrafo está dentro de un div con la clase "contenedor".</p>
</div>
```

**CSS:**

```css
.contenedor p {
  color: green;
}
```

Este código cambiará el color del párrafo solo si está dentro de un `<div>` con la clase `contenedor`.

---

### **4. Propiedades básicas de CSS**

CSS tiene muchas propiedades que permiten darle estilo a la página. Vamos a ver algunas de las más importantes:

#### 4.1. **Color del texto**

```css
color: red;
```

#### 4.2. **Tamaño de la fuente**

```css
font-size: 20px;
```

#### 4.3. **Fuente (tipo de letra)**

```css
font-family: Arial, sans-serif;
```

#### 4.4. **Estilo del texto (negrita, cursiva, subrayado)**

- Negrita:

  ```css
  font-weight: bold;
  ```

- Cursiva:

  ```css
  font-style: italic;
  ```

- Subrayado:

  ```css
  text-decoration: underline;
  ```

#### 4.5. **Alineación del texto**

```css
text-align: center;
```

#### 4.6. **Margen y Padding**

El **margen** es el espacio **fuera** de un elemento, y el **padding** es el espacio **dentro** del elemento.

```css
/* Margen de 10px alrededor del elemento */
margin: 10px;

/* Padding de 20px dentro del elemento */
padding: 20px;
```

#### 4.7. **Color de fondo**

```css
background-color: lightblue;
```

#### 4.8. **Bordes**

Puedes agregar bordes a los elementos usando la propiedad `border`.

```css
border: 2px solid black;
```

---

### **5. Modelo de Caja (Box Model)**

Uno de los conceptos más importantes en CSS es el **modelo de caja**, que define cómo se calcula el tamaño de un elemento.

Cada elemento HTML es una caja que tiene:

1. **Contenido**: El área donde va el contenido (texto o imágenes).
2. **Padding**: El espacio dentro de la caja, entre el contenido y el borde.
3. **Borde**: El borde que rodea el contenido y el padding.
4. **Margen**: El espacio fuera de la caja, separando el elemento de otros elementos.

![Modelo de Caja en CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model/boxmodel.png)

**Ejemplo**:

```css
div {
  width: 200px;
  padding: 10px;
  border: 5px solid black;
  margin: 20px;
}
```

---

### **6. Posicionamiento en CSS**

CSS ofrece diferentes maneras de posicionar elementos en la página:

#### 6.1. **Posición estática (Static)**

Es la posición predeterminada. Los elementos siguen el flujo normal del documento.

```css
position: static;
```

#### 6.2. **Posición relativa (Relative)**

El elemento se posiciona **en relación** a su posición original.

```css
position: relative;
top: 20px; /* Mueve el elemento hacia abajo 20px de su posición original */
```

#### 6.3. **Posición absoluta (Absolute)**

El elemento se posiciona **en relación** al elemento contenedor más cercano que tenga `position: relative` o `absolute`.

```css
position: absolute;
top: 50px;
left: 100px;
```

#### 6.4. **Posición fija (Fixed)**

El elemento se mantiene en la misma posición, incluso cuando se hace scroll en la página.

```css
position: fixed;
top: 0;
left: 0;
```

---

### **7. Estructurando una página con CSS**

Aquí les muestro cómo combinar lo aprendido hasta ahora para crear una página básica con HTML y CSS:

**HTML:**

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="styles.css">
    <title>Mi página con CSS</title>
  </head>
  <body>
    <header>
      <h1>Bienvenidos a mi página estilizada con CSS</h1>
    </header>
    <main>
      <section>
        <h2>Sobre mí</h2>
        <p>Soy un estudiante que está aprendiendo HTML y CSS.</p>
      </section>
      <section>
        <h2>Mis hobbies</h2>
        <ul>
          <li>Leer libros</li>
          <li>Jugar videojuegos</li>
          <li>Programar</li>
        </ul>
      </section>
    </main>
    <footer>
      <p>Gracias por visitar mi página.</p>
    </footer>
  </body>
</html>
```

**CSS (archivo `styles.css`):**

```css
/* Estilos globales */
body {
  font

-family: Arial, sans-serif;
  background-color: #f0f0f0;
  margin: 0;
  padding: 0;
}

/* Encabezado */
header {
  background-color: #4CAF50;
  color: white;
  text-align: center;
  padding: 20px;
}

/* Secciones */
section {
  padding: 20px;
  margin: 10px;
  background-color: white;
  border: 1px solid #ccc;
}

/* Lista de hobbies */
ul {
  list-style-type: square;
}

/* Pie de página */
footer {
  text-align: center;
  padding: 10px;
  background-color: #333;
  color: white;
}
```

---

### **8. Referencias para practicar y aprender más**

1. **W3Schools (CSS Tutorial)**: [https://www.w3schools.com/css/](https://www.w3schools.com/css/)
2. **MDN Web Docs (CSS Basics)**: [https://developer.mozilla.org/es/docs/Learn/CSS](https://developer.mozilla.org/es/docs/Learn/CSS)
3. **Codecademy (CSS Course)**: [https://www.codecademy.com/learn/learn-css](https://www.codecademy.com/learn/learn-css)
4. **FreeCodeCamp (Responsive Web Design)**: [https://www.freecodecamp.org/learn/responsive-web-design/](https://www.freecodecamp.org)
- **Soy Dalto**: [https://www.youtube.com/@soydalto](https://www.youtube.com/@soydalto)
  - Canal con tutoriales sencillos para aprender HTML y otros temas de desarrollo web.

---

### **Resumen**

1. **CSS** se usa para dar estilo a una página web.
2. Se puede usar CSS en línea, interno o externo (¡el externo es el mejor método!).
3. Los **selectores** ayudan a aplicar estilos a diferentes elementos HTML.
4. Algunas propiedades básicas son: `color`, `font-size`, `padding`, `margin`, y `border`.
5. El **modelo de caja** es clave para entender cómo se comportan los elementos en CSS.
6. CSS ofrece varias formas de posicionar elementos: estática, relativa, absoluta y fija.