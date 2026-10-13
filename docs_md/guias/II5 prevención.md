<!-- Fuente: II5 prevención.pdf -->
<!-- Convertido: 2026-10-11T19:46:07 -->

Prevención
Aseguramiento de la calidad del software
Unidad temática II Tema 5
Ing. Ernesto Suárez
Cultura de calidad

Introducción
Se aborda el tema 5 de la unidad temática II del programa de aseguramiento
de la calidad del software y los estándares que lo respaldan.
• Introducción a la prevención
• Estrategias preventivas principales
• Impacto de la prevención
• Herramientas y metodologías para prevención
• Casos de éxito y buenas prácticas
• Lista de chequeo de requisitos para el proyecto
• Conclusiones

Introducción a la prevención
Refiere a las estrategias y
actividades planificadas
para evitar la aparición de
defectos durante el
Definición
desarrollo.
Análisis y control de
requisitos, revisiones y Se diferencia claramente de la
pruebas tempranas, detección (encontrar defectos
Actividades Diferencias
formación del equipo, existentes) y la corrección
automatización de procesos. (arreglar esos defectos)
Un enfoque preventivo eficaz Incluye la definición de
reduce costos a largo plazo, procesos, estándares y
Impacto Conformación
mejora la confiabilidad y metodologías orientados a
seguridad del software, y minimizar riesgos y errores
contribuye a la satisfacción desde las fases iniciales.
del cliente.

Estrategias preventivas
Análisis exhaustivo de requisitos: Definir y entender completamente las necesidades antes de iniciar el desarrollo.
Evitar ambigüedades, reduciendo defectos futuros y desviaciones.
Revisiones y control de calidad temprano: Inspecciones formales y revisiones de código en equipo (peer
reviews). Detectar fallos iniciales antes de la integración completa.
Diseño de enfoque con calidad: Construcción de arquitecturas robustas y mantenibles. Identificación de
riesgos y soluciones de forma anticipada.
Pruebas unitarias y automatizadas tempranas: Implementación de pruebas desde las primeras etapas del
desarrollo. Automatización para asegurar elevación continua en la calidad.
Capacitación y formación continua: Actualización en buenas prácticas y nuevos estándares. Fortalecimiento de
competencias para la prevención efectiva.

Impacto de la prevención
Goerik (2020) y Gremba & Myers Según Crosby (1994), la prevención permite evitar
(2024) confirman que la prevención errores y defectos antes de que ocurran, lo que reduce
es un elemento imprescindible en la necesidad de costosas correcciones durante fases
modelos IDEAL y estándares avanzadas del proyecto.
internacionales como SWEBOK (IEEE, Reducción
de defectos
2004).
Deming (1994) enfatiza que la
calidad debe construirse desde el
Estudios como GIDYC, CEISOFT y principio mediante prevención
Buenas Satisfacción
LISI (2011) muestran que invertir prácticas del cliente sistemática, generando productos
en prevención es clave para confiables que cumplen expectativas.
mejorar el desempeño y
Impacto de
competitividad del software
la
colombiano, naturalmente validado
prevención
en el contexto local.
La aplicación constante de
Fenton y Bieman (2014) resaltan Casos en la Mejora actividades preventivas facilita un
que el uso de métricas y industria continua proceso de mejora continua (Juran,
mediciones relacionadas con 1974; Ishikawa, 1985), que es
prevención permite predecir la fundamental para mantener altos
Validación
calidad y mejorar procesos, estándares en software.
científica de
validando los beneficios métricas
preventivos.

Herramientas y metodologías en prevención
para garantizar la calidad según IEEE 730
Revisión y auditorías
Pruebas
Requisitos
Reportes
Auditorías
Pruebas no
funcionales
Técnicas y herramientas
incluidas en el
Verificación de plan de Prácticas para Control de
consistencia verificación y reporte,
Inspección código
validación seguimiento y
Revisiones
resolución de Gestión de
gerenciales Pruebas
Métodos para
fallas configuración
preventivas y de
controlar
aseguramiento Responsabilidad Automatización
versiones
es claras para de CI/CD
Seguridad y
prevención y
Análisis estático
trazabilidad
corrección
y seguimiento
para evitar
rápida.
introducir
accidentalment
e defectos

