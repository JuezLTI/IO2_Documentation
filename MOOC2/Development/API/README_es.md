<p align="right">
  <a href="README.md">[EN]</a>
  <a href="README_es.md">[ES]</a>
  <a href="README_pt.md">[PT]</a>
  <a href="README_tr.md">[TR]</a>
  <a href="README_sv.md">[SV]</a>
</p>


# API Interna

JuezLTI está estructurado en diferentes módulos, como se explica en la [Arquitextura](../Architecture/README_es.md). Cuatro clases de módulos participan en esta estructura, a saber: 

 - **Vista de Estudiante** - donde los estudiantes intentan resolver el ejercicio.
 - **Validador** de los intentos enviados por los estudiantes desde el módulo anterior.
 - **Gestor de _Feedback_** - procesa informes generados por los validadores para producir mensajes con significado para el estudiante. 
 - 
 - **Repositorio centralizado** - contiene ejercicios así como algunas configuraciones.

 Debemos anotar que, mientras que la mayoría de los módulos anteriores se ejecutan con una única instancia, cada **Validador** es un tipo de módulo con varias instancias, existiendo un validador para lenguajes de programación, un validador de lenguajes de marcas y un validador para bases de datos. Además de los validadores desarrollados durante el proyecto, se ha procurado hacer extensible la plataforma para que cualquier institución implemente sus propios validadores.

El sguiente diagrama ilustra la comunicación entre los distintos módulos. Utilizando la **Vista de Estudiante**, un estudiante envía su intento de solución al **Validador** correspondiente. Este componente evalúa el intento utilizando un ejercicio recuperado desde el **Repositorio Centralizado** y poduce un **informe**. El validador envñia el informe al **Gestor de _Feedback_** para producir un _**feedback**_ que es devuelto a la **Vista del Estudiante** y presentada a dicho estudiante.  

![Comunicación entre módulos](generic-evaluator-architecture.svg)

La comunicación entre los módulos está regulada por una [API normalizada en Swagger](https://github.com/JuezLTI/APIs/blob/d981488ba77f238f2aaeb6f862ab1c2a0e8252d9/v2/API.yaml#L16) interna. La mayoría de los datos comunicados son no-estructurados, con la excepción de los ejercicios y los informes en los que se usa, respectivamente:

- [`YAPExIL`](YAPExIL/README_es.md) -  un formato de ejercicios de programación.
- [`PEARL`](PEARL/README_es.md) un formato común para informes de evaluación.

