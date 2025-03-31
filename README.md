# SIMULACRO-DE-EXAMEN


Parte I: Conceptos y Teoría
Pregunta 1: Modelos OSI y TCP/IP

*a) Describe las principales diferencias entre el modelo OSI y el modelo TCP/IP, considerando aspectos como el número de capas, la orientación (teórica vs. práctica) y el manejo de la capa de aplicación.*

*b) Explica brevemente las ventajas y limitaciones de cada uno de estos modelos.*


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


Pregunta 2: 
Función de la Capa de Transporte
*Explica el papel de la capa de transporte en ambos modelos (OSI y TCP/IP). En tu respuesta, menciona cómo se garantiza la entrega de datos y da ejemplos de protocolos asociados a esta capa.*


La capa de transporte en los modelos OSI y TCP/IP tiene como función principal garantizar la comunicación confiable de extremo a extremo entre dispositivos en una red. Esta capa se encarga de asegurar que los datos lleguen completos, en el orden correcto y sin errores.

En el modelo OSI, la capa de transporte es la cuarta capa. Proporciona servicios como el control de flujo, detección y corrección de errores, y control de la conexión. Divide los datos en segmentos y se asegura de que la información transmitida por las capas superiores llegue correctamente a su destino, independientemente de la red utilizada.

En el modelo TCP/IP, también existe una capa de transporte que cumple funciones similares. Utiliza dos protocolos principales:
	•	TCP (Transmission Control Protocol): Es un protocolo orientado a conexión. Asegura la entrega de los datos utilizando confirmaciones (ACKs), números de secuencia y retransmisiones en caso de pérdida. Garantiza fiabilidad, orden y control de flujo.
	•	UDP (User Datagram Protocol): Es un protocolo no orientado a conexión. No garantiza la entrega ni el orden de los datos, pero permite una transmisión más rápida. Es útil en aplicaciones en tiempo real como videollamadas o juegos en línea.

Ambos modelos coinciden en que la capa de transporte permite a las aplicaciones comunicarse de forma robusta, gestionando cómo se envían y reciben los datos entre los extremos de una red.

