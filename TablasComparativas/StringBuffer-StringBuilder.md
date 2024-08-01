| Característica               | StringBuffer                      | StringBuilder                     |
|------------------------------|-----------------------------------|-----------------------------------|
| **Mutabilidad**              | Mutable                           | Mutable                           |
| **Hilos (Thread-Safe)**      | Sí (es sincronizado)              | No (no es sincronizado)           |
| **Rendimiento**              | Más lento debido a la sincronización | Más rápido en ausencia de múltiples hilos |
| **Uso**                      | Cuando se necesita seguridad en hilos | Cuando no se necesita seguridad en hilos |
| **Introducción**             | JDK 1.0                           | JDK 1.5                           |
| **API**                      | Parte de `java.lang`              | Parte de `java.lang`              |
| **Aplicación**               | Utilizado en aplicaciones multihilo | Utilizado en aplicaciones de un solo hilo |
