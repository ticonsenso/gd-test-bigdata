# Evaluación Técnica: Ingeniero de datos y Administrador de Base de Datos
Hemos preparado una evaluación teórica y algunos ejercicios o problemas prácticos del día a día en el mundo del desarrollo, admninistración, integración y BigData. Queremos con esto validar y valorar tus conocimientos e iniciativas para resolverlos.

Se han incluido aspectos de administración de Base de Datos que permiten resolver situaciones de contingencia, performance y recuperación de información sobre las bases de datos. También se consideran escenarios en los que se requiere habilitar nuevos repositorios o ambientes sandbox.

`Importante`: Se evaluará la forma en que el candidato organice sus ficheros, uso de estándares para la creación de estructuras, adecuada gestión de celdas en los notebook y documentación con la explicación del ejercicio. Adicionalmente se tomará en cuenta el enfoque empleado para garantizar la optimización de consultas y el uso eficiente de los recursos de infraestructura, también se dará importancia sobre la arquitectura planteada que permita la recuperación y disponibilidad de los datos en caso de un desastre, y finalmente se valorará la estrategia para dimensionar el crecimiento de recursos.


## Valoración Teórica: Evaluación de conocimientos teóricos
**Descripción:** Responda las siguientes preguntas de acuerdo su criterio tomando en consideración las mejores prácticas y siendo óptimos en cuanto a tiempos, costos y seguridad.

 - **Pregunta 1 - (3pts):** En un escenario donde existen tres ambientes de bases de datos (Desarrollo, Calidad y Producción) con versión Oracle Database 19c y edición DBCS SE cada una ¿Cuál sería su estrategia para realizar una copia de datos entre Producción y Calidad sin infringir licenciamiento, sin generar downtime y en el mejor tiempo posible sabiendo que la base de datos pesa 5TB y tiene 6000 índices? - (3pts)

 - **Pregunta 2 - (3pts):** En un escenario donde existen los siguientes ambientes de base de datos: 

            | Ambiente   | Versión  | Edición  | Features                                                      |
            |------------|----------|----------|---------------------------------------------------------------|
            | Calidad    | 12       | SE       | Ninguno                                                       |
            | Producción | 12       | EE       | In Memory Database, Partitioning, Diagnostic and Tunning Pack |
            
    ¿Cuál sería su estrategia para realizar una copia de datos sin infringir licenciamiento, sin downtime y en el menor tiempo posible? - (3pts)

 - **Pregunta 3 - (2pts):** Una base de datos productiva presenta un tamaño de 8TB en sus tablespaces, se realizan actividades de depuración de tablas y objetos binarios recuperando 4TB, sin embargo al observar el consumo general de la base de la base de datos en sus datafiles la misma no presenta mayor disminución de tamaño. ¿Qué debemos hacer para recuperar los 4TB que fueron depurados de las tablas considerando que el release es Oracle Database 19c sin generar downtime? 

 - **Pregunta 4 - (2pts):** Un desarrollador reporta que eliminó accidentalmente un objeto en la base de datos Oracle productiva luego de solicitar un acceso privilegiado. Este objeto es esencial para que la aplicación funcione correctamente ¿Qué estrategia y actividades aplicaría para recuperar la operación del sistema a un estado normal? 

 - **Pregunta 5 - (4pts):** Usted recibe un incidente en el que se notifica que un servicio web consumido desde un paquete Plsql reporta un error de conexión. El inconveniente se presenta luego de realizar un upgrade base de datos. ¿Qué estrategia adoptaría para resolver el problema con una base de datos Oracle Database? 

 - **Pregunta 6 - (3pts):** Se dispone de un ambiente productivo con una base de datos Primaria y otra en Standby. Sus tnsnames consideran un cambio automático entre las instancias cuando existe un proceso de switchover o failover. Un equipo que se conecta a la base de datos presenta constantes problemas de conexión sin embargo el monitoreo de la base de datos indica un estado saludable. ¿Qué actividades realizaría para llegar a un diagnóstico y solución del problema? 

 - **Pregunta 7 - (3pts):** Se solicita realizar la migración de una base de datos Oracle que pesa 5TB y que opera sobre infraestructura Sparc a un ambiente Cloud. La migración debe involucrar el mínimo downtime y garantizar consistencia en la nueva base de datos migrada.  ¿Qué herramientas pueden usarse para realizar esta actividad? ¿Si la base de datos fuente es una Enterprise Edition y tiene habilitado Partitioning, Transparent Data Encription, In-Memory qué base de datos en Cloud podemos desplegar con el mejor costo? 


