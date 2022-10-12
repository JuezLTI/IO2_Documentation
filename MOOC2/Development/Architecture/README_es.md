<p align="right">
  <a href="README.md">[EN]</a>
  <a href="README_es.md">[ES]</a>
  <a href="README_pt.md">[PT]</a>
  <a href="README_tr.md">[TR]</a>
  <a href="README_sv.md">[SV]</a>
</p>

## Arquitectura de JuezLTI

El objetivo de JuezLTI es el de proveer evaluación de ejercicios en un amplio rango de lenguajes utilizados en ciencias de la computación directamente desde un LMS.

Para conseguir este objetivo, JuezLTI utiliza una combinación de características:

1. la interoperabilidad con el LMS facilitada por el _framework_ **TSUGI**.
2. un diseño modular, que permite la incorporación de validadores para nuevos tipos de ejercicios. 
3. un sistema genérico de _feedback_ para ayudar a los estudiantes a superar sus dificultades.
4. un repositorio centralizado desde donde se pueden importar y exportar ejercicios.

![Componentes de JuezLTI](JuezLTI_Components.svg)

La arquitectura de JuezLTI se describe según el diagrama de componentes UML anterior.

En el centro de esta arquitectura, encontramos **CodeTest**, es el componente principal desarrollado como un módulo de TSUGI, el _framework_ que provee el soporte LTI. A su vez, CodetTest está compuesto por **TeacherView** y **StudentView**. 

El primero es un entorno web utilizado por los docentes para configurar las actividades, añadiendo ejercicios desde el repositorio central.

El segundo es el entorno web en el que los estudiantes intentan resolver los ejercicios propuestos.

Este componete basado en _TSUGI_ confía en varios tipos de componentes descritos en la parte superior del diagrama.

De derecha a izquierda, encontramos: **Authorkit**, **Repositorio Centralizado**, los **Validadores** y el **Sistema de Feedback**.

_AuthorKit_ es un sistema de creación de ejercicios que puede ser usado por los docentes para crear ejercicios de JuezLTI.

El repositorio centralizado actúa como un contenedor de ejercicios para el sistema.

Los validadores son los componentes que ejecutan el código enviado por el estudiante y califica el resultado.

Por último, el sistema de _feedback_ provee información relacionada con el resultado de la resolución del ejercicio.

JuezLTI es un proyecto de **código abierto** distribuido bajo una licencia Apache 2.0.

Puede ser instalado en los servidores de cualquier institución educativa y configurada para comunicar con el Systema de Gestión del Aprendizaje (LMS) de la institución.

Está disponible en GitHub en dos formas diferentes: producción y desarrollo.

El primero permite el desarrollo del sistema completo, con varios componentes docker en un servidor de producción accesible desde Internet.

Con el segundo, cualquiera puede desplegar la plataforma localmente y contribuir al desarrollo de JuezLTI.
