## Excepciones Marcadas y No Marcadas en Java

### Introducción
En Java, las excepciones son eventos que interrumpen el flujo normal de ejecución de un programa. Se clasifican en dos categorías principales: **marcadas** y **no marcadas**. Esta distinción se basa en cómo el compilador de Java maneja estas excepciones.

### Excepciones Marcadas
* **Definición:** Son aquellas excepciones que el compilador obliga al programador a manejar o declarar que pueden ser lanzadas. Esto significa que si un método puede lanzar una excepción marcada, debe declararlo en su firma utilizando la palabra clave `throws`.
* **Características:**
    * Generalmente representan condiciones de error que pueden ser anticipadas y manejadas por el programador.
    * Ejemplos comunes: `IOException`, `SQLException`, `ClassNotFoundException`.
* **Razón de ser:** El compilador fuerza al programador a manejar estas excepciones para garantizar que el programa sea más robusto y evite errores en tiempo de ejecución.

### Excepciones No Marcadas
* **Definición:** Son excepciones que no son obligatorias de manejar o declarar. El compilador no obliga al programador a hacer nada al respecto.
* **Características:**
    * Generalmente representan errores de programación o condiciones inesperadas.
    * Ejemplos comunes: `NullPointerException`, `ArithmeticException`, `ArrayIndexOutOfBoundsException`.
* **Razón de ser:** Estas excepciones suelen indicar errores en el código que deberían ser corregidos en lugar de ser manejados.

### Resumen de las Diferencias

| Característica | Excepciones Marcadas | Excepciones No Marcadas |
|---|---|---|
| Manejo por el compilador | Obligatorio | No obligatorio |
| Declaración en la firma del método | Sí (con `throws`) | No |
| Tipo de error | Generalmente predecible | Generalmente imprevisto |
| Ejemplo | `IOException`, `SQLException` | `NullPointerException`, `ArithmeticException` |

### ¿Por qué esta distinción?
* **Excepciones marcadas:** Permiten al programador anticipar y manejar errores comunes, como problemas de E/S o base de datos, haciendo el código más robusto.
* **Excepciones no marcadas:** Se centran en errores de programación que deberían ser corregidos, como intentar acceder a un índice de arreglo invalido o dividir por cero.

### Mejor Prácticas
* **Manejar las excepciones marcadas:** Siempre que sea posible, intenta manejar las excepciones marcadas para evitar que el programa se detenga inesperadamente.
* **Evitar lanzar excepciones no marcadas:** Intenta corregir los errores que causan excepciones no marcadas en lugar de depender de su manejo.
* **Usar excepciones personalizadas:** Crea excepciones personalizadas para representar errores específicos de tu aplicación.

**En resumen:**

La distinción entre excepciones marcadas y no marcadas ayuda a los programadores a escribir código más seguro y confiable. Al comprender las diferencias y siguiendo las mejores prácticas, puedes construir aplicaciones Java más robustas.
