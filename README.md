# CODELAB: APROVISIONAMIENTO DE INSTANCIAS DE COMPUTO
![image](https://github.com/user-attachments/assets/7c80964e-47f1-488c-90b8-8ba868b612a6)
___________________________________________________________________________________________
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
