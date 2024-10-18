# Development of a Forensic Analysis Methodology

Se nos ha encargado realizar nuestra propia metodología para el análisis forense digital. Durante este documento pasaremos por cuatro bloques donde analizaremos las normas existentes relacionadas con el análisis forense digital e intentaremos adaptarlas a nuestras necesidades dando forma a una nueva metodología propia.

## Investigación de normas y estándares forenses
Existen varias normativas que aluden al análisis forense digital, pero entre ellos destacan seis documentos que, aun tratando temas variados; engloban un contexto que nos puede ser útil para nuestra metodología. A continuación, hablaremos de ellos.

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

Algunas de las normas y estándares analizados tienen similitudes entre si. Aunque existen algunas similitudes y solapamientos entre ellos, cada uno tiene un enfoque y alcance particular que analizaremos a continuación.

### UNE 71506, NIST Special Publication 800-86 e ISO/IEC 27037:2012(E)
Aunque estas tres normas cubren gran parte del proceso de análisis forense digital sólo el UNE 71506 cubre el proceso completo mientras que el ISO/IEC 27037:2012(E) se centra en la identificación, recolección, adquisición y preservación de las evidencias digitales y el NIST Special Publication 800-86 se centra en integrar técnicas forenses en la respuesta a incidentes. Además el UNE 71506 es una norma española aplicable en el contexto legal y forense español, mientras que el NIST Special Publication 800-86 está más orientada a las organizaciones de los EE.UU. y el ISO/IEC 27037:2012(E) está diseñada para poder aplicarse internacionalmente.
|          | Ámbito | Características principales |
|:--------:|:------:|:---------------------------:|
| **UNE 71506** | España | Proceso completo del análisis forense |
| **NIST Special Publication 800-86** | Internacional | Fases iniciales del análisis forense |
| **ISO/IEC 27037:2012(E)** | EE.UU. | Integración técnicas forenses en respuesta a incidentes |

### UNE 71505-3 y UNE 197010

Estas dos normas se relacionan con el manejo de las evidencias digitales y tecnologías de la información y comunicación (TIC).También son relevantes para el campo de la informática forense y peritaje tecnológico. Y además ambas son normas UNE (Una Norma Española), diseñadas para el uso en un contexto español.

Aunque también tiene varias diferencias como pueden ser que la UNE 71505-3 trata sobre formatos de intercambios de evidencias y mecanismo para mantener su confiabilidad, también se enfoca en las fases de gestión y manejo técnico de las evidencias en cambio la norma UNE 197010 establece requisitos formales ara informes y dictámenes periciales, sin entrar en métodos específicos de análisis y también se centra en la fase final de presentación de resultados en forma de informes y dictámenes.

|          | Características principales |
|:--------:|:---------------------------:|
| **UNE 71505-3** | Formatos de intercambio de evidencias y mecanismos para mantener su confiabilidad. Enfoque en fases de gestión y manejo técnico de las evidencias. |
| **UNE 197010** | Requisitos formales para informes y dictámenes periciales. Enfoque en la presentación final de resultados. |

### RFC 4998 y RFC 6283
Ambas se centran en demostrar la existencia de datos en momento concreto con el uso de marcas de tiempo, el RFC 4998 es más amplio, definiendo los requisitos generales para el registro de evidencias además de definir el estándar ERS mientras que el RFC 6283 se centra específicamente en la implementación del estándar ERS con el uso de XML.
|          | Características principales |
|:--------:|:---------------------------:|
| **RFC 4998** | Estándar ERS y requisitos para el registro de evidencias |
| **RFC 6283** | Adaptación de ERS con XML |

### RFC 3227 y RFC 4810

Aunque ambos RFCs tratan sobre la preservación de datos, el RFC 4810 tiene un enfoque diferente al del RFC 3227, ya que no se centra en la recolección de evidencia digital en un contexto inmediato, sino que trata el almacenamiento seguro y la recuperación de archivos digitales a largo plazo, enfocandose en la autenticidad y la disponibilidad a largo plazo.

|          | Características principales |
|:--------:|:---------------------------:|
| **RFC 3227** | Recolección de evidencia digital en un contexto inmediato |
| **RFC 4810** | Almacenamiento seguro y recuperación de archivos digitales a largo plazo |


___
## Desarrollo de metodología propia

