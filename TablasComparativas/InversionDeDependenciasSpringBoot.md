## Inversión de Dependencia en Spring Boot

### ¿Qué es la Inversión de Dependencia?

La inversión de dependencia (Dependency Inversion Principle, DIP) es uno de los principios SOLID de la programación orientada a objetos. En términos simples, significa que las clases de alto nivel no deben depender de las clases de bajo nivel. Ambas deben depender de abstracciones.

**En Spring Boot, este principio se implementa a través de la inyección de dependencias (DI).**

### ¿Cómo funciona en Spring Boot?

1. **Abstracciones:** Se definen interfaces o clases abstractas que representan las funcionalidades que necesitamos.
2. **Implementaciones:** Se crean clases concretas que implementan estas abstracciones.
3. **Inyección:** Spring Boot se encarga de crear las instancias de las clases y de inyectarlas en las clases que las necesitan, siguiendo las configuraciones que definimos.

**Ejemplo:**

```java
// Interfaz (abstracción)
public interface DataSource {
    void getConnection();
}

// Implementaciones concretas
public class MySQLDataSource implements DataSource {
    // ...
}

public class OracleDataSource implements DataSource {
    // ...
}

// Clase de servicio que depende de la interfaz
public class MyService {
    private final DataSource dataSource;

    @Autowired
    public MyService(DataSource dataSource) {
        this.dataSource = dataSource;
    }

    // ...
}
