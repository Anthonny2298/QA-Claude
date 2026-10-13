<!-- Fuente: II1 Mejoramiento continuo del proceso.pdf -->
<!-- Convertido: 2026-10-11T19:46:05 -->

Mejoramiento continuo
del proceso
Aseguramiento de la calidad del software
Unidad temática II Tema 1
Ing. Ernesto Suárez

Introducción
Se aborda el tema 1 de la unidad temática II del programa de
aseguramiento de la calidad del software y los estándares que lo
respaldan.
• Introducción al mejoramiento continuo
• Modelos y ciclos fundamentales para el mejoramiento continuo
• Estándares relevantes
• Definiciones y conceptos clave del SQA
• Factores críticos que causan fallas
• Componentes clave

Introducción al mejoramiento continuo
Importancia: El mejoramiento continuo es un
La naturaleza cambiante y compleja del enfoque sistemático para incrementar la
desarrollo de software requiere que las eficacia y la calidad en los procesos de
organizaciones adopten un ciclo de mejora Definición desarrollo de software mediante la
continua para adaptarse a nuevas implementación constante de cambios
tecnologías, demandas y fallas potenciales. para perfeccionarlos.
En la ingeniería de software, esta cultura
implica adoptar procesos y estándares
Objetivo principal:
(como ISO/IEC 25010 y 730) que permiten
Garantizar la entrega de software con
medir, analizar y mejorar sistemáticamente
Mejoramiento alta calidad y eficiencia, reduciendo
Importancia Objetivo
la calidad del software, fomentando una continuo defectos y optimizando recursos
cultura organizacional orientada a la
mediante revisiones periódicas y
excelencia y la mejora continua.
ajustes controlados.
Fundamentos clásicos:
•Deming: Ciclo PDCA (Planear, Hacer, Verificar, Actuar)
Fundamentos clásicos:
como motor para la mejora incremental y sostenida.
•Crosby: Enfatiza que la calidad es cumplir con
Fundamentos •Juran: La trilogía de calidad (planificación, control y
los requisitos y promueve la visión de "cero
clásicos
mejora) apunta a integrar la calidad en todas las etapas del
defectos" como meta del mejoramiento.
proceso.

Modelos y ciclos fundamentales
para el mejoramiento continuo
Actuar:
Ajustar para
Planificar:
mejora Planificación de la
Definir
Planificación
Actuar Planificar Enfoque de Crosby: calidad: Definir
objetivos y Cero defectos. de la calidad
objetivos y planes
Prevención.
planes
Ciclo PDCA de Deming
Hacer:
Verificar Hacer Trilogía
Ejecutar el
Verificar: Mejoramiento de la
plan de
Control de la calidad:
Evaluar calidad: Cambio y
Juran monitoreo, corrección
resultados avances
Estos modelos forman la base metodológica para Control
Mejoramiento de la
implementar una cultura de mejora continua en cualquier
de la calidad
calidad
organización de desarrollo de software, alineándose con
estándares internacionales.

Estándares relevantes
para el mejoramiento continuo
Estos estándares facilitan la implementación de
•ISO/IEC 730:
procesos coherentes y medibles, que soportan el
Norma que establece requisitos para
ciclo de mejora continua, contribuyendo a la calidad
ISO/IEC
procesos de aseguramiento de
sostenible del software. También es importante
730
calidad de software, con énfasis en
mencionar ISO 9001:2015, ISO/IEC 12207,
actividades sistemáticas de
ISO/IEC/IEEE 29119, CMMI (Capability Maturity
verificación y validación, que
Model Integration) y ISO/IEC 33000 e información
fortalecen la mejora continua del
sobre estos estándares la encontrarán en las notas
proceso.
de esta lámina.
SQA •ISO/IEC 25010:
•Modelo IDEAL del SEI:
Define un modelo de calidad para
Marco estructurado para la mejora de
productos de software basado en
procesos software que incluye
características como funcionalidad,
etapas: Iniciación, Diagnóstico, Modelo
ISO/IEC
fiabilidad, usabilidad, eficiencia,
IDEAL
Establecimiento, Actuación y 25010
del SEI mantenibilidad y portabilidad, que
Lecciones aprendidas; promueve la
guían el aseguramiento y mejora
mejora continua alineada con
continua.
estándares.

