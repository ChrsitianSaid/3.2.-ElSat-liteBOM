# 3.2.-ElSat-liteBOM

# 🛰️ Práctica BOM – Ventanas del navegador

## 📌 Descripción del proyecto

Este proyecto consiste en desarrollar un sistema de interacción entre dos ventanas del navegador mediante JavaScript y el **Browser Object Model (BOM)**.

La aplicación está formada por una ventana principal (`index.html`) y una ventana secundaria o satélite (`satelite.html`), que se comunican entre sí utilizando diferentes propiedades y métodos predefinidos del navegador.

El objetivo es poner en práctica la apertura y posicionamiento de ventanas, la detección del sistema operativo, la manipulación del historial de navegación y el uso de temporizadores.

## 🎯 Objetivos

- Identificar las diferencias entre los objetos del BOM y los objetos nativos de JavaScript.
- Utilizar `window.open()` para abrir ventanas secundarias.
- Calcular dinámicamente la posición de una ventana utilizando las dimensiones disponibles de la pantalla.
- Detectar el sistema operativo mediante `navigator.userAgent`.
- Establecer comunicación entre ventanas utilizando `window.opener`.
- Diferenciar el comportamiento de `location.assign()` y `location.replace()`.
- Implementar temporizadores mediante JavaScript para controlar el cierre automático de una ventana.

## 📁 Estructura del proyecto

```text
3.2.-ElSat-liteBOM/
│
├── index.html
├── satelite.html
├── analisis.md
├── README.md
│
└── css/
    └── styles.css
```

| Archivo | Descripción |
|---|---|
| `index.html` | Ventana principal desde la que se lanza la ventana satélite. |
| `satelite.html` | Ventana secundaria que contiene las funciones de interacción. |
| `analisis.md` | Documento teórico sobre los objetos predefinidos de JavaScript. |
| `css/styles.css` | Hoja de estilos compartida por ambas páginas. |
| `README.md` | Documentación general del proyecto. |

## ⚙️ Funcionalidades implementadas

### 1. Lanzamiento y centrado dinámico

Desde la página principal se puede abrir una ventana secundaria mediante `window.open()`.

La ventana tiene unas dimensiones fijas de **400 × 300 píxeles** y su posición se calcula dinámicamente utilizando:

- `screen.availWidth`: anchura disponible de la pantalla.
- `screen.availHeight`: altura disponible de la pantalla.

El cálculo permite solicitar que la ventana aparezca centrada en el monitor del usuario.

### 2. Detección del sistema operativo

Al cargar `satelite.html`, se consulta la propiedad `navigator.userAgent` para identificar el entorno del usuario.

La aplicación comprueba si la cadena contiene referencias a:

- Windows.
- Mac.
- Linux.

Posteriormente, muestra un mensaje de bienvenida personalizado en la ventana satélite.

### 3. Control del historial de navegación

La ventana secundaria puede modificar la dirección de la ventana principal mediante `window.opener`.

Se han implementado dos comportamientos:

**Redirigir con historial**

Utiliza `window.opener.location.assign()` para navegar a la página web de Ilerna, conservando la posibilidad de regresar a la página anterior mediante el historial.

**Redirigir sin historial**

Utiliza `window.opener.location.replace()` para sustituir la entrada actual del historial, evitando regresar a ella mediante el botón atrás.

### 4. Autodestrucción de la ventana

La ventana satélite incorpora un botón que inicia una cuenta atrás de cinco segundos.

Durante este proceso se muestra el tiempo restante y, al finalizar, se ejecuta `window.close()` para intentar cerrar automáticamente la ventana.

La cuenta atrás utiliza temporizadores de JavaScript.

## 🛠️ Tecnologías utilizadas

| Tecnología | Uso |
|---|---|
| HTML5 | Estructura de las páginas. |
| CSS3 | Diseño visual y adaptación a diferentes pantallas. |
| JavaScript | Lógica de interacción y manipulación del navegador. |
| BOM | Acceso a las propiedades y funcionalidades del navegador. |
| XAMPP | Servidor local para realizar las pruebas. |
| Git y GitHub | Control de versiones y alojamiento del proyecto. |
| GitHub Pages | Despliegue de la aplicación en la nube. |


## 🧪 Comprobaciones realizadas

- Apertura de la ventana satélite.
- Cálculo dinámico de las coordenadas de apertura.
- Comprobación del tamaño de 400 × 300 píxeles.
- Detección del sistema operativo.
- Redirección de la ventana principal conservando el historial.
- Redirección sustituyendo la entrada actual del historial.
- Cuenta atrás de cinco segundos.
- Cierre automático de la ventana secundaria.

**Nota:** Los navegadores pueden aplicar restricciones propias al posicionamiento y cierre de ventanas emergentes. Por ello, el resultado puede variar según el navegador y su configuración.

## 📚 Conceptos principales aprendidos

Durante el desarrollo de esta práctica se han trabajado los siguientes conceptos:

- Browser Object Model (BOM).
- Objeto global `window`.
- Objeto `screen`.
- Objeto `navigator`.
- Propiedad `navigator.userAgent`.
- Método `window.open()`.
- Propiedad `window.opener`.
- Métodos `location.assign()` y `location.replace()`.
- Temporizadores `setTimeout()` y `setInterval()`.
- Método `window.close()`.
