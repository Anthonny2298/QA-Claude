<!-- Fuente: II2 Especificaciones libres de defectos.pdf -->
<!-- Convertido: 2026-10-11T19:46:06 -->

Especificación libre
de defectos
Aseguramiento de la calidad del software
Unidad temática II Tema 2
Ing. Ernesto Suárez

Introducción
Se aborda el tema 2 de la unidad temática II del programa de
aseguramiento de la calidad del software y los estándares que lo
respaldan.
• Introducción a las especificaciones del software.
• Especificaciones libres de defectos.
• Tipos comunes de defectos de especificaciones del software.
• Técnicas y herramientas.
• Estándares y buenas prácticas.
• Conclusiones.

Introducción a las especificaciones
del software
Las especificaciones de software son documentos o modelos que describen detalladamente qué debe hacer un
sistema de software, incluyendo funcionalidades, restricciones, interfaces y comportamientos esperados.
Definición
Constituyen la base para diseñar, desarrollar, probar y mantener el software, asegurando que todos los
involucrados tengan un entendimiento común de los requisitos.
Importancia
Especificaciones claras y completas ayudan a prevenir errores tempranamente, reducir costos asociados a
rectificaciones y mejorar la calidad del producto final (LC=Life cicle, ciclo de vida).
Impacto en
el LC
Errores, ambigüedades o inconsistencias pueden generar malentendidos, retrabajo, demoras y aumentar los costos
del proyecto.
Riesgos de
defectos

Especificaciones Libres de Defectos:
Concepto
Son retos: la complejidad creciente de sistemas;
Una buena especificación reduce
El objetivo de producir los cambios continuos en requisitos;
significativamente los errores y
la dificultad en capturar necesidades reales.
especificaciones libres de
ambigüedades, lo que previene
defectos es garantizar que el
Mejora comunicación entre stakeholders. que se propaguen a etapas
documento o modelo de
Facilita la validación y verificación.
posteriores donde el costo de
requisitos sea un reflejo fiel de lo Favorece la trazabilidad y mantenimiento.
corregirlos es mucho mayor.
que realmente se necesita y
Era común en los procesos
debe construirse. Esto implica Es la base para minimizar errores en fases
posteriores del desarrollo, reduciendo retrabajo y tradicionales que las
que sean completas, sin dejar costos asociados.
especificaciones quedaran
partes importantes sin cubrir,
incompletas o ambiguas, pero hoy
Especificaciones que están completas, claras,
claras para evitar malos
consistentes, sin ambigüedades ni contradicciones,
en día, dada la complejidad mayor
que describen fielmente los requisitos y
entendidos, coherentes en su
restricciones del software.
de los sistemas y la rapidez con
totalidad y sin contradicciones
que cambian los requisitos, es un
internas o externas.
gran desafío mantener esta
calidad en las especificaciones.
El equipo debe emplear técnicas como la revisión continua, validaciones con
usuarios finales y herramientas formales para lograr especificaciones libres de
defectos.

Defectos en Especificaciones de Software
Tipos Comunes
La falta de trazabilidad imposibilita el seguimiento de cambios y
validaciones, afectando la gestión efectiva de requisitos y el
Las especificaciones defectuosas suelen presentar varios tipos
mantenimiento. Finalmente, errores en los requisitos funcionales
de problemas que afectan directamente la calidad del producto
o no funcionales pueden derivar en un software que no cumple
y el éxito del proyecto. La ambigüedad es uno de los defectos
sus objetivos o que falla en aspectos esenciales como
más frecuentes y dañinos, ya que puede inducir a
rendimiento, seguridad o usabilidad. Identificar y corregir estos
interpretaciones erróneas en distintas fases del proyecto.
defectos en etapas tempranas es vital para garantizar
La incompletitud implica que faltan requisitos importantes o
especificaciones libres de defectos y sistemas de alta calidad.
detalles que son esenciales para satisfacer las necesidades del
cliente o las restricciones del sistema. Las contradicciones
internas dificultan la coherencia y generan conflictos durante la
implementación y las pruebas.
Errores en Requisitos
Contradicciones
Ambigüedad Incompletitud Falta de Trazabilidad Funcionales y No
Internas
Funcionales
Cuando un requisito Falta de información Requisitos que se No se puede seguir el Requisitos
puede interpretarse o requisitos contradicen entre sí origen y evolución incorrectos,
de múltiples esenciales que dentro del mismo de los requisitos, irrelevantes o
maneras, afectan el diseño y documento o con dificultando el inapropiados que
generando desarrollo. otros documentos. control y afectan el
confusión. mantenimiento. comportamiento
esperado y calidad
del sistema.

Especificaciones Libres de Defectos:
Técnicas y Herramientas
Revisiones y validaciones formales Lenguaje de especificación Revisión por pares
| Evaluaciones  | Uso de UML,  |     |
| ------------- | ------------ | --- |
Talleres y
| estructuradas  | diagramas,  |     |
| -------------- | ----------- | --- |
sesiones
modelos formales
| para detectar  |     | colaborativas  |
| -------------- | --- | -------------- |
para describir
| ambigüedades y  | requisitos con  | para mejorar  |
| --------------- | --------------- | ------------- |
comprensión y
| errores. | claridad y  |     |
| -------- | ----------- | --- |
calidad.
precisión.
| Gestión de trazabilidad | Gestión de cambios |     |
| ----------------------- | ------------------ | --- |
Control
Herramientas para  sistemático de
rastrear requisitos
modificaciones
desde origen hasta
para mantener
pruebas y  integridad y
mantenimiento. consistencia.

Especificaciones Libres de Defectos:
Estándares y Buenas Prácticas
Buenas prácticas:
ISO/IEC/IEEE 29148:
Norma internacional para la • Desarrollo iterativo con
gestión y especificación de
validaciones frecuentes.
requisitos de software.
• Participación activa de
stakeholders.
• Uso de plantillas y documentación
estandarizada.
• Herramientas de gestión de
requisitos para trazabilidad y
control de cambios.
IEEE 830:
CMMI e IDEAL:
Recomendaciones para la
Integración de prácticas de
elaboración de
mejora continua para madurar
especificaciones claras,
procesos de especificación.
completas y verificables.

Conclusiones
• Especificaciones libres de defectos son fundamentales para calidad y
éxito de software.
• Técnicas formales, estandarización y participación activa de
stakeholders son claves.
• La mejora continua y el cumplimiento de estándares contribuyen a
especificaciones más robustas.

Referencias
CMMI Institute. (2018). CMMI for Development, Version 2.0. Carnegie Mellon University.
IEEE. (1998). IEEE Recommended Practice for Software Requirements Specifications (IEEE Std
830-1998). IEEE.
International Organization for Standardization. (2011). ISO/IEC/IEEE 29148: Systems and
software engineering — Life cycle processes — Requirements engineering. ISO.
Laporte, C., & April, A. (2018). Software quality assurance. John Wiley and Sons.
Software Engineering Institute. (1996). The IDEAL model: A user’s guide for software process
improvement. Carnegie Mellon University. http://www.sei.cmu.edu/ideal.brige.html
Sommerville, I. (2011). Software Engineering (9th ed.). Pearson.
Ortega Cabrera, E. E., & Villavicencio Cabezas, M. (2011). Medición de la calidad de
productos de software en un ambiente académico usando la norma ISO/IEC 9126. Escuela
Superior Politécnica del Litoral (ESPOL).
Zárate, R. F. D. (2016). Aplicación de métricas de calidad en uso utilizando la ISO 9126. CORE.