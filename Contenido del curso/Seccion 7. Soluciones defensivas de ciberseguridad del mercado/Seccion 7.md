# Seccion 7

## Contenido del curso
- [**Video 37:** Introducción a las soluciones de ciberseguridad](#video-37)
- [**Video 38:** Soluciones de SIEM](#video-38)
- [**Video 39:** Soluciones de EDR y XDR](#video-39)
- [**Video 40:** Soluciones de SOAR](#video-40)
- [**Video 41:** Soluciones de NGFW](#video-41)

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


<a id="video-39"></a>
## Video 39: Soluciones de EDR y XDR

### Resumen breve
En este video veremos cómo **EDR** y **XDR** ayudan a detectar y frenar ataques en tiempo real. Si SIEM es el “centro de control” de eventos, EDR/XDR son la “respuesta activa” para contener amenazas en endpoints y en varios dominios (red, correo, identidad y nube).

### Conceptos clave
- **EDR (Endpoint Detection and Response):** protege equipos finales (laptops, servidores, estaciones) con telemetría, detección y respuesta.
- **XDR (Extended Detection and Response):** amplía EDR y correlaciona señales de endpoint + red + identidad + correo + nube.
- **Detección en tiempo real:** identifica comportamientos anómalos (ejecución sospechosa, robo de credenciales, C2).
- **Respuesta automatizada:** aislar host, matar proceso malicioso, bloquear hash/IP/dominio y abrir caso en SOC.

### ¿Cómo se relaciona con SIEM?
- **SIEM** centraliza logs y correlaciona eventos para visibilidad global.
- **EDR/XDR** ejecuta acciones de contención rápida en los activos afectados.
- En equipos maduros, se usan juntos: SIEM para contexto y XDR/EDR para respuesta táctica.

### Soluciones líderes de EDR/XDR (comparativa práctica)
> *Nota:* costos aproximados, varían por número de endpoints, módulos y retención de datos.

1. **Microsoft Defender for Endpoint / Defender XDR**
   - **Fuerte en:** integración con ecosistema Microsoft (M365, Entra, Sentinel).
   - **Despliegue:** cloud-first, agentes en endpoints.
   - **Costo típico:** medio (licencias por usuario/dispositivo según plan).

2. **CrowdStrike Falcon (EDR/XDR)**
   - **Fuerte en:** telemetría de endpoint y respuesta rápida con enfoque cloud.
   - **Despliegue:** SaaS con agente ligero.
   - **Costo típico:** medio-alto según módulos (EDR, Identity, etc.).

3. **SentinelOne Singularity**
   - **Fuerte en:** automatización de respuesta y capacidades de rollback/ransomware.
   - **Despliegue:** cloud con agente en endpoint.
   - **Costo típico:** medio-alto por endpoint y capacidades avanzadas.

4. **Palo Alto Cortex XDR**
   - **Fuerte en:** correlación entre endpoint, red y otros controles Palo Alto.
   - **Despliegue:** híbrido/cloud según arquitectura.
   - **Costo típico:** medio-alto, escala por volumen y módulos.

5. **Trend Micro Vision One**
   - **Fuerte en:** cobertura XDR en endpoint, correo y nube con gestión unificada.
   - **Despliegue:** SaaS con integración multiplataforma.
   - **Costo típico:** medio, variable por cobertura y tamaño de empresa.

### Ejemplo práctico (fácil y concreto)
Una persona abre un archivo malicioso por phishing:
1. **EDR** detecta ejecución de script sospechoso en el equipo.
2. **XDR** correlaciona que esa misma cuenta también tuvo login raro en nube.
3. Se activa respuesta: aislamiento del endpoint, bloqueo del dominio de phishing y reseteo de credenciales.

Resultado: el ataque se contiene antes de que cifre otros equipos o robe más datos.

### Mini guía para elegir EDR/XDR
1. Define qué activos quieres proteger (solo endpoint o también identidad/correo/nube).
2. Evalúa capacidad de respuesta automática (aislar, bloquear, rollback).
3. Verifica integración con SIEM/SOAR y herramientas actuales.
4. Revisa cobertura multiplataforma (Windows, Linux, macOS, móviles).
5. Calcula costo total: licencias, operación SOC, tuning y retención.

### Errores comunes
- Comprar XDR sin inventario de activos y sin casos de uso claros.
- Activar agentes sin plan de tuning (genera falsos positivos).
- No entrenar al SOC en playbooks de respuesta.
- Medir solo cantidad de alertas y no impacto real reducido.

### Preguntas de entrevista
- **Pregunta:** ¿Cuál es la diferencia práctica entre EDR y XDR?
- **Respuesta:** EDR se enfoca en endpoint; XDR amplía detección/correlación y respuesta en múltiples dominios.

- **Pregunta:** ¿Por qué combinar SIEM con XDR mejora la defensa?
- **Respuesta:** Porque SIEM aporta contexto global y XDR ejecuta contención rápida con acciones directas.

- **Pregunta:** ¿Qué criterio técnico es clave al evaluar EDR/XDR?
- **Respuesta:** Calidad de detección, automatización de respuesta, integraciones y costo operativo sostenible.


<a id="video-40"></a>
## Video 40: Soluciones de SOAR

### Resumen breve
En este video aprenderás qué es **SOAR** y por qué ayuda a los equipos SOC a responder incidentes más rápido y con menos trabajo manual. Además, conectamos este tema con tu crecimiento profesional: saber operar SIEM+EDR+SOAR también mejora cómo te presentas en tu CV de ciberseguridad.

### Conceptos clave
- **SOAR (Security Orchestration, Automation and Response):** plataforma que orquesta herramientas de seguridad, automatiza tareas repetitivas y guía la respuesta a incidentes.
- **Orquestación:** conectar SIEM, EDR, firewall, correo, IAM y ticketing para ejecutar acciones coordinadas.
- **Automatización:** ejecutar pasos automáticos (enriquecer IOC, bloquear IP, abrir ticket, notificar equipo).
- **Playbooks:** flujos de respuesta predefinidos para incidentes comunes (phishing, malware, cuenta comprometida).

### ¿Por qué SOAR importa tanto?
- Reduce tiempos de respuesta (MTTR).
- Disminuye fatiga por alertas repetitivas.
- Mejora consistencia: todos siguen el mismo procedimiento.
- Permite que analistas junior resuelvan más casos con guía estructurada.

### Soluciones SOAR del mercado (visión práctica)
> *Nota:* costos y capacidades cambian según conectores, casos de uso y volumen de alertas.

1. **Cortex XSOAR (Palo Alto)**
   - Fuerte en playbooks avanzados y ecosistema amplio de integraciones.
2. **Splunk SOAR (Phantom)**
   - Fuerte en integración con entorno Splunk/SIEM y automatización SOC.
3. **IBM SOAR (Resilient)**
   - Fuerte en gestión formal de incidentes y trazabilidad empresarial.
4. **Microsoft Sentinel + Logic Apps (enfoque SOAR)**
   - Fuerte en automatización cloud para organizaciones Microsoft.
5. **Swimlane**
   - Fuerte en low-code y orquestación flexible para equipos SOC.

### Ejemplo práctico (simple)
Escenario: llega un correo de phishing con enlace malicioso.
1. SIEM genera alerta por URL sospechosa.
2. SOAR ejecuta playbook: consulta reputación de dominio + extrae IOC.
3. Si riesgo alto: bloquea dominio en proxy/firewall, busca el correo en buzones y lo pone en cuarentena.
4. Abre ticket, notifica al SOC y documenta evidencia automáticamente.

Resultado: de 30-40 minutos manuales a 2-5 minutos automatizados.

### Palabras clave (con breve descripción)
- **SOAR:** automatiza y coordina respuesta a incidentes entre varias herramientas.
- **Playbook:** receta paso a paso para responder un tipo de incidente.
- **Orquestación:** integración de sistemas de seguridad para actuar en cadena.
- **Automatización:** ejecución automática de tareas repetitivas del SOC.
- **MTTR:** tiempo promedio que tardas en contener/resolver un incidente.
- **IOC (Indicator of Compromise):** evidencia técnica de posible compromiso (hash, IP, dominio, URL, etc.).

### Valor práctico para empleabilidad (CV en ciberseguridad)
Aunque el foco del video es SOAR, este conocimiento te ayuda a construir mejor tu currículum:
- Usa un formato claro y escaneable (1 página si eres junior).
- Destaca logros medibles con verbos de acción.
- Adapta el CV según vacante (SOC, blue team, detección/respuesta).
- Resalta certificaciones y práctica real (labs, CTF, playbooks, casos).

**Ejemplo de logro en CV:**
- “Diseñé un playbook de phishing en SOAR que redujo el tiempo de contención de 35 a 6 minutos en pruebas de laboratorio”.

### Errores comunes
- Automatizar sin validar proceso manual primero.
- Crear playbooks largos y difíciles de mantener.
- No definir criterios de severidad/escala.
- No medir resultados (MTTD/MTTR, falsos positivos, casos cerrados).

### Preguntas de entrevista
- **Pregunta:** ¿Qué problema resuelve SOAR en un SOC?
- **Respuesta:** Reduce trabajo manual y acelera la respuesta mediante playbooks y automatización.

- **Pregunta:** ¿Cuál es la diferencia entre SIEM y SOAR?
- **Respuesta:** SIEM detecta/correlaciona eventos; SOAR ejecuta respuesta automatizada y orquestada.

- **Pregunta:** ¿Qué deberías automatizar primero en SOAR?
- **Respuesta:** Casos repetitivos y de bajo riesgo (phishing básico, enriquecimiento IOC, bloqueo inicial y ticketing).


<a id="video-41"></a>
## Video 41: Soluciones de NGFW

### Resumen breve
En este video conocerás qué es un **NGFW (Next-Generation Firewall)** y por qué es clave para proteger redes modernas. Un NGFW no solo filtra puertos e IP, también inspecciona aplicaciones, usuarios y amenazas avanzadas para bloquear ataques con mayor contexto.

### Conceptos clave
- **NGFW:** firewall de nueva generación con control por aplicación, inspección profunda (DPI), prevención de intrusiones (IPS) y visibilidad avanzada.
- **Control por aplicación:** permite reglas por tipo de app (ej. bloquear TOR, limitar redes sociales, permitir GitHub para desarrollo).
- **Inspección TLS/SSL:** analiza tráfico cifrado para detectar malware oculto.
- **Integración con identidad:** políticas por usuario/grupo (AD/IdP), no solo por IP.

### ¿Qué problema resuelve un NGFW?
- Reduce riesgo de malware, C2 y movimiento lateral.
- Aplica políticas más precisas que un firewall tradicional.
- Mejora cumplimiento al registrar y auditar tráfico crítico.
- Permite segmentación y control de acceso entre zonas de red.

### Soluciones NGFW del mercado (referencia práctica)
1. **Palo Alto Networks NGFW**
   - Fuerte en App-ID/User-ID, visibilidad y ecosistema de seguridad.
2. **Fortinet FortiGate**
   - Fuerte en rendimiento/precio e integración con Security Fabric.
3. **Cisco Secure Firewall (Firepower)**
   - Fuerte en entornos enterprise Cisco y políticas centralizadas.
4. **Check Point Quantum**
   - Fuerte en prevención avanzada y administración unificada.
5. **Sophos Firewall**
   - Fuerte en simplicidad operativa y buen ajuste para pymes.

### Ejemplo práctico (concreto)
Escenario: una oficina híbrida necesita controlar tráfico de usuarios remotos.
1. Se permite solo SaaS corporativo (M365, Jira, GitHub) por grupo.
2. Se bloquean apps de alto riesgo y categorías maliciosas.
3. Se activa IPS + DNS filtering + inspección TLS para detectar C2.
4. Si se detecta comportamiento anómalo, se aplica bloqueo automático.

Resultado: menor exposición, menos incidentes y mayor trazabilidad para auditoría.

### Palabras clave (con breve descripción)
- **NGFW:** firewall con inspección avanzada y control por aplicación/usuario.
- **DPI:** análisis profundo de paquetes para entender contenido y contexto.
- **IPS:** motor que detecta y bloquea intentos de explotación en red.
- **Segmentación:** separar redes/sistemas para limitar propagación de ataques.
- **C2 (Command and Control):** canal usado por malware para recibir órdenes.
- **Política basada en identidad:** regla de seguridad definida por usuario o rol.

### Errores comunes
- Activar funciones avanzadas sin tuning (muchos falsos positivos).
- No revisar impacto de inspección TLS en rendimiento y privacidad.
- Mantener reglas demasiado abiertas (“allow any any”).
- No alinear reglas con procesos del negocio.

### Valor profesional (CV en ciberseguridad)
Tomando las ideas de currículum efectivo y aplicándolas a este tema:
- Usa formato limpio y viñetas cortas para que RRHH lea rápido.
- Incluye un perfil profesional claro (SOC/Blue Team/Redes de Seguridad).
- Describe logros con verbos de acción y métricas.
- Adapta tu CV a cada vacante (NGFW, SOC, NOC seguridad).
- Resalta certificaciones relevantes (ej. NSE, PCNSA, CCNP Security, Security+).

**Ejemplo de logro en CV:**
- “Implementé políticas NGFW por aplicación y reduje en 45% el tráfico a dominios maliciosos en 3 meses”.

### Preguntas de entrevista
- **Pregunta:** ¿Qué diferencia un NGFW de un firewall tradicional?
- **Respuesta:** El NGFW añade visibilidad por aplicación/usuario, IPS e inspección avanzada, no solo filtrado de puertos/IP.

- **Pregunta:** ¿Por qué inspeccionar tráfico TLS en un NGFW?
- **Respuesta:** Porque gran parte del tráfico malicioso viaja cifrado; sin inspección se pierde visibilidad.

- **Pregunta:** ¿Qué revisarías antes de desplegar un NGFW?
- **Respuesta:** Inventario de aplicaciones críticas, rendimiento esperado, políticas por identidad, plan de tuning y monitoreo continuo.
