## Clases Inmutables en Java

### ¿Qué es una clase inmutable?

Una clase inmutable en Java es aquella cuyo estado no puede ser modificado después de su creación. Una vez que se instancia un objeto de una clase inmutable, sus atributos permanecen constantes a lo largo de su ciclo de vida.

### Características de una clase inmutable:

* **Atributos finales:** Todos los atributos de la clase deben ser declarados como `final` para garantizar que no puedan ser modificados después de la inicialización.
* **Constructor único:** La clase debe tener un constructor que inicialice todos los atributos.
* **Sin métodos modificadores:** No debe haber métodos que modifiquen el estado interno del objeto.
* **Copia defensiva:** Si la clase contiene referencias a objetos mutables, se deben crear copias defensivas de estos objetos al pasarlos a otros métodos o devolverlos como resultado.
* **Clase declarada como final:** Opcionalmente, se puede declarar la clase como `final` para evitar que sea extendida y así garantizar que su inmutabilidad se mantenga en todas las subclases.

### Ejemplo de una clase inmutable:

```java
public final class Persona {
    private final String nombre;
    private final int edad;

    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }

    // Getters, pero sin setters
    public String getNombre() {
        return nombre;
    }

    public int getEdad() {
        return edad;
    }
}
