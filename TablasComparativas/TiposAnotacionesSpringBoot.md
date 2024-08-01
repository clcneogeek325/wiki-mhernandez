## Tipos de Anotaciones en Spring Boot

Spring Boot hace un amplio uso de las anotaciones para simplificar la configuración y el desarrollo de aplicaciones. Estas anotaciones proporcionan una forma concisa y declarativa de configurar el comportamiento de la aplicación.

### Anotaciones Clave en Spring Boot

* **@SpringBootApplication:**
  * Combina las anotaciones `@Configuration`, `@EnableAutoConfiguration` y `@ComponentScan`.
  * Se utiliza en la clase principal de una aplicación Spring Boot para iniciar la aplicación.

* **@RestController:**
  * Combina las anotaciones `@Controller` y `@ResponseBody`.
  * Se utiliza para crear controladores REST que devuelven datos directamente en el cuerpo de la respuesta HTTP.

* **@RequestMapping:**
  * Mapea solicitudes HTTP a métodos de controlador.
  * Tiene variantes como `@GetMapping`, `@PostMapping`, `@PutMapping`, `@DeleteMapping`, etc., para métodos HTTP específicos.

* **@Service:**
  * Indica que una clase es un servicio, que normalmente contiene la lógica de negocio de la aplicación.

* **@Repository:**
  * Indica que una clase es un repositorio, que normalmente interactúa con la base de datos.

* **@Component:**
  * Anotación genérica para indicar que una clase es un bean de Spring, que puede ser inyectado en otras clases.

* **@Autowired:**
  * Se utiliza para inyectar dependencias en un bean.

### Otras Anotaciones Comunes
* **@Configuration:** Define una clase de configuración.
* **@EnableAutoConfiguration:** Habilita la autoconfiguración de Spring Boot.
* **@ComponentScan:** Busca componentes, servicios y repositorios en paquetes específicos.
* **@Bean:** Define un bean de Spring.
* **@Value:** Inyecta valores de propiedades en un bean.
* **@Profile:** Activa o desactiva configuraciones basadas en perfiles.

### Resumen de las Anotaciones
Las anotaciones en Spring Boot son una forma concisa y poderosa de configurar y personalizar el comportamiento de una aplicación. Algunas de las anotaciones más comunes incluyen:

* **@SpringBootApplication:** Punto de entrada de la aplicación.
* **@RestController:** Crea controladores REST.
* **@RequestMapping:** Mapea solicitudes HTTP.
* **@Service, @Repository, @Component:** Definen componentes de la aplicación.
* **@Autowired:** Inyecta dependencias.

### Ejemplo
```java
@SpringBootApplication
public class MySpringBootApplication {
    public static void main(String[] args) {
        SpringApplication.run(MySpringBootApplication.class, args);
    }
}

@RestController
public class MyController {

    @Autowired
    private MyService myService;

    @GetMapping("/hello")
    public String hello() {
        return myService.getMessage();
    }
}

@Service
public class MyService {
    public String getMessage() {
        return "Hello, World!";
    }
}
```
