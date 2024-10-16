# P01.-Development-of-a-Forensic-Analysis-Methodology

Para nuestra normativa, despues de valorar las diferentes opciones disponibles hemos optado por utilizar de base la normativa UNE 71506. 
El análisis forense de evidencias digitales debe seguir un proceso metódico, auditable y repetible. El objetivo es responder a preguntas sobre el tiempo de intrusión, su origen, los sistemas afectados, los métodos usados, y los activos alterados o accedidos.

## Pasos preliminares

Antes de iniciar el análisis, se deben cumplir los siguientes pasos preliminares:

1. **Comprobar competencias**: Verificar si el análisis solicitado está dentro de la competencia del laboratorio forense.
2. **Revisión documental**: Estudiar la documentación adjunta para contextualizar las evidencias y las relaciones entre ellas.
3. **Supervisión de la cadena de custodia**: Comprobar quién recogió las evidencias, cuándo, dónde, y cómo se almacenaron hasta llegar al laboratorio.
4. **Autorizaciones**: Obtener permisos legales para realizar el análisis, según la normativa vigente.
5. **Comprobación de estado**: Verificar que las evidencias no están dañadas y son susceptibles de análisis.
6. **Evidencias adicionales**: Si se encuentran nuevas evidencias (memorias, discos, etc.), estas deben ser registradas y se deben obtener nuevas autorizaciones para analizarlas.
7. **Hora del BIOS**: Registrar la hora del BIOS del equipo donde se alojan los discos para poder comparar la cronología.
8. **Establecer prioridades**: Definir criterios de prioridad en el análisis.

### 1. Recuperación de ficheros borrados
Este proceso busca recuperar archivos eliminados de las estructuras de almacenamiento (como tablas FS o MFT). Además, se recuperan archivos de áreas no asignadas del disco o ficheros "huérfanos". También se localizan fragmentos de archivos mediante la búsqueda de sus cabeceras. La trazabilidad de toda la información recuperada debe estar documentada en el informe.

### 2. Estudio de particiones y sistemas de archivos
Se analiza la estructura de almacenamiento (particiones, volúmenes físicos y lógicos, sistemas RAID, etc.). Este proceso incluye:
- Enumeración de particiones actuales y previas.
- Identificación de áreas ocultas (HPA, DCO).
- Reconocimiento de sistemas de archivos en contenedores y discos cifrados.
- Análisis de archivos comprimidos y sus cabeceras.

### 3. Estudio del sistema operativo
Se identifican los sistemas operativos instalados, su fecha de instalación, actualizaciones, usuarios, privilegios y las últimas actividades registradas. También se examinan los dispositivos de hardware y software reconocidos por el sistema.

### 4. Estudio de la seguridad implementada
Este proceso evalúa si las evidencias han sido comprometidas mediante métodos de intrusión, modificación o eliminación. Se debe identificar malware (virus, troyanos, etc.) y evaluar su impacto en el sistema.

### 5. Análisis detallado de los datos obtenidos
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
