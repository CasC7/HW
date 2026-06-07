# HW

CAP 2

La siguiente evidencia muestra el análisis de una prueba de Denegación de Servicio (DoS) realizada en un entorno de laboratorio controlado sobre la máquina vulnerable Metasploitable 2 (192.168.100.20). Para esta práctica se utilizaron las herramientas tcpdump, hping3 y tshark con el objetivo de generar, capturar y analizar tráfico malicioso de tipo SYN Flood.

En la primera parte de la evidencia se observa la captura de tráfico realizada con tcpdump, herramienta utilizada para monitorear y almacenar los paquetes de red generados durante la prueba. Posteriormente, mediante hping3 se ejecutó un ataque SYN Flood dirigido al puerto 80 del servidor web de Metasploitable 2, enviando una gran cantidad de paquetes TCP SYN para saturar la tabla de conexiones del servicio HTTP.

Finalmente, el archivo de captura fue analizado con tshark utilizando estadísticas de entrada/salida por segundo. Los resultados muestran un incremento considerable en la cantidad de paquetes por segundo respecto al tráfico normal (baseline), evidenciando un comportamiento anómalo característico de un ataque DoS. Este tipo de análisis permite comprender cómo herramientas de monitoreo e IDS/SIEM pueden detectar patrones de tráfico inusuales asociados a intentos de agotamiento de recursos en servidores.

La práctica permitió identificar el impacto que un SYN Flood puede generar sobre la disponibilidad de servicios de red, así como la importancia de implementar mecanismos de defensa como rate limiting, fail2ban y monitoreo continuo del tráfico.
