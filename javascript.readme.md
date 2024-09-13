### Guía detallada y didáctica de **JavaScript**

¡Hola de nuevo! Ya hemos cubierto **HTML** para la estructura y **CSS** para el estilo de las páginas web. Ahora es momento de aprender **JavaScript**, el lenguaje que permite agregar **interactividad** y **dinamismo** a las páginas web. ¡Con JavaScript podrás hacer que tus páginas cobren vida!

---

### **1. ¿Qué es JavaScript?**

**JavaScript** (o JS) es un lenguaje de programación que se utiliza para crear interacciones dinámicas en las páginas web. Mientras HTML estructura el contenido y CSS lo estiliza, JavaScript **controla el comportamiento** de la página web, permitiendo hacer cosas como responder a clics, validar formularios, cambiar el contenido sin recargar la página, etc.

---

### **2. ¿Cómo usar JavaScript en HTML?**

JavaScript puede integrarse en una página web de **tres maneras principales**:

1. **JavaScript en línea (Inline JavaScript)**: Colocar el código directamente dentro de las etiquetas HTML.
2. **JavaScript interno (Internal JavaScript)**: Colocar el código dentro de la página HTML, en la sección `<script>`.
3. **JavaScript externo (External JavaScript)**: Colocar el código en un archivo separado con extensión `.js` y vincularlo a la página HTML.

### Ejemplos:

#### 2.1. **JavaScript en línea (Inline JavaScript)**

Este método no se usa mucho, pero permite agregar pequeñas acciones dentro de las etiquetas HTML.

```html
<button onclick="alert('¡Hola, mundo!')">Haz clic aquí</button>
```

#### 2.2. **JavaScript interno (Internal JavaScript)**

El código JavaScript se coloca dentro de la etiqueta `<script>` en el documento HTML, normalmente en la sección `<head>` o al final del `<body>`.

```html
<!DOCTYPE html>
<html>
  <head>
    <script>
      function mostrarAlerta() {
        alert("¡Hola, mundo!");
      }
    </script>
  </head>
  <body>
    <button onclick="mostrarAlerta()">Haz clic aquí</button>
  </body>
</html>
```

#### 2.3. **JavaScript externo (External JavaScript)**

Es el método más recomendado, ya que permite tener el código JavaScript en un archivo separado.

**HTML:**

```html
<!DOCTYPE html>
<html>
  <head>
    <script src="script.js"></script>
  </head>
  <body>
    <button onclick="mostrarAlerta()">Haz clic aquí</button>
  </body>
</html>
```

**Archivo JavaScript (`script.js`):**

```javascript
function mostrarAlerta() {
  alert("¡Hola, mundo!");
}
```

---

### **3. Conceptos básicos de JavaScript**

#### 3.1. **Variables**

Las **variables** son como cajones donde almacenamos datos. Puedes usar `var`, `let` o `const` para declararlas:

```javascript
let nombre = "Juan"; // Declara una variable llamada "nombre"
const edad = 25; // Declara una constante llamada "edad"
var ciudad = "Madrid"; // Viejo estilo, no tan recomendado
```

- **`let`**: Se usa para declarar variables cuyo valor puede cambiar.
- **`const`**: Se usa para declarar variables que no cambian.
- **`var`**: Es la forma más antigua de declarar variables, pero tiene problemas de alcance. No es recomendable en el código moderno.

#### 3.2. **Tipos de datos**

En JavaScript, podemos trabajar con diferentes tipos de datos:

- **Cadenas de texto (Strings)**: Se escriben entre comillas.

  ```javascript
  let saludo = "Hola, mundo";
  ```

- **Números (Numbers)**: Pueden ser enteros o decimales.

  ```javascript
  let edad = 30;
  let precio = 19.99;
  ```

- **Booleanos (Booleans)**: Solo pueden ser `true` o `false`.

  ```javascript
  let esEstudiante = true;
  let tieneLicencia = false;
  ```

#### 3.3. **Operaciones matemáticas**

JavaScript permite hacer operaciones matemáticas básicas.

```javascript
let suma = 5 + 3;       // 8
let resta = 10 - 4;     // 6
let multiplicacion = 6 * 2; // 12
let division = 20 / 5;  // 4
```

#### 3.4. **Concatenar cadenas de texto**

Puedes unir (o concatenar) cadenas de texto con el símbolo `+`.

```javascript
let nombre = "Ana";
let saludo = "Hola, " + nombre + "!";
console.log(saludo); // Muestra "Hola, Ana!" en la consola
```

---

### **4. Funciones en JavaScript**

Las **funciones** son bloques de código que puedes reutilizar. Se definen usando la palabra clave `function`.

```javascript
function saludar() {
  alert("¡Hola, mundo!");
}
```

También puedes pasar **parámetros** a las funciones para que trabajen con diferentes valores.

```javascript
function saludar(nombre) {
  alert("¡Hola, " + nombre + "!");
}

saludar("Juan"); // Muestra "¡Hola, Juan!"
saludar("Ana");  // Muestra "¡Hola, Ana!"
```

---

