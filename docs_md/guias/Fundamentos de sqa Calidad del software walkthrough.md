<!-- Fuente: Fundamentos de sqa Calidad del software walkthrough.pdf -->
<!-- Convertido: 2026-10-11T19:47:23 -->

Proceso de aseguramiento de la calidad:
Walkthrough
Aseguramiento de la calidad del software
Ing. Ernesto Suárez
Walkthrough

Walkthrough: Técnica Estática de Revisión
Objetivos
Definir walkthrough y diferenciarlo de
inspección formal (ISO 29119-1:2022).
Diseñar procedimiento completo alineado ISO
29119-2 (procesos) y 29119-4 (técnicas).
Aplicar checklist práctica en SRS y diagramas
UML para proyectos UCAB.

¿Qué es un Walkthrough?
Características
Informal: Sin moderador externo ni
métricas formales de defectos.
Revisión estática informal liderada
Guiada por autor: Presentación +
por el autor para obtener feedback discusión abierta (45-60 min máx.).
técnico y mejorar el trabajo de
Foco: Comprensión, alternativas de
producto (SRS, diseño, código).
diseño, no solo errores.
Participantes: 5-7 (autor, espectadores,
registrador).
ISO 29119-4:5.2 Walkthrough | Diferencia clave: Informal vs. Inspección formal

Conceptos Básicos
Técnica estática de revisión según ISO/IEC/IEEE 29119-4
Un walkthrough es una revisión estática informal donde el autor
del documento o código guía a un grupo para obtener
Walkthrough es más flexible
retroalimentación sobre el producto de trabajo (por ejemplo,
y menos estructurado. No
especificaciones, diagramas, código).
requiere checklist riguroso
ni roles formales como
moderador.
| Informal     | Temprana     | Colaborativa |     |
| ------------ | ------------ | ------------ | --- |
| Proceso no   | Enfocado en  | Involucra    |     |
| formal, sin  | identificar  | discusión    |     |
Inspección formal es más
| moderador  | mejoras,  | abierta y  |     |
| ---------- | --------- | ---------- | --- |
estructurada. Requiere
| externo  | aclarar dudas  | colaboración  |     |
| -------- | -------------- | ------------- | --- |
checklist riguroso y rol
| obligatorio. | y detectar  | entre         |                        |
| ------------ | ----------- | ------------- | ---------------------- |
|              | errores     | participantes | formal como moderador. |
|              | tempranos.  | .             |                        |
Duración recomendada:45 a
60 minutos para mantener
efectividad.
Basado en ISO/IEC/IEEE 29119-4:5.2 y literatura académica relevante.
Revisión de requisitos (SRS),
diseño preliminar, diagramas
UML, fragmentos de código.

Fundamento Normativo
29119-1:
Conceptos-Define
pruebas estáticas
(walkthroughcomo
ISO/IEC/IEEE 29119: Marco para Walkthrough peer review
informal).
Detección temprana de defectos reduce
costos 20-30% post-entrega.
ISO/IEC/IEEE
29119: Marco
29119-1 29119-2 29119-4
para
Walkthrough
29119-4: Técnicas
29119-2:
Estáticas-
Procesos-Integra
Procedimiento
walkthroughen
detallado:
Test Planningy
preparación,
diseño de pruebas.
sesión, cierre.

Roles y Responsabilidades
ISO 29119-4:5.2 Roles
Rol Responsabilidades Clave
Autor Presenta material, guía sesión, responde dudas.
Espectadores Dan feedback técnico, usan checklist básica.
Registrador Anota issues, acuerdos y acciones follow-up.
Registrador
Total participantes: 5-7 (evita >10 para foco).
Flexibilidad: Los roles pueden rotar
Autor
Espectador Espectador
Ambiente: Colaborativo, sin confrontación.
Espectador

Procedimiento Paso a Paso del Walkthrough
| Preparación |     | Sesión |     | Cierre |     |
| ----------- | --- | ------ | --- | ------ | --- |
Autor distribuye
|     |     |     | Autor conduce  |     | Registrador  |
| --- | --- | --- | -------------- | --- | ------------ |
materiales (SRS,
|     |     |     | presentación  |     | documenta issues |
| --- | --- | --- | ------------- | --- | ---------------- |
diagramas, código)
|     |     |     | guiada. |     | y acuerdos. |
| --- | --- | --- | ------- | --- | ----------- |
con anticipación.
|     | Participantes    |     | Discusión abierta    |     | Define acciones  |
| --- | ---------------- | --- | -------------------- | --- | ---------------- |
|     | revisan          |     | para aclaraciones y  |     | correctivas y    |
|     | preliminarmente. |     | sugerencias.         |     | responsables.    |
Duración recomendada: 45-60 minutos para máxima eficacia.
ISO/IEC/IEEE 29119-4 Procedimiento Walkthrough

