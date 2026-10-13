<!-- Fuente: II7 Control estadístico.pdf -->
<!-- Convertido: 2026-10-11T19:46:08 -->

Control estadístico

Aseguramiento de la calidad del software
Unidad temática II Tema 7
Ing. Ernesto Suárez
Cultura de calidad

Introducción

Se aborda el tema 7 de la unidad temática II del programa de
aseguramiento de la calidad del software y los estándares que lo
respaldan.
• Introducción al control estadístico
• Fundamentos estadísticos de control
• Herramientas clásicas del control estadístico y aplicaciones
• Capacidad del proceso y mejora continua
• Desafíos y consideraciones en control estadístico
• Conclusiones

Introducción al control estadístico

Definición

Metodología para monitorizar y controlar la variabilidad en
procesos productivos o de servicios, usando herramientas
estadísticas.

Objetivo

Detectar a tiempo desviaciones significativas que
podrían generar productos fuera de especificación,
permitiendo acciones preventivas para mantener la
calidad.

Método

Aplica gráficos de control basados en estadísticas
de muestras tomadas del proceso, facilitando
identificar variaciones causadas por causas
comunes (esperadas) o causas especiales
(anómalas).

Importancia

Esencial para mejorar la eficiencia,
reducir defectos y potenciar la
satisfacción del cliente en entornos
industriales y de software.

Fundamentos estadísticos del control

La supervisión activa mediante
herramientas estadísticas fomenta la
mejora continua y reducción de defectos.

Media: valor promedio del conjunto de datos.
Desviación estándar: medida que indica cuánto
varían los datos respecto a la media.
Distribución: patrón o forma con que se
distribuyen los datos (normal, binomial, etc.).

Mejora
continua

Conceptos
básicos

Eliminar
causas
especiales

Variación
natural
versus
especial

Detectar y eliminar causas especiales permite
que el proceso opere bajo control estadístico,
garantizando calidad homogénea y
predecible.

Se distingue la variación natural (causas
comunes) que es inherente al proceso, de
las causas especiales que producen desviaciones
anormales.

Herramientas clásicas
para el control estadístico de procesos

Visualizan paso a paso un proceso,
Diagramas de
ayudando a identificar puntos críticos
flujo
para el control de calidad y
oportunidades de mejora.

Facilitan la recolección y organización de
datos, simplificando el registro de
ocurrencias y defectos.

Hojas de
verificación o
listas de chequeo

Espina de
pescado

Permite identificar y estructurar las
causas raíz de un problema de calidad,
facilitando la búsqueda de soluciones
efectivas.

Pareto

Ordena problemas o causas según su
frecuencia o impacto, ayudando a
enfocar esfuerzos en los factores más
significativos bajo la regla 80/20.

Monitorean la variabilidad del proceso a
lo largo del tiempo, detectando desvíos
fuera de los límites de control que
indican problemas en el proceso.

Control

Analiza la relación entre dos variables
para detectar correlaciones que puedan
Dispersión
influir en la calidad.

Representa la distribución de frecuencias
de un conjunto de datos, facilitando la
identificación de patrones y variabilidad.

Histograma

Herramientas clásicas
para el control estadístico de procesos
• Ejemplo: Gráfico p
(y np para n constante):
para proporciones de unidades
defectuosas.

Una muestra (j) podría ser un módulo que a su vez tiene un número de requisitos
asociados a él (nj) y que puede ser constante o variable, en la tabla es constante pero
generalmente será variable en nuestro caso. La pj es la frecuencia relativa de defectos
como división de defectos para la muestra entre el número de elementos (nj) de esa
muestra. Si se multiplica por 100 la pj, tendríamos un porcentaje de defectos de la
muestra. Por encima (más de 2 desviaciones estándares por encima del promedio) o por
debajo (menos de una desviación estándar por debajo del promedio) de los umbrales
supone problemas a controlar para esa muestra.

Gráficos de control: son la principal herramienta para monitorizar procesos estadísticamente.

Herramientas clásicas
para el control estadístico de procesos

• Ejemplo: Pareto

El 80% de las consecuencia proviene del 20% de las causas. El famoso
80/20. Por ejemplo, el tipo de queja 1 se produce 26 veces en una unidad
de tiempo (y 26 entre 86 que es el total de quejas por 100 es 30%). La queja
2 se produce 20 veces en una unidad de tiempo y así sucesivamente. Vemos
ya que el 72% de las quejas se produce por los tres primeros tipos de queja
solamente (80/20). Es urgente atender esos tres tipos de quejas. El tipo de
queja en nuestro caso pudiera ser un defecto, la frecuencia el número de
fallas que están asociadas a ese defecto como su causa y a partir de ahí
calcular el Pareto para priorizar atención en mantenimiento.

