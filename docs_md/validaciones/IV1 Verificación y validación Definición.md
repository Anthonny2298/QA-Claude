<!-- Fuente: IV1 Verificación y validación Definición.pdf -->
<!-- Convertido: 2026-10-11T19:49:21 -->

Verificación y validación:
Definición
Aseguramiento de la calidad del software
Unidad temática IV Tema 1
Ing. Ernesto Suárez
Definición

ASEGURAMIENTO DE LA
CALIDAD DEL SOFTWARE
UNIDAD TEMÁTICA IV: Tema 1
VERIFICACIÓN Y VALIDACIÓN
Ingeniería Informática
Universidad Católica Andrés Bello (UCAB)
Presentación académica y rigorosa basada en estándares de la industria
y la literatura clásica.

Estructura de la Unidad IV
Verificación y Validación: La Doble Garantía de Calidad
Calidad
|                    | 1   |                    | 2   |                        | 3   |
| ------------------ | --- | ------------------ | --- | ---------------------- | --- |
| Tema 1: Definición |     | Tema 2: Estándares |     | Tema 3: Evaluación de  |     |
Madurez
| Conceptos, diferencias y el propósito  |     | Modelos de referencia (CMM,  |     |     |     |
| -------------------------------------- | --- | ---------------------------- | --- | --- | --- |
| de V&V.                                |     | ISO/IEC/IEEE 12207).         |     |     |     |
Capacidad del proceso de desarrollo
de software.
El Aseguramiento de la Calidad del Software (SQA) requiere un enfoque sistemático y dual para garantizar tanto la corrección técnica
como la idoneidad para el propósito.

Tema 1: Definición de Verificación
El Proceso de Construir Correctamente
La Verificación es el proceso sistemático para comprobar que el software cumple
con los requisitos técnicos especificados y con los estándares de diseño y desarrollo
establecidos.
Pregunta clave: ¿Estamos construyendo el producto correctamente?
Se realiza de forma continua a lo largo de todo el ciclo de vida del desarrollo.
Busca detectar errores y defectos lo más temprano posible, minimizando el costo de corrección.
Ejemplos de actividades de Verificación incluyen:
• Revisión de requerimientos y especificaciones.
• Inspección y análisis estático de código.
• Pruebas unitarias y de integración.

Tema 1: Definición de Validación
El Proceso de Construir el Producto Correcto
La Validación es el proceso para asegurar que el software cumple con las
necesidades, expectativas y propósito del usuario final y del negocio.
Pregunta clave: ¿Estamos construyendo el producto correcto?
Se enfoca en el software final o en versiones suficientemente completas para
probarse en contextos reales.
Busca garantizar que el producto satisface su propósito y resuelve
el problema para el que fue creado.
Actividades típicas de Validación:
• Pruebas de sistema (funcionales y no funcionales).
• Pruebas de aceptación con usuarios finales (UAT).
• Evaluación de usabilidad, rendimiento y seguridad.

Verificación vs. Validación: Diferencias Fundamentales
Aunque complementarios, la Verificación y la Validación (V&V) tienen objetivos, enfoques y momentos de aplicación distintos
en el ciclo de vida del desarrollo de software (Sommerville, 2021).
Aspecto Verificación Validación
Objetivo Conformidad con especificaciones técnicas Cumplimiento de necesidades reales
Enfoque Procesos y productos intermedios Producto terminado, contexto operacional
(documentación, código)
Momento Continuo durante el desarrollo Fases finales o post-desarrollo
Ejemplos Inspección de código, pruebas Pruebas de aceptación, pruebas de
estáticas, pruebas unitarias usabilidad, pruebas de sistema
Fuente: Adaptado de ISTQB Syllabus (2023) y bibliografía clásica de Ingeniería de Software.

Impacto en el SQA
La Importancia de V&V
Reducción de Costos Mejora de la Calidad
Detección de defectos en etapas Garantiza que el software es
tempranas, donde el costo de robusto, consistente
corrección es exponencialmente (Verificación) y apto para el uso
menor. (Validación).
Satisfacción del Cliente
Asegura que el producto final resuelve los problemas para los que fue
diseñado y cumple las expectativas operacionales.
Como expertos en SQA, nuestro objetivo es implementar un marco de V&V que sea
proactivo y cubra todas las dimensiones de la calidad.

