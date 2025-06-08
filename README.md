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