Gráficos de control: son la principal herramienta para
monitorizar procesos estadísticamente.

Capacidad del Proceso y Mejora Continua
en Desarrollo Ágil

La capacidad del proceso (medida con índices
como Cp y Cpk) indica qué tan bien un proceso
puede producir resultados dentro de los
límites especificados, clave para mantener
calidad en ciclos cortos de desarrollo .

En entornos ágiles, la capacidad se evalúa
frecuentemente en términos de velocidad,
estabilidad de entregas y número de defectos
por iteración.

El control estadístico se integra con
metodologías ágiles para permitir feedback
rápido y ajustes continuos, buscando reducir
variabilidad y mejorar calidad .

Ejemplos prácticos en desarrollo ágil:

Uso de métricas para controlar el número de errores detectados en pruebas
en cada sprint.

Monitoreo constante de tiempos de entrega y revisión por Kanban para
detectar cuellos de botella.

Implementación de pruebas automatizadas con métricas de cobertura para
asegurar calidad en entregas incrementales .

La mejora continua es clave en agile,
alimentada por métricas que permiten la
identificación rápido de problemas y su
corrección oportuna.

Desafíos y Consideraciones en la Implementación
de Control Estadístico en Desarrollo Ágil

La transición al control
estadístico en entornos ágiles
enfrenta retos como
resistencia al cambio
organizacional, falta de
formación y experiencia en
técnicas estadísticas, y
adaptabilidad a ciclos cortos e
iterativos .

La gestión de la incertidumbre
inherente a proyectos ágiles
puede dificultar la recolección
consistente y la interpretación
precisa de métricas para
control estadístico .

Las organizaciones deben
fomentar una cultura flexible
y colaborativa, con
comunicación transparente y
compromiso del equipo para
superar barreras y aprovechar
beneficios .

Capacitación continua y apoyo
en herramientas adecuadas
son críticos para un uso
efectivo de control estadístico
en equipos ágiles .

Se recomienda comenzar con
proyectos piloto y adaptación
progresiva para ajustar
prácticas a la realidad del
equipo y proceso .

Conclusiones para la agilidad

• El control estadístico de calidad es vital para monitorizar y mejorar procesos de
desarrollo y pruebas en entornos ágiles, aportando rigor y datos objetivos para
decisiones.

• Las metodologías ágiles mejoran la productividad, reducen defectos y aceleran la
entrega, gracias a ciclos cortos y métricas constantes que alimentan el control
estadístico.

• La integración de técnicas estadísticas en ciclos ágiles permite detectar
desviaciones y facilitar la mejora continua, fortaleciendo la calidad y la
satisfacción del cliente.

• Sin embargo, la adopción exitosa requiere superar retos culturales, técnicos y

organizacionales, impulsando formación continua y un compromiso colaborativo
en los equipos.

• Estudios muestran que equipos ágiles con control estadístico adecuado logran

mejores resultados en calidad del producto, eficiencia y rentabilidad.

Conclusiones generales

• El control estadístico de calidad (CEC) es una herramienta fundamental para

monitorear, controlar y mejorar la calidad en procesos productivos y de servicios.

• Permite detectar variaciones tanto comunes como especiales, lo cual facilita

actuar preventivamente para reducir defectos y costos asociados.

• La aplicación sistemática de CEC mejora la capacidad y eficiencia del proceso, lo

que se traduce en productos o servicios más consistentes y mayor satisfacción del
cliente.

• La clave del éxito es recopilar datos precisos y confiables, usar métodos

estadísticos adecuados y aplicar acciones correctivas basadas en los hallazgos.

• Además de corregir problemas inmediatos, el control estadístico permite

anticipar y prevenir futuras desviaciones, consolidando una cultura de mejora
continua.

• Los gráficos de control, junto con otras herramientas estadísticas de calidad, son

indispensables para la gestión eficaz y profesional de la calidad.

Referencias
• A. Al-Jadaa, Software Metrics, Birzeit University, 2014.

C. Laporte, A. April y K. Bencherif, Teaching Software Quality Assurance
in an Undergraduate Software Engineering Program, SQP, 2007.

• K. Ishikawa, What is Total Quality Control?: The Japanese Way, Prentice

Hall, 1985.

• J. Gremba and C. Myers, The Ideal Model: Practical Guide for

Improvement, Software Engineering Institute, 2024.

• R. Rood and J. Parker, Software Quality Assurance 101 Best Practices,

Made Easy, 2022.

• W. Edwards Deming, The New Economics: For Industry, Government,

Education, MIT, 1994.