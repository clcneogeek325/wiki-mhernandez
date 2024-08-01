## Diferencia entre @Controller y @RestController en Spring Boot

### ¿Qué hacen?
Ambas anotaciones se utilizan para crear controladores en aplicaciones Spring Boot, pero tienen comportamientos distintos.

* **@Controller:**
    * Se utiliza para crear controladores tradicionales que renderizan vistas HTML.
    * Cuando un método de un controlador anotado con `@Controller` devuelve una cadena, Spring busca una vista con ese nombre para renderizarla al cliente.
    * Necesita de `@ResponseBody` para devolver datos directamente en el cuerpo de la respuesta HTTP (sin renderizar una vista).

* **@RestController:**
    * Es una combinación de `@Controller` y `@ResponseBody`.
    * Se utiliza para crear controladores RESTful que devuelven datos directamente en el cuerpo de la respuesta, como JSON o XML.
    * No es necesario usar `@ResponseBody` en los métodos, ya que se asume de forma implícita.

### Tabla comparativa

| Característica | @Controller | @RestController |
|---|---|---|
| Propósito | Renderizar vistas HTML | Devolver datos directamente |
| Serialización | Requiere `@ResponseBody` | Serializa automáticamente |
| Uso típico | Aplicaciones web tradicionales | API RESTful |

### Ejemplo

```java
// @Controller
@Controller
public class MyController {
    @GetMapping("/hello")
    public String hello() {
        return "hello"; // Busca la vista hello.html
    }
}

// @RestController
@RestController
public class MyRestController {
    @GetMapping("/greeting")
    public Greeting greeting(@RequestParam(value="name", defaultValue="World") String name) {
        return new Greeting(counter.incrementAndGet(), String.format("Hello, %s!", name));
    }
}
