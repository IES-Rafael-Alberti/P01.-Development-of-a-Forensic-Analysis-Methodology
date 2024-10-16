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
    Define el formato de Evidence Record Syntax (ERS) o Sintaxis de Registro de Evidencias en español complementando al RFC 4998 adaptando el formato para expresarlo en XML y poder integrarlos facilmente en sistemas modernos.

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

Para adaptar la fase de analisis, despues de valorar las diferentes opciones disponibles hemos optado por utilizar de base la normativa UNE 71506. 
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


### Presentación de resultados


___
## Resumen de la metodología
### Adquisición de evidencia digital


### Preservación y almacenamiento de la evidencia


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
  1. Información del sistema.
  2. Dispositivos conectados (USBs, impresoras, móviles).
  3. Escritorio y papelera de reciclaje.
  4. Conexiones de red y protocolos.
  5. Comunicaciones realizadas.
  6. Registros del sistema.
  7. Espacios no asignados del disco.
  8. Archivos de hibernación y paginación.
  9. Cola de impresión.
  10. Enlaces a archivos recientes.
  11. Carpetas de usuarios.
  12. Programas instalados.
  13. Metadatos.
  14. Aplicaciones de virtualización.
  15. Bases de datos.
  16. Archivos cifrados y particiones protegidas.
  17. Historial de navegación y cookies.
  18. Correos electrónicos.
  19. Registros de mensajería instantánea y chats.

#### Pasos preliminares


### Documentación de hallazgos


### Presentación de resultados

___
