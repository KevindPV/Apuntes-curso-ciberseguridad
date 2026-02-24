# Seccion 5

## Implantar la seguridad para protegernos de los ataques

### Resumen breve
En seguridad de sistemas no existe una única defensa perfecta. Se aplican varias capas (red, aplicaciones, endpoints y monitoreo) para reducir riesgos y detectar ataques a tiempo.

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

## Preguntas de entrevista
- ¿Cuál es la diferencia práctica entre IDS e IPS?
- ¿Por qué un WAF no reemplaza un firewall de red?
- ¿Qué aporta SIEM y qué aporta SOAR en conjunto?
- ¿Por qué la DMZ reduce impacto pero no elimina riesgo?