Tras realizar un estudio de las normas existentes, hemos decidido incluir en nuestra metodología las normas ISO/IEC 27037:2012(E), UNE 71506:2013, UNE 71506. En cada apartado analizaremos en que normativa se basa y el porqué de nuestra elección. 

### Adquisición de evidencia digital
Para la adquisición de evidencia digital hemos decidido basarnos en la norma ISO/IEC 27037:2012(E) ya que está diseñada para aplicarse en el ámbito internacional a diferencia de la UNE 71506 que se centra más en el ámbito español. Esto nos permitirá mantener nuestra metodología aunque trabajemos fuera del ámbito español.

Durante la identificación de evidencias y la adquisición deberemos de ir rellenando nuestro acta de adquisición de evidencias digitales. Para ello usaremos el siguiente modelo:
#### Acta de Adquisición de Evidencias Digitales
| Acta de Adquisición de Evidencias Digitales |                                   |
|---------------------------------------------|-----------------------------------|
| **1. Información General**                  |                                   |
| Número de Caso                              |                                   |
| Fecha y Hora de Adquisición                 |                                   |
| Lugar de Adquisición                        |                                   |
| Analista Forense                            |                                   |
| Número de Identificación del Analista       |                                   |
| **2. Descripción del Dispositivo/Evidencia** |                                   |
| Tipo de Dispositivo                         |                                   |
| Marca y Modelo                              |                                   |
| Número de Serie                             |                                   |
| Capacidad de Almacenamiento                 |                                   |
| Estado Físico                               |                                   |
| **3. Metodología de Adquisición**           |                                   |
| Herramientas Utilizadas                     |                                   |
| Método de Adquisición                       |                                   |
| Hash de Verificación MD5                    |                                   |
| Hash de Verificación SHA-256                |                                   |
| **4. Detalles del Proceso**                 |                                   |
| Hora de Inicio                              |                                   |
| Hora de Finalización                        |                                   |
| Observaciones                               |                                   |
| **5. Testigos**                             |                                   |
| Nombre del Testigo 1                        |                                   |
| Firma Testigo 1                             |                                   |
| Nombre del Testigo 2                        |                                   |
| Firma Testigo 2                             |                                   |
| **6. Declaración del Analista**             | Yo, _______________________, certifico que la información contenida en esta acta es verdadera y precisa según mi mejor conocimiento y habilidad. La adquisición de evidencias se realizó siguiendo los procedimientos forenses estándar y manteniendo la integridad de la evidencia en todo momento. |
| Firma del Analista                          |                                   |
| Fecha                                       |                                   |
| **8. Anexos**                               | - Fotografías del dispositivo<br>- Logs de la herramienta de adquisición<br>- Otros documentos relevantes |

Deberemos de actuar de distinta manera dependiendo de si el dispositivo se encuentra encendido desde la incidencia que estamos investigando o si el dispositivo se ha apagado en algún momento desde la incidencia.

**Adquisición de dispositivos encendidos**
1) Realizar la adquisición de la memoria volátil del dispositivo
2) Realizar la adquisición de la memoria no volátil del dispositivo.
3) Apagar el dispositivo y desconectar su batería en caso de ser un dispositivo portátil.
4) Etiquetar, desconectar y asegurar todos los cables del dispositivo, etiquetando también los puertos para reconstruirlo luego.
5) Poner cinta adhesiva sobre el botón de encendido del dispositivo y el lector ded CDs.
6) Almacenar el dispositivo en un recipiente adecuado y sellándolo.

**Adquisición de dispositivos apagados**
1) Realizar la adquisición de la memoria no volátil del dispositivo.
2) Desconectar el cable de corriente retirando primero el extremo conectado al dispositivo.
3) Etiquetar, desconectar y asegurar todos los cables del dispositivo, etiquetando también los puertos para reconstruirlo luego.
4) Poner cinta adhesiva sobre el botón de encendido del dispositivo y el lector ded CDs.
5) Almacenar el dispositivo en un recipiente adecuado y sellándolo.

### Preservación y almacenamiento de la evidencia

Para la fase de preservación nos hemos basamos en la UNE 71506:2013. Consideramos que de todos los documentos que hay es donde mejor se explica y desarrolla lo que es la preservación y almacenamiento de evidencias. Veremos como el documento nos da un enfoque detallado y práctico para mantener una correcta integridad de las evidencias que recopilaremos. 

