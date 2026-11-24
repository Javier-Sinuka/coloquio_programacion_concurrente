# 📚 Programación Concurrente – Preguntero para el Coloquio

![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Disponible-brightgreen)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## 🌐 Acceso a la página

**[Acceder al Preguntero Interactivo](https://javier-sinuka.github.io/coloquio_programacion_concurrente/)**

No requiere instalación, registro ni descarga de archivos.
Se puede acceder directamente desde cualquier navegador.

## 📖 Acerca del proyecto

Este repositorio contiene una guía de estudio interactiva
orientada a la preparación del coloquio de la asignatura
Programación Concurrente.

El objetivo es facilitar el estudio y la comprensión de los
conceptos abordados durante el cursado, mediante una recopilación
organizada de preguntas y respuestas, complementadas con
explicaciones, ejemplos prácticos, diagramas y simulaciones
interactivas.

La guía respeta el orden del preguntero original y amplía sus
respuestas para favorecer la comprensión de los conceptos,
en lugar de su simple memorización.

## 📑 Contenido académico

Entre los principales temas abordados se encuentran:

### Fundamentos de concurrencia

- Operaciones atómicas.
- Interleaving.
- Secciones críticas y exclusión mutua.
- Condiciones de carrera.
- Verificación de programas concurrentes.
- Sistemas reactivos.
- Arquitecturas dirigidas por eventos (EDA).

### Procesos, hilos y sincronización

- Concurrencia y paralelismo.
- Procesos e hilos de ejecución.
- Estados de los hilos.
- Semáforos y locks.
- Mecanismos de sincronización en Java.
- CountDownLatch y CyclicBarrier.
- Fairness, FIFO y ownership.
- Problemas asociados a la ejecución concurrente.

### Lenguajes, gramáticas y autómatas

- Lenguajes formales.
- Alfabetos, símbolos y palabras.
- Expresiones regulares.
- Gramáticas formales.
- Jerarquía de Chomsky.
- Autómatas finitos.
- Autómatas de pila.
- Máquinas de Turing.
- Determinismo y no determinismo.

### Redes de Petri (RdP)

- Fundamentos y componentes de una red.
- Marcado y sensibilización de transiciones.
- Clasificación de las redes de Petri.
- Concurrencia, sincronización y conflictos.
- Sifones, trampas y sumideros.
- Matrices de incidencia.
- Ecuación de estado.
- Grafos de alcanzabilidad.
- Invariantes.
- Seguridad, acotación y vivacidad.
- Análisis de bloqueos (deadlocks).

## ⚙️ Funcionalidades

| Funcionalidad | Descripción |
|---|---|
| Preguntas desplegables | Permite consultar cada respuesta individualmente. |
| Buscador integrado | Facilita la búsqueda de preguntas y conceptos específicos. |
| Índice temático | Permite navegar entre los diferentes bloques de contenido. |
| Seguimiento del progreso | Permite marcar las preguntas que ya fueron estudiadas. |
| Almacenamiento local | Conserva el progreso al cerrar o recargar la página. |
| Filtro de pendientes | Muestra únicamente las preguntas aún no estudiadas. |
| Expandir todas | Permite visualizar simultáneamente las respuestas. |
| Ejemplos visuales | Facilita la comprensión mediante diagramas y esquemas. |
| Simuladores interactivos | Permite experimentar con modelos de redes de Petri. |
| Modo claro y oscuro | Permite adaptar la interfaz a las preferencias del usuario. |
| Exportación a PDF | Permite imprimir o guardar el material de estudio. |
| Diseño responsive | Compatible con computadoras y dispositivos móviles. |

## 🕸️ Simulación interactiva de Redes de Petri

La plataforma incorpora tres simuladores de redes de Petri,
pensados para complementar el estudio teórico con la
experimentación práctica.

Estos permiten:

- Visualizar plazas, transiciones, arcos y tokens.
- Identificar las transiciones sensibilizadas.
- Ejecutar disparos de forma interactiva.
- Observar la evolución del marcado.
- Consultar las secuencias de disparos.
- Reiniciar los modelos a su estado inicial.
- Analizar situaciones de bloqueo.
- Relacionar el comportamiento de las redes con sus
  propiedades matemáticas y estructurales.

La finalidad de estos simuladores es facilitar la comprensión
del funcionamiento de las redes de Petri y de los mecanismos
de sincronización presentes en sistemas concurrentes.

## 💻 Tecnologías utilizadas

El proyecto fue desarrollado utilizando:

- **HTML5:** estructura y contenido de la plataforma.
- **CSS3:** diseño visual, adaptación a dispositivos y temas.
- **JavaScript:** lógica, filtros, simulaciones e interactividad.
- **SVG:** representación gráfica de diagramas y redes de Petri.
- **LocalStorage:** persistencia del progreso y las preferencias.
- **GitHub Pages:** alojamiento y publicación de la plataforma.

La aplicación funciona íntegramente del lado del cliente,
sin necesidad de un servidor backend ni una base de datos.

## 🚀 Ejecución local

También es posible utilizar la plataforma de manera local,
clonando el repositorio:

    git clone https://github.com/Javier-Sinuka/coloquio_programacion_concurrente.git
    cd coloquio_programacion_concurrente

Una vez descargado, basta con abrir el archivo `index.html`
desde cualquier navegador web.

## 📚 Referencias complementarias

- [Documentación oficial de Java - Semaphore](https://docs.oracle.com/en/java/javase/25/docs/api/java.base/java/util/concurrent/Semaphore.html)
- [Documentación oficial de Java - Thread.State](https://docs.oracle.com/en/java/javase/25/docs/api/java.base/java/lang/Thread.State.html)
- [Documentación oficial de Java - Condition](https://docs.oracle.com/en/java/javase/25/docs/api/java.base/java/util/concurrent/locks/Condition.html)
- [Petri Nets: Properties, Analysis and Applications - Tadao Murata](https://disco.ethz.ch/courses/hs15/des/lectures/murata.pdf)
- [Estudio complementario sobre Redes de Petri](https://arxiv.org/abs/2006.05600)

## 🤝 Contribuciones

Cualquier sugerencia, corrección conceptual o propuesta de
mejora es bienvenida.

En caso de identificar algún error en las respuestas, ejemplos
o simulaciones, se puede abrir una Issue en este repositorio
o realizar una Pull Request con la corrección correspondiente.

## ⚠️ Aclaración importante

**Este material NO constituye un apunte oficial de la cátedra.**

Se trata de una iniciativa estudiantil desarrollada con fines
exclusivamente educativos, cuyo objetivo es complementar el
material proporcionado durante el cursado y facilitar la
preparación del coloquio.

El contenido puede presentar errores, imprecisiones u omisiones,
por lo que se recomienda contrastar las respuestas con el
material oficial de la asignatura y las explicaciones de los
docentes.

---

Desarrollado por estudiantes, para estudiantes. 🎓

¡Éxitos en el coloquio!
