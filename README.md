# SIMULACRO-DE-EXAMEN


**Parte I: Conceptos y Teoría
Pregunta 1: Modelos OSI y TCP/IP**

**a) Describe las principales diferencias entre el modelo OSI y el modelo TCP/IP, considerando aspectos como el número de capas, la orientación (teórica vs. práctica) y el manejo de la capa de aplicación.**

**b) Explica brevemente las ventajas y limitaciones de cada uno de estos modelos.**


A)
-MODELO OSI-

Numero de capas--> Tiene 7 capas: Fisica, enlace de datos, red, transporte, sesion, presentacion, Aplicacion
Orientacion--> Teorica: fue diseñado como un modelo de referencia estandarizado
Separacion de conceptos--> Distingue claramente entre servicio, interfaz y protocolo
Capas superiores--> Incluye sesion y presentacion como capas independientes
Soporte para conexiones--> Solo soporta comunicacion orientada a conexion en la capa de transporte


-MODELO TCP/IP-

Numero de capas--> Tiene 4 capas: Acceso a red, Internet, Transporte y Aplicacion
Orientacion--> Practica: basado en protocolos reales en uso como IP, TCP y UDP
Separacion de conceptos--> No distingue de forma clara estos conceptos (puede causar ambigüedad en ingenierÃ­a de software)
Capas superiores--> Estas funciones estan integradas dentro de la capa de aplicacion
Soporte para conexiones--> Soporta orientado y no orientado a conexion (TCP y UDP)


B)

--Modelo OSI--

Ventajas:
	•	Buena estructura modular y clara separación entre capas
	•	Útil como herramienta de enseñanza y diseño conceptual
	•	Fomenta la interoperabilidad y estandarización

Limitaciones:
	•	Complejo y poco implementado tal cual en sistemas reales
	•	Algunos servicios están duplicados en varias capas, lo que puede generar ineficiencia


--Modelo TCP/IP--

Ventajas:
	•	Modelo realista y funcional, usado ampliamente en Internet
	•	Protocolos maduros y probados (TCP, IP, UDP, etc.)
	•	Flexible y adaptable a nuevas tecnologías

Limitaciones:
	•	Menor claridad en la separación de funciones y capas
	•	Dificultad para mapearlo directamente a ciertos entornos teóricos
	•	No incluye explícitamente capas como sesión o presentación





**Pregunta 2: 
Función de la Capa de Transporte**

**Explica el papel de la capa de transporte en ambos modelos (OSI y TCP/IP). En tu respuesta, menciona cómo se garantiza la entrega de datos y da ejemplos de protocolos asociados a esta capa.**


La capa de transporte en los modelos OSI y TCP/IP tiene como función principal garantizar la comunicación confiable de extremo a extremo entre dispositivos en una red. Esta capa se encarga de asegurar que los datos lleguen completos, en el orden correcto y sin errores.

En el modelo OSI, la capa de transporte es la cuarta capa. Proporciona servicios como el control de flujo, detección y corrección de errores, y control de la conexión. Divide los datos en segmentos y se asegura de que la información transmitida por las capas superiores llegue correctamente a su destino, independientemente de la red utilizada.

En el modelo TCP/IP, también existe una capa de transporte que cumple funciones similares. Utiliza dos protocolos principales:
	•	TCP (Transmission Control Protocol): Es un protocolo orientado a conexión. Asegura la entrega de los datos utilizando confirmaciones (ACKs), números de secuencia y retransmisiones en caso de pérdida. Garantiza fiabilidad, orden y control de flujo.
	•	UDP (User Datagram Protocol): Es un protocolo no orientado a conexión. No garantiza la entrega ni el orden de los datos, pero permite una transmisión más rápida. Es útil en aplicaciones en tiempo real como videollamadas o juegos en línea.

Ambos modelos coinciden en que la capa de transporte permite a las aplicaciones comunicarse de forma robusta, gestionando cómo se envían y reciben los datos entre los extremos de una red.




**Pregunta 3: TCP vs. UDP**
**Compara y contrasta TCP y UDP en términos de:**

