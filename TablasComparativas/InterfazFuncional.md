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

### ¿Qué son las funciones lambda?

Las funciones lambda en Java son una forma concisa de representar una interfaz funcional. Son como pequeñas funciones anónimas que puedes definir directamente en el lugar donde las necesitas.

### ¿Qué es una interfaz funcional?

Una interfaz funcional es una interfaz que define exactamente un método abstracto. Sirve como un tipo para las expresiones lambda.

### ¿Por qué usar funciones lambda?

    Código más conciso: Eliminan la necesidad de escribir clases anónimas completas.
    Programación funcional: Permiten adoptar un estilo de programación más funcional.
    Integración con Streams: Se utilizan extensivamente con la API de Streams para realizar operaciones como map, filter, reduce, etc.

### ¿Cómo se usan?

1.  **Definir la interfaz funcional:**
    
    Java
    
    ```
    @FunctionalInterface
    interface MiOperacion {
        int operar(int a, int b);
    }
    ```
    
    Usa el código [con precaución](/faq#coding).
    
2.  **Crear una instancia usando una expresión lambda:**
    
    Java
    
    ```
    MiOperacion suma = (a, b) -> a + b;
    ```
    
    Usa el código [con precaución](/faq#coding).
    
3.  **Crear una instancia usando una referencia a método:**
    
    Java
    
    ```
    MiOperacion resta = Integer::subtract; // Referencia al método subtract de la clase Integer
    ```
    
    Usa el código [con precaución](/faq#coding).
    
4.  **Usar la instancia:**
    
    Java
    
    ```
    int resultadoSuma = suma.operar(3, 5);
    int resultadoResta = resta.operar(10, 4);
    ```
    
    Usa el código [con precaución](/faq#coding).
    

### Ejemplos prácticos con las interfaces funcionales predefinidas:

*   **Predicate:**
    
    Java
    
    ```
    Predicate<Integer> esPar = x -> x % 2 == 0;
    boolean resultado = esPar.test(4); // true
    ```
    
    Usa el código [con precaución](/faq#coding).
    
*   **Function:**
    
    Java
    
    ```
    Function<String, Integer> longitud = String::length;
    int longitudPalabra = longitud.apply("Hola");
    ```
    
    Usa el código [con precaución](/faq#coding).
    
*   **Consumer:**
    
    Java
    
    ```
    Consumer<String> imprimir = System.out::println;
    imprimir.accept("Mensaje");
    ```
    
    Usa el código [con precaución](/faq#coding).
    
*   **Supplier:**
    
    Java
    
    ```
    Supplier<String> saludo = () -> "Hola, mundo!";
    String mensaje = saludo.get();
    ```
    
    Usa el código [con precaución](/faq#coding).
    

### Uso con Streams:

Java

```
List<Integer> numeros = Arrays.asList(1, 2, 3, 4, 5);
List<Integer> cuadrados = numeros.stream()
                                  .map(x -> x * x)
                                  .collect(Collectors.toList());
```

Usa el código [con precaución](/faq#coding).

En este ejemplo, `map` toma una función (una interfaz funcional) para transformar cada elemento del stream.

### Resumen

Las interfaces funcionales son una herramienta poderosa en Java 8 y versiones posteriores. Permiten un estilo de programación más declarativo y funcional. Al entender cómo crear y usar interfaces funcionales, puedes escribir código más conciso y expresivo, especialmente cuando trabajas con colecciones de datos y operaciones de transformación.

**Puntos clave:**

*   **Un solo método abstracto:** Define el contrato de la interfaz.
*   **Expresiones lambda:** Forma concisa de crear instancias de interfaces funcionales.
*   **Referencias a métodos:** Otra forma de crear instancias, referenciando métodos existentes.
*   **Streams:** Se utilizan ampliamente con streams para realizar operaciones como map, filter, reduce.


