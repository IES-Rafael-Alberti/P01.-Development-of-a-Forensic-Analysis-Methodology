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


### Análisis de la evidencia


### Documentación de hallazgos


### Presentación de resultados


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


### Análisis de la evidencia


### Documentación de hallazgos


### Presentación de resultados