**-Orientación a conexión
-Fiabilidad y control de errores
-Velocidad y orden de entrega
-Ejemplos de aplicaciones en las que se emplea cada uno**



 1. Orientación a conexión
	•	TCP: Es orientado a conexión. Antes de transmitir datos, establece una conexión entre emisor y receptor mediante un proceso llamado handshake de tres pasos.
	•	UDP: Es no orientado a conexión. No establece conexión previa; simplemente envía los datos sin verificar si el receptor está listo.
 

 2. Fiabilidad y control de errores
	•	TCP: Es fiable. Garantiza que los datos lleguen completos, sin errores y en el orden correcto. Utiliza:
	•	Confirmaciones de recepción (ACKs)
	•	Números de secuencia
	•	Retransmisión en caso de pérdida
	•	Control de flujo y congestión
	•	UDP: Es no fiable. No realiza control de errores, no hay confirmaciones ni retransmisiones. Si se pierden datos, el protocolo no los recupera.
 

  3. Velocidad y orden de entrega
	•	TCP: Es más lento debido a sus mecanismos de control, pero garantiza la entrega ordenada.
	•	UDP: Es más rápido, ideal para aplicaciones en tiempo real, pero no garantiza el orden ni la entrega.


 4. Ejemplos de aplicaciones
	•	TCP se usa en aplicaciones donde la fiabilidad es crucial:
	•	Navegadores web (HTTP/HTTPS)
	•	Correo electrónico (SMTP, IMAP, POP3)
	•	Transferencia de archivos (FTP)
 __
	•	UDP se usa en aplicaciones donde la velocidad es más importante que la fiabilidad:
	•	Streaming de audio y video (YouTube, Netflix)
	•	Videollamadas (Zoom, Skype)
	•	Juegos en línea
	•	DNS (Domain Name System)



**Pregunta 4: Protocolo para Transferencia de Archivos
a) ¿Qué protocolo de la capa de aplicación se utiliza tradicionalmente para la transferencia de archivos en redes TCP/IP?
b) Menciona al menos dos alternativas a este protocolo, resaltando sus diferencias principales en cuanto a seguridad o funcionalidad.**



A)

El protocolo tradicionalmente utilizado para la transferencia de archivos en redes TCP/IP es el FTP (File Transfer Protocol).
	•	FTP es un protocolo de la capa de aplicación que permite la transferencia de archivos entre un cliente y un servidor.
	•	Utiliza el puerto 21 para el control de la conexión y puede establecer una conexión separada para la transmisión de datos.
	•	Funciona sobre TCP, lo que garantiza una transferencia fiable.

 B)

 1.	SFTP (SSH File Transfer Protocol)
	•	Es una alternativa segura a FTP.
	•	Transfiere archivos a través de una conexión cifrada mediante SSH (puerto 22).
	•	A diferencia de FTP, todos los datos y credenciales están cifrados, lo que protege la información durante la transmisión.
	•	Proporciona funcionalidades adicionales como gestión de permisos y operaciones remotas sobre archivos.

2.	FTPS (FTP Secure)
	•	Es una extensión de FTP que añade soporte para cifrado SSL/TLS.
	•	Utiliza los mismos comandos que FTP, pero cifra la sesión de control y, opcionalmente, la de datos.
	•	Puede ser más compatible con clientes FTP tradicionales que SFTP, pero requiere certificados digitales.


**Pregunta 5:**


**Resolución de Nombres en DNS
Describe detalladamente el proceso de resolución de nombres en DNS, desde que un usuario ingresa una URL en el navegador hasta que se establece la conexión con el servidor web. Incluye en tu respuesta el rol de la caché y de los servidores raíz.**


1. El usuario ingresa una URL en el navegador.

Cuando un usuario escribe una dirección web (por ejemplo, www.ejemplo.com) en el navegador, este necesita conocer la dirección IP correspondiente para poder contactar con el servidor que aloja esa página web. Las redes solo entienden direcciones IP, no nombres.

⸻

2. El sistema operativo consulta la caché DNS local.

Antes de realizar una consulta externa, el sistema operativo revisa si la IP ya está guardada en su memoria caché.
Esta caché almacena las respuestas de consultas anteriores durante un período determinado (TTL - Time To Live).
	•	Si se encuentra la IP en caché, se utiliza directamente.
	•	Si no está o ha caducado, se continúa con la búsqueda.

⸻