Casos
Con el modelo Test Maturity Model Integration
Con el modelo Test Maturity Model
Integration:
Ejemplo
Organizaciones con niveles 4 y 5 orientan su
proceso de prueba a la prevención de
defectos
Impacto cuantitativo
Mediante análisis sistemático de la causa raíz,
previenen la repetición de errores,
enfocándose en fases tempranas.
Lecciones prácticas
Resultado: Mejora continua, reducción de
costes de retrabajo y disminución
significativa de incidencias en producción.

Casos
Con el modelo Test Maturity Model Integration
Ejemplo en sector Telco:
Ejemplo
En un operador de
telecomunicaciones con múltiples
sistemas integrados, se identificaron
defectos por problemas de entorno
Impacto cuantitativo
en un 80% de casos.
Acción correctiva: creación de listas
de chequeo para asegurar
disponibilidad y comunicación entre
Lecciones prácticas
sistemas, reduciendo errores críticos.

Casos
Con el modelo Test Maturity Model Integration
Ejemplo
Impacto cuantitativo:
Aumento del 15% en cobertura de
Impacto cuantitativo
requisitos probados.
Reducción del 18% en defectos
detectados en producción.
Lecciones prácticas Mejora del 12% en tiempos de
entrega de productos.

Casos
Con el modelo Test Maturity Model Integration
Lecciones prácticas:
No todos los defectos se analizan en
Ejemplo
profundidad, solo aquellos con impacto
crítico (costos, frecuencia, daño).
Herramientas de análisis incluyen diagramas
de causa-efecto (Ishikawa), técnica de los
Impacto cuantitativo
cinco porqués, y esquemas de clasificación de
defectos.
Importancia de la documentación y
seguimiento formal para ejecutar acciones de
Lecciones prácticas
prevención eficaces.

Casos
Con el modelo Test Maturity Model Integration
Ejemplo aplicado a calidad de requerimientos
Problema: El sistema no autentica correctamente a los usuarios.
Ejemplo
1. ¿Por qué no autentica correctamente?
Porque el módulo de autenticación falla con ciertos perfiles.
2. ¿Por qué falla con ciertos perfiles?
Porque no se validan los campos obligatorios en la base de datos.
Impacto cuantitativo
3. ¿Por qué no se validan esos campos?
Porque el requerimiento no especificaba validación por perfil.
4. ¿Por qué el requerimiento no lo especificaba?
Porque no se definieron criterios de aceptación diferenciados.
Lecciones prácticas
5. ¿Por qué no se definieron esos criterios?
Porque no hubo revisión técnica del requerimiento antes de su aprobación.
Causa raíz: Falta de revisión técnica en la etapa de validación de
requerimientos.

| Criterio  |                                                            | Si  No  N/A  |
| --------- | ---------------------------------------------------------- | ------------ |
|           | Es Completo si y sólo si cumple con los requerimientos en  | X            |
Lista de chequeo  ☐  ☐
él especificados.
|     | a. ¿Todos los casos de uso establecidos en el diagrama de  | X   |
| --- | ---------------------------------------------------------- | --- |
☐  ☐
| Completitud:   | casos de uso del sistema se encuentran especificados?       |     |
| -------------- | ----------------------------------------------------------- | --- |
| Se identifica  | b. ¿Se desarrolla en el artefacto la especificación de los  | X   |
de requisitos ☐  ☐
| y precisa las  | requerimientos suplementarios necesarios?               |     |
| -------------- | ------------------------------------------------------- | --- |
| partes que     | c. ¿Se cuenta con un histórico de revisiones para cada  | X   |
☐  ☐
| componen el  | versión del artefacto?                                       |     |
| ------------ | ------------------------------------------------------------ | --- |
| producto de  | d. ¿Se cuenta con un diagrama de actividades o flujo básico  | X   |
☐  ☐
| software.   | de actividades que represente cada caso de uso del sistema?   |     |
| ----------- | ------------------------------------------------------------- | --- |

