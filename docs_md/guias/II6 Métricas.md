<!-- Fuente: II6 Métricas.pdf -->
<!-- Convertido: 2026-10-11T19:46:07 -->

Métricas
Aseguramiento de la calidad del software
Unidad temática II Tema 6
Ing. Ernesto Suárez
Cultura de calidad

Introducción
Se aborda el tema 6 de la unidad temática II del programa de aseguramiento
de la calidad del software y los estándares que lo respaldan.
• Introducción
• Concepto y clasificación
• Métricas frecuentes y aplicación
• Recolección y análisis de métricas
• Uso práctico de métricas en la toma de decisiones
• Métricas en estándares (IEEE 1061)
• Caso
• Conclusiones

Preliminares
Por medio de métricas, se
Las métricas son medidas cuantitativas
puede monitorear la
que permiten evaluar atributos del
evolución del proyecto,
software y sus procesos para
detectar áreas problemáticas
garantizar la calidad y desempeño
y tomar decisiones basadas en
esperado.
datos concretos.
Cuantitativas Monitoreo
Objetivas
Estándares
En calidad del software, las
La aplicación sistemática de
métricas brindan una base objetiva
métricas está alineada con
para analizar, controlar y mejorar
estándares internacionales
iterativamente productos y
como IEEE 1061 y SWEBOK.
procesos.

Concepto y clasificación
Miden aspectos del
proceso de desarrollo, por
Proceso ejemplo, tiempo de ciclo,
Según Al-Jadaa , las métricas son
eficiencia, tasas de
Clasificar las métricas permite
medidas cuantitativas que defectos.
seleccionar indicadores
permiten evaluar aspectos del
adecuados para monitoreo
software y sus procesos para
Relacionadas con específico y mejora continua.
mejorar la calidad. características del
software en sí, como Producto Cada categoría aporta
IEEE 1061 define métricas como
tamaño, complejidad,
información clave distinta para
"una función que relaciona un fiabilidad.
evaluación y toma de decisiones
conjunto de datos, obtenidos de
(Crosby, 1994 ; Fenton y Bieman,
un producto, proyecto o proceso,
2014 ).
con un valor numérico Enfocadas en la gestión,
Proyecto incluyendo cumplimiento
cuantificable".
de plazos, costos y alcance.

Métricas clave en calidad de software
Mide número de defectos
encontrados por unidad de
Densidad de
defectos tamaño (líneas de código,
módulos).
Porcentaje de código,
Porcentaje de defectos
funcionalidades, requisitos
corregidos sin generar nuevos
Tasa de evaluados durante las pruebas.
problemas. Cobertura de
resolución en
Indica la exhaustividad y
pruebas
Indicador valioso para la calidad primera pasada
efectividad del proceso de
del proceso de reparación y
pruebas (cobertura de
pruebas.
requisitos, cobertura de código,
cobertura de riesgos).
Medición del tiempo promedio
Número de fallos por unidad de
para corregir fallos detectados.
Tiempo medio tiempo en operación.
Refleja eficiencia del equipo de Tasa de fallos
de reparación
Mide confiabilidad en
soporte y calidad del proceso de
producción y ayuda a priorizar
corrección
mantenimiento.

Recolección y análisis de métricas
| s • | s   |     |     | o • | s • |
| --- | --- | --- | --- | --- | --- |
Es fundamental definir  Aplicación de técnicas  Las métricas deben
| o   | o   |     |     | c   | e   |
| --- | --- | --- | --- | --- | --- |
qué datos se necesitan  • estadísticas para  informar sobre el
| t   | t   | Eliminar  |     | i   | n   |
| --- | --- | --------- | --- | --- | --- |
| a   | a   |           |     | t   |     |
y  c ó m o   o b t e n e r l o s   i n c o n s is t e n c i a s  y   s i n t e r p r e t a r  te n d encias,  o e s t a d o   d e l  p ro y e c to y
| d   | d   |     |     | í   | i   |
| --- | --- | --- | --- | --- | --- |
  c o n f ia b l e m e n t e . d c o r r e l a c i o n e s  y   s g u i a r  a c c io n e s  d e
| e   |   e | d a t o s   d | u p li c a d o s  para  |     |     |
| --- | --- | ------------- | ----------------------- | --- | --- |
|     |     |               |                         | a   | i c |
d • M é t o d o s  c o m u n e s   d e v i t a r   s e s g o s . p a t r o n e s . m e jo r a .
|     |     |     |     | t   | e   |
| --- | --- | --- | --- | --- | --- |
|     |     |     |     | s   |     |
n incluyen herramientas  a • Confirmar precisión y  e • Uso de gráficos,  d • Se recomienda
| ó   | z   |     |     |     |   e |
| --- | --- | --- | --- | --- | --- |
automatizadas de  e completitud para  s histogramas y análisis  establecer umbrales y
| i c |     |     |     | i   | d   |
| --- | --- | --- | --- | --- | --- |
recopilación, registros  i s de regresión para  criterios de alerta para
| c   | p   | análisis correcto. |     | i   |     |
| --- | --- | ------------------ | --- | --- | --- |
|     | m   |                    |     | l   | a   |
e de defectos, sistemas  á descubrimiento de  interpretación rápida.
| l                    |     |     |     |             | m                       |
| -------------------- | --- | --- | --- | ----------- | ----------------------- |
| o de seguimiento de  | i   |     |     | n insights. |                         |
|                      | l   |     |     |             | • Los resultados deben  |
| c                    |     |     |     | A           | o                       |
proyectos y reportes  y • Importancia de  t integrarse en ciclos de
| e           |     |     |     |     |     |
| ----------- | --- | --- | --- | --- | --- |
| R manuales. | n   |     |     |     |   y |
contextualizar  mejora continua (e.g.,
|     | ó   |     |     |     |     |
| --- | --- | --- | --- | --- | --- |
• La calidad de los datos  resultados con base en  n modelo IDEAL) .
i
|     | c   |     |     |     | ó   |
| --- | --- | --- | --- | --- | --- |
impacta directamente  a el proyecto y entorno .
i
|     | d   |     |     |     | c   |
| --- | --- | --- | --- | --- | --- |
en la utilidad de las  a
i
| métricas. | l   |     |     |     | u   |
| --------- | --- | --- | --- | --- | --- |
a
|     | V   |     |     |     | l   |
| --- | --- | --- | --- | --- | --- |
a
v
E

