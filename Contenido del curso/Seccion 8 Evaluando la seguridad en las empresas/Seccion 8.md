# Seccion 8: Evaluando la seguridad en las empresas

## Contenido del curso
- [**Video 42:** Auditorías de seguridad](#video-42)
- [**Video 43:** Controles de seguridad en ISO 27001](#video-43)

<a id="video-42"></a>
## Video 42: Auditorías de seguridad

### Resumen breve
En este video aprenderás cómo una auditoría de seguridad ayuda a una empresa a saber si sus controles realmente funcionan. La auditoría no es solo “revisar papeles”: sirve para detectar brechas, priorizar mejoras y reducir riesgos de negocio.

### Conceptos clave
- **Auditoría de seguridad:** evaluación sistemática de políticas, procesos y controles para verificar su eficacia.
- **Control de seguridad:** medida para reducir probabilidad o impacto de una amenaza.
- **ISO/IEC 27001:** marco para gestionar seguridad de la información con enfoque basado en riesgos.
- **Anexo A (ISO 27001:2022):** catálogo de **93 controles** para tratar riesgos.

### Relación con ISO 27001 y controles (base para la Lección 43)
La auditoría se vuelve más útil cuando se conecta con la selección de controles de ISO 27001. El **Anexo A** no obliga a implementar todo, sino a justificar qué controles aplican según el contexto de la organización y sus riesgos.

Los controles se agrupan en cuatro categorías:
1. **Organizacionales (37):** políticas, roles, gestión de proveedores, continuidad.
2. **De personas (8):** formación, responsabilidades, medidas disciplinarias.
3. **Físicos (14):** control de acceso físico, protección de instalaciones y equipos.
4. **Tecnológicos (34):** hardening, monitoreo, cifrado, control de acceso lógico.

### Ejemplo práctico (sencillo y concreto)
**Escenario:** Empresa de e-commerce con riesgo de robo de datos de clientes.

Durante la auditoría se encuentra:
- No hay MFA en cuentas administrativas.
- Los accesos de ex empleados siguen activos.
- El monitoreo de logs existe, pero sin alertas útiles.

**Mejora aplicada con enfoque ISO 27001:**
- Control tecnológico: activar MFA y políticas de acceso mínimo.
- Control organizacional: proceso formal de alta/baja de usuarios.
- Control de personas: capacitación de phishing para equipos críticos.
- Control físico: restringir acceso al cuarto de servidores.

**Resultado:** baja la probabilidad de compromiso y mejora la trazabilidad para auditorías futuras.

### Mini guía para seleccionar controles correctamente
1. Identifica activos críticos (datos, sistemas, procesos clave).
2. Evalúa riesgos (impacto x probabilidad).
3. Selecciona controles del Anexo A que reduzcan esos riesgos.
4. Justifica inclusión/exclusión en la **Declaración de Aplicabilidad (SoA)**.
5. Mide efectividad con indicadores (incidentes, tiempos de respuesta, hallazgos).

### Errores comunes
- Implementar controles “por moda” y no por riesgo real.
- Copiar controles de otra empresa sin adaptar contexto.
- Hacer auditoría solo para cumplir y no para mejorar.
- No dar seguimiento a hallazgos y acciones correctivas.

### Palabras clave
- **Controles de seguridad:** medidas para prevenir, detectar o corregir incidentes.
- **ISO 27001:** norma para establecer y mejorar un SGSI.
- **Riesgos:** posibilidad de que una amenaza afecte activos del negocio.
- **Anexo A:** lista de controles de referencia para tratamiento de riesgos.
- **Organización:** contexto de negocio que define prioridades y nivel de control.

### Valor práctico
Esta lección te da una base real para auditar y fortalecer seguridad en empresas: entender qué controlar, por qué controlarlo y cómo demostrar que funciona. Esto mejora cumplimiento, reduce vulnerabilidades y facilita decisiones de inversión en ciberseguridad.

### Resumen de un párrafo
En esta lección se explica cómo las auditorías de seguridad permiten evaluar si los controles de una organización son eficaces para mitigar riesgos. Se conecta este proceso con ISO 27001, especialmente con el Anexo A, que agrupa 93 controles en categorías organizacionales, de personas, físicas y tecnológicas. La clave no es aplicar todos los controles, sino seleccionar y justificar los más adecuados al contexto de cada empresa. Con este enfoque, la organización mejora su postura de seguridad, reduce vulnerabilidades y crea un ciclo de mejora continua basado en evidencia.

### Preguntas de entrevista
- **Pregunta:** ¿Para qué sirve una auditoría de seguridad en una empresa?
- **Respuesta:** Para validar la eficacia de controles, detectar brechas y priorizar mejoras basadas en riesgo.

- **Pregunta:** ¿ISO 27001 obliga a implementar los 93 controles del Anexo A?
- **Respuesta:** No. Exige seleccionar y justificar qué controles aplican según el contexto y los riesgos de la organización.

- **Pregunta:** ¿Qué documento demuestra qué controles aplican y por qué?
- **Respuesta:** La Declaración de Aplicabilidad (SoA).


<a id="video-43"></a>
## Video 43: Controles de seguridad en ISO 27001

### Resumen breve
En este video verás cómo ISO 27001 te ayuda a elegir controles de seguridad de forma inteligente, según el riesgo real de tu empresa. La idea clave es simple: no se trata de aplicar todos los controles, sino los que realmente reducen riesgos y tienen sentido para el negocio.

### Conceptos clave
- **ISO 27001:** marco para implementar y mejorar un SGSI con enfoque basado en riesgos.
- **Anexo A:** lista de controles de referencia para tratar riesgos identificados.
- **Selección basada en contexto:** cada organización elige controles según su tamaño, sector, activos y amenazas.
- **SoA (Declaración de Aplicabilidad):** documento que justifica qué controles se aplican y por qué.

### Ideas principales
- ISO 27001 define un marco para implementar controles efectivos según necesidades reales.
- El Anexo A reúne controles recomendados para tratar riesgos concretos.

### Ideas secundarias
- Se deben elegir solo controles relevantes y justificar su inclusión/exclusión.
- Los controles se agrupan en cuatro categorías para facilitar implementación y seguimiento.

### Categorías de controles (Anexo A 2022)
1. **Organizacionales:** políticas, roles, gestión de terceros, continuidad.
2. **De personas:** formación, responsabilidades y concienciación.
3. **Físicos:** protección de instalaciones y acceso físico.
4. **Tecnológicos:** control de acceso lógico, cifrado, monitoreo, hardening.

### PDCA aplicado a controles de seguridad
- **Plan:** analizar riesgos y definir controles.
- **Do:** implementar controles y procesos.
- **Check:** medir si los controles funcionan (KPIs, auditorías, hallazgos).
- **Act:** corregir, mejorar y actualizar controles.

Este ciclo evita controles “estáticos” y mantiene el SGSI vivo ante nuevas amenazas.

### Ejemplo práctico (sencillo y concreto)
**Escenario:** empresa SaaS con riesgo de acceso no autorizado a datos de clientes.

- **Plan:** riesgo alto por cuentas privilegiadas sin MFA.
- **Do:** implementar MFA, revisión de privilegios y alertas de login anómalo.
- **Check:** medir intentos bloqueados, incidentes y tiempos de respuesta.
- **Act:** ajustar políticas, reforzar capacitación y endurecer acceso remoto.

**Resultado:** menos probabilidad de compromiso y mejor evidencia para auditoría.

### Documentación y auditoría del SGSI
Para que los controles aporten valor, deben quedar documentados:
- objetivo del control,
- riesgo que trata,
- responsable,
- evidencia de operación,
- resultado de revisión.

Esto facilita auditorías internas/externas y mejora la trazabilidad de decisiones.

### Palabras clave
- **ISO 27001:** norma para gestionar seguridad con enfoque basado en riesgos.
- **Controles de seguridad:** medidas para prevenir, detectar o corregir eventos.
- **Gestión de riesgos:** proceso para identificar, evaluar y tratar riesgos.
- **Anexo A:** catálogo de controles de referencia para tratamiento de riesgos.
- **Documento (SoA):** registro formal que justifica qué controles aplican.

### Valor práctico
Saber seleccionar e implementar controles correctamente permite construir una seguridad más eficiente y adaptable. Evita gastar en controles innecesarios y mejora cumplimiento, auditoría y resiliencia operativa.

### Resumen de un párrafo
En esta lección se estudian los controles de seguridad del Anexo A de ISO 27001 como base para tratar riesgos de forma estructurada. Se enfatiza que no todos los controles aplican a todas las empresas: cada organización debe seleccionar y justificar los más relevantes según su contexto. La división en controles organizacionales, de personas, físicos y tecnológicos facilita la implementación y el seguimiento. Además, el uso del ciclo PDCA y la documentación en el SGSI aseguran mejora continua, mayor trazabilidad y mejor preparación para auditorías.



### Tipos de pentest (según nivel de conocimiento)
- **Caja blanca:** el pentester conoce arquitectura, credenciales y documentación interna.
  - *Útil para:* revisar en profundidad controles técnicos y lógica de seguridad.
  - *Ejemplo:* validar seguridad de una API con acceso al código y diagramas.
- **Caja negra:** el pentester parte como atacante externo, sin información previa.
  - *Útil para:* medir exposición real hacia Internet.
  - *Ejemplo:* simular ataque a portal público sin credenciales internas.
- **Caja gris:** el pentester recibe información parcial (por ejemplo, una cuenta de usuario estándar).
  - *Útil para:* simular amenazas internas o cuentas comprometidas.
  - *Ejemplo:* evaluar qué puede hacer un usuario con permisos limitados.

### Fases de un pentest (paso a paso)
1. **Planificación:** definir alcance, reglas de juego, autorizaciones y ventanas de prueba.
2. **Recopilación de información:** reunir datos técnicos de activos, dominios, tecnologías y superficie de ataque.
3. **Fase de reconocimiento:** mapear servicios y rutas de ataque probables.
4. **Explotación:** validar vulnerabilidades de forma controlada para demostrar impacto real.
5. **Persistencia:** comprobar si un atacante podría mantener acceso en el tiempo.
6. **Escalada de privilegios:** evaluar si es posible pasar de usuario básico a privilegios altos.
7. **Documentación final:** entregar hallazgos, evidencias, criticidad y plan de remediación.

### Relación práctica entre auditoría y pentest
- La **auditoría** verifica si los controles existen y se aplican correctamente.
- El **pentest** demuestra si esos controles realmente resisten un ataque real.
- Combinados, entregan una visión más completa del riesgo y de la madurez de seguridad.


### Preguntas de entrevista
- **Pregunta:** ¿ISO 27001 obliga a implementar todos los controles del Anexo A?
- **Respuesta:** No. Se deben seleccionar los controles relevantes y justificar su aplicación en la SoA según el análisis de riesgos.

- **Pregunta:** ¿Cómo se relaciona PDCA con los controles de seguridad?
- **Respuesta:** PDCA permite planear controles, implementarlos, medir su eficacia y mejorarlos continuamente.

- **Pregunta:** ¿Por qué documentar controles en el SGSI es tan importante?
- **Respuesta:** Porque permite demostrar eficacia, facilitar auditorías y sostener decisiones de mejora continua.
