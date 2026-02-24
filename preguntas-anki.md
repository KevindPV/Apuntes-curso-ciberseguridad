# Preguntas tipo Anki - Ciberseguridad

## Fundamentos

- **Pregunta:** ¿Cuál es la diferencia entre vulnerabilidad, amenaza y riesgo?
- **Respuesta:** Una vulnerabilidad es una debilidad, una amenaza es algo que puede explotar esa debilidad y el riesgo es la probabilidad e impacto de que eso ocurra.

- **Pregunta:** ¿Qué significa el principio de mínimo privilegio?
- **Respuesta:** Que cada usuario, proceso o sistema debe tener solo los permisos estrictamente necesarios para realizar su función.

## Redes

- **Pregunta:** ¿Qué diferencia hay entre un firewall stateful y uno stateless?
- **Respuesta:** El stateless filtra paquetes de forma aislada por reglas fijas; el stateful mantiene el estado de conexiones y decide usando contexto de sesión.

- **Pregunta:** ¿Para qué sirve la segmentación de red en ciberseguridad?
- **Respuesta:** Para limitar movimiento lateral, reducir superficie de ataque y contener incidentes.

## Aplicaciones web

- **Pregunta:** ¿Qué es una inyección SQL?
- **Respuesta:** Es un ataque donde se manipulan consultas SQL mediante entradas no validadas para leer, modificar o borrar datos.

- **Pregunta:** ¿Cómo se previene XSS de forma básica?
- **Respuesta:** Validando entradas, escapando salida según contexto (HTML/JS/URL) y aplicando políticas como Content Security Policy (CSP).

## Respuesta a incidentes

- **Pregunta:** ¿Cuáles son fases típicas de respuesta a incidentes?
- **Respuesta:** Preparación, identificación, contención, erradicación, recuperación y lecciones aprendidas.

- **Pregunta:** ¿Por qué es importante preservar evidencia durante un incidente?
- **Respuesta:** Para análisis forense, cumplimiento legal y entender causa raíz sin contaminar pruebas.

## Sección 5 - Seguridad en los sistemas

- **Pregunta:** ¿Cuál es la diferencia principal entre IDS e IPS?
- **Respuesta:** El IDS detecta y alerta actividad sospechosa; el IPS detecta y además bloquea tráfico malicioso en tiempo real.

- **Pregunta:** ¿Qué función cumple una DMZ en la arquitectura de red?
- **Respuesta:** Aislar servicios expuestos a Internet de la red interna para reducir impacto en caso de compromiso.

- **Pregunta:** ¿Por qué un WAF no reemplaza un firewall tradicional?
- **Respuesta:** Porque el WAF protege capa de aplicación web (HTTP/HTTPS), mientras el firewall tradicional filtra tráfico de red por IP/puerto/protocolo.

- **Pregunta:** ¿Qué diferencia hay entre SIEM y SOAR?
- **Respuesta:** SIEM centraliza y correlaciona eventos de seguridad; SOAR automatiza y orquesta la respuesta usando playbooks.

- **Pregunta:** ¿Para qué sirve EDR en un incidente?
- **Respuesta:** Para detectar comportamiento malicioso en endpoints y ejecutar acciones de contención como aislar equipos o poner archivos en cuarentena.

- **Pregunta:** En una arquitectura con DMZ, ¿por qué no se debe exponer directamente la red local a Internet?
- **Respuesta:** Porque aumenta mucho el riesgo; la DMZ crea una capa intermedia para publicar servicios y contener impactos si ocurre una intrusión.

- **Pregunta:** ¿Cómo interpretar rápidamente un diagrama con Red local, DMZ y firewalls?
- **Respuesta:** Primero ubica zonas, luego controles (firewalls/router) y finalmente el flujo de tráfico; la regla general es que Internet accede a DMZ, no directamente a la red local.

## Sección 5 - Video 25 (Portmaster)

- **Pregunta:** ¿Qué es Portmaster y cuál es su principal utilidad?
- **Respuesta:** Es un firewall gratuito y de código abierto que permite monitorear y controlar conexiones por aplicación para mejorar seguridad y privacidad.

- **Pregunta:** ¿Qué es DNS explicado de forma simple?
- **Respuesta:** Es el sistema que traduce nombres de dominio (como google.com) a direcciones IP para poder conectar con servidores en Internet.

- **Pregunta:** ¿Cómo contribuye Portmaster a proteger el DNS?
- **Respuesta:** Permite cambiar a resolutores más privados, monitorear consultas sospechosas y reducir rastreo/bloquear conexiones no deseadas.

## Sección 5 - Video 26 (Seguridad en la nube)

- **Pregunta:** ¿Cuáles son los tipos de nube más comunes?
- **Respuesta:** Privada, pública, híbrida y comunitaria.

- **Pregunta:** ¿Qué significa IaaS, PaaS y SaaS?
- **Respuesta:** IaaS = infraestructura como servicio, PaaS = plataforma como servicio, SaaS = software como servicio.

- **Pregunta:** ¿Qué riesgo cloud es muy común por mala configuración?
- **Respuesta:** Exponer públicamente almacenamiento o servicios sin control de acceso adecuado.

## Sección 5 - Video 27 (Seguridad en dispositivos IoT)

- **Pregunta:** ¿Por qué un dispositivo IoT puede considerarse una “puerta” a la red?
- **Respuesta:** Porque está conectado y, si tiene fallas o mala configuración, puede ser explotado para acceder a otros sistemas de la red.

- **Pregunta:** ¿Qué controles básicos deben aplicarse en IoT?
- **Respuesta:** Cambiar credenciales por defecto, actualizar firmware, cifrar comunicaciones y segmentar dispositivos en una red separada.

- **Pregunta:** ¿Qué riesgo implica almacenar la contraseña WiFi en texto plano en un IoT?
- **Respuesta:** Que un atacante que comprometa el dispositivo puede recuperar la clave y obtener acceso a la red inalámbrica.