Uso práctico de métricas en la toma
de decisiones
Las métricas permiten un
seguimiento continuo del
Indicadores clave para la gestión
desempeño del software y del
proceso.
Sirven para detectar desviaciones
tempranas y áreas críticas que
Toma de decisiones basada en datos
requieren atención inmediata.
Ayudan a fundamentar
decisiones de asignación de
Limitaciones y riesgos
recursos, priorización de
pruebas y corrección.
Facilitan la planificación de
mejoras y la predicción de
Integración en ciclos de mejora continua
riesgos.

Uso práctico de métricas en la toma
de decisiones
Métricas clave alimentan bucles
Indicadores clave para la gestión
de retroalimentación para la
mejora progresiva (e.g., IDEAL,
CMMI).
Promueven la cultura de calidad y
Toma de decisiones basada en datos
responsabilidad en todos los
equipos.
Interpretación incorrecta o
métricas mal definidas pueden
Limitaciones y riesgos
conducir a decisiones erróneas.
Es vital contextualizar datos y
complementar métricas con juicio
experto.
Integración en ciclos de mejora continua

Estándar IEEE 1061
para Métricas de Calidad del Software
Objeto o aspecto del software
Entidad de
a medir (producto, proceso,
s
medición
e
recurso).
l
a
| i   |              | Característica que se desea  |                                    |
| --- | ------------ | ---------------------------- | ---------------------------------- |
| c   | Atributo de  |                              | Facilita comunicación clara entre  |
| n   |              | evaluar (fiabilidad,         | equipos y stakeholders.            |
calidad
e
mantenibilidad, eficiencia).
s
e

s Función que cuantifica la  Mejora la precisión y relevancia
Métrica
e
de métricas usadas en proyectos.
| t   |     | entidad respecto al atributo. |     |
| --- | --- | ----------------------------- | --- |
n
e
| n   | Escala de  |                      |                       |
| --- | ---------- | -------------------- | --------------------- |
|     |            | Unidad y rango para  | Proporciona un marco  |
o
estandarizado para facilitar la
|     | medición | interpretar la métrica. |                                |
| --- | -------- | ----------------------- | ------------------------------ |
| p   |          |                         | comparación y mejora continua. |
m
| o   | Método de  |     |     |
| --- | ---------- | --- | --- |
Procedimiento para obtener
C
|     | recolección | datos válidos y confiables. |     |
| --- | ----------- | --------------------------- | --- |
IEEE 1061: Estándar internacional para definir, seleccionar y evaluar métricas de software para la gestión de calidad.

Conclusiones
• Las métricas son herramientas indispensables para medir objetivamente la
calidad y desempeño del software y sus procesos.
• Permiten identificar áreas críticas, guiar la toma de decisiones y fomentar
la mejora continua en proyectos de desarrollo.
• Deben ser seleccionadas cuidadosamente, adaptándose al contexto y
objetivos específicos para ser efectivas.
• La recolección y análisis riguroso de datos es esencial para evitar
interpretaciones erróneas y potenciar su valor.
• Integrar métricas en estándares y modelos de calidad (IEEE 1061, IDEAL,
ISO 25010) fortalece la cultura de calidad y profesionaliza la gestión.
• Finalmente, la comunicación clara y compromiso de todo el equipo son
clave para transformar datos en acciones que mejoren la calidad del
software.

Referencias
| • A. Al-Jadaa, | Software Metrics, Birzeit |     |     | University, 2014. |     |
| -------------- | ------------------------- | --- | --- | ----------------- | --- |
• I. Sommerville, Software Engineering, Pearson, 2011.
IEEE, IEEE Standard for a Software Quality Metrics Methodology, IEEE
Std 1061-1998, 1998.
•
IEEE Computer Society, Guide to the Software Engineering Body of
| Knowledge | (SWEBOK), IEEE Std |     | 1074-2006, 2006. |     |     |
| --------- | ------------------ | --- | ---------------- | --- | --- |
•
| J. Gremba                         | and C. Myers, | The Ideal Model: Practical |     |                  | Guide for |
| --------------------------------- | ------------- | -------------------------- | --- | ---------------- | --------- |
| Improvement, Software Engineering |               |                            |     | Institute, 2024. |           |
• N. Fenton and J. Bieman, Software Metrics: A Rigorous & Practical
Approach, Chapman & Hall, 2014.
• P. Crosby, Completeness: Quality for the 21st Century, McGraw Hill,
1994