### **5. Eventos en JavaScript**

Los **eventos** son acciones que suceden en la página web, como un clic, movimiento del ratón, o la carga de la página. JavaScript puede "escuchar" esos eventos y responder a ellos.

#### 5.1. **Eventos de clic**

Puedes agregar eventos de clic a elementos, como botones.

```html
<button id="miBoton">Haz clic aquí</button>

<script>
  document.getElementById("miBoton").onclick = function() {
    alert("¡Hiciste clic en el botón!");
  };
</script>
```

#### 5.2. **Eventos de carga de la página**

```javascript
window.onload = function() {
  console.log("La página se ha cargado completamente.");
};
```

---

### **6. Manipular el DOM (Document Object Model)**

El **DOM** es la estructura de la página web que puedes manipular con JavaScript para cambiar el contenido, los estilos, o agregar elementos.

#### 6.1. **Seleccionar elementos del DOM**

Usa `document.getElementById()` o `document.querySelector()` para seleccionar elementos del HTML.

```html
<p id="miParrafo">Este es un párrafo.</p>

<script>
  let parrafo = document.getElementById("miParrafo");
  console.log(parrafo); // Muestra el párrafo en la consola
</script>
```

#### 6.2. **Cambiar contenido de un elemento**

Puedes cambiar el texto dentro de un elemento usando `.innerHTML` o `.textContent`.

```javascript
document.getElementById("miParrafo").innerHTML = "Este es el nuevo texto.";
```

#### 6.3. **Cambiar estilos de un elemento**

JavaScript permite cambiar el estilo de los elementos.

```javascript
document.getElementById("miParrafo").style.color = "blue";
```

---

### **7. Condicionales en JavaScript**

Los **condicionales** permiten tomar decisiones en el código basadas en condiciones.

#### 7.1. **`if` y `else`**

```javascript
let edad = 18;

if (edad >= 18) {
  console.log("Eres mayor de edad");
} else {
  console.log("Eres menor de edad");
}
```

#### 7.2. **Comparaciones**

Puedes hacer comparaciones usando operadores como `==`, `===`, `>`, `<`, `>=`, `<=`.

- `==` compara si los valores son iguales (sin importar el tipo).
- `===` compara si los valores y tipos son iguales.

```javascript
let numero = 10;

if (numero === 10) {
  console.log("El número es 10");
}
```

---

### **8. Bucles en JavaScript**

Los **bucles** permiten ejecutar un bloque de código varias veces.

#### 8.1. **Bucle `for`**

Un bucle `for` se usa cuando sabes cuántas veces quieres repetir el código.

```javascript
for (let i = 0; i < 5; i++) {
  console.log("El valor de i es: " + i);
}
```

#### 8.2. **Bucle `while`**

Se usa cuando no sabes cuántas veces se repetirá el código, pero quieres que continúe mientras se cumpla una condición.

```javascript
let contador = 0;

while (contador < 3) {
  console.log("Contador: " + contador);
  contador++;
}
```

---

### **9. Crear una página interactiva con JavaScript**

Vamos a combinar lo aprendido para crear una página simple que cambia el texto y color de un párrafo cuando el usuario hace clic en un botón.

**HTML:**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Página interactiva</title>
    <script src="script.js"></script>
  </head>
  <body>
    <h1>Interactividad con JavaScript</h1>
    <p id="texto">Este es un

 texto que cambiará.</p>
    <button onclick="cambiarTexto()">Cambiar texto</button>
  </body>
</html>
```

**JavaScript (`script.js`):**

```javascript
function cambiarTexto() {
  let parrafo = document.getElementById("texto");
  parrafo.innerHTML = "¡El texto ha cambiado!";
  parrafo.style.color = "red";
}
```

---

### **10. Referencias para aprender más y practicar**

1. **W3Schools (JavaScript Tutorial)**: [https://www.w3schools.com/js/](https://www.w3schools.com/js/)
2. **MDN Web Docs (Guía de JavaScript)**: [https://developer.mozilla.org/es/docs/Learn/JavaScript](https://developer.mozilla.org/es/docs/Learn/JavaScript)
3. **Codecademy (JavaScript Course)**: [https://www.codecademy.com/learn/introduction-to-javascript](https://www.codecademy.com/learn/introduction-to-javascript)
4. **FreeCodeCamp**: [https://www.freecodecamp.org](https://www.freecodecamp.org)
- **Soy Dalto**: [https://www.youtube.com/@soydalto](https://www.youtube.com/@soydalto)
  - Canal con tutoriales sencillos para aprender HTML y otros temas de desarrollo web.

---

### **Resumen**

1. **JavaScript** agrega interactividad a las páginas web.
2. Puedes integrar JavaScript en línea, internamente o en archivos externos.
3. Las **variables** almacenan datos, y las **funciones** permiten reutilizar código.
4. Puedes usar **eventos** para responder a acciones del usuario.
5. Manipular el **DOM** permite cambiar el contenido o los estilos de la página.
6. Los **condicionales** y **bucles** permiten tomar decisiones y repetir acciones en el código.