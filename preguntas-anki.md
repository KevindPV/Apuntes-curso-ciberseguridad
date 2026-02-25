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

- **Pregunta:** ¿Qué objetivo principal tiene la segmentación de red en entornos IoT?
- **Respuesta:** Limitar el movimiento lateral de un atacante para que el compromiso de un dispositivo no afecte toda la red.

- **Pregunta:** Da un ejemplo concreto de segmentación en una casa con IoT.
- **Respuesta:** Crear una red separada para cámaras/bombillas/TV y bloquear que esa red acceda a laptops o móviles personales.

## Sección 5 - Video 29 (Estándares, reglamentos y buenas prácticas)

- **Pregunta:** ¿Qué es ISO 27001 en una frase?
- **Respuesta:** Es un estándar internacional para gestionar la seguridad de la información mediante un SGSI basado en riesgos.

- **Pregunta:** ¿Cuál es la diferencia principal entre GDPR y HIPAA?
- **Respuesta:** GDPR regula datos personales en la UE de forma general; HIPAA protege específicamente datos de salud en EE. UU.

- **Pregunta:** ¿Para qué sirven los CIS Controls?
- **Respuesta:** Para aplicar controles prácticos y priorizados que reduzcan riesgo rápidamente.

- **Pregunta:** ¿Qué aporta NIST CSF a una organización?
- **Respuesta:** Un marco por funciones (Identificar, Proteger, Detectar, Responder, Recuperar) para organizar y mejorar el programa de ciberseguridad.

- **Pregunta:** ¿Qué mide un enfoque CMM en ciberseguridad?
- **Respuesta:** El nivel de madurez de procesos, desde prácticas ad-hoc hasta procesos optimizados con mejora continua.


## Sección 5 - Video 30 (Gestión de riesgos)

- **Pregunta:** ¿Cuál es la fórmula básica de gestión de riesgos?
- **Respuesta:** Riesgo = impacto x probabilidad.

- **Pregunta:** ¿Qué representa la dimensión de consecuencias en una matriz de riesgo?
- **Respuesta:** El nivel de daño potencial si el incidente ocurre (despreciable hasta catastrófico).

- **Pregunta:** ¿Qué fases tiene la gestión de riesgos?
- **Respuesta:** Identificación, evaluación, respuesta, monitoreo y reporte.

- **Pregunta:** ¿Qué significa tratar un riesgo mediante “mitigación”?
- **Respuesta:** Reducir su probabilidad o impacto aplicando controles de seguridad.


- **Pregunta:** ¿Por qué es útil un documento de gadgets de ciberseguridad para estudiantes?
- **Respuesta:** Porque conecta teoría con herramientas reales del mercado y mejora preparación para entrevistas y práctica profesional.

- **Pregunta:** Menciona dos ejemplos de gadgets y su utilidad.
- **Respuesta:** Autenticador físico para reforzar MFA y analizador de red para detectar tráfico anómalo/dispositivos no autorizados.


## Sección 5 - Video 31 (Gestión de incidentes)

- **Pregunta:** ¿Cuáles son las fases típicas de gestión de incidentes?
- **Respuesta:** Detección e identificación, clasificación y priorización, contención y erradicación, investigación y análisis, recuperación, comunicación, documentación y aprendizaje.

- **Pregunta:** ¿Qué objetivo tiene la fase de contención?
- **Respuesta:** Limitar el impacto y evitar que el incidente se propague a más sistemas.

- **Pregunta:** ¿Qué se valida en la fase de recuperación?
- **Respuesta:** Que los servicios vuelvan a operar y que la integridad de datos/sistemas sea correcta.

- **Pregunta:** ¿Por qué documentar un incidente es importante?
- **Respuesta:** Porque permite mejorar controles, actualizar procedimientos y reducir probabilidad de recurrencia.


## Sección 6 - Video 33 (Introducción a ISO 27001)


- **Pregunta:** ¿Qué significa proteger la confidencialidad, integridad y disponibilidad (CIA)?
- **Respuesta:** Confidencialidad = acceso solo autorizado; Integridad = datos correctos y no alterados; Disponibilidad = datos/sistemas accesibles cuando se necesitan.

- **Pregunta:** ¿ISO 27001 reemplaza leyes como GDPR?
- **Respuesta:** No. ISO 27001 ayuda a organizar controles y evidencias para cumplir requisitos, pero no sustituye obligaciones legales.

- **Pregunta:** ¿Por qué ISO 27001 puede ayudar a ganar contratos?
- **Respuesta:** Porque demuestra madurez en seguridad y cumplimiento, algo que muchos clientes y licitaciones exigen como requisito.
- **Pregunta:** ¿Qué busca ISO 27001 en una organización?
- **Respuesta:** Implementar y mejorar un SGSI para proteger la información con enfoque basado en riesgos.

- **Pregunta:** ¿Qué ventaja aporta ISO 27001 frente a clientes y socios?
- **Respuesta:** Demuestra madurez y compromiso con seguridad, mejorando confianza y reputación.

- **Pregunta:** ¿Por qué ISO 27001 mejora la empleabilidad en ciberseguridad?
- **Respuesta:** Porque es un estándar ampliamente reconocido en roles de GRC, auditoría, riesgos, compliance y operación de seguridad.


## Sección 6 - Video 34 (Estructura de la ISO 27001)


- **Pregunta:** ¿Qué es el Anexo A de ISO 27001 en palabras simples?
- **Respuesta:** Es una lista de 93 controles de seguridad que ayuda a tratar riesgos dentro del SGSI.

- **Pregunta:** ¿Cuáles son los 4 grupos de controles del Anexo A (2022)?
- **Respuesta:** Organizacionales, de personas, físicos y tecnológicos.

- **Pregunta:** ¿Qué es la Declaración de Aplicabilidad (SoA)?
- **Respuesta:** Es el documento que indica qué controles aplicas, cuáles no y por qué.

- **Pregunta:** ¿ISO 27001 obliga a aplicar los 93 controles del Anexo A?
- **Respuesta:** No; exige justificar inclusión o exclusión según riesgos y contexto del negocio.
- **Pregunta:** ¿Qué es PDCA en palabras simples?
- **Respuesta:** Es una rueda de mejora continua: planear, hacer, revisar y mejorar.

- **Pregunta:** ¿Qué se hace en la fase Check?
- **Respuesta:** Se mide y revisa si los controles realmente están funcionando.

- **Pregunta:** ¿Qué cláusula de ISO 27001:2022 habla de mejora continua?
- **Respuesta:** La cláusula 10 (Mejora).

- **Pregunta:** ¿Para qué sirve la cláusula 4 (Contexto)?
- **Respuesta:** Para entender el entorno del negocio, qué información es crítica y qué riesgos hay.


## Sección 6 - Video 36 (El Futuro de la ISO 27001)

- **Pregunta:** ¿Por qué ISO 27001 será cada vez más importante para empresas?
- **Respuesta:** Porque mejora confianza, facilita cumplimiento y se vuelve requisito en más contratos y sectores.

- **Pregunta:** ¿Qué buenas prácticas sostienen un SGSI saludable?
- **Respuesta:** Liderazgo activo, documentación útil, formación continua e integración con otros sistemas de gestión.

- **Pregunta:** ¿Qué error común puede arruinar una implementación ISO 27001?
- **Respuesta:** Crear mucha documentación sin uso real y sin seguimiento de acciones correctivas.

- **Pregunta:** ¿Qué indicadores simples muestran madurez en ISO 27001?
- **Respuesta:** % de controles implementados, incidentes gestionados y nivel de cumplimiento en auditorías internas.
