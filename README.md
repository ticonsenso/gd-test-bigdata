# Evaluación Conocimientos Plataformas Big Data
Este repositorio de GitHub contiene un proyecto diseñado para evaluar las habilidades técnicas en el ciclo de vida de un datawarehouse. Se busca analizar la capacidad para el diseño conceptual y lógico, la construcción de un modelo de datos sencillo, y la implementación de procesos de transformación y carga utilizando una plataforma de procesamiento distribuido como Spark.

## Requisitos
- Docker
- VSCode
- Extensión VSCode Dev Containers
- IDE Base de datos (DBeaver)
- Navegador Web Moderno (Google Chrome, Microsoft Edge, Firefox)

## Proceso levantamiento proyecto
1. Abrir VSCode
2. Instalar extensión Dev Containers
3. Pulsar Ctrl + Shift + P
4. Escoger: "Dev Containers: Clone Repository in Named Container Volume" 
5. Colocar la URL de clonación de proyecto de Github
6. Ingresar nombre del volumen, ejemplo: vsc-prueba

## Inicializar proyecto
Una vez que se haya levantado el dev containers, procedemos a levantar el jupyter con el siguiente comando:

- jupyter lab --allow-root

En consola se mostrara una url para abrir en el navegador, similar a:

- http://localhost:8888/lab?token=020cdb433de383556f61ba0273c4455cf031f98b4fe3f2ac
- http://127.0.0.1:8888/lab?token=020cdb433de383556f61ba0273c4455cf031f98b4fe3f2ac

Validar el puerto en que se abre la imagen, en VSCode en la ventana "PORTS" se puede revisar el puerto que se mapeo a su host local, por lo general, se levanta en el puerto 8888.

## Estructura del proyecto
El proyecto maneja la siguiente estructura:

- **/notebooks:** es aquí donde se desarrollará la evaluación, se crearán los notebooks necesarios, se incluye un notebook de prueba, donde se muestra la conexión a la base de datos postgres, que es la base usada dentro del contenedor para la evaluación. Dentro de este directorio se construirá todas las estructuras necesarias para llegar a la solución explicada en el documento de evaluación.