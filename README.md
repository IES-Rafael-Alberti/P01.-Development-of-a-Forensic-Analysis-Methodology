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

### Adquisición de evidencia digital (ISO/IEC 27037:2012(E))
 Para la adquisición de evidencia digital hemos decidido centrarnos en la norma ISO/IEC 27037:2012(E) ya que está diseñada para aplicarse en el ámbito internacional a diferencia de la UNE 71506 que se centra más en el ámbito español. Esto nos permitirá mantener nuestra metodología aunque trabajemos fuera del ámbito español.

 Esta parte de la metodología se centra en la identificación de posibles evidencias digitales y objetos relacionados (como por ejemplo post-its en un monitor con posibles contraseñas) y en la adquisición de dichas evidencias ya sea en la propia escena de la investigación o en nuestro laboratorio forense.

 Cuando identifiquemos las posibles evidencias deberemos de fotografiar y anotar todas las posibles evidencias digitales, su estado y su localización. Deberemos de asegurarnos de no cambiar el estado de dichos dispositivos (por ejemplo encender un portatil que se encontraba apagado) y de que nadie manipule las evidencias.

 Tras haber realizado el proceso de identificación deberemos de determinar si debemos de recolectar las fuentes de evidencias para realizar su adquisición más tarde en nuestro laboratorio forense o adquirirlas in situ. Para esto deberemos de tener en cuenta si los dispositivos están encendidos o no, la volatilidad de las posibles evidencias, la existencia de encriptado de los discos. Si por ejemplo nos encontramos con un equipo encendido con discos encriptados pero cuya clave se encuentra en la memoria volátil del equipo deberíamos de realizar la adquisición en ese momento, ya que podríamos perder el acceso a esos discos duros encriptados.

 Según si pensamos realizar una adquisición o una recolección y si el equipo se encuentra encendido o apagado deberemos de seguir unos pasos distintos:

 **Recolección de dispositivos encendidos**
1) Considerar la adquisición de la memoria volátil del dispositivo y de su estado actual antes de apagarlo. Debemos de realizar esta adquisición documentando todo el proceso y con nuestras propias herramientas ya que no podemos confiar en las del propio dispositivo.
2) Apagar el dispositivo y desconectar su batería en caso de ser un dispositivo portátil.
3) Etiquetar, desconectar y asegurar todos los cables del dispositivo, etiquetando también los puertos para reconstruirlo luego.
4) Poner cinta adhesiva sobre el botón de encendido del dispositivo para evitar su encendido, además de sobre el lector de DVDs en caso de tenerlo.
5) Almacenar el dispositivo en un recipiente adecuado y sellándolo.

**Recolección de dispositivos apagados**
1) Desconectar el cable de corriente retirando primero el extremo conectado al dispositivo.
2) Etiquetar, desconectar y asegurar todos los cables del dispositivo, etiquetando también los puertos para reconstruirlo luego.
3) Poner cinta adhesiva sobre el botón de encendido del dispositivo para evitar su encendido, además de sobre el lector de DVDs en caso de tenerlo.
4) Almacenar el dispositivo en un recipiente adecuado y sellándolo.

**Adquisición de dispositivos encendidos**
1) Considerar la adquisición de la memoria volátil del dispositivo y de su estado actual antes de apagarlo. Debemos de realizar esta adquisición documentando todo el proceso y con nuestras propias herramientas ya que no podemos confiar en las del propio dispositivo.
2) Realizar la adquisición de la memoria no volátil del dispositivo documentando todo el proceso y realizando la imagen usando una herramienta validada. Esta imagen deberá ser almacenada en un dispositivo de almacenamiento nuevo o formateado de manera segura.

**Adquisición de dispositivos apagados**
1) Asegurarnos de que el dispositivo realmente está apagado.
2) Desconectar el dispositivo de almacenamiento si aún está conectado al equipo.
3) Realizar la imagen del dispositivo de almacenamiento usando una herramienta validada, documentando el proceso y almacenando la imagen en un dispositivo de almacenamiento nuevo o formateado de manera segura.
4) Almacenar el dispositivo en un recipiente adecuado y sellándolo.

### Preservación y almacenamiento de la evidencia

Para la fase de preservación nos hemos basamos en la UNE 71506:2013. Consideramos que de todos los documentos que hay es donde mejor explica y desarrolla lo que es la preservación y almacenamiento de evidencias. Veremos como el documento nos da un enfoque detallado y práctico para mantener una correcta integridad de laas evidencias que recopilaremos. 

