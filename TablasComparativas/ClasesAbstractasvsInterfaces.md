## Clases Abstractas vs. Interfaces

### Clases Abstractas
* **Definición:** Son clases que no pueden ser instanciadas directamente, es decir, no se pueden crear objetos de ellas. Sirven como base para otras clases, proporcionando una implementación parcial o completa de métodos y atributos.
* **Características:**
    * Pueden contener métodos abstractos (sin implementación) y métodos concretos (con implementación).
    * Pueden tener atributos, tanto abstractos como concretos.
    * Una clase puede heredar de una sola clase abstracta.

### Interfaces
* **Definición:** Son contratos que especifican un conjunto de métodos que una clase debe implementar. No proporcionan ninguna implementación.
* **Características:**
    * Contienen únicamente métodos abstractos (sin implementación).
    * No pueden tener atributos, solo constantes (public static final).
    * Una clase puede implementar múltiples interfaces.

### Resumen de Diferencias

| Característica | Clase Abstracta | Interfaz |
|---|---|---|
| Instanciación | No se puede | No se puede |
| Métodos | Abstractos y concretos | Solo abstractos |
| Atributos | Sí, abstractos y concretos | Solo constantes |
| Herencia simple o múltiple | Simple | Múltiple |
| Implementación | Parcial o completa | Ninguna |

### ¿Cuándo usar cada uno?

* **Clases Abstractas:**
    * Cuando existe una relación "es un" entre clases y se quiere compartir código común.
    * Cuando se necesita una implementación parcial de métodos.
* **Interfaces:**
    * Cuando se quiere definir un contrato que varias clases no relacionadas pueden implementar.
    * Para lograr polimorfismo y desacoplamiento.

### Ejemplo en Java

```java
// Clase abstracta
abstract class Animal {
    public abstract void hacerSonido();
    public void moverse() {
        System.out.println("El animal se mueve");
    }
}

// Interfaz
interface Volador {
    void volar();
}

// Clase concreta que hereda de Animal e implementa Volador
class Pajaro extends Animal implements Volador {
    @Override
    public void hacerSonido() {
        System.out.println("Pío pío");
    }

    @Override
    public void volar() {
        System.out.println("El pájaro vuela");
    }
}
```
