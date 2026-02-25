# Seccion 7

## Contenido del curso
- [**Video 37:** Introducción a las soluciones de ciberseguridad](#video-37)
- [**Video 38:** Soluciones de SIEM](#video-38)

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


<a id="video-38"></a>
## Video 38: Soluciones de SIEM

### Resumen breve
Un **SIEM** (Security Information and Event Management) ayuda a reunir eventos de seguridad en un solo lugar, detectar patrones peligrosos y responder más rápido ante amenazas. En esta clase verás por qué es una pieza central del SOC y cómo elegir una solución sin gastar de más.

### Conceptos clave
- **Centralización de eventos:** juntar logs de firewall, endpoints, servidores, nube e identidad en una sola plataforma.
- **Correlación de datos:** unir señales separadas para descubrir ataques que no se ven con alertas aisladas.
- **Detección en tiempo real:** generar alertas rápidas cuando aparece comportamiento sospechoso.
- **Casos de uso:** reglas concretas (ej. fuerza bruta + inicio exitoso + acceso privilegiado).

### ¿Por qué SIEM es crítico en empresas?
- Reduce puntos ciegos al consolidar fuentes de datos.
- Acelera investigación y respuesta del blue team/SOC.
- Permite auditoría, cumplimiento y trazabilidad de incidentes.
- Facilita métricas de seguridad para dirección (MTTD, MTTR, falsos positivos).

### Soluciones SIEM del mercado (comparativa práctica)
> *Nota:* costos aproximados; cambian por volumen de logs, retención, conectores y soporte.

1. **Splunk Enterprise / Splunk ES**
   - **Fuerte en:** búsqueda avanzada, analítica potente, ecosistema amplio.
   - **Ideal para:** organizaciones con equipos maduros y alto volumen de datos.
   - **Costo típico:** medio-alto/alto según ingesta diaria.

2. **Microsoft Sentinel**
   - **Fuerte en:** integración nativa con Azure y ecosistema Microsoft.
   - **Ideal para:** empresas que ya usan M365, Entra ID y servicios Azure.
   - **Costo típico:** pago por uso (ingesta/retención), flexible pero requiere control.

3. **IBM QRadar**
   - **Fuerte en:** correlación robusta y visibilidad en entornos empresariales grandes.
   - **Ideal para:** compañías con operación SOC formal y necesidades complejas.
   - **Costo típico:** medio-alto, depende de EPS/FPS y módulos.

4. **LogRhythm**
   - **Fuerte en:** enfoque SOC integrado, casos de uso prearmados y respuesta.
   - **Ideal para:** equipos que quieren operación guiada sin construir todo desde cero.
   - **Costo típico:** medio, con variación por tamaño y funcionalidades.

5. **Securonix**
   - **Fuerte en:** analítica de comportamiento (UEBA) y enfoque cloud-first.
   - **Ideal para:** organizaciones que priorizan detección avanzada en nube/híbrido.
   - **Costo típico:** medio-alto, según volumen y capacidades activadas.

### Ejemplo práctico (sencillo y concreto)
Una empresa detecta muchos intentos fallidos de login. El SIEM correlaciona:
1) 20 intentos fallidos en VPN,
2) inicio exitoso desde país inusual,
3) acceso a servidor financiero fuera de horario.

Con esa correlación, el SOC sube la severidad, bloquea sesión, fuerza cambio de credenciales y abre investigación. Sin SIEM, estos eventos aparecerían separados y podrían pasar desapercibidos.

### Mini guía para elegir un SIEM
1. Define 5-10 casos de uso críticos antes de comprar.
2. Calcula volumen real de logs (GB/día) y retención requerida.
3. Evalúa integraciones nativas con tus sistemas actuales.
4. Mide esfuerzo operativo: ¿tu equipo podrá mantener reglas y tuning?
5. Compara costo total: licencia + almacenamiento + personal + soporte.

### Errores comunes
- Elegir SIEM solo por marca y no por casos de uso.
- Ingerir “todo” sin estrategia (sube costo y ruido).
- No afinar reglas (muchos falsos positivos).
- No definir playbooks de respuesta para alertas críticas.

### Preguntas de entrevista
- **Pregunta:** ¿Qué problema resuelve un SIEM en una empresa?
- **Respuesta:** Centraliza eventos, correlaciona señales y mejora detección/respuesta ante amenazas.

- **Pregunta:** ¿Qué diferencia hay entre alerta y correlación?
- **Respuesta:** Una alerta puede venir de un solo evento; correlación une varios eventos para identificar un ataque con más contexto.

- **Pregunta:** ¿Qué revisarías antes de seleccionar un SIEM?
- **Respuesta:** Casos de uso, integraciones, volumen de logs, costo total y capacidad operativa del equipo.