Como factor fundamental nos comentan la importancia de preservar la información digital tal y como nos la encontramos originalmente (sin modificarlas), asegurando así su validez y confiabilidad. ¿Para qué es importante esto? Bueno, es especialmente importante cuando en un caso forense los datos se mantengan intactos, así garantizamos que cualquier análisis que se haga posteriormente puedan utilizar los mismos datos por si en algún momento se necesita un contraanálisis o alguna revisión.  
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

Simultáneamente, los técnicos a parte de seguir los principios antes mencionados para una preservación correcta de las evidencias también deberán llevar a cabo los siguientes pasos:

Los técnicos deberán de seguir una premisas para garantizar la seguridad de las premisas antes de ser analizada por los especialistas forenses. Las premisas que nos detallan son:

+ **Precintar y sellar las evidencias**, tendremos que guardarlas en recipientes adecuados como pueden ser contenedores, cajas, bolsas... También deberán de estar selladas de una forma segura, garantizando así la no manipulación o alteración de las evidencias. 

+ **Almacenamiento hasta el análisis**, es decir, las evidencias deben mantenerse protegidas hasta que se lleve a cabo el análisis de los técnicos forenses.

+ **Atención especial para dispositivos que requieran de energía**. Nos referimos con esto a dispositivos que necesiten de alimentación externa para funcionar como pueden ser equipos informáticos o máviles. Esto requiere que haya que mantenerlos conectados a una fuente segura para así evitar la posible pérdida de datos.   

A continuación hemos creado un informe donde quedará por escrito la información de importancia en la cadena de custodia. Esta cadena hace referencia al proceso por el que pasan las evidencias desde que se ha llevado la adquisición.  
En este proceso se recoge a quien se entrega las evidencias, datos sobre la misma, si se crean copias de las evidencias, comprobaciones de hash, etc. Esto más que nada es para llevar un registro y preservar la integridad de las mismas, debido a que si en algún momento existe cualquier alteración de los datos se sepa en que parte de la cadena ha ocurrido. 

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

Este documento nos servirá para continuar con la metodología que hemos escogido.

### Análisis de la evidencia

Para adaptar la fase de análisis, después de valorar las diferentes opciones disponibles hemos optado por utilizar de base la normativa UNE 71506. Este manual se centra en el análisis forense y lo explica de manera sencilla y concisa pero mantiene la base funcional que necesitamos. 

El análisis forense de evidencias digitales debe seguir un proceso metódico, auditable y repetible. El objetivo es responder a preguntas sobre el tiempo de intrusión, su origen, los sistemas afectados, los métodos usados, y los activos alterados o accedidos.
Antes de iniciar el análisis, se deben cumplir los siguientes pasos preliminares:

#### Pasos Preliminares

1. **Comprobar competencias**: Verificar si el análisis solicitado está dentro de la competencia del laboratorio forense.
2. **Revisión documental**: Estudiar la documentación adjunta para contextualizar las evidencias y las relaciones entre ellas.
3. **Supervisión de la cadena de custodia**: Comprobar quién recogió las evidencias, cuándo, dónde, y cómo se almacenaron hasta llegar al laboratorio.
4. **Autorizaciones**: Obtener permisos legales para realizar el análisis, según la normativa vigente.
5. **Comprobación de estado**: Verificar que las evidencias no están dañadas y son susceptibles de análisis.
6. **Evidencias adicionales**: Si se encuentran nuevas evidencias (memorias, discos, etc.), estas deben ser registradas y se deben obtener nuevas autorizaciones para analizarlas.
7. **Hora del BIOS**: Registrar la hora del BIOS del equipo donde se alojan los discos para poder comparar la cronología.
8. **Establecer prioridades**: Definir criterios de prioridad en el análisis.

#### Recuperación de ficheros borrados
Este proceso busca recuperar archivos eliminados de las estructuras de almacenamiento (como tablas FS o MFT). Además, se recuperan archivos de áreas no asignadas del disco o ficheros "huérfanos". También se localizan fragmentos de archivos mediante la búsqueda de sus cabeceras. La trazabilidad de toda la información recuperada debe estar documentada en el informe.

#### Estudio de particiones y sistemas de archivos
Se analiza la estructura de almacenamiento (particiones, volúmenes físicos y lógicos, sistemas RAID, etc.). Este proceso incluye:
- **Enumeración** de particiones actuales y previas.
- **Identificación** de áreas ocultas (HPA, DCO).
- **Reconocimiento** de sistemas de archivos en contenedores y discos cifrados.
- **Análisis** de archivos comprimidos y sus cabeceras.