|     | e. ¿Se identifican todos los usuarios que participan en el  | X  ☐  ☐  |
| --- | ----------------------------------------------------------- | -------- |
sistema en el diagrama de casos de uso?
|     | Es Pertinente si y sólo si cumple con los requerimientos en  | X  ☐  ☐  |
| --- | ------------------------------------------------------------ | -------- |
él especificados.
|     | a. ¿Los desarrollos de actividades de casos de uso cuentan  | X  ☐  ☐  |
| --- | ----------------------------------------------------------- | -------- |
Pertinente:
con las especificaciones relevantes, tales como: flujo
Precisar si
alterno, precondiciones, postcondiciones, etc…?
todo lo que
|     | b. ¿Los requisitos funcionales cuentan con las  | X   |
| --- | ----------------------------------------------- | --- |
☐  ☐
contiene el
especificaciones relevantes, tales como: campos, rangos de
producto es
valor, validaciones, etc…?
importante.
|     | c. ¿Los casos de uso especificados en el artefacto cumplen  | X  ☐  ☐  |
| --- | ----------------------------------------------------------- | -------- |
con los requerimientos y funcionalidades deseados del
sistema?
|     | Es Correcto si y sólo si cumple con los requerimientos en él  | X   |
| --- | ------------------------------------------------------------- | --- |
☐  ☐
| Correcto: Lo  | especificados.                                       |     |
| ------------- | ---------------------------------------------------- | --- |
| mostrado no   | a. ¿Los requisitos suplementarios especificados son  | X   |
☐  ☐
| contiene  | completamente verificables?                            |     |
| --------- | ------------------------------------------------------ | --- |
| errores.  | b.  ¿Los requerimientos funcionales especificados son  | X   |
☐  ☐
completamente verificables?
|             | Es Coherente si y sólo si cumple con los requerimientos en  | X     |
| ----------- | ----------------------------------------------------------- | ----- |
| Coherente:  |                                                             | ☐  ☐  |
| La          | él especificados.                                           |       |
X
| información  | a. ¿Los requerimientos suplementarios coinciden con los     | ☐  ☐  |
| ------------ | ----------------------------------------------------------- | ----- |
| mostrada no  | rangos de calidad previamente establecidos en el artefacto  |       |
| contradice   | del BRIEF?                                                  |       |
con la dada
X
|     | b. ¿Los casos de uso y sus especificaciones se contradicen  | ☐  ☐  |
| --- | ----------------------------------------------------------- | ----- |
en otro
con los entregables (backlog) previamente establecidos en el
módulo del
artefacto del BRIEF?
software.

Conclusión
• La prevención es pilar fundamental de la cultura de calidad.
• Previene errores antes de que ocurran, mejora eficiencia y ahorra
costos.
• Estrategias y herramientas preventivas potencian la calidad del
software.

Referencias
• Bass, L., Clements, P., & Kazman, R. (2012). Software Architecture in Practice (3rd ed.). Addison-Wesley.
• Crosby, P. (1994). Completitud, calidad para el siglo XXI. McGraw Hill.
• Deming, W. (1994). The new economics: for industry, government, education. Massachusetts Institute of
Technology.
• Fenton, N., & Bieman, J. (2014). Software metrics: a rigorous & practical approach. Chapman & Hall.
• GIDYC, CEISOFT & LISI (2011). Estudio de la Industria Nacional del Software: informe técnico. Proyecto de
Investigación FONACIT.
• Goerik, S. (2020). The future of software quality assurance. McGraw Hill.
• Gremba, J., & Myers, C. (2024). The ideal model: practical guide for improvement. Software Engineering
Institute.
• IEEE (2004). SWEBOK.
• Ishikawa, K. (1985). What is total quality control?: the Japanese way. Prentice Hall.
• Juran, J. M., & Gryna, F. M. (1993). Juran's Quality Handbook (5th ed.). McGraw-Hill.
• Kaner, C., Falk, J., & Nguyen, H. Q. (1999). Testing Computer Software (2nd ed.). Wiley.
• MTP Blog, junio 2025 - Prevención de defectos en QA de software
Caso sector Telco, MTP Blog, junio 2025 (ejemplos con listas de chequeo para integración de sistemas)
• Pfleeger, S. L., & Atlee, J. M. (2006). Software Engineering: Theory and Practice (4th ed.). Prentice Hall.
• Pressman, R. S. (2010). Software Engineering: A Practitioner's Approach (7th ed.). McGraw-Hill.