Técnicas Clave en Verificación y Validación
Las técnicas se pueden clasificar según su enfoque (estático vs. dinámico) y su propósito (funcional vs. no funcional).
Enfoque de Verificación (¿Cómo se Enfoque de Validación (¿Satisface al
construye?) usuario?)
Verificación Estática Validación Funcional
Análisis de código y documentación sin ejecutar el Comprobar que las funciones y características del
programa. Incluye inspecciones, revisiones de pares y software operan conforme al uso esperado por el
análisis de herramientas estáticas. usuario.
Validación No Funcional
Verificación Dinámica
Evaluación de atributos de calidad como rendimiento,
Implica la ejecución del código, típicamente mediante usabilidad, seguridad, capacidad de carga, y
pruebas unitarias y pruebas de integración. fiabilidad.

Ejemplo Práctico: Aplicación Móvil de Pagos
Fase de Verificación Fase de Validación
Se comprueba que el módulo de autenticación utiliza el cifrado correcto (según Se realizan pruebas de aceptación (UAT) donde usuarios reales confirman que la
especificación técnica) y que las pruebas unitarias de transferencia de fondos aplicación permite realizar pagos en 3 clics y que la interfaz es intuitiva y fácil de
son exitosas. usar, cumpliendo la promesa de valor.
La coexistencia de ambas fases asegura un producto técnicamente sólido y funcionalmente relevante.

Preguntas de Práctica (Estilo ISTQB)
Consolidando los conceptos clave de V&V, esenciales para el examen de certificación.
|             | 1   |             | 2   |             | 3   |
| ----------- | --- | ----------- | --- | ----------- | --- |
| Pregunta 1: |     | Pregunta 2: |     | Pregunta 3: |     |
¿Cuál de las siguientes actividades se  ¿Qué pregunta clave responde la  ¿En qué etapa del desarrollo se realiza
relaciona típicamente con la  Validación? principalmente la validación?
verificación?
|                                 |     | • a) ¿Estamos construyendo el  |     | • a) Durante el diseño. |     |
| ------------------------------- | --- | ------------------------------ | --- | ----------------------- | --- |
| • a) Pruebas de aceptación con  |     | producto correcto?             |     |                         |     |
• b) Antes de la codificación.
usuarios finales.
• b) ¿Estamos construyendo el
• c) Cuando el software está casi
| • b) Pruebas de sistema. |     | producto correctamente? |     |     |     |
| ------------------------ | --- | ----------------------- | --- | --- | --- |
completo o en producción.
| • c) Revisión de especificaciones y  |     | • c) ¿El código está libre de errores? |     |     |     |
| ------------------------------------ | --- | -------------------------------------- | --- | --- | --- |
• d) Durante la planificación.
pruebas unitarias.
• d) ¿El software pasó las pruebas
| • d) Evaluación de usabilidad. |     | unitarias? |     |     |     |
| ------------------------------ | --- | ---------- | --- | --- | --- |

Referencias Bibliográficas del Tema 1
Fuentes primarias y manuales universalmente aceptados en el Aseguramiento de la Calidad del Software y Testing (SQA/ISTQB).
ISTQB (2023). Probador certificado de ISTQB, programa de estudio
nivel básico, versión 4.0 [Versión en español].
ISTQB_CTFL_Syllabus-v4.0_ES_.pdf
ISTQB (2018). Probador certificado del ISTQB: programa de estudio –
nivel básico [Versión en español].
CTFL-2018-ES-PROGRAMA_DE_ESTUDIO-V001.32.pdf
ISTQB (2016). Programa de estudio ISTQB: Testing de seguridad, nivel
avanzado [Versión en español].
ISTQB_CT-SEC-2016_ES_PROGRAMA-DE-ESTUDIO-V001.25.pdf
Se recomienda encarecidamente la consulta de los programas oficiales del ISTQB como guía para la enseñanza y el estudio de conceptos de calidad.