Checklist Estándar para Walkthrough
Ítem Checklist Cumple (S/N) Observación/Issue Prioridad
Requisitos
Alta/Media/Baja
trazables/completos
Términos
ambiguos/pendientes
Casos de uso/riegos
identificados
Consistencia con
estándares UCAB Personaliza
por artefacto
Viabilidad técnica
Exporta a
(SRS → Diseño
estimada
Excel/Jira para
→ Código).
Marca S/N
seguimiento.
durante
Plantilla práctica ISO/IEC/IEEE 29119-4
sesión; discute
Basado en 29119-4 técnicas estáticas
observaciones.

Diferencias con Otras Técnicas
Walkthrough
Fases
tempranas
|         |            |                | Roles         | Estándar  |     | (SRS/Diseño  |
| ------- | ---------- | -------------- | ------------- | --------- | --- | ------------ |
| Técnica | Formalidad | Foco Principal |               |           |     | UCAB)        |
|         |            |                | Estructurados | Principal |     |              |
Feedback/suge
| Walkthrough | Informal |     | Autor guía | 29119-4 |     |     |
| ----------- | -------- | --- | ---------- | ------- | --- | --- |
rencias
|     |     | Detección  | Moderador |     |     |     |
| --- | --- | ---------- | --------- | --- | --- | --- |
¿Cuánd
| Inspección | Formal |          |            | 29119-4 |     |     |
| ---------- | ------ | -------- | ---------- | ------- | --- | --- |
|            |        | defectos | /checklist |         |     |     |
o usar?
|        |          | Cumplimiento  |          | IEEE 1028/ |              |     |
| ------ | -------- | ------------- | -------- | ---------- | ------------ | --- |
| Review | Variable |               | Flexible |            |              |     |
|        |          | general       |          | 29119-4    | Inspección:  |     |
Código  Review:
crítico/ Cumplimiento
contractual
riesgo alto
|     | Walkthrough vs. Inspección |     | vs. Review |     |     |     |
| --- | -------------------------- | --- | ---------- | --- | --- | --- |
Comparativa según ISO/IEC/IEEE 29119-4
ISO 29119-4:5.2-5.3

Evidencia Académica y Beneficios
|           |         | s 25-40% en  | I Costo    | s Proyectos  |
| --------- | ------- | ------------ | ---------- | ------------ |
| Beneficio | Impacto | o            | O          | e            |
|           |         | t            | R          | li           |
|           |         | c fases      | detección  | 29119-3      |
|           |         | e            |            | g            |
á
|                    |                  | f e           |            |  s         |
| ------------------ | ---------------- | ------------- | ---------- | ---------- |
|                    |                  | tempranas     | 10x menor  | (ejemplos  |
| Detección temprana | 30% menos rework | d             |            | o          |
|                    |                  |  n            |            | s          |
|                    |                  | (SRS/Diseño). | vs.        | a reales). |
|                    |                  | ó             |            | C          |
ic
producción.
c
| Mejora colaboración | +20% comprensión equipo | u   |     |     |
| ------------------- | ----------------------- | --- | --- | --- |
d
e
R
| Métricas accionables | Issues/hora documentados |     |     |     |
| -------------------- | ------------------------ | --- | --- | --- |

Integración Ágil y Proyectos UCAB
|     |     | 0Revisión | sJira (issues),  |     | a1  |
| --- | --- | --------- | ---------------- | --- | --- |
|     |     |           | a                |     | ic  |
Walkthrough en Entornos Ágiles UCAB t nSRS  t nConfluence nwalkthrough/
|     |     | ir  | e   |     | e   |
| --- | --- | --- | --- | --- | --- |
p
Adaptación ISO/IEC/IEEE 29119 para sprints biblioteca  im(checklist/ u semana en
|     |     | S   |     |     | c   |
| --- | --- | --- | --- | --- | --- |
e
|     |     | UCAB (pre- | a         |     | fases  |
| --- | --- | ---------- | --------- | --- | ------ |
|     |     |            | r rexport |     | r      |
F
|     |     | backlog) | e   |     | tempranas. |
| --- | --- | -------- | --- | --- | ---------- |
HExcel).
| Fase Ágil        | Artefacto Walkthrough  |     |     | Duración |     |
| ---------------- | ---------------------- | --- | --- | -------- | --- |
| Sprint Planning  | SRS + User Stories     |     |     | 45 min   |     |
| Diseño Iterativo | Diagrama UML secuencia |     |     | 60 min   |     |
| Código Inicial   | Fragmentos críticos    |     |     | 30 min   |     |

Referencias
• ISO/IEC/IEEE, "29119-1:2022 Software testing — Part 1: Concepts and
definitions."​
• ISO/IEC/IEEE, "29119-4:202x Software testing — Part 4: Test
techniques."​
• S. Reid, "ISO/IEC/IEEE 29119: The new international software testing
standards," 2014.
• M. Sethi, "Testing, review, inspection and walkthrough," IJLRST, vol. 6,
no. 1, 2017.