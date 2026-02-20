# Laboratorio-Redes---Interconexion

Laboratorio 1 Red - Interconexión: 

Resumen

En este laboratorio se diseñó y configuró una topología de red doméstica utilizando Cisco Packet Tracer, con el propósito de permitir que los dispositivos de la familia Pérez puedan acceder al sitio web disneyplus.com mediante servicios en la nube. La solución se fundamenta en un modelo Cliente-Servidor, donde los dispositivos finales solicitan recursos a un servidor remoto configurado con IP estática 1.1.1.1.

Se implementaron servicios esenciales como DHCP para la asignación automática de direcciones IP dentro de la red local, DNS para la traducción del nombre de dominio a su dirección IP correspondiente y HTTP para la entrega del contenido web a los clientes. La comunicación fue comprobada mediante pruebas de conectividad y acceso exitoso desde los navegadores, evidenciando que el flujo de datos entre la red doméstica y la nube funciona correctamente y cumple con los principios del modelo OSI/TCP-IP.

Introducción:
En este laboratorio se busca como hacer una topología de red en donde se permita integrar dispositivos con servicios en la nube, y que existe comunicación de datos entre ellos. Todo eso logrado en Cisco Packet Tracer.

Cisco Packet Tracer
	Cisco Packet Tracer es un software de simulación de redes de computadores. El objetivo principal es ayudar a estudiantes a aprender los principios de redes de una forma mas practica sin la necesidad de conseguir dispositivos costosos. Aunque no remplaza practicas en equipamiento real, si ayuda a desarrollar habilidades en el diseño y simulación de redes. [1]


Marco Teórico:

Red de computadores
	Una red de computadores es un grupo de dispositivos interconectados que pueden recibir y/o enviar datos. Puede ser cualquier dispositivo, como puede ser un computador tradicional, un celular, o hasta un sensor inteligente. El internet es una gigantesca red de redes de computadores que comunica computadores de todo el mundo entre si. [2]

Topologías de red.
	Si en una red de computadores esta conectada a muchos dispositivos, surge la cuestión de como se sabe para quien es cual mensaje. Existen ciertas formas de diseñar una topología. Define la organización de los nodos. En este proyecto se destaca la topología de Estrella en el segmento doméstico y una conexión Punto a punto hacia la WAN
- Anillo: Cada dispositivo esta conectado en cadena entre ellos mismos. 
- Malla: Cada dispositivo esta individualmente conectado al resto de dispositivos.
- Estrella: Existe un dispositivo central que esta individualmente conectado a cada dispositivo.
- Bus: Cada dispositivo esta conectado a una gran conexión que conecta al resto de dispositivos. Esta conexión grande funciona como una calle, y los dispositivos como las casas que comparten la calle.
- Arbol: Los dispositivos están conectados en una forma de árbol. Es decir, esta formados de una forma jerárquica.
	Cada topología tiene su propia ventaja y desventaja. [2].

Tipos de redes:
- LAN (Red de area local)
	Cubre un area limitada. Puede ser una casa o un pequeño colegio. [2]
- WLAN (Red de area local inalambrica)
	Lo mismo que el LAN, pero permite conexiones inalámbricas de radio tipo Wi-Fi. [3]
- WAN (Red de area ancha)
	Una red que se extiende por un área geográfica grande y cubre muchos LANs y WLANs. [2]

Desarrollo de la Solución: Elementos de Red, el sistema se basa en un modelo Cliente-Servidor, donde los dispositivos finales solicitan recursos a un nodo centralizado [4].
-Dispositivos:
End devices: Clientes(Laptop, Smartphone,PC) que consumen servicios.
Wireless Router: Punto de acceso y gestión de IPs locales via DHCP. [5]
Cloud (Internet): Simulación de infraestructura de transporte global.
Server (Disney): Host con IP estática 1.1.1.1 que provee servicios DNS y Web.[6]

Protocolos y Servicios
-DNS: Traduce la URL disneyplus.com a la IP 1.1.1.1. [6]
-HTTP: Entrega el contenido web solicitado por los navegadores de los clientes.[6]
-DHCP: Asigna dinámicamente las IPs 192.168.0.x a los dispositivos domésticos.[5]

Evaluación y Resultados

Se realizaron pruebas de extremo a extremo:

-Validación IP: El Smartphone recibió correctamente la configuración 192.168.0.100 vía DHCP.
-Mapeo de Nube: Se configuró el enlace físico en la nube entre los puertos Coaxial7 y Ethernet6.
-Resolución de Nombres: Desde la Laptop se accedió exitosamente a http://disneyplus.com, confirmando la operatividad del DNS.

Desafíos y Conclusiones
Desafío: El mapeo correcto de las interfaces dentro del objeto "Cloud" en Packet Tracer, ya que requiere una correspondencia exacta entre puertos físicos para que el tráfico circule.

Conclusión: La simulación demuestra que la infraestructura de red es transparente para el usuario final cuando los servicios de resolución de nombres (DNS) están correctamente integrados.

[1] (s.a.). What is Cisco Packet Tracer. Geeksforgeeks. Recuperado de: https://www.geeksforgeeks.org/computer-networks/what-is-cisco-packet-tracer/

[2] (s.a.). Redes de computadores. Khan Academy. Recuperado de: https://es.khanacademy.org/computing/ap-computer-science-principles/the-internet/x2d2f703b37b450a3:connecting-networks/a/computer-networks-overview

[3] (s.a.). What is WLAN? HPE. Recuperado de: https://www.hpe.com/asia_pac/en/what-is/wlan.html

[4] IBM, "Client-server model definition," 2024. [En línea]. Recuperado de: https://www.ibm.com/docs/en/cloud-paks/cp-biz-design/1.1.x?topic=architecture-client-server-model

[5] Cisco Systems, "Understanding DHCP Basics," 2024. [En línea]. Recuperado de: https://www.cisco.com/c/en/us/support/docs/ip/dynamic-address-allocation-resolution/12714-10.html

[6] Cloudflare, "What is DNS? | How DNS works," 2024. [En línea]. Recuperado de: https://www.cloudflare.com/learning/dns/what-is-dns/
