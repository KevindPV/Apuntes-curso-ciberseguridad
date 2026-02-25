# Seccion 7

## Contenido del curso
- [**Video 37:** Introducción a las soluciones de ciberseguridad](#video-37)

<a id="video-37"></a>
## Video 37: Introducción a las soluciones de ciberseguridad

### Resumen breve
En esta lección se presenta una visión práctica de soluciones defensivas del mercado para proteger empresas. La meta es que puedas reconocer qué hace cada herramienta, cuándo conviene usarla y cómo combinarla con otras defensas.

### Ideas principales
- Es clave conocer varias herramientas de ciberseguridad para defender organizaciones de forma realista.
- Se introducen soluciones como **XDR** y **SIEM**.
- Se explica la monitorización de logs con herramientas como **Splunk**.

### Ideas secundarias
- Se conecta con temas anteriores: gestión de riesgos y defensas del blue team.
- Se comparan opciones del mercado (incluyendo rangos de precio/licenciamiento).
- El enfoque puede adaptarse según necesidades del equipo o grupo.

### Conceptos importantes (explicación sencilla)

#### Firewalls
Filtran tráfico de red para permitir o bloquear conexiones según reglas.

**Ejemplo simple:**
Permitir solo HTTPS (443) hacia un servidor web y bloquear servicios no usados.

#### IDS (Sistema de Detección de Intrusos)
Detecta actividad sospechosa y alerta al equipo de seguridad.

**Ejemplo simple:**
Detectar escaneos de puertos repetidos desde una misma IP y generar alerta.

#### SIEM (Security Information and Event Management)
Centraliza y correlaciona eventos de seguridad de múltiples fuentes (firewall, endpoints, servidores, nube).

**Ejemplo simple:**
SIEM relaciona: login fallidos + acceso admin raro + descarga masiva de datos y dispara alerta crítica.

#### XDR (Extended Detection and Response)
Amplía la detección y respuesta unificando señales de endpoint, red, correo, identidad y nube.

**Ejemplo simple:**
XDR detecta phishing en correo + ejecución de archivo malicioso en endpoint + conexión sospechosa a C2 y automatiza contención.

#### Monitorización de logs (ej. Splunk)
Permite buscar, visualizar y alertar sobre eventos relevantes para investigación y respuesta.

**Ejemplo simple:**
Crear dashboard con intentos de login por país y alertar cuando aparezca un país no habitual para cuentas privilegiadas.

### Comparativa rápida SIEM vs XDR
- **SIEM:** ideal para centralizar logs y correlacionar eventos de muchas fuentes.
- **XDR:** ideal para detección/respuesta integrada y rápida entre varias capas.
- En empresas maduras, suelen usarse juntos.

### Valor práctico para tu carrera
Esta lección te prepara para:
- Identificar soluciones defensivas según contexto empresarial.
- Hacer preguntas correctas al evaluar herramientas (cobertura, integración, costo, madurez del equipo).
- Entender mejor roles como analista SOC, blue team, ingeniero de seguridad y GRC técnico.

### Errores comunes
- Comprar herramientas sin casos de uso definidos.
- Implementar SIEM/XDR sin definir fuentes de datos ni reglas de alerta.
- No entrenar al equipo en operación y respuesta.
- Medir solo “cantidad de alertas” y no calidad de detección.

### Preguntas de entrevista (con respuestas)
- **Pregunta:** ¿Cuál es la diferencia práctica entre SIEM y XDR?
- **Respuesta:** SIEM prioriza agregación/correlación de logs; XDR prioriza detección y respuesta integrada entre múltiples dominios.

- **Pregunta:** ¿Por qué Splunk es útil en ciberseguridad?
- **Respuesta:** Porque permite centralizar, buscar y analizar logs para detección, investigación forense y alertamiento.

- **Pregunta:** ¿Qué debería evaluar una empresa antes de adquirir una solución defensiva?
- **Respuesta:** Casos de uso, integración con su entorno, costo total (licencia + operación), capacidades del equipo y métricas de efectividad.
