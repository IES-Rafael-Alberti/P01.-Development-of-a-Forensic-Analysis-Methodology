# P01.-Development-of-a-Forensic-Analysis-Methodology
## Comparativa entre las distintas normas
|              | Enfoque general | Destaca por |
| :----------: | :-------------: | :---------: |
| **UNE 71506** | Adquisición , preservación y gestión de las evidencias digitales | Norma más específica para España adaptando estándares internacionales y se centra en la validez legal de las evidencias|
| **ISO/IEC 27037:2012(E)** | Identificación, adquisición y preservación de las evidencias digitales | Es aplicable a nivel internacional y tiene una gran adaptavilidad |
| **RFC 3227** | Adquisición y preservación de las evidencias digitales | Énfasis en documentar cada paso del proceso forense |
| **NIST Special Publication 800-86** | Proceso completo del análisis forense | Ser usado a nivel internacional y centrarse en como usar el análisis forense para responder a incidentes de seguridad |
| **RFC 4810** | Gestión y preservación de las evidencias digitales | Centrarse en la preservación de las evidencias a largo plazo |
| **RFC 4998** | Gestión y preservación de las evidencias digitales | Describir un formato estándar para los registros de evidencia |
| **RFC 6283** | Gestión y preservación de las evidencias digitales | Adaptar el formato definido en el RFC 4998 adaptándolo para expresarlo en XML y poder integrarlos facilmente en sistemas modernos |
| **UNE 71505-3** | Gestión y preservación de las evidencias digitales | Se centra más en la admisión legal de las evidencias |
| **UNE 197010** | Documentación | Establecer los requisitos que deben tener los informes |

## Metodología propia
### Adquisición de evidencia digital
Nuestro primer paso deberá identificar las evidencias digitales y objetos relacionados (por ejemplo papeles con posibles contraseñas) de la escena sin modificar el estado de estas (apagar o encender dispositivos) y asegurarnos de que nadie más manipule estas evidencias.

El siguiente paso será determinar si debemos de recolectar las evidencias para realizar su adquisición en el laboratorio o adquirirlas in situ. Para esto debemos de tener en cuenta si los dispositivos están encendidos, la volatilidad de las posibles evdencias, la existencia de encriptado de los discos ya que la contraseña puede estar almacenada como memoria volatil o en otro dispositivo.

#### Recolección de dispositivos encendidos
1) Considerar la adquisición de la memoria volátil del dispositivo y de su estado actual antes de apagarlo. Debemos de realizar esta adquisición documentando todo el proceso y con nuestras propias herramientas ya que no podemos confiar en las del propio dispositivo.
2) Apagar el dispositivo y desconectar su batería en caso de ser un dispositivo portatil.
3) Etiquetar, desconectar y asegurar todos los cables del dispositivo, etiquetando también los puertos para reconstruirlo luego.
4) Poner cinta adhesiva sobre el botón de encendido del dispositivo para evitar su encendido, además de sobre el lector de DVDs en caso de tenerlo.
5) Almacenar el dispositivo en un recipiente adecuadoy sellandolo.

#### Recolección de dispositivos apagados
1) Desconectar el cable de corriente retirando primero el extremo conectado al dispositivo.
2) Etiquetar, desconectar y asegurar todos los cables del dispositivo, etiquetando también los puertos para reconstruirlo luego.
3) Poner cinta adhesiva sobre el botón de encendido del dispositivo para evitar su encendido, además de sobre el lector de DVDs en caso de tenerlo.
4) Almacenar el dispositivo en un recipiente adecuadoy sellandolo.

#### Adquisición de dispositivos encendidos
1) Considerar la adquisición de la memoria volátil del dispositivo y de su estado actual antes de apagarlo. Debemos de realizar esta adquisición documentando todo el proceso y con nuestras propias herramientas ya que no podemos confiar en las del propio dispositivo.
2) Realizar la adquisición de la memoria no volátil del dispositivo documentando todo el proceso y realizando la imagen usando una herramienta validada. Esta imagen deberá ser almacenada en un dispositivo de almacenamiento nuevo o formateado de manera segura.

#### Adquisición de dispositivos apagados
1) Asegurarnos de que el dispositivo realmente está apagado.
2) Deconectar el dispositivo de almacenamiento si aún está conectado al equipo.
3) Realizar la imagen del dispositivo de almacenamiento usando una herramienta validada, documentando el proceso y almacenando la imagen en un dispositivo de almacenamiento nuevo o formateado de manera segura.
4) Almacenar el dispositivo en un recipiente adecuadoy sellandolo.
