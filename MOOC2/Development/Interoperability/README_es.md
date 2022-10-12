<p align="right">
  <a href="README.md">[EN]</a>
  <a href="README_es.md">[ES]</a>
  <a href="README_pt.md">[PT]</a>
  <a href="README_tr.md">[TR]</a>
  <a href="README_sv.md">[SV]</a>
</p>

# Interoperabilidad

JuezLTI utiliza la versión 1.0 del estándar _**L**earning **T**ools **I**nteroperability_ (LTI) para la comunicación con el LMS.

Este estándar de interoperabilidad fue propuesto por el _IMS Global Learning Consortium_ \cite{lti2010} y es soportado por LMS de referencia como Moodle, Canvas o Sakai.

Con _LTI_ un conjunto de servicios pueden ser utilizados para extender la funcionalidad del LMS usando una arquitectura _SOA_ (Service Oriented Architecture).

El LMS se convierte en un _marketplace_ en el que un docente puede seleccionar los recursos desde diferentes proveedores para mejorar la experiencia de aprendizaje. 

JuezLTI está basado en **TSUGI**, un _framework_ que simplifica el desarrollo y despliegue de aplicaciones LTI.

La primera aplicación de **TSUGI** fue un MOOC autocontenido para la enseñanza de Python -- [py4e.com](py4e.com). 

Fue desarrollado por uno de sus autores, el Dr. Charles Severance, fundador del LMS de código abierto Sakai y que actualmente trabaja para el IMS. 

LTI ha sido ampliamente utilizado desde 2010, no solo para propósitos de evaluación de código sino también para proveer evaluaciones complejas no soportadas directamente por el LMS, tal como Dig4E, una herramienta para aprender conceptos sobre los estándar de imágenes digitales fijas de alta calidad. 

Para utilizar JuezLTI, el docente debe solicitar una pareja key/secret en la web del proyecto.

Con dichas credenciales, y la URL facilitada, el docente podrá añadir actividades JuezLTI como una actividad externa en el LMS. 

Los estudiantes se identifican en JuezLTI usando la información provista por el LMS. 

Cuando un estudiante o un docente abre la actividad, el LMS se comunica con JuezLTI utilizando LTI, a través del _framework_ **Tsugi** para identificar el rol del usuario y presentar la interfaz apropiada. Entonces, el LMS envía la propiedad <code>resource_link_id</code> identificando así la actividad requerida. 

De esta forma, se pueden añadir distintas actividades con la misma _key_. 

Tras la evaluación, JuezLTI informa al LMS de la calificación obtenida por la solución de los ejercicios usando un servicio LTI. 

En resumen, existe una comunicación bidireccional entre JuezLTI y el LMS: JuezLTI almacena la información de los estudiantes y sus resultados y devuelve la calificación obtenida al LMS.
