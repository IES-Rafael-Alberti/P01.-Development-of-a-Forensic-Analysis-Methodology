# Proyecto 1: Development of a Forensic Analysis Methodology

## Investigación de normas y estándares forenses

+ ### UNE 71506
    Es una norma de origen español que establece la metodología para el análisis forense de evidencias informáticas. Define las distintas fases del proceso: preservación, adquisición, análisis y presentación de las evidencias digitales. Nos indica como debemos proceder para que las pruebas obtenidas sean legalmente válidas en España adaptando estándares internacionales.

+ ### NIST Special Publication 800-86
    Ofrece una guía para la integración de técnicas forenses en la respuesta a incidentes. Detalla los procesos y principios para la adquisición, examinación, análisis y documentación de las evidencias digitales, con énfasis en que la integridad de los datos se mantenga.

+ ### RFC 4810
    Describe las mejores prácticas para la adquisición, la preservación y el almacenamiento de las evidencias digitales. Proporciona directrices para la preservación de los logs y otros datos relevantes para la investigación forense.

+ ### RFC 3227
    Establece pautas para la adquisición y preservación de evidencias digitales. Recalca la importancia de la integridad de los datos y proporciona directrices para la documentación de todo el proceso de adquisición y manipulación de evidencias.

+ ### RFC 4998
    Define el formato de Evidence Record Syntax (ERS) o Sintaxis de Registro de Evidencias en español y nos describe cómo generar y verificar marcas de tiempo que se podrán utilizar para demostrar la existencia de datos en un momento específico.

+ ### RFC 6283
    Define el formato de Evidence Record Syntax (ERS) o Sintaxis de Registro de Evidencias en español complementando al RFC 4998 adaptando el formato para expresarlo en XML y poder integrarlos fácilmente en sistemas modernos.

+ ### UNE 71505-3
    Se centra específicamente en la admisión legal de las evidencias en España a través de unos estándares y directrices para la gestión de las evidencias digitales. Proporciona por ejemplo los formatos estandarizados para el intercambio de evidencias entre sistemas o entidades o los mecanismos de seguridad necesarios para proteger las evidencias contra accesos no autorizados y alteraciones.

+ ### UNE 1970010
    Es una norma española que establece los criterios generales para la elaboración de informes y dictámenes periciales sobre las Tecnologías de la Información y las Comunicaciones (TIC), ofreciendo una guía para presentar los hallazgos forenses.

+ ### ISO/IEC 27037:2012(E)
    Es una norma internacional que proporciona directrices para la identificación, recolección, adquisición y preservación de las evidencias digitales. Proporciona pautas a seguir para asegurar la integridad y autenticidad de las evidencias digitales desde la escena del incidente hasta su posible presentación en un juicio.


___
## Comparativa de las normas y estándares


___
## Desarrollo de metodología propia
### Adquisición de evidencia digital


### Preservación y almacenamiento de la evidencia


### Análisis de la evidencia


### Documentación de hallazgos

Para realizar un buen análisis forense hemos decidido centrarnos en la norma UNE 71506 ya que se adapta perfectamente al contexto de leyes nacionales y legales en España. A continuación te dejo algunas de las razones más importantes:

1) Metodología específica para un análisis forense digital. Ya que otras normas como ISO/IEC 27037:2012(E) y la NIST 800-86 proporcionan unos principios generales para el manejo de pruebas en cambio UNE 71506 ofrece una metodología más detallada y estructurada para un análisis forense.
2) La norma UNE 71506 defiende una planificación  metodológica detallada y una secuencia temporal clara para cada fase del análisis, lo que permite la creación de registros auditable a lo largo de todo el proceso. Aunque la ISO/IEC 27037 también se ocupa de la preservación y análisis de la evidencia, la UNE 71506 ofrece un enfoque más integral para la documentación de todo el ciclo de vida de la evidencia

Aquí dejamos cómo deberiamos documentar un análisis forense.

+ Un documento de recepción de evidencias/muestras electrónicas. Mediante este registro, se lleva el control de entrada de peticiones del análisis, así como de las evidencias a estudiar.
+ Un registro de la documentación recibida. Los documentos que deben acompañar a una evidencia digital pueden ser los siguientes:
    + Descripción de las evidencias electrónicas.
    + Reseña de la cadena de custodia hasta la llegada de las mismas al entorno de análisis forense.
    + Estudios solicitados en dicho análisis.
    + Permisos necesarios para la realización de los estudios solicitados.