#### Estudio del sistema operativo
Se identifican los sistemas operativos instalados, su fecha de instalación, actualizaciones, usuarios, privilegios y las últimas actividades registradas. También se examinan los dispositivos de hardware y software reconocidos por el sistema.

#### Estudio de la seguridad implementada
Este proceso evalúa si las evidencias han sido comprometidas mediante métodos de intrusión, modificación o eliminación. Se debe identificar malware (virus, troyanos, etc.) y evaluar su impacto en el sistema.

#### Análisis detallado de los datos obtenidos
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

Para realizar un buen análisis forense nos hemos basado en la norma UNE 71506 ya que se adapta perfectamente al contexto de leyes nacionales y legales en España. A continuación le dejo un ejemplo de como se debería hacer un acta de documentación de hallazgos:
#### Acta de Documentación de Hallazgos - Análisis Forense Digital

| Sección | Contenido |
|---------|-----------|
| **Información General** | **Caso**: [Número de caso]<br>**Fecha**: [Fecha actual]<br>**Analista**: [Nombre del analista] |
| **1. Documento de Recepción de Evidencias/Muestras Electrónicas** | **Fecha y hora de recepción**: [Fecha y hora]<br>**Número de referencia**: [Número único de referencia]<br>**Solicitud del análisis**: [Nombre y cargo]<br>**Motivo del análisis**: [Breve descripción del caso]<br><br>**Evidencias recibidas**:<br>Evidencia 1: [Descripción breve de la evidencia 1]<br>Evidencia 2: [Descripción breve de la evidencia 2] |
| **2. Registro de Documentación Recibida** | - Descripción detallada de las evidencias electrónicas<br>- Informe de la cadena de custodia<br>- Solicitud formal de estudios a realizar<br>- Autorizaciones legales para el análisis |
| **3. Registro de Reseña de las Evidencias Electrónicas** | **Evidencia 1**: [Nombre/Número de referencia]<br>**Tipo de dispositivo**: [Ej. Disco duro externo]<br>**Marca y modelo**: [Detalles]<br>**Número de serie**: [Número]<br>**Capacidad**: [Ej. 1 TB]<br>**Estado físico**: [Ej. Sin daños aparentes]<br>**Observaciones adicionales**: [Cualquier detalle relevante]<br><br>**Evidencia 2**: [Repetir el proceso para cada evidencia] |
| **4. Registro del Tratamiento Inicial** | **Herramienta utilizada**: [Ej. FTK Imager]<br>**Fecha y hora de inicio**: [Fecha y hora]<br>**Fecha y hora de finalización**: [Fecha y hora]<br>**Hash de la imagen original**: [Valor hash]<br>**Hash de la copia forense**: [Valor hash]<br>**Observaciones**: [Cualquier incidencia o detalle relevante] |
| **5. Registro de Situación de Evidencias/Muestras** | **Evidencia 1**: [Nombre/Número de referencia]<br>**Ubicación actual**: [Ej. Laboratorio forense, armario de seguridad]<br>**Estado actual**: [Ej. En análisis, En espera, Análisis completado]<br><br>**Operaciones realizadas**:<br>[Fecha/hora] - [Operación] - [Responsable]<br>[Fecha/hora] - [Operación] - [Responsable] |
| **6. Registro de Tareas del Análisis Inicial** | **Tarea 1**:<br>Descripción: [Descripción breve]<br>Inicio: [Fecha y hora]<br>Finalización: [Fecha y hora]<br>Hallazgos preliminares: [Resumen breve]<br><br>**Tarea 2**:<br>Descripción: [Descripción breve]<br>Inicio: [Fecha y hora]<br>Finalización: [Fecha y hora]<br>Hallazgos preliminares: [Resumen breve] |
| **7. Registro de Tareas del Análisis de Datos Definitivo** | **Tarea 1**:<br>Descripción: [Descripción detallada]<br>Inicio: [Fecha y hora]<br>Finalización: [Fecha y hora]<br>Herramientas utilizadas: [Lista de herramientas]<br>Hallazgos: [Descripción detallada hallazgos]<br>Ubicación temporal evidencia: [Si aplicable]<br><br>**Tarea 2**: [Repetir para cada tarea del análisis definitivo] |
| **Conclusiones Preliminares** | [Breve resumen de los hallazgos más significativos y su relevancia para el caso] |
| **Firma del Analista** | [Nombre del Analista]<br>[Firma]<br>[Fecha] |

