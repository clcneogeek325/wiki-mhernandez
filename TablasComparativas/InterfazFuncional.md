## Interfaces Funcionales en Java

### ¿Qué es una interfaz funcional?

Una **interfaz funcional** en Java es una interfaz que define exactamente un método abstracto. Esta característica la hace especialmente útil para trabajar con expresiones lambda y referencias a métodos, elementos clave de la programación funcional en Java.

### Características principales:

* **Un solo método abstracto:** Esta es la característica definitoria de una interfaz funcional.
* **@FunctionalInterface:** Aunque opcional, se recomienda usar esta anotación para indicar explícitamente que una interfaz está diseñada para ser funcional.
* **Uso con expresiones lambda:** Las interfaces funcionales permiten asignar expresiones lambda a variables de tipo de esa interfaz, lo que simplifica la escritura de código.
* **Referencias a métodos:** También se pueden asignar referencias a métodos a variables de tipo de interfaz funcional.

### Por qué son importantes:

* **Programación funcional:** Las interfaces funcionales son fundamentales para la programación funcional en Java, permitiendo tratar funciones como valores de primera clase.
* **Lambdas y streams:** Son ampliamente utilizadas con las expresiones lambda y los streams de Java 8, facilitando operaciones como map, filter, reduce, etc.
* **Código más conciso:** Las interfaces funcionales permiten escribir código más conciso y expresivo.

### Ejemplos de interfaces funcionales predefinidas en Java:

* **Predicate:** Representa un predicado (una función booleana de un argumento).
* **Function:** Representa una función que acepta un argumento y produce un resultado.
* **Consumer:** Representa una operación que acepta un argumento y no devuelve un resultado.
* **Supplier:** Representa un proveedor de resultados.

### Ejemplo de una interfaz funcional personalizada:

```java
@FunctionalInterface
public interface MiOperacion {
    int operar(int a, int b);
}