## Valoración Práctica: Aplicación práctica de los conocimientos y habilidades en situaciones reales. 

### Ejercicio 1: Diseño arquitectónico de la infraestructura requerida para soportar procesos de analítica en un entorno cloud. (6pts)
**Descripción:** Diseñar una arquitectura que soporte la aplicación inicial y que permita el escalamiento con un enfoque de alta disponibilidad, recuperación y seguridad. Determine el ambiente cloud más eficiente en términos de costo, rendimiento, seguridad y escalabilidad.

**Requisitos:**
- Crear diagrama de arquitectura en Draw.io (1p)
- Arquitectura de Base de Datos empleada (1p)
- Arquitectura de Redes propuesta (1p)
- Estimación de costos de infraestructura (1p)
- Elementos de seguridad propuestos (1p)
- Tiempos requeridos para esalación de recursos (1)

**Entregables:**
Incluir dentro del proyecto:
- Diagrama arquitectónico de la solución.
- Matriz de costos y especificación de recursos requeridos.


### Ejercicio 2: Diseño y construcción de esquema de base de datos. (5pts)
**Descripción:** Diseñar un esquema de base de datos para una aplicación de comercio electrónico para una empresa llamada MP3. Los clientes tendrán acceso a un catálogo de productos, y podrán realizar órdenes de compra con uno o varios artículos (Nombre, descripción y precio), el sistema no posee una pasarela de pago, para realizar el pago se deberá realizar desde cualquier corresponsal con el número de orden de compra.

**Requisitos:**
- Crear diagrama entidad-relación (1p)
- Construir estructuras basado en el diagrama (1p)
- Incluir atributos relevantes como PK, FK, Nombres de clientes, detalle de productos, fecha de orden de compra (1p)
- Incluir datos de personas o productos con tildes, ñ, guión bajo, guión medio. (1p)
- Incluir valores decimales con 5 dígitos. (1p)

**Entregables:**
Incluir dentro del proyecto:
- Diagrama entidad-relación
- Script SQL con los DLL de las estructuras y la insercción de los datos de prueba.


### Ejercicio 3: Diseño y construcción de modelo data warehouse. (5pts)
**Descripción**: Se plantea diseñar un modelo data warehouse sencillo a partir del resultado del ejercicio 1, construido directamente con notebooks jupyter, para ello el modelo debe satisfacer las siguientes necesidades:
- Productos más vendidos
- Clientes con el mayor número de pedidos
- Corresponsal con el mayor número de pedidos
- Total de pagos diario y mensual por productos
- Total de pagos diario y mensual por clientes
- Total de pagos diario y mensual por corresponsal

**Requisitos:**
- Diseñar un modelo de data warehouse de tipo estrella, incluir tablas de hechos y dimensiones que satisfagan los reportes de BI
- Construcción de diagrama data warehouse.

**Entregables:**
Incluir dentro del proyecto:
- Diagrama de data warehouse (1p)
- Notebook Jupyter que realice lo siguiente:
    - Limpieza de datos: (2p)
        - Nombres en mayúsculas, sin tildes, sin ñ, sin guiones bajos y medios.
        - Valores numéricos con solo dos decimales redondeados al inmediato superior.
    - Integración de los datos: (2p)
        - Scripts con la creación de las tablas de dimensiones
        - Scripts con la creación de las tablas de hechos


### Ejercicio 4: Reportes BI (7pts)
**Descripción:** Con la estructura DWH construida en el ejercicio 2, se debe generar los mismos reportes solicitados por el área de negocio.
- Top 10 Productos más vendidos (1p)
- Top 5 Clientes con el mayor número de pedidos (1p)
- Top 5 Corresponsales con el mayor número de pedidos (1p)
- Total de pagos diario y mensual por productos (1p)
- Total de pagos diario y mensual por clientes (1p)
- Total de pagos diario y mensual por corresponsal (1p)
- Variación diaria, mensual de pedidos por productos y corresponsal (1p)

**Entregables:**
- Notebook Jupyter con las consultas, agregaciones y filtros necesarios para presentar el reporte solicitado. 