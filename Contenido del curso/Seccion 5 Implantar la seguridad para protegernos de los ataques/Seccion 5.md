# Seccion 5

## Contenido de la seccion
- [**Video 24:** Implantar la seguridad para protegernos de los ataques](#video-24)
- [**Video 25:** Practicamos con el firewall Portmaster](#video-25)

<a id="video-24"></a>
## Implantar la seguridad para protegernos de los ataques

### Resumen breve
En seguridad de sistemas no existe una única defensa perfecta. Se aplican varias capas (red, aplicaciones, endpoints y monitoreo) para reducir riesgos y detectar ataques a tiempo.


## Imagen de referencia de la arquitectura

![Diagrama de red con Red local, DMZ, firewalls, router e Internet](./img/img1.svg)

### ¿Cómo entender esta imagen paso a paso?
1. **Identifica las zonas**:
   - A la izquierda está la **Red local** (equipos internos de la empresa).
   - En el centro está la **DMZ** (servidores expuestos como web/correo/app).
   - A la derecha está **Internet**.
2. **Observa los firewalls**:
   - El primer firewall separa red interna y zonas intermedias.
   - El segundo firewall protege la salida/entrada hacia Internet.
3. **Sigue el recorrido del tráfico**:
   - Un usuario de Internet no debería llegar directo a la red local.
   - Primero pasa por controles (firewalls/router) y, si aplica, llega a servicios en DMZ.
4. **Idea clave de seguridad**:
   - La DMZ actúa como “zona colchón”. Si comprometen un servidor público, aún hay barreras para llegar a la red interna.

**Ejemplo muy sencillo:**
- Tu empresa publica una web en DMZ.
- Un atacante explota la web.
- Gracias a firewalls + segmentación, el atacante no puede conectarse directamente al servidor de nómina que está en la red local.

## Conceptos clave (explicación sencilla)

### 1) Zona Desmilitarizada (DMZ)
La **DMZ** es una red intermedia entre Internet y la red interna de la empresa.
- Ahí se colocan servicios expuestos (web, correo, DNS).
- Si un atacante compromete un servidor en la DMZ, aún no entra directo a la red interna.

**Ejemplo simple:**
Una tienda online publica su servidor web en la DMZ. La base de datos de clientes queda en la red interna. Si atacan la web, no deberían llegar fácilmente a los datos internos.

### 2) Firewalls
Un **firewall** filtra tráfico según reglas (IP, puerto, protocolo, dirección).
- Decide qué conexiones se permiten y cuáles se bloquean.

**Ejemplo simple:**
Permitir solo `HTTPS (443)` hacia el servidor web y bloquear puertos innecesarios como `23 (Telnet)`.

### 3) WAF (Web Application Firewall)
El **WAF** protege aplicaciones web analizando peticiones HTTP/HTTPS.
- Bloquea patrones típicos de ataques web (SQLi, XSS, etc.).

**Ejemplo simple:**
Si un atacante envía `"' OR 1=1 --"` en un formulario, el WAF puede detectarlo y bloquear la petición.

### 4) IDS (Sistema de Detección de Intrusos)
Un **IDS** detecta actividad sospechosa y **alerta**, pero normalmente no bloquea por sí mismo.
- Funciona como “alarma” de seguridad.

**Ejemplo simple:**
Detecta múltiples intentos de escaneo de puertos desde una IP y genera una alerta al equipo de seguridad.

### 5) IPS (Sistema de Prevención de Intrusos)
El **IPS** detecta y además **bloquea** automáticamente tráfico malicioso.
- Suele estar en línea (inline), por eso puede detener ataques en tiempo real.

**Ejemplo simple:**
Si identifica un exploit conocido en el tráfico, corta esa conexión antes de que llegue al servidor.

### 6) EDR (Endpoint Detection and Response)
El **EDR** protege equipos finales (laptops, servidores, estaciones de trabajo).
- Detecta comportamientos maliciosos en procesos, archivos y memoria.
- Ayuda a contener incidentes (aislar host, matar proceso, cuarentena de archivo).

**Ejemplo simple:**
Un usuario ejecuta un archivo sospechoso. El EDR detecta comportamiento tipo ransomware y aísla el equipo de la red.

### 7) SIEM (Security Information and Event Management)
El **SIEM** centraliza logs/eventos de múltiples fuentes y correlaciona alertas.
- Permite ver “la película completa” del ataque.

**Ejemplo simple:**
Correlaciona: 1) login fallidos en VPN, 2) acceso exitoso raro, 3) creación de usuario admin. Con eso dispara una alerta crítica.

### 8) SOAR (Security Orchestration, Automation and Response)
El **SOAR** automatiza respuestas usando playbooks.
- Toma alertas del SIEM/EDR y ejecuta acciones automáticas para reducir tiempo de respuesta.

**Ejemplo simple:**
Ante phishing confirmado: bloquea hash, bloquea dominio en DNS, abre ticket y notifica al SOC automáticamente.

### 9) ACL (Access Control List)
Una **ACL** es una lista de reglas de permiso/denegación para tráfico o acceso.
- Se usa en routers, firewalls, switches y también en sistemas de archivos.

**Ejemplo simple:**
ACL de red: “solo la subred de administración puede acceder por SSH al servidor”.

## Mini ejemplo integrado (visión por capas)
1. Internet llega al firewall perimetral.
2. Tráfico web permitido entra a la DMZ.
3. WAF filtra ataques de aplicación.
4. IDS/IPS monitorizan y bloquean amenazas de red.
5. EDR protege cada endpoint.
6. SIEM correlaciona eventos de todo el entorno.
7. SOAR automatiza acciones de respuesta.
8. ACL limita movimientos y accesos no autorizados.