### Presentación de resultados
Hemos seleccionado el UNE 71506 ya te permite asegurar el cumplimiento de las normativas nacionales, lo cual es muy importante para los procedimientos legales en España. Si bien otras normas como la ISO/IEC 27037:2012(E) o la NIST SP 800-86 ofrecen buenas indicaciones, su enfoque internacional no se alinea tan directamente con las necesidades específicas de un proceso forense en España.Aquí tenemos un acta de ejemplo de como se deberían presentar las pruebas para un análisis forense.

#### Acta de Presentación de Pruebas - Análisis Forense

#### Información General

| Campo | Descripción |
|-------|-------------|
| Número de Caso | [Insertar número] |
| Fecha del Informe | [Insertar fecha] |
| Perito Informático | [Nombre del perito] |
| Organismo Solicitante | [Nombre del organismo] |

#### Asunto

[Breve descripción del caso y objetivo del análisis forense]

#### Evidencias/Muestras Recibidas

| Ítem | Descripción | Número de Serie | Estado de Recepción |
|------|-------------|-----------------|---------------------|
| 1    | [Ej. Disco duro externo] | [Número] | [Ej. Sin daños aparentes] |
| 2    | [Ej. Smartphone] | [Número] | [Ej. Pantalla agrietada] |

#### Resolución o Estudios Efectuados sobre las Evidencias/Muestras

1. [Descripción del primer estudio realizado]
   - Metodología: [Breve explicación]
   - Herramientas utilizadas: [Lista de herramientas]
   - Hallazgos principales: [Resumen de hallazgos]

2. [Descripción del segundo estudio realizado]
   - Metodología: [Breve explicación]
   - Herramientas utilizadas: [Lista de herramientas]
   - Hallazgos principales: [Resumen de hallazgos]

#### Situación Final de las Evidencias/Muestras


| Ítem | Estado Final | Ubicación Actual |
|------|--------------|------------------|
| 1    | [Ej. Intacto] | [Ej. Devuelto al organismo solicitante] |
| 2    | [Ej. Sin cambios] | [Ej. Almacenado en laboratorio forense] |


#### Conclusiones Finales

[Resumen conciso de las conclusiones principales del análisis forense, utilizando un lenguaje claro y comprensible]

#### Anexos del Informe

1. [Título del Anexo 1]: [Breve descripción del contenido]
2. [Título del Anexo 2]: [Breve descripción del contenido]

#### Declaración de Conformidad

Este informe pericial ha sido elaborado siguiendo las directrices de la norma UNE 71506 y UNE 197001, asegurando el cumplimiento de las normativas nacionales para procedimientos legales en España.

#### Entrega y Custodia de Evidencias

Se adjunta el recibo de control de evidencias para su devolución firmada, confirmando la recepción de este informe y las muestras objeto de estudio por parte del organismo solicitante.

[Firma del Perito Informático]
[Nombre del Perito]
[Número de Colegiado]
[Fecha]


___
## Resumen de la metodología

Una vez realizada nuestra metodología, esquematizaremos las partes que la componen para tener una guía visual de cómo funciona de forma muy reducida el flujo de acciones. Veremos los cuatro apartados que la componen:

### [Adquisición de evidencia digital](#adquisición-de-evidencia-digital)

