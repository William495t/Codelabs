# CODELAB: APROVISIONAMIENTO DE INSTANCIAS DE COMPUTO
![image](https://github.com/user-attachments/assets/7c80964e-47f1-488c-90b8-8ba868b612a6)
_____________________________________________________________________________________________________________________________________________________________________________
# CODELAB:  Domain-Driven Design (DDD)
¿Qué es Domain-Driven Design (DDD) y cuál es su objetivo principal?
Es un enfoque para diseñar software centrado en el dominio del negocio. Su objetivo es alinear el modelo de software con el conocimiento experto del dominio.

¿Cuál es la diferencia entre una Entidad y un Objeto de Valor en DDD?
Una Entidad tiene identidad única y persistencia en el tiempo; un Objeto de Valor no tiene identidad y se define solo por sus atributos.

¿Qué es un Bounded Context y por qué es importante en DDD?
Es un límite explícito donde un modelo de dominio aplica con claridad. Es clave para evitar ambigüedades y separar responsabilidades.

¿Cuál es el propósito del Lenguaje Ubicuo (Ubiquitous Language) en DDD?
Unificar el lenguaje entre desarrolladores y expertos del dominio para mejorar comunicación y claridad en el modelo.

¿Qué es un Agregado (Aggregate) y cómo garantiza la consistencia en el dominio?
Es un conjunto de objetos relacionados con una raíz que controla su acceso. Asegura reglas de negocio y consistencia dentro de sus límites.

¿Cómo se relacionan los Repositorios en DDD con la infraestructura de persistencia?
Los Repositorios abstraen el acceso a datos, ocultando detalles de persistencia y permitiendo trabajar con objetos del dominio.

¿Qué son los Eventos de Dominio y cómo mejoran la comunicación entre Bounded Contexts?
Son mensajes que indican algo que ocurrió en el dominio. Facilitan integración y comunicación asíncrona entre contextos.

¿Cómo se diferencian los Servicios de Aplicación y los Servicios de Dominio en DDD?
Los Servicios de Aplicación coordinan casos de uso y orquestan lógica, mientras que los Servicios de Dominio contienen lógica que no pertenece a una entidad específica.

¿Cómo DDD facilita el diseño de software en sistemas complejos y escalables?
Divide el dominio en contextos manejables, enfoca el diseño en reglas de negocio y promueve colaboración efectiva.

¿Cómo se puede combinar DDD con Clean Architecture en una aplicación de microservicios?
Usando DDD para modelar el dominio dentro de cada microservicio y Clean Architecture para estructurarlo en capas, separando dominio, aplicación e infraestructura.
_____________________________________________________________________________________________________________________________________________________________________________
# CODELAB:  Diseño Arquitectonico Attribute-Driven Design (ADD)
¿Cuál es el propósito principal de la metodología ADD en el diseño de arquitecturas de software?
Guiar el diseño arquitectónico basado en los atributos de calidad requeridos, alineando decisiones técnicas con las necesidades del negocio.

¿Qué atributos de calidad se consideran en ADD y por qué son importantes en el proceso de diseño?
Fiabilidad, rendimiento, seguridad, escalabilidad, disponibilidad, entre otros. Son importantes porque determinan cómo debe comportarse el sistema bajo diferentes condiciones.

Explica la importancia de la selección del módulo a diseñar en ADD. ¿Cuáles son los criterios principales para elegir un módulo?
Es clave para enfocar el diseño en lo más crítico. Se elige por prioridad de escenarios de calidad, riesgos técnicos o impacto funcional.

¿Cómo influyen las tácticas arquitectónicas en la toma de decisiones dentro de ADD? Menciona dos ejemplos de tácticas y su aplicación.
Las tácticas guían decisiones que satisfacen atributos de calidad.

- Caching: mejora rendimiento.

- Redundancia: aumenta disponibilidad.

¿Cuál es la relación entre los escenarios de calidad y la evaluación de la arquitectura en ADD?
Los escenarios definen condiciones medibles para evaluar si la arquitectura cumple los atributos de calidad deseados.

Describe los principales pasos del proceso ADD y cómo se interrelacionan.

- Identificar drivers (requisitos, restricciones, atributos).

- Seleccionar módulo a diseñar.

- Elegir patrones/tácticas.

- Refinar módulos en submódulos.

- Evaluar decisiones.

- Repetir con otros módulos.
Cada paso influye en el siguiente y se ajusta según nuevos conocimientos o escenarios.

¿Por qué es crucial documentar las decisiones arquitectónicas en ADD? Menciona al menos tres elementos que deben incluirse en la documentación.
Para asegurar trazabilidad, comunicación y validación. Debe incluir:

- Decisión tomada

- Justificación (escenario y táctica)

- Impacto en otros módulos o atributos

En un proyecto real, ¿cómo se puede evaluar si una arquitectura diseñada con ADD cumple con los atributos de calidad esperados?
Mediante pruebas específicas, revisiones de arquitectura (como ATAM), y validación contra escenarios definidos.

¿Cuáles son los beneficios de utilizar ADD en comparación con otros enfoques de diseño arquitectónico?

- Centrado en necesidades reales del sistema

- Basado en atributos de calidad

- Estructurado y repetible

- Fomenta decisiones justificadas

¿Qué desafíos pueden surgir al aplicar ADD en un equipo de desarrollo y cómo podrían abordarse?

Falta de experiencia en atributos/tácticas: resolver con capacitación

Escenarios mal definidos: mejorar colaboración con stakeholders

Dificultad para documentar decisiones: usar plantillas y herramientas de apoyo
_____________________________________________________________________________________________________________________________________________________________________________
# CODELAB: Clean Architecture

1. **¿Qué problema busca resolver Clean Architecture en el desarrollo de software?**
   Busca desacoplar la lógica de negocio del resto del sistema (frameworks, UI, BD), facilitando cambios, pruebas y mantenimiento.

2. **¿Cuáles son las principales capas de Clean Architecture y qué responsabilidad tiene cada una?**

   * **Entidad (Domain)**: contiene lógica de negocio pura.
   * **Casos de Uso (Application)**: orquesta reglas del negocio según acciones del sistema.
   * **Interfaz (Interface Adapters)**: adapta datos entre capas internas y externas (controllers, presenters).
   * **Infraestructura (Frameworks & Drivers)**: incluye frameworks, bases de datos, servicios externos.

3. **¿Qué relación tiene Clean Architecture con el principio de Inversión de Dependencias (DIP) en SOLID?**
   Se basa en DIP: las capas de alto nivel (dominio) no dependen de las de bajo nivel (infraestructura); la dependencia es invertida mediante interfaces.

4. **¿Por qué es importante desacoplar la lógica de negocio de la infraestructura en una aplicación?**
   Porque permite cambiar tecnologías (como la base de datos) sin afectar la lógica central, y mejora la capacidad de prueba y mantenimiento.

5. **¿Cómo Clean Architecture facilita la escalabilidad y mantenibilidad de un sistema?**
   Al separar responsabilidades, permite escalar partes del sistema sin afectar otras, facilita pruebas unitarias y localiza errores más rápido.

6. **¿Qué diferencia hay entre la capa de dominio y la capa de aplicación en Clean Architecture?**

   * **Dominio**: contiene las **reglas de negocio puras** (entidades, lógica central).
   * **Aplicación**: contiene la **lógica específica de casos de uso**, que usa entidades y coordina acciones.

7. **¿Por qué los controladores (controllers) y la base de datos deben estar en la capa de infraestructura?**
   Porque son detalles técnicos que pueden cambiar. Se mantienen fuera del núcleo para que el dominio permanezca independiente.

8. **¿Qué ventajas tiene usar una interfaz en la capa de dominio para definir repositorios en lugar de usar directamente JpaRepository?**

   * Desacopla del framework (Spring Data)
   * Facilita pruebas con mocks
   * Mantiene la lógica del dominio limpia e independiente

9. **¿Cómo interactúan los casos de uso (UseCases) con las entidades de dominio en Clean Architecture?**
   Los casos de uso orquestan entidades para ejecutar operaciones del sistema. Usan interfaces para acceder a datos y servicios sin acoplarse a la implementación.

10. **¿Cómo se puede aplicar Clean Architecture en una aplicación de microservicios con Spring Boot?**

* Cada microservicio implementa su Clean Architecture de forma independiente.
* Spring Boot se usa en la capa de infraestructura.
* Los `@Service` manejan casos de uso, los `@RestController` están en interfaz, y la lógica de negocio vive en el dominio.
_____________________________________________________________________________________________________________________________________________________________________________
# CODELAB: Proceso con enfoque ADD y Clean Architecture

### 1. **¿Qué es Attribute-Driven Design (ADD) y cuál es su propósito en el diseño de software?**

ADD es una metodología de diseño arquitectónico basada en **atributos de calidad** (como rendimiento, seguridad, disponibilidad). Su propósito es estructurar la arquitectura en función de **requisitos no funcionales** y decisiones justificadas.


### 2. **¿Cómo se relaciona ADD con Clean Architecture en el proceso de diseño de sistemas?**

ADD define **qué** cualidades debe cumplir la arquitectura, y Clean Architecture proporciona un enfoque estructural **para implementar esas decisiones**, separando responsabilidades en capas.


### 3. **¿Cuáles son los pasos principales del método ADD para definir una arquitectura de software?**

1. Identificar drivers del sistema (atributos, restricciones, funcionalidad).
2. Seleccionar el módulo a diseñar.
3. Elegir patrones y tácticas arquitectónicas.
4. Dividir el módulo en submódulos.
5. Documentar decisiones.
6. Repetir para otros módulos.

### 4. **¿Cómo se identifican los atributos de calidad en ADD y por qué son importantes?**

Se identifican a través de **escenarios de calidad** definidos junto a stakeholders. Son claves porque **dirigen las decisiones arquitectónicas** para satisfacer necesidades críticas del negocio.

### 5. **¿Por qué Clean Architecture complementa ADD en la implementación de una solución?**

Porque ADD te dice **qué necesitas lograr** (según los atributos), y Clean Architecture te da **una estructura desacoplada y flexible** para implementarlo de forma sostenible y mantenible.


### 6. **¿Qué criterios se deben considerar al definir las capas en Clean Architecture dentro de un proceso ADD?**

* Separación de responsabilidades.
* Independencia de frameworks y tecnologías.
* Cumplimiento de atributos de calidad (e.g., rendimiento, seguridad).
* Claridad en la dirección de las dependencias (dominio al centro).


### 7. **¿Cómo ADD ayuda a tomar decisiones arquitectónicas basadas en necesidades del negocio?**

Traduciendo requerimientos de negocio en **atributos de calidad medibles** y **tácticas concretas**, ADD permite justificar cada decisión técnica con base en valor y riesgo.


### 8. **¿Cuáles son los beneficios de combinar ADD con Clean Architecture en un sistema basado en microservicios?**

* ADD asegura que cada microservicio se diseña para cumplir atributos clave.
* Clean Architecture proporciona una estructura estándar y desacoplada por servicio.
* Juntas permiten escalabilidad, mantenimiento y evolución independientes.

### 9. **¿Cómo se asegura que la arquitectura resultante cumpla con los atributos de calidad definidos en ADD?**

Mediante:

* Validación de escenarios de calidad.
* Uso de tácticas comprobadas.
* Revisiones arquitectónicas (como ATAM).
* Pruebas no funcionales (performance, carga, seguridad).


### 10. **¿Qué herramientas o metodologías pueden ayudar a validar una arquitectura diseñada con ADD y Clean Architecture?**

* **ATAM** (Architecture Tradeoff Analysis Method)
* **QA scenarios testing**
* **ADR (Architecture Decision Records)**
* Herramientas como **C4 Model**, **Arc42**, y **SonarQube** para validación de diseño y calidad técnica.
_____________________________________________________________________________________________________________________________________________________________________________
# CODELAB: SPRINGBOOT 1

1. **¿Qué es Spring Boot y para qué sirve?**
   Es un framework que simplifica la creación de aplicaciones Java con Spring, eliminando configuraciones complejas y permitiendo ejecutar apps de forma rápida y autónoma.


2. **¿Qué hace la anotación `@SpringBootApplication`?**
   Es una anotación compuesta que habilita:

   * `@Configuration`: define beans.
   * `@EnableAutoConfiguration`: configura automáticamente Spring.
   * `@ComponentScan`: escanea componentes en el paquete base.


3. **¿Cómo se inicia una aplicación Spring Boot?**
   Ejecutando el método `main` con `SpringApplication.run(...)`, que arranca el servidor embebido.


4. **¿Qué función tiene la anotación `@RestController`?**
   Marca una clase como controlador REST, combinando `@Controller` y `@ResponseBody`, para retornar datos (JSON) directamente.

5. **¿Cómo defines una URL en un controlador de Spring Boot?**
   Usando `@RequestMapping`, `@GetMapping`, `@PostMapping`, etc.
   Ejemplo:

   ```java
   @GetMapping("/hola")
   public String saludar() {
       return "Hola Mundo";
   }
   ```

6. **¿Cuál es el puerto por defecto en el que corre Spring Boot?**
   El **puerto 8080**.


7. **¿Cómo cambias el puerto de la aplicación?**
   En el archivo `application.properties`:

   ```properties
   server.port=9090
   ```


8. **¿Qué comando de Maven permite ejecutar una aplicación Spring Boot?**

   ```bash
   mvn spring-boot:run
   ```


9. **¿Cómo puedes probar un endpoint de Spring Boot en el navegador?**
   Inicia la app y visita la URL en el navegador, por ejemplo:
   `http://localhost:8080/hola`


10. **¿Para qué sirve el archivo `application.properties`?**
    Para configurar parámetros de la app: puerto, conexión a base de datos, logs, perfiles, etc.
_____________________________________________________________________________________________________________________________________________________________________________
# CODELAB: SPRINGBOOT 2

**1. ¿Cuál es el propósito de Spring Boot y por qué es útil en el desarrollo de aplicaciones Java?**
Simplifica el desarrollo al eliminar configuraciones manuales, integrando dependencias y permitiendo ejecutar apps rápidamente como servicios standalone.


**2. ¿Cómo se configura una base de datos PostgreSQL en un proyecto Spring Boot usando `application.properties`?**

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/mi_basedatos  
spring.datasource.username=usuario  
spring.datasource.password=contraseña  
spring.jpa.hibernate.ddl-auto=update  
spring.jpa.show-sql=true
```


**3. ¿Qué hace la anotación `@Entity` en la clase `Pais` y por qué es necesaria?**
Indica que la clase es una entidad JPA y se mapeará a una tabla en la base de datos.


**4. ¿Cuál es la función de `JpaRepository` y por qué se usa en la capa de persistencia?**
Proporciona operaciones CRUD predefinidas, evitando código repetitivo y facilitando el acceso a datos.


**5. ¿Cómo se implementa la inyección de dependencias en el servicio `PaisService` y por qué es importante?**
Mediante `@Autowired` o constructor; es importante para desacoplar componentes y facilitar pruebas y mantenimiento.


**6. ¿Cuál es la diferencia entre `@RestController` y `@Service` en Spring Boot?**
`@RestController` expone endpoints HTTP; `@Service` contiene la lógica de negocio reutilizable.


**7. ¿Cómo se define un endpoint en un controlador REST para buscar un país por su nombre?**

```java
@GetMapping("/pais/nombre/{nombre}")
public Pais buscarPorNombre(@PathVariable String nombre) {
    return paisService.buscarPorNombre(nombre);
}
```


**8. ¿Por qué es útil Docker para ejecutar PostgreSQL en lugar de instalarlo manualmente?**
Permite ejecutar PostgreSQL en contenedores aislados, rápido, sin afectar el sistema operativo y fácilmente replicable.


**9. ¿Cómo se ejecuta y prueba la API REST en IntelliJ IDEA?**
Ejecutando la clase principal (`main`) y accediendo a los endpoints con Postman, navegador o curl.


**10. ¿Cómo se maneja la eliminación de un país en el API y qué código de respuesta devuelve el servidor?**
Se usa `@DeleteMapping("/pais/{id}")` y devuelve HTTP **204 No Content** si la eliminación es exitosa.
_____________________________________________________________________________________________________________________________________________________________________________
# CODELAB: Clean Architecture en microservicios Spring Boot

**1. ¿Cuál es el propósito principal de Clean Architecture en el desarrollo de software?**
Separar responsabilidades y desacoplar el dominio del negocio de la infraestructura para lograr sistemas mantenibles, testeables y adaptables al cambio.


**2. ¿Qué beneficios aporta Clean Architecture a un microservicio en Spring Boot?**

* Código más limpio y modular
* Fácil de probar y mantener
* Independencia de frameworks
* Facilidad para escalar y evolucionar el servicio

**3. ¿Cuáles son las principales capas de Clean Architecture y qué responsabilidad tiene cada una?**

* **Entidad/Dominio**: lógica de negocio central
* **Aplicación/UseCases**: coordinación de acciones del sistema
* **Interfaces (adapters)**: entrada/salida (controllers, DTOs)
* **Infraestructura**: frameworks, BD, servicios externos


**4. ¿Por qué se recomienda desacoplar la lógica de negocio de la infraestructura en un microservicio?**
Para permitir cambios tecnológicos sin afectar las reglas de negocio y facilitar pruebas independientes del entorno.


**5. ¿Cuál es el rol de la capa de aplicación y qué tipo de lógica debería contener?**
Coordinar casos de uso concretos del sistema. Debe contener la lógica de flujo y orquestación, no lógica de negocio compleja.


**6. ¿Qué diferencia hay entre un UseCase y un Service en Clean Architecture?**
Un **UseCase** representa una operación del negocio. Un **Service** puede ser un componente técnico o utilitario; los UseCases están enfocados en acciones del sistema.


**7. ¿Por qué se recomienda definir Repositories como interfaces en la capa de dominio en lugar de usar directamente JpaRepository?**
Para desacoplar el dominio de la tecnología de persistencia y facilitar cambios y pruebas unitarias.


**8. ¿Cómo se implementa un UseCase en un microservicio con Spring Boot y qué ventajas tiene?**
Como una clase en la capa de aplicación, inyectando interfaces del dominio. Ventajas: lógica clara, testable y reutilizable.


**9. ¿Qué problemas podrían surgir si no aplicamos Clean Architecture en un proyecto de microservicios?**

* Acoplamiento fuerte a frameworks
* Dificultad para probar y mantener
* Poca flexibilidad para cambios
* Código duplicado y desorganizado


**10. ¿Cómo Clean Architecture facilita la escalabilidad y mantenibilidad en un entorno basado en microservicios?**
Permite modificar, extender o escalar servicios de forma independiente gracias a su estructura modular y separación clara de responsabilidades.
_____________________________________________________________________________________________________________________________________________________________________________