3. Si no hay coincidencia, la solicitud se envía al servidor DNS configurado en la red.

Este es el servidor DNS recursivo, generalmente proporcionado por el proveedor de internet (ISP) o configurado manualmente (como Google DNS: 8.8.8.8).
Este servidor se encarga de buscar la IP correspondiente al nombre de dominio solicitado.

⸻

4. El servidor DNS busca en su caché. Si no encuentra la respuesta, reenvía la solicitud a servidores DNS raíz.

El servidor recursivo también mantiene una caché con resultados recientes.
	•	Si tiene la respuesta, la devuelve.
	•	Si no, envía la solicitud a uno de los 13 servidores raíz distribuidos globalmente.
Los servidores raíz no conocen las IP finales, pero saben qué servidor es responsable del dominio de nivel superior (por ejemplo, .com).

⸻

5. Los servidores raíz responden con el servidor de nombres del dominio.

El servidor raíz le dice al resolutor dónde encontrar el servidor TLD (Top-Level Domain) correspondiente.
Por ejemplo:
	•	Para www.ejemplo.com, el servidor raíz responderá con la dirección del servidor que gestiona .com.

⸻

6. El servidor DNS del dominio devuelve la dirección IP correspondiente.

El resolutor recursivo consulta al servidor autoritativo del dominio (por ejemplo, el de ejemplo.com).
Este servidor tiene la información exacta y responde con la dirección IP final del subdominio consultado (por ejemplo, www.ejemplo.com → 192.0.2.10).

⸻

7. El navegador establece una conexión con el servidor web usando la IP obtenida.

Con la dirección IP ya resuelta, el navegador inicia una conexión con el servidor web correspondiente, generalmente a través del protocolo TCP (puerto 80 para HTTP o 443 para HTTPS).
Luego, comienza la solicitud de contenido web (por ejemplo, descarga de la página HTML).




**Pregunta 6:**


**Comunicación en el Modelo TCP/IP
Explica el proceso de comunicación entre dos dispositivos en una red utilizando el modelo TCP/IP. Describe el rol y la función de cada capa (Aplicación, Transporte, Internet y Acceso a Red) durante el envío y recepción de datos.**



Durante el envío de datos (emisor):


1. Capa de Aplicación
	•	Es donde se genera la información que el usuario quiere enviar (por ejemplo, una solicitud HTTP desde un navegador o un correo electrónico).
	•	Los protocolos de esta capa incluyen: HTTP, FTP, SMTP, DNS, TELNET, entre otros.
	•	La capa entrega los datos a la capa de transporte.

2. Capa de Transporte
	•	Su función principal es garantizar la entrega fiable (si se usa TCP) o rápida pero sin garantías (si se usa UDP).
	•	Divide el mensaje en segmentos (TCP) o datagramas (UDP).
	•	Añade información de control como número de puerto, secuencia, ACKs, etc.
	•	Protocolos: TCP (fiable, orientado a conexión) y UDP (rápido, sin conexión).

3. Capa de Internet
	•	Se encarga de encaminar los datos desde el origen hasta el destino, incluso a través de múltiples redes.
	•	Añade la dirección IP de origen y destino.
	•	Utiliza el protocolo IP (Internet Protocol).
	•	Puede fragmentar los paquetes si son demasiado grandes para la red.

4. Capa de Acceso a la Red (o Enlace y Física)
	•	Gestiona la transmisión real a través del medio físico (cable, wifi, fibra, etc.).
	•	Añade la dirección MAC del dispositivo local y del destino en la misma red.
	•	Convierte los paquetes en tramas, luego en bits, y los envía físicamente.

⸻

Durante la recepción de datos (receptor):


El proceso se invierte, capa por capa:
	1.	Capa de Acceso a Red: Recibe los bits, reconstruye las tramas y verifica la integridad física.
	2.	Capa de Internet: Lee la dirección IP, valida que el paquete está destinado a él y lo reenvía a la capa de transporte.
	3.	Capa de Transporte: Reconstruye los segmentos/datagramas, asegura orden, fiabilidad (si usa TCP), y entrega los datos al puerto correspondiente.
	4.	Capa de Aplicación: Entrega los datos al programa final (como un navegador, app de correo, etc.), y el usuario ve la información.