Modelo IDEAL
El modelo IDEAL es un marco estructurado 1.Iniciar (Initiating): Preparar la
desarrollado por el Software Engineering organización para el cambio obteniendo
Institute (SEI) para guiar la implementación de apoyo, recursos y compromisos. En la fase
mejoras sistemáticas en procesos de Iniciar, se asegura el patrocinio y la
organizacionales. infraestructura necesaria para el proyecto
5. Aprender (Learning): Revisar resultados,
Iniciar de mejora. Es crucial contar con el
extraer lecciones y ajustar para el siguiente
compromiso de la dirección.
ciclo de mejora. Se analizan los resultados y se
documentan las lecciones aprendidas para
2. Diagnosticar
alimentar futuros ciclos de mejora.
(Diagnosing): Evaluar el estado
Aprender Diagnosticar actual de los procesos para
identificar fortalezas y áreas de
4. Actuar (Acting): Implementar las mejoras,
mejora. Durante Diagnosticar, la
capacitar al equipo y monitorear el progreso.
organización evalúa críticamente
Implica la ejecución efectiva del plan, incluyendo
sus procesos actuales para
capacitación, implementación de mejoras piloto y
detectar fortalezas y debilidades
monitoreo constante.
mediante métodos formales.
3. Establecer (Establishing): Definir un plan de
acción con objetivos, prioridades y recursos Actuar Establecer
para implementar mejoras. Se desarrolla un
plan estratégico de mejora basado en el
diagnóstico, con objetivos claros, prioridades
y asignación de recursos.

Modelo IDEAL
Iniciar
Aprender Diagnosticar
Actuar Establecer
Beneficios:
Proporciona un enfoque disciplinado y sistemático para el mejoramiento de procesos.
Facilita la gestión del cambio y la sostenibilidad en las mejoras.
Es adaptable a diferentes tamaños y tipos de organizaciones.
Este modelo es especialmente valioso porque proporciona un proceso iterativo que ayuda
a las organizaciones a evolucionar sus procesos de manera controlada y sostenible,
minimizando riesgos y maximizando beneficios.

Aseguramiento de la calidad del software:
Definición y conceptos clave del SQA
Definición
El aseguramiento de la Diferencia entre "Que
Factores críticos que causan
calidad del software (SQA) es funcione" y "Que no falle": Importancia de SQA:
fallas:
Previene defectos desde
un conjunto de actividades
"Que funcione": Software
sistemáticas que garantizan Requerimientos mal etapas tempranas, reduce
cumple técnicamente con sus
que el software cumpla con definidos errores en producción y
funciones.
mejora la satisfacción del
los requisitos funcionales y
Código mal implementado
"Que no falle": Software no cliente mediante procesos de
de calidad, asegurando que
presenta errores que afecten Pruebas insuficientes verificación, validación y
el producto final sea
la experiencia del usuario mejora continua.
confiable, eficiente y Despliegues apresurados
final.
satisfaga las expectativas del
usuario.

Factores críticos que causan fallas
Porcentaje Aproximado
Causa Principal Descripción Breve
(%)
Definición insuficiente o errónea de requisitos
Requerimientos mal definidos 40 - 50
funcionales y no funcionales
Problemas en la fase de diseño afectan
Defectos en diseño y prototipado 15 - 20
funcionalidades y rendimiento
Falta de cobertura adecuada de pruebas, pruebas
Pruebas insuficientes 10 - 15
incompletas o mal diseñadas
Errores en la codificación, aunque menos
Código mal implementado No especificado directo
frecuentes cuando hay buenas pruebas
Problemas de comunicación y coordinación que
Falta de colaboración entre equipos Significativo no numérico
derivan en defectos