+ Registro de reseña de las evidencias electrónicas. Este documento describe de forma detallada y completa tanto la evidencia digital como el estado en el que se encuentra en el momento de la recepción.
+ Registro del tratamiento inicial: Se debe detallar el proceso de volcado forense de datos o la realización de la imagen correspondiente.
+ Registro de situación de evidencias/muestras. Este documento debe reflejar las operaciones llevadas a cabo sobre una evidencia digital, dónde se realizan estas operaciones, por quién y el momento temporal en que se efectúan.
+ Registro de tareas del análisis inicial.
+ Registro de tareas del análisis de datos definitivo con la expresión temporal de los distintos procesos que se lleven a cabo, así como de la ubicación temporal de la evidencia si se paraliza temporalmente el estudio de la misma.
### Presentación de resultados
Hemos seleccionado el UNE 71506 ya te permite asegurar el cumplimiento de las normativas nacionales, lo cual es muy importante para los procedimientos legales en España.Si bien otras normas como la ISO/IEC 27037:2012(E) o la NIST SP 800-86 ofrecen buenas indicaciones, su enfoque internacional no se alinea tan directamente con las necesidades específicas de un proceso forense en España.

Las RFC, por su parte, son demasiado técnicas y específicas, mientras que la UNE 71506 abarca el proceso completo del análisis forense desde la identificación hasta la presentación en un contexto forense legal español.

Para la realización de la presentación se debe materializar en un informe pericial, el cual debe acompañar los términos técnicos con un lenguaje fácil de comprender dirigiddo al organismo o entidad que solicita ese estudio.
El término *informe pericial* se considera equivalente al término *informe técnico-forense*.

Para la parte general se tendrá en cuenta la norma UNE 197001, con la característica de que en este caso, su contenido trata sobre aspectos técnicos propios de las tecnologías de la información.

Una vez el informe pericial sea redactado se debe remitir al organismo solicitante del estudio los equipos y soportes digitales estudiados, acompañando del correspondiente recibo o documento de control de evidencias.Dicho recibo debe devolverse al organismo o empresa que lo emite, una vez haya llegado el informe y las muestras objeto de estudio al organismo o entiddad que lo solicitó, dando asi por finalizado la trazabilidad y proceso de custodia de las evidencias del análisis forense.
___
## Resumen de la metodología
### Adquisición de evidencia digital


### Preservación y almacenamiento de la evidencia


### Análisis de la evidencia


### Documentación de hallazgos

1) Ventajas de la Norma UNE 71506
    + Metodología detallada: A diferencia de otras normas (ISO/IEC 27037, NIST 800-86), UNE 71506 proporciona una estructura más específica para el análisis forense digital.
    + Planificación metodológica clara: Secuencia temporal bien definida y registros auditables durante todo el proceso.
    + Enfoque integral: Mejora la documentación de todo el ciclo de vida de la evidencia.
2) Proceso de Documentación
    + Aceptación de pruebas:
        + Crear un documento con todas las evidencias electrónicas.
        + Gestionar solicitudes de análisis y evidencias.
    + Registro de documentación:
        + Describir evidencias, estudios solicitados, permisos y cadena de custodia.
    + Registro de evidencias:
        + Descripción detallada de las evidencias y su estado al recibirlas.
    + Registro de tratamiento inicial:
        + Documentar el proceso de volcado forense o creación de imágenes.
    + Registro de situación de evidencias:
        + Registrar operaciones realizadas sobre la evidencia, quién las realizó y cuándo.
    + Registro de tareas de análisis inicial:
        + Documentar las primeras tareas del análisis forense.
    + Registro de tareas de análisis final:
        + Incluir una secuencia temporal de los procesos y la ubicación de la evidencia si se suspende el análisis.


### Presentación de resultados


1) Enfoque de la UNE 71506:
    + Cubre el proceso forense completo:
        + Identificación.
        + Análisis.
        + Presentación.
        + Aplicación directa al contexto legal español.
2) Informe pericial (o técnico-forense):
    + Debe acompañar términos técnicos con lenguaje accesible.
    + Norma UNE 197001 aplicable en la parte general, enfocada en tecnologías de la información.
3) Proceso de finalización:
    + Redactar el informe y remitirlo junto a los equipos y soportes digitales al organismo solicitante.
    + Adjuntar un recibo o documento de control de evidencias, que debe devolverse al emisor para concluir la trazabilidad y custodia de las evidencias.
