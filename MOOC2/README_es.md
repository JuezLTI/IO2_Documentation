<p align="right">
  <a href="README.md">[EN]</a>
  <a href="README_es.md">[ES]</a>
  <a href="README_pt.md">[PT]</a>
  <a href="README_tr.md">[TR]</a>
  <a href="README_sv.md">[SV]</a>
</p>

# Manual de despliegue
El segundo bloque se centrará en la instalación de JuezLTI y su integración en los LMS de las instituciones educativas. Si bien el consorcio ofrecerá, durante la ejecución del proyecto, una plataforma gratuita para su uso (JuezLTI-central), JuezLTI está diseñada para permitir la instalación en los servidores propios de cualquier institución que quiera adoptarla.

Esta tarea la llevará a cabo principalmente [EdF](http://www.edf.global/), ya que son especialistas en la integración de herramientas educativas y serán quienes lleven a cabo la configuración y despliegue de los contenedores Docker.

Gracias a este contenedor Docker, JuezLTI permitirá una instalación sencilla y modular, permitiendo que cada institución configure fácilmente los módulos (programación/bases de datos/lenguajes de marcas) a instalar en sus servidores o su instalación distribuida en la nube, a través de proveedores de servicios de computación en la nube.

Todo ello se definirá en su correspondiente bloque a través de los siguientes apartados:
- Instalación de JuezLTI servidores propios
- Despliegue de JuezLTI en la nube.
- Configuración de JuezLTI.
- Comunicación entre JuezLTI y el LMS.
- Integración de repositorios de ejercicios.

# Manual de desarrollo

JuezLTI se lanzará con una licencia Apache 2.0, lo que permitirá a cualquier institución o desarrollador ampliar las funcionalidades de la herramienta, adaptándola a las particularidades de la institución. Se necesita un manual específico para facilitar la tarea de programación. 

Este manual será desarrollado principalmente por [INESC TEC](http://www.inesctec.pt/), y constará de las siguientes secciones:
- [El estándar LTI](Development/LTI/README_es.md)
- [Arquitectura de JuezLTI](Development/Architecture/README_es.md)
- Desarrollo de módulos con TSUGI
- [API interna](Development/API/README_es.md)
- Desarrollo de clientes JuezLTI
- Desarrollo de ejercicios con JuezLTI