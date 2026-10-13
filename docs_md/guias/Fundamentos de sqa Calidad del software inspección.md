<!-- Fuente: Fundamentos de sqa Calidad del software inspección.pdf -->
<!-- Convertido: 2026-10-11T19:47:23 -->

Proceso de aseguramiento de la calidad:
Inspección
Aseguramiento de la calidad del software
Ing. Ernesto Suárez
Inspección

Inspección: Técnica Estática Formal
ISO/IEC/IEEE 29119-4
| Definir | inspección | vs. walkthrough (29119-1:2022). |
| ------- | ---------- | ------------------------------- |
Diseñar procedimiento formal con moderador y métricas.
| Aplicar checklist |     | en código/diseño crítico UCAB. |
| ----------------- | --- | ------------------------------ |

Conceptos Básicos
|                       |     | Checklist        |     | Conteo y       |     | 60-120 min +  |
| --------------------- | --- | ---------------- | --- | -------------- | --- | ------------- |
|                       |     | rigurosa,        |     | clasificación  |     | reuniones     |
| Definición: Revisión  |     | métricas de      |     | defectos       |     | previas/      |
| estática formal       | l   | defectos, roles  | o   | (mayor/        | n   |               |
posteriores.
a
| sistemática para detectar  |     | fijos. |     |         |     |     |
| -------------------------- | --- | ------ | --- | ------- | --- | --- |
|                            |     |        | c   |         | ó   |     |
|                            | m   |        |     | menor). |     |     |
| defectos, liderada por     |     |        | o   |         |     |     |
i
c
| moderador independiente  | r   |     | F   |     |     |     |
| ------------------------ | --- | --- | --- | --- | --- | --- |
a
o
(no autor).
r
F
u
D

Fundamento Normativo
|     | Rol | Responsabilidades |
| --- | --- | ----------------- |
29119-4: Procedimiento  Dirige proceso,
| detallado (5.3  | Moderador | imparcial, mide  |
| --------------- | --------- | ---------------- |
| Inspección).​   |           | efectividad.     |
Prepara material, no
Autor
29119-2: Integración en
defiende en sesión.
Test Management
| Process. |     | Lee material para  |
| -------- | --- | ------------------ |
Lector
grupo, resalta defectos.
Analiza con checklist,
29119-1: Pruebas
Inspector
clasifica defectos.
estáticas formales.
Documenta defectos
|     | Registrador | con  |
| --- | ----------- | ---- |
severidad/prioridad.

Procedimiento Paso a Paso
Preparación
Planificación:
| individual:  | Sesión reunión:  | Seguimiento:  |
| ------------ | ---------------- | ------------- |
Moderador  Reescritura: Autor
| Participantes  | Lector guía, grupo  | Verifica cierres,  |
| -------------- | ------------------- | ------------------ |
selecciona  corrige.
| revisan (2-4  | registra defectos. | métricas finales. |
| ------------- | ------------------ | ----------------- |
material/checklist.
horas).

Checklist Estándar Inspección
| Categoría Defectos | Ejemplos Código/Diseño         | Severidad (1-5) |
| ------------------ | ------------------------------ | --------------- |
| Sintáctico         | Errores gramática/nomenclatura | 1-2             |
| Semántico          | Lógica inconsistente           | 3-4             |
| Estilo/Estándares  | Cumplimiento IEEE              | 1-3             |
| Riesgo             | Vulnerabilidades               | 4-5             |

Diferencias con Otras Técnicas
| Técnica | Formalidad | Foco Defectos | Métricas |
| ------- | ---------- | ------------- | -------- |
Inspección Alta Conteo/clasificación Densidad defectos/página
| Walkthrough | Baja  | Feedback general | No formal |
| ----------- | ----- | ---------------- | --------- |
| Review      | Media | Cumplimiento     | Variable  |

Evidencia Académica
Defectos detectados: 55-85% efectividad (IEEE 29119).
ROI: 1 hora inspección = 5-10 horas pruebas dinámicas evitadas.
Casos: Proyectos críticos NASA/empresas (IEEE 29119-3 ejemplos).

Integración Ágil/UCAB
Sprint Planning: Inspección diseño/backlog items críticos.
Herramientas: Jira (defectos), SonarQube (métricas automáticas).
Frecuencia: Código >500 líneas o riesgo alto.

Métricas y Mejora Continua
| s <1/mil  | e <5% a  | d Defectos  |
| --------- | -------- | ----------- |
| o         | p        | a           |
t
|     | a   | d   |
| --- | --- | --- |
c
líneas  pruebas  encontrados
|     | c   | i   |
| --- | --- | --- |
e
v
s
f
|         | e            | i              |
| ------- | ------------ | -------------- |
| e       |              | t              |
| código. |   dinámicas. | c vs. totales. |
d
a
e
|     | s   |     |
| --- | --- | --- |
| d   |     | f   |
|     | a   | E   |
| a   | T   |     |
d
i
s
n
e
D

Referencias
• ISO/IEC/IEEE, "29119-1:2022 Software testing — Part 1: Concepts and
definitions."​
• ISO/IEC/IEEE, "29119-4:202x Software testing — Part 4: Test
techniques."​
• ISO/IEC/IEEE, "29119-4:202x Software testing — Part 4: Test
techniques."
• M. Sethi, "Testing, review, inspection and walkthrough," IJLRST, vol. 6,
no. 1, 2017.
• S. Reid, "ISO/IEC/IEEE 29119: The new international software testing
standards," 2014.