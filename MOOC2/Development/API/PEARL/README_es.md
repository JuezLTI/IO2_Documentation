<p align="right">
  <a href="README.md">[EN]</a>
  <a href="README_es.md">[ES]</a>
  <a href="README_pt.md">[PT]</a>
  <a href="README_tr.md">[TR]</a>
  <a href="README_sv.md">[SV]</a>
</p>

# PEARL 

El formato _**P**rogramming **E**xercise **A**ccessement **R**eport **L**anguage_ (PEARL) es utilizado para homogeneizar los informes de evaluación. Los tres tipos de solicitud manejadas por un servicio que utilice PEARL son: 

 - `ListCapabilities`: devuelve, a los clientes, las capacidades de evaluación de un validador particular;
 - `EvaluateSubmission`: permite la solicitud de la evaluación de un ejercicio de programación específico;
 - `GetReport`: permite al cliente recibir un informe de una evaluación específica utilizando un ticket.

![Esquema PEARL](PEARL_UML.svg)

El diagrama representado en la figura anterior incluye dos elementos principales: `request` (solicitud) y `reply` (respuesta). El primero replica la solicitud y los parámetros recibidos por el servicio de evaluación y el último contiene el resultado de esa solicitud.

El elemento `request` contiene un sub-elemento en función del tipo de función. El elemento `reply` incluye dos sub-elementos que representan las posibles respuestas del servicio, más concretamente, los elementos `capabilities` y `report`.

El elemento `capabilities` es utilizado en una respuesta del tipo `ListCapabilities`. Este elemento tiene varios sub-elementos de capacidad, cada uno de los cuales contiene varias características para describirla. El atributo `ticket` contiene un ticket que permite recuperar un informe en un momento posterior.