## Errores comunes
- Pensar que el firewall por sí solo es suficiente.
- Exponer base de datos en la DMZ.
- No revisar alertas de SIEM/EDR.
- Automatizar en SOAR sin validar playbooks (falsos positivos).

## Preguntas de entrevista (con respuestas)

- **Pregunta:** ¿Cuál es la diferencia práctica entre IDS e IPS?
- **Respuesta:** El IDS detecta y alerta eventos sospechosos; el IPS detecta y bloquea tráfico malicioso en tiempo real porque está en línea con el flujo de red.

- **Pregunta:** ¿Por qué un WAF no reemplaza un firewall de red?
- **Respuesta:** Porque protegen capas distintas: el firewall de red controla tráfico por IP/puerto/protocolo (capa de red/transporte) y el WAF inspecciona peticiones HTTP/HTTPS para frenar ataques de aplicación (como SQLi o XSS).

- **Pregunta:** ¿Qué aporta SIEM y qué aporta SOAR en conjunto?
- **Respuesta:** El SIEM centraliza y correlaciona eventos para detectar incidentes; el SOAR ejecuta playbooks automáticos para responder más rápido (bloqueos, tickets, notificaciones, contención).

- **Pregunta:** ¿Por qué la DMZ reduce impacto pero no elimina riesgo?
- **Respuesta:** Porque segmenta y aísla servicios expuestos, dificultando el acceso directo a la red interna; aun así, si hay malas configuraciones o vulnerabilidades, un atacante puede avanzar lateralmente.


<a id="video-25"></a>
## 25. Practicamos con el firewall Portmaster

### Resumen breve
Portmaster es un **firewall gratuito y de código abierto** (muy usado en Windows y también disponible en Linux) que permite ver y controlar conexiones salientes y entrantes del sistema para detectar actividad sospechosa y mejorar privacidad.

### ¿Qué es Portmaster y por qué usarlo?
- Es una capa adicional de control sobre la red, más enfocada en visibilidad y privacidad.
- Permite revisar **qué aplicación se conecta**, **a qué dominio/IP**, y **con qué frecuencia**.
- Ayuda a detectar comportamiento anómalo (por ejemplo, una app que no debería hablar con servidores externos).

**Ejemplo simple:**
Instalas un programa de edición de imágenes y Portmaster muestra conexiones frecuentes a dominios desconocidos. Esto puede indicar telemetría excesiva o posible riesgo.

### ¿Qué es DNS? (explicado fácil)
El **DNS (Domain Name System)** es como la agenda de Internet:
- Tú escribes `google.com`.
- El DNS traduce ese nombre a una IP (por ejemplo, `142.250.x.x`) para que tu equipo sepa a dónde conectarse.

Sin DNS, tendrías que recordar IPs numéricas para cada sitio web.

### ¿Cómo ayuda Portmaster a proteger el DNS?
Portmaster mejora la seguridad y privacidad DNS al permitir:
1. **Cambiar el DNS por defecto** por uno más privado y confiable.
2. **Reducir filtraciones de privacidad**, evitando resolutores DNS inseguros del ISP cuando no conviene.
3. **Monitorear conexiones DNS** para identificar solicitudes raras a dominios sospechosos.
4. **Bloquear rastreadores y anuncios**, lo que reduce superficie de seguimiento y conexiones innecesarias.

**Ejemplo simple:**
Si malware intenta resolver dominios maliciosos para recibir instrucciones, Portmaster puede ayudar a detectarlo por el patrón de consultas y permitir bloquear ese tráfico.

### Funciones prácticas vistas en clase
- Monitoreo de conexiones entrantes/salientes en tiempo real.
- Filtros por país, dominio o aplicación para investigar eventos.
- Opción **Safe Privacy Network** con enfoque de `split tunneling` (definir qué tráfico pasa por qué ruta).
- Configuración simple de DNS para mejorar privacidad y, en muchos casos, rendimiento de navegación.

### Recomendaciones de uso
- Instálalo y revisa conexiones periódicamente.
- Empieza con modo observación y luego endurece reglas gradualmente.
- Prioriza bloquear conexiones que no tengan justificación funcional.
- Combínalo con buenas prácticas: sistema actualizado, antivirus y navegación segura.

### Errores comunes
- Bloquear todo sin criterio y romper aplicaciones legítimas.
- No revisar alertas ni historial de conexiones.
- Dejar DNS por defecto sin evaluar privacidad/seguridad.

### Preguntas de entrevista (con respuestas)
- **Pregunta:** ¿Qué ventaja ofrece Portmaster frente al firewall básico del sistema?
- **Respuesta:** Mayor visibilidad por aplicación/dominio, mejor control de conexiones salientes y funciones enfocadas en privacidad (como gestión DNS y bloqueo de rastreadores).

- **Pregunta:** ¿Qué es DNS y por qué es crítico en ciberseguridad?
- **Respuesta:** Es el sistema que traduce dominios a IP; si se manipula o usa sin protección, puede redirigir tráfico a sitios maliciosos o exponer hábitos de navegación.

- **Pregunta:** ¿Cómo ayuda un firewall como Portmaster ante malware basado en red?
- **Respuesta:** Permite detectar patrones anómalos de conexión y bloquear comunicaciones sospechosas por app, dominio o destino.
