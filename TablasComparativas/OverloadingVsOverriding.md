## Sobrecarga (Overloading) vs. Sobreescritura (Overriding) de Métodos

### Sobrecarga de Métodos
* **Definición:** Consiste en definir múltiples métodos con el mismo nombre dentro de una misma clase, pero con diferentes listas de parámetros (diferentes tipos, número o orden de parámetros).
* **Objetivo:** Permitir que un método realice tareas similares con diferentes entradas.
* **Características:**
    * Ocurre dentro de una misma clase.
    * Los métodos sobrecargados tienen el mismo nombre pero diferentes firmas (lista de parámetros).
    * El compilador determina qué método invocar en tiempo de compilación basándose en los argumentos proporcionados.

### Sobreescritura de Métodos
* **Definición:** Ocurre cuando un método en una subclase redefine un método que ya existe en su superclase.
* **Objetivo:** Permitir que una subclase proporcione una implementación más específica o personalizada de un método heredado.
* **Características:**
    * Ocurre entre una clase y su subclase.
    * Los métodos sobreescritos tienen el mismo nombre, los mismos tipos de parámetros y el mismo tipo de retorno.
    * El compilador determina qué método invocar en tiempo de ejecución basándose en el tipo del objeto en el que se invoca el método (polimorfismo).

### Resumen de Diferencias

| Característica | Sobrecarga | Sobreescritura |
|---|---|---|
| Ocurre en | Misma clase | Clase y subclase |
| Nombre del método | Mismo | Mismo |
| Parámetros | Diferentes | Mismos |
| Tipo de retorno | Puede ser diferente | Mismo |
| Resolución | Tiempo de compilación | Tiempo de ejecución |
| Objetivo | Múltiples versiones de un método | Personalización de métodos heredados |

### Ejemplo en Java

```java
class Calculadora {
    public int sumar(int a, int b) {
        return a + b;
    }

    public double sumar(double a, double b) {
        return a + b;
    }
}

class Animal {
    public void hacerSonido() {
        System.out.println("El animal hace un sonido");
    }
}

class Perro extends Animal {
    @Override
    public void hacerSonido() {
        System.out.println("Guau guau");
    }
}