Como factor fundamental nos comentan la importancia de preservar la información digital tal y como nos las encontramos originalmente (sin modificarlas), asegurando así su validez y confiabilidad. ¿Para qué es importante esto? Bueno, es especialmente importante cuando en un caso forense los datos se mantengan intactos, así garantizamos que cualquier análisis que se haga posteriormente puedan utilizar los mismos datos por si en algún momento se necesita un contraanalisis o alguna revisión.  
<!-- Toda organización o empresa debe tener en consideración los siguientes principios al manejar datos o evidencias electrónicas que puedan ser sometidas a un análisis forense:
1.  Se deben establecer protocolos claros y detallados para la protección de la evidencias digitales durante el análisis forense. Esto es para garantizar que no se altera la evidencia de niguna manera, ya sea de manera internacional o accidental. Estos nos pueden ayudar a prevenir situaciones como:  
    + **Tampering** (manipulación intencionado): evitamos que alguien manipule las evidencias de manera intencionada.
    + **Descargas electroestáticas**: proteger las evidencias de posibles descargas electroestáticas capaces de corromper los datos.
    + **Campos magnéticos**: proteger las evidencias de posibles campos electrmagnéticos capaces de alterar la información.
    + **Conexión accidental a redes inalámbricas**: evitamos que las evidencias se conecten a redes, lo que podría ocasionar la modificación de datos. 

2. Los técnicos encargados de manejar las evidencias por primera vez deben tener extremo cuidado al almacenarlas en soportes correctamente adecuados. Esto es importante tanto para mantener la integridad de las evidencias como también para la preservación de otras pruebas que pueden estar presentes en las evidencias. A otras pruebas se refiere con:
    + **Huellas dactilares**: las impresiones de las huellas que han sido dejadas en los dispositivos.
    + **Restos orgánicos asociados con el AD**: esto engloba a el material biológico, como puede ser pelo, piel, sudor..., que podrían contener información genética.
    + **Partículas diversas**: materiales o sustancias que pueden llegar a ser utiles en el análisis forense (como por ejemplo, polvo o fibras). 

3. En este apartado se comenta la importancia de que el personal encargado de la manipulación de las evidencias debe portar una indumentaria y equipamiento adecuado para evitar posibles alteraciones accidentales de las evidencias. Entre esto destaca: 
    + **Indumentaria adecuada**: los técnicos deberán usar ropa que este especialmente diseñada para evitar descargas electroestáticas, las cuales podrían dañar los datos de las evidencias.
    + **Evitar dispositivos que generen señales de radiofrecuencia**: los técnicos no deberan llevar dispositivos consigo que emitan señales de radio como puede ser un móvil. Estas señales podrían interferir con la evidencia, pudiendo alterar datos.
    + **Soportes aislados**: en algunso casos, es necesario el uso de cajas especiales las cuales bloquean interferencias externas (como ondas de radio o campos electromagnéticos). Esto sirve para proteger los datos originales y evitar cualquier modificación de los datos. -->


Simultaneamente, los técnicos a parte de seguir los principios antes mencionados para una preservación correcta de las evidencias también deberán llevar a cabo los siguientes pasos:

1. Los técnicos deberan de seguir una premisas para garantizar la seguridad de las premisas antes de ser analizada por los especialistas forenses. Las premisas que nos detallan son:

    + **Precintar y sellar las evidencias**, tendremos que guardarlas en recipientes adecuados como pueden ser contenedores, cajas, bolsas... También deberán de estar selladas de una forma segura, garantizando así la no manipulación o alteración de las evidencias. 

    + **Almacenamiento hasta el análisis**, es decir, las evidencias deben mantenerse protegida hasta que se lleve a cabo el analisis de los técnicos forenses.

    + **Atención especial para dispositivos que requieran de energía**. Nos referimos con esto a dispositivos que necesiten de alimentación externa para funcionar como pueden ser equipos informáticos o moviles. Esto requiere que haya que mantenerlos conectados a una fuente segura para así evitar la posible perdida de datos. 

