# Seccion 8: Evaluando la seguridad en las empresas

## Contenido del curso
- [**Video 42:** Auditorías de seguridad](#video-42)

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