Mejoramiento Continuo en Software:
Componentes Clave
Implementación de Retroalimentación y Integración con
Medición y monitoreo Análisis de Causas:
Cambios: Aprendizaje: Estándares:
Uso de métricas y Identificación de las
Realización de Documentación de Aplicación coherente
KPIspara evaluar la causas raíz de
acciones correctivas y lecciones aprendidas de normas ISO, IEEE y
calidad del software y problemas para
preventivas basadas y ajuste continuo de modelos como IDEAL
la eficiencia de los garantizar soluciones
en evidencias y procesos y para asegurar calidad
procesos. efectivas y duraderas.
resultados. estándares. y mejora sistemática.
Lamedición y monitoreoes esencial Elanálisis de causaspermite ir más Laimplementación de Laretroalimentación y
Finalmente, integrar estas
para obtener datos objetivos sobre allá de los síntomas para encontrar el cambiosasegura que las mejoras aprendizajefomentan la cultura
actividades con estándares
cómo funcionan los procesos y qué origen real de los problemas, propuestas se pongan en práctica, de calidad porque se
internacionales como ISO/IEC 25010,
tan bien cumple el software con los utilizando herramientas como involucrando a todos los equipos documentan éxitos y fallos para
730 y modelos prácticos como IDEAL
estándares. Esto puede incluir diagramas de causa-efecto y análisis relevantes y usando metodologías mejorar continuamente los
asegura que el proceso de
métricas de defectos, cobertura de de fallas. ágiles o tradicionales según la procesos y evitar repetir errores.
mejoramiento esté alineado con las
pruebas, tiempos de respuesta y organización.
mejores prácticas mundiales.
satisfacción del usuario.

Referencias
| Al-Jadaa, A. (2014). | Software metrics. Birzeit |     | University. |     |
| -------------------- | ------------------------- | --- | ----------- | --- |
BrowserStack. (2025). 7 causas raíz de defectos de software y sus soluciones. Recuperado de https://www.browserstack.com/guide/root-causes-for-
software-defects-and-its-solutionstranslate.google
| Crosby, P. B. (1994). | Completitud, calidad para el siglo XXI. McGraw Hill. |     |     |     |
| --------------------- | ---------------------------------------------------- | --- | --- | --- |
Deming, W. E. (1994). The new economics: Forindustry, government, education. Massachusetts Institute of Technology.
GIDYC, CEISOFT, & LISI. (2011). Estudio de la industria nacional del software: Informe técnico. Proyecto de Investigación FONACIT.
Gremba, J., & Myers, C. (2024). The ideal model: Practical guide for improvement. Software Engineering Institute.
Innevo. (2024). Evita defectos: Importancia de las etapas del ciclo de vida del software. Recuperado de https://innevo.com/blog/etapas-del-ciclo-
de-vida-del-softwareinnevo
International Organization forStandardization. (2011). ISO/IEC 25010:2011 - Systems and software engineering— Systemsand software quality
| requirementsand evaluation |     | (SQuaRE) — | Systemand software quality | models. ISO. |
| -------------------------- | --- | ---------- | -------------------------- | ------------ |
International Organization forStandardization. (2008). ISO/IEC 730:2008 - Software quality assurance processes. ISO.
| Juran, J. M. (1974).             | Quality | control handbook. McGraw Hill. |                                 |     |
| -------------------------------- | ------- | ------------------------------ | ------------------------------- | --- |
| Laporte, C., & April, A. (2018). |         | Software quality               | assurance. John Wiley and Sons. |     |
Rood, R., & Parker, J. (2022). Software quality assurance 101 best practices, made easy. [s.n.].
SEI. (1996). The IDEAL model: A user’s guide forsoftware process improvement. Software Engineering
Institute. http://www.sei.cmu.edu/ideal.brige.html
ISO/IEC. (2011). Systems and software engineering —Systemsand software quality requirements and evaluation (SQuaRE) —System and
| software quality | models (ISO/IEC 25010). International Organization |     |     | forStandardization. |
| ---------------- | -------------------------------------------------- | --- | --- | ------------------- |
Pinkster, I., Burgt, B., Janssen, D., & Venendaal, E. (2004). Successful test management: An integral approach. Springer.