## CADENA DE CUSTODIA
|  |  |  |
|-------------|-----------|-----------|
|  |  |
| **1. INFORMACIÓN DEL CASO** |  |  |
| **Campo** | **Valor** |  |
|  |  |
| Número de Caso | [Insertar número] |
| Tipo de Investigación | [Especificar] |
| Fecha de Adquisición | [DD/MM/AAAA] |
| Lugar de Adquisición | [Dirección completa] |
|  |  |
| **2. DESCRIPCIÓN EVIDENCIA EN ORIGINAL** |  |  |
| **Campo** | **Valor** |  |
|  |  |
| Tipo de Dispositivo | [Ej. Disco duro, USB, tarjeta SD] |
| Marca y Modelo | [Especificar] |
| Número de Serie | [Especificar] |
| Capacidad | [Ej. 1TB] |
| Estado Físico | [Describir cualquier daño visible] |
| Hash de la Evidencia Original | [MD5 y SHA-256] |
|  |  |
| **3. PRESERVACIÓN DE LA EVIDENCIA ORIGINAL** |  |  |
| **Campo** | **Valor** |  |
|  |  |
| Fecha de Entrega al Juzgado | [DD/MM/AAAA] |
| Hora de Entrega | [HH:MM] |
| Recibido por | [Nombre y cargo del funcionario judicial] |
| Ubicación en el Juzgado | [Especificar] |
| Firma del Funcionario Judicial | ________________________ |
|  |  |
| **4. CREACIÓN Y VERIFICACIÓN DE COPIAS** |  |  |
| **Campo** | **Valor** |  |
|  |  |
| Fecha y Hora de Creación (Defensa) | [DD/MM/AAAA, HH:MM] |
| Técnico Responsable (Defensa) | [Nombre y cargo] |
| Hash de la Copia (Defensa) | [MD5 y SHA-256] |
| Verificación de Integridad (Defensa) | [Confirmar que coincide con el original] |
| Entregado a (Defensa) | [Nombre del representante de la defensa] |
| Fecha y Hora de Entrega (Defensa) | [DD/MM/AAAA, HH:MM] |
| Firma del Receptor (Defensa) | ________________________ |
| Fecha y Hora de Creación (Fiscalía) | [DD/MM/AAAA, HH:MM] |
| Técnico Responsable (Fiscalía) | [Nombre y cargo] |
| Hash de la Copia (Fiscalía) | [MD5 y SHA-256] |
| Verificación de Integridad (Fiscalía) | [Confirmar que coincide con el original] |
| Entregado a (Fiscalía) | [Nombre del representante de la fiscalía] |
| Fecha y Hora de Entrega (Fiscalía) | [DD/MM/AAAA, HH:MM] |
| Firma del Receptor (Fiscalía) | ________________________ |
|  |  |
| **5. REGISTRO DE ACCESOS Y VERIFICACIONES** |  |  |
| **Campo** | **Valor** |  |
|  |  |
| Fecha y Hora (Acceso) | [DD/MM/AAAA, HH:MM] |
| Parte Accediendo (Acceso) | [Defensa/Fiscalía] |
| Propósito (Acceso) | [Ej. Análisis] |
| Hash Verificado (Acceso) | [MD5/SHA-256] |
| Coincide con Original (Acceso) | [Sí/No] |
| Firma (Acceso) | [Firma] |


### Análisis de la evidencia

Para adaptar la fase de analisis, despues de valorar las diferentes opciones disponibles hemos optado por utilizar de base la normativa UNE 71506. Este manual se centra en el analisis forense y lo explica de manera sencilla y concisa pero mantiene la base funcional que necesitamos. 

El análisis forense de evidencias digitales debe seguir un proceso metódico, auditable y repetible. El objetivo es responder a preguntas sobre el tiempo de intrusión, su origen, los sistemas afectados, los métodos usados, y los activos alterados o accedidos.
Antes de iniciar el análisis, se deben cumplir los siguientes pasos preliminares:

1. **Comprobar competencias**: Verificar si el análisis solicitado está dentro de la competencia del laboratorio forense.
2. **Revisión documental**: Estudiar la documentación adjunta para contextualizar las evidencias y las relaciones entre ellas.
3. **Supervisión de la cadena de custodia**: Comprobar quién recogió las evidencias, cuándo, dónde, y cómo se almacenaron hasta llegar al laboratorio.
4. **Autorizaciones**: Obtener permisos legales para realizar el análisis, según la normativa vigente.
5. **Comprobación de estado**: Verificar que las evidencias no están dañadas y son susceptibles de análisis.
6. **Evidencias adicionales**: Si se encuentran nuevas evidencias (memorias, discos, etc.), estas deben ser registradas y se deben obtener nuevas autorizaciones para analizarlas.
7. **Hora del BIOS**: Registrar la hora del BIOS del equipo donde se alojan los discos para poder comparar la cronología.
8. **Establecer prioridades**: Definir criterios de prioridad en el análisis.

#### 1. Recuperación de ficheros borrados
Este proceso busca recuperar archivos eliminados de las estructuras de almacenamiento (como tablas FS o MFT). Además, se recuperan archivos de áreas no asignadas del disco o ficheros "huérfanos". También se localizan fragmentos de archivos mediante la búsqueda de sus cabeceras. La trazabilidad de toda la información recuperada debe estar documentada en el informe.