[Acta de Adquisición de Evidencias Digitales](#acta-de-adquisición-de-evidencias-digitales)

| Dispositivo encendido | Dispositivo apagado |
| :-------------------: | :-----------------: |
| 1. Adquisición memoria volátil <br> 2. Adquisición memoria no volátil <br> 3. Apagar dispositivo <br> 4. Adquisición de cables <br> 5. Tapar botón de encendido y lector de CDs <br> 6. Almacenamiento | 1. Adquisición memoria no volátil <br> 2. Apagar dispositivo <br> 3. Adquisición de cables <br> 4. Tapar botón de encendido y lector de CDs <br> 5. Almacenamiento|


### [Preservación y almacenamiento de la evidencia](#preservación-y-almacenamiento-de-la-evidencia)

La fase de preservación se basa en la UNE 71506:2013, que ofrece un enfoque detallado para mantener la integridad de las evidencias digitales. Es crucial preservar la información tal como se encuentra originalmente, asegurando su validez y confiabilidad para análisis posteriores y posibles contraanálisis.

Hemos creado una parte del informe centrado en la [cadena de custodia](#cadena-de-custodia).

| Sección | Título |
|---------|--------|
| 1       | INFORMACIÓN DEL CASO |
| 2       | DESCRIPCIÓN EVIDENCIA EN ORIGINAL |
| 3       | PRESERVACIÓN DE LA EVIDENCIA ORIGINAL |
| 4       | CREACIÓN Y VERIFICACIÓN DE COPIAS |
| 5       | REGISTRO DE ACCESOS Y VERIFICACIONES |

Esta tabla proporciona una visión general de las principales secciones de la cadena de custodia, facilitando una rápida referencia a los aspectos clave del proceso de preservación de evidencias digitales.


### [Análisis de la evidencia](#análisis-de-la-evidencia)

| Fase | Descripción |
|------|-------------|
| **[Pasos preliminares](#pasos-preliminares)** | 1. Comprobar competencias<br>2. Revisión documental<br>3. Supervisión de la cadena de custodia<br>4. Autorizaciones<br>5. Comprobación de estado<br>6. Evidencias adicionales<br>7. Hora del BIOS<br>8. Establecer prioridades |
| **[Recuperación de ficheros borrados](#recuperación-de-ficheros-borrados)** | - Recuperar archivos eliminados<br>- Localizar fragmentos de archivos<br>- Documentar trazabilidad |
| **[Estudio de particiones y sistemas de archivos](#estudio-de-particiones-y-sistemas-de-archivos)** | - Enumeración de particiones<br>- Identificación de áreas ocultas<br>- Reconocimiento de sistemas de archivos<br>- Análisis de archivos comprimidos |
| **[Estudio del sistema operativo](#estudio-del-sistema-operativo)** | - Identificar sistemas operativos instalados<br>- Examinar usuarios y privilegios<br>- Analizar dispositivos de hardware y software |
| **[Estudio de la seguridad implementada](#estudio-de-la-seguridad-implementada)** | - Evaluar compromiso de evidencias<br>- Identificar malware<br>- Evaluar impacto en el sistema |
| **[Análisis detallado de los datos obtenidos](#análisis-detallado-de-los-datos-obtenidos)** | 1. Información del sistema<br>2. Dispositivos conectados<br>3. Escritorio y papelera<br>4. Conexiones de red<br>5. Comunicaciones<br>6. Registros del sistema<br>7. Espacios no asignados<br>8. Archivos de sistema<br>9. Cola de impresión<br>10. Enlaces recientes<br>11. Carpetas de usuarios<br>12. Programas instalados<br>13. Metadatos<br>14. Aplicaciones de virtualización<br>15. Bases de datos<br>16. Archivos cifrados<br>17. Navegación por Internet<br>18. Correos electrónicos<br>19. Registros de mensajería |

### Documentación de hallazgos

1. Se basa en la norma UNE 71506, adaptada al contexto legal español.
2. Incluye un acta de documentación de hallazgos con las siguientes secciones:
   - **Información General**
   - **Documento de Recepción de Evidencias/Muestras Electrónicas**
   - **Registro de Documentación Recibida**
   - **Registro de Reseña de las Evidencias Electrónicas**
   - **Registro del Tratamiento Inicial**
   - **Registro de Situación de Evidencias/Muestras**
   - **Registro de Tareas del Análisis Inicial**
   - **Registro de Tareas del Análisis de Datos Definitivo**
   - **Conclusiones Preliminares**
   - **Firma del Analista**

3. Cada sección contiene campos específicos para detallar la información relevante del análisis forense.

### Presentación de resultados

1. Se utiliza la norma UNE 71506 para asegurar el cumplimiento de normativas nacionales en España.
2. Se presenta un acta de presentación de pruebas con las siguientes secciones:
   - **Información General**
   - **Asunto**
   - **Evidencias/Muestras Recibidas**
   - **Resolución o Estudios Efectuados sobre las Evidencias/Muestras**
   - **Situación Final de las Evidencias/Muestras**
   - **Conclusiones Finales**
   - **Anexos del Informe**
   - **Declaración de Conformidad**
   - **Entrega y Custodia de Evidencias**

3. El formato es más conciso y orientado a la presentación de resultados.
4. Se adjunta un recibo de control de evidencias para su devolución firmada.

