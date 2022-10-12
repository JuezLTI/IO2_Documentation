<p align="right">
  <a href="README.md">[EN]</a>
  <a href="README_es.md">[ES]</a>
  <a href="README_pt.md">[PT]</a>
  <a href="README_tr.md">[TR]</a>
  <a href="README_sv.md">[SV]</a>
</p>

# The LTI Standard

La especificación **L**earning **T**ools **I**nteroperability (LTI) de IMS se puede definir como una forma estandarizada de integrar contenido de terceros en cursos dentro de un LMS o plataforma. Sin LTI, los LMS y los proveedores de contenido tendrían que depender de integraciones personalizadas con perjuicio de la interoperabilidad y la escalabilidad.

Esta especificación evolucionó a partir de un mecanismo simple para lanzar aplicaciones web desde el LMS, para admitir múltiples servicios para intercambiar datos de forma segura con estas aplicaciones.

LTI es un estándar compatible con todos los proveedores de LMS de referencia y, por lo tanto, maximiza la recompensa de adaptar una aplicación web educativa.

Actualmente, el consorcio IMS recomienda la adopción de la versión 1.3. Como resumen, LTI 1.3 utiliza OAuth2 y mensajes firmados mediante JSON Web Tokens (JWT) para autenticar de forma segura a los estudiantes y pasar datos entre el LMS y la herramienta de aprendizaje externa.

Esta versión incluye LTI Advantage, definido como un paquete de servicios que agregan nuevas funciones para mejorar la integración de cualquier herramienta con cualquier LMS en el núcleo de LTI 1.3. Los tres servicios característicos de LTI Advantage son los siguientes:

 - **Servicios de aprovisionamiento de nombres y roles (NRPS)**: otorga a la herramienta acceso a la lista de usuarios y sus roles para un contexto específico (por ejemplo, un curso o grupo). **NRPS** permite que la herramienta externa solicite una lista de miembros del contexto que la lanzó. Una vez que la herramienta recibe la lista de miembros, puede leer todos los estudiantes y profesores inscritos en el contexto, incluso si aún no han iniciado la herramienta.

 - **Servicios de asignación y calificación (AGS)**: permite a los docentes sincronizar calificaciones entre herramientas de terceros y su LMS. Este servicio devuelve calificaciones numéricas y comentarios del docente a un libro de calificaciones de LMS. Por ejemplo, un docente puede ver cuándo un estudiante ha comenzado una tarea o si la ha completado. El docente también puede recibir el estado de una calificación, incluso si requiere una entrada manual por su parte.

 - **Enlaces profundos (DL)**: ofrece un enfoque más simplificado para agregar enlaces LTI a un LMS. Los mensajes de enlaces profundos permiten que las herramientas de aprendizaje externas aparezcan dentro de un LMS como lo harían las herramientas internas. Con _Deep Linking_, las herramientas de aprendizaje externas ahora pueden permitir a los profesores configurar contenido o actividades específicas dentro de la herramienta. En LTI 1.1, se tenía que exponer todo el contenido de la herramienta, incluso si el profesor solo quería que la clase usara un recurso específico. _Deep Linking_ permite a los profesores seleccionar cualquier contenido que necesiten y compartir el enlace para lanzar ese contenido con su curso. Por ejemplo, una herramienta puede permitir que un profesor configure un capítulo específico de un libro electrónico cuando sus alumnos seleccionen un enlace, en lugar de obligarlos a iniciar la herramienta y luego navegar a ese capítulo.
    
La adopción de LTI 1.3 debe ser una decisión cuidadosa. En la mayoría de los casos, LTI 1.1 es suficiente en los casos de uso en los que un estudiante inicia una actividad desde el LMS, la resuelve en la herramienta externa y luego se retorna una calificación al libro de calificaciones del LMS. Sin embargo, las nuevas características de LTI 1.3 podrían aplicarse en casos de uso relevantes. Por ejemplo, considerando el uso de tablas de clasificación: los nombres y roles obtenidos de los proveesores de servicios podrían usarse para completar las tablas de clasificación con los nombres de los estudiantes antes de que se presentaran por primera vez; Los enlaces profundos podrían usarse para incrustarse en las tablas de clasificación de contenido LMS generadas sobre la marcha por la herramienta.