#### 2. Estudio de particiones y sistemas de archivos
Se analiza la estructura de almacenamiento (particiones, volúmenes físicos y lógicos, sistemas RAID, etc.). Este proceso incluye:
- **Enumeración** de particiones actuales y previas.
- **Identificación** de áreas ocultas (HPA, DCO).
- **Reconocimiento** de sistemas de archivos en contenedores y discos cifrados.
- **Análisis** de archivos comprimidos y sus cabeceras.

#### 3. Estudio del sistema operativo
Se identifican los sistemas operativos instalados, su fecha de instalación, actualizaciones, usuarios, privilegios y las últimas actividades registradas. También se examinan los dispositivos de hardware y software reconocidos por el sistema.

#### 4. Estudio de la seguridad implementada
Este proceso evalúa si las evidencias han sido comprometidas mediante métodos de intrusión, modificación o eliminación. Se debe identificar malware (virus, troyanos, etc.) y evaluar su impacto en el sistema.

#### 5. Análisis detallado de los datos obtenidos
Se realiza un análisis exhaustivo de las evidencias electrónicas utilizando software forense especializado. Este análisis incluye la clasificación y, opcionalmente, el indexado de los datos, lo que agiliza la búsqueda de información clave mediante palabras o criterios específicos.

El análisis debe incluir:

1. Información del sistema (hardware, última actividad, configuración regional, etc.).
2. Dispositivos conectados (USBs, impresoras, móviles, etc.).
3. Escritorio del usuario y papelera de reciclaje.
4. Conexiones de red y protocolos utilizados.
5. Comunicaciones realizadas desde el equipo.
6. Registros del sistema y auditoría.
7. Espacios no asignados en el disco.
8. Archivos de hibernación, paginación y de intercambio.
9. Cola de impresión.
10. Enlaces a archivos recientes.
11. Carpetas de los distintos usuarios.
12. Programas instalados (ofimáticos, de imagen, audio, video, contabilidad, etc.).
13. Metadatos.
14. Aplicaciones de virtualización y sus configuraciones.
15. Bases de datos y gestores de bases de datos.
16. Archivos cifrados y particiones protegidas.
17. Navegación por Internet (historial, cookies).
18. Correos electrónicos y correos web.
19. Registros de mensajería instantánea y chats.
    


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

Primero identificar evidencias digitales y objetos relacionados fotografiándolos y anotando todo sobre ellos.

Luego decidir si realizar una adquisición o recolección dependiendo del estado de los dispositivos y si están encendidos o no.

|                 | Dispositivo encendido | Dispositivo apagado |
| :-------------: | :-------------------: | :-----------------: |
| **Recolección** | 1. Adquisición de memoria volátil <br> 2. Apagarlo y desconectar batería si tiene <br> 3. Etiquetar, desconectar y asegurar cables <br> 4. Cinta sobre el botón de inicio y lector de CDs <br> 5. Almacenamiento y sellado| 1. Desconectar cable de corriente <br> 2. Etiquetar, desconectar y asegurar cables <br> 3. Cinta sobre el botón de inicio y lector de CDs <br> 4. Almacenamiento y sellado|
| **Adquisición** | 1. Adquisición de la memoria volátil <br> 2. Adquisición de la memoria no volátil| 1. Asegurar que está apagado <br> 2. Desconectar dispositivo de almacenamiento <br> 3. Bloquear la escritura y realizar la imagen del dispositivo de almacenamiento <br> 4. Almacenamiento y sellado|

### Preservación y almacenamiento de la evidencia

Escogemos la UNE 71506:2013 para este apartado por su enfoque detallado y práctico poniendo ejemplos, sobre la preservación y almacenamiento de evidencias. Donde explica de manera esquemática como mantener la integridad de las evidencias digitales. 

+ **Preservación de información digital.**

    - Es clave mantener las evidencias recogidas en su estado orginal (sin ninguna modificación)
    - Esto importante para garantizar y confiabilidad de los datos.
    - Permiten posibles revisones de análisis 

+ **Principios para manejo de evidencias digitales**

    - Estableceremos protocolos claros con el objetivo de proteger las evidencias de alteraciones intencionadas o accidentales.
    - Prevención de situaciones: 
        1. Manipulación intencionada (tampering). 
        2. Descargas electroestáticas
        3. Campos magnéticos
        4. Conexión accidental a redes inalámbricas

