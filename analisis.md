1. El objeto window se considera el objeto global del entorno del navegador (BOM). Explica la diferencia entre este y un objeto nativo global del lenguaje JavaScript como Math o JSON. ¿Por qué no hace falta escribir window.Math?

    R/: El objeto window representa el entorno de ejecución (el navegador), mientras que objetos como Math o JSON son objetos nativos estándar del lenguaje JavaScript, independientes de dónde se ejecute el código.

    No hace falta escribir window.Math porque window actúa como el contenedor global en el navegador; cualquier propiedad o método de window (incluidos los objetos nativos del lenguaje) se puede invocar directamente sin especificar su procedencia.

2. Identifica a qué categoría (BOM u objeto nativo de JS) pertenecen las siguientes instrucciones que utilizaremos en la práctica:

window.open(): Pertenece al BOM. El objeto window representa la ventana del navegador y proporciona métodos para controlar la interfaz del  navegador, como abrir una nueva pestaña o ventana.

parseFloat(): Pertenece a los objetos/funciones nativos de JavaScript (aunque en el navegador está disponible en el ámbito global a través de window.parseFloat(), es una función estándar del lenguaje ECMAScript para convertir cadenas en números decimales).

Math.floor(): Pertenece a un objeto nativo de JavaScript. Math es el objeto integrado estándar del lenguaje para realizar operaciones matemáticas, independiente del navegador.

navigator.userAgent: Pertenece al BOM (Browser Object Model). El objeto navigator contiene información sobre el navegador del usuario y el sistema operativo, lo cual es propio del entorno de ejecución de la web.