+ **Almacenamiento adecuando de evidencias**

    - Los técnicos deben almacenar evidencias en soporte adecuados para mantener la integridad. 
    - Preservar otras pruebas en la evidencia:
        1. Huellas dactilares
        2. Restos orgánicos asociados al ADN (pelo, piel, etc.) 
        3. Partículas diversas (polvo, fibras, etc.)

+ **Equipamiento adecuado para los técnicos**

    - Indumentaria adecuada (evitar descargas electroestáticas)
    - Evitar dispositivos que emitan radiofrecuencias (móviles u otros dispositivos que puedan emitir señales)
    - Soporte aislado (cajas especiales que bloqueen interferencias externas como ondas de radio o campos electromagnéticos)

+ **Pasos adicionales para la preservación de las evidencias**

    - Precintar y sellas evidencias (evitar la manipulación usando contenedores, cajas o bolsas selladas)
    - Almacenamiento hasta el análisis (mantener protegidas las evidencias hasta el análisis)
    - Atención a dispositivos que requieran energía (mantenerlos conectados para evitar la pérdida de datos)

### Análisis de la evidencia

#### Fase Preliminar: Preparación y Verificación
1. **Comprobar competencias**: Verificar la idoneidad del laboratorio para el análisis.
2. **Revisión documental**: Analizar la documentación adjunta para entender el contexto de las evidencias.
3. **Supervisión de la cadena de custodia**: Revisar la recolección, almacenamiento y transferencia de evidencias.
4. **Autorizaciones**: Obtener los permisos legales necesarios para el análisis.
5. **Comprobación del estado de las evidencias**: Verificar la integridad y disponibilidad para el análisis.
6. **Registro de evidencias adicionales**: Documentar cualquier nueva evidencia encontrada y obtener permisos adicionales.
7. **Registrar la hora del BIOS**: Documentar la hora del BIOS del equipo para futuras referencias de cronología.
8. **Establecer prioridades**: Definir el orden de análisis según la criticidad y relevancia.

#### Fase 1: Recuperación de Ficheros Borrados
- **Recuperación de archivos eliminados**: Buscar en la tabla de archivos (FS o MFT) y en áreas no asignadas.
- **Localización de archivos huérfanos y fragmentados**: Identificar y reconstruir ficheros a partir de cabeceras.
- **Documentación de la trazabilidad**: Registrar todas las acciones y resultados de recuperación.

#### Fase 2: Estudio de Particiones y Sistemas de Archivos
- **Enumeración de particiones**: Identificar particiones actuales y anteriores.
- **Detección de áreas ocultas**: Buscar áreas protegidas (HPA, DCO).
- **Reconocimiento de sistemas de archivos**: Analizar contenedores, discos cifrados y archivos comprimidos.

#### Fase 3: Análisis del Sistema Operativo
- **Identificación de sistemas operativos**: Determinar las versiones, fechas de instalación y actualizaciones.
- **Análisis de usuarios y privilegios**: Revisar los usuarios registrados y sus niveles de acceso.
- **Registro de hardware y software**: Listar dispositivos conectados y aplicaciones reconocidas.

#### Fase 4: Evaluación de la Seguridad Implementada
- **Detección de intrusiones y malware**: Identificar posibles alteraciones o compromisos en las evidencias.
- **Evaluación del impacto**: Determinar el alcance del daño causado por el malware.

#### Fase 5: Análisis Detallado de los Datos Obtenidos
- **Análisis exhaustivo**: Usar software especializado para clasificar y buscar datos relevantes.
- **Áreas de interés específicas**:

| N.º | Área de interés                            | N.º | Área de interés                          |
|-----|--------------------------------------------|-----|------------------------------------------|
| 1   | Información del sistema                    | 11  | Carpetas de usuarios                     |
| 2   | Dispositivos conectados (USBs, impresoras) | 12  | Programas instalados                     |
| 3   | Escritorio y papelera de reciclaje         | 13  | Metadatos                                |
| 4   | Conexiones de red y protocolos             | 14  | Aplicaciones de virtualización           |
| 5   | Comunicaciones realizadas                  | 15  | Bases de datos                           |
| 6   | Registros del sistema                      | 16  | Archivos cifrados y particiones protegidas|
| 7   | Espacios no asignados del disco            | 17  | Historial de navegación y cookies        |
| 8   | Archivos de hibernación y paginación       | 18  | Correos electrónicos                     |
| 9   | Cola de impresión                          | 19  | Registros de mensajería y chats          |
| 10  | Enlaces a archivos recientes               |     |                                          |


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

