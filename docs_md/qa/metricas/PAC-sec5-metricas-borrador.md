# Borrador - Aportes del Líder de Métricas al PAC (Proyecto 9)

Autor: Anthonny Baladi (Líder de Métricas)
Versión del borrador: 0.2 (12/10/2026). Ajustado a las listas de chequeo entregadas por la Escriba.
Estado: BORRADOR para revisión del equipo. Los umbrales marcados "(propuesto)" requieren acuerdo del equipo.
Capa de seguridad: pendiente de aprobación (ver `propuesta-objetivos-SMART-seguridad.md`). Este borrador cubre la revisión general.

Destino en el PAC:
- Parte A -> Sección 2.1 Organización (fila Líder de Métricas)
- Parte B -> Sección 5 Métricas
- Parte C -> Sección 9.1 Registros de Calidad: Métricas

---

## Parte A. Sección 2.1 - Descripción del trabajo (fila Líder de Métricas)

> Definición, seguimiento y control estadístico de las métricas de proceso, proyecto y producto del PACS. Diseña la ficha de cada métrica (entidad, atributo, fórmula, escala, método de recolección y umbral), consolida los datos generados por la aplicación de las listas de chequeo, aplica técnicas de control estadístico (gráfico p, Pareto, dispersión), realiza comparaciones y correlaciones entre métricas y elabora el informe de métricas del proceso de revisión. Responsable de la gobernanza de los datos de medición y, junto con la Escriba, actúa como revisor interno de los procesos.

Fuentes: proyecto.md, tabla de roles (Líder de Métricas); plantilla "esquema para estándares de proceso", sección ISO/IEC 29110 (el Líder de Métricas como auditor interno).

---

## Parte B. Sección 5 - Métricas

### 5.0 Texto introductorio

Las métricas del presente plan se definen siguiendo la estructura de IEEE 1061 (entidad de medición, atributo de calidad, función de la métrica, escala de medición y método de recolección) [II6 Métricas] y se clasifican en métricas de proceso, de producto y de proyecto [II6 Métricas]. Su propósito es aportar el control cuantitativo que caracteriza al nivel 4 "Gestionado" del modelo CMM, nivel que la plantilla del proyecto asigna como "responsabilidad directa del Líder de Métricas" [plantilla, esquema para estándares de proceso]. IEEE 730 establece que el plan defina "indicadores para evaluar procesos y productos" y que el aseguramiento se base en evidencias objetivas, entre ellas las métricas documentadas [III4 730].

Dado que la Fase 1 del PACS se limita a técnicas estáticas, todas las métricas se alimentan de la aplicación de las listas de chequeo refinadas por el equipo sobre las especificaciones del sistema Corpomotriz Los Salias: la ERS (4 historias de usuario y 4 requisitos suplementarios) y el DAS.

**Instrumentos y unidades de análisis**

| Instrumento | Dimensiones | Ítems contables | Se aplica a | Aplicaciones |
| --- | --- | --- | --- | --- |
| I1. Lista por HU individual (29148 + INVEST) | Identificación, Valor, Claridad, Completitud, Viabilidad, Revisión | 13 | Cada HU | 4 |
| I2. Lista de HU según buenas prácticas ágiles | Estructura narrativa, Criterios INVEST, Criterios de aceptación, Colaboración y contexto, Trazabilidad y claridad | 18 | Cada HU | 4 |
| I3. Lista del conjunto de HU | Cobertura funcional, Coherencia, Priorización, Revisión colaborativa, Evolución, Redundancia, Trazabilidad | 11 | Conjunto de las 4 HU | 1 |
| I4. Lista de requerimientos funcionales y complementarios | Completitud, Pertinente, Correcto, Coherente | 12 | ERS completa | 1 |
| I5. Lista del DAS | Pendiente | Pendiente | DAS | 1 |
| | | | **Total** | **11** |

**Definición operativa de defecto**: todo ítem marcado "No" en una aplicación de un instrumento. Los ítems "N/A" se excluyen del denominador.

**Regla de conteo para I4**: cada criterio de I4 tiene una fila resumen ("Es Completo si y sólo si cumple con los requerimientos en él especificados") y sub-ítems a, b, c... La fila resumen se deriva de sus sub-ítems (Sí solo si todos son Sí) y no se cuenta como ítem, para no contar dos veces el mismo defecto.

### 5.1 Tabla de métricas (formato de la plantilla del PAC)

| N | Definición | Objetivo | Procedimiento | Responsables |
| --- | --- | --- | --- | --- |
| M1 | **Distribución de defectos por dimensión** (Producto; descriptiva de frecuencia y porcentaje). Para cada instrumento, frecuencia absoluta de defectos por dimensión y porcentaje sobre el total del instrumento: %_k = (defectos_k / defectos_totales) x 100. | Identificar las dimensiones de calidad que concentran la mayoría de los defectos para priorizar las recomendaciones (regla 80/20). | 1. Contar los "No" por dimensión en todas las aplicaciones de cada instrumento. 2. Ordenar de mayor a menor frecuencia. 3. Calcular % y % acumulado. 4. Construir un diagrama de Pareto por instrumento. | Revisores (registro); Anthonny Baladi (cálculo y análisis). |
| M2 | **Índice de Conformidad de la Especificación (ICE)** (Producto; descriptiva como índice). ICE_j = Sí_j / (Sí_j + No_j), escala 0 a 1, por aplicación j. Su complemento p_j = 1 - ICE_j es la proporción de defectos usada en el gráfico p. | Medir el grado en que cada especificación cumple los atributos de calidad evaluados (ISO/IEC/IEEE 29148, INVEST, buenas prácticas ágiles) y detectar especificaciones fuera de control. | 1. Calcular ICE_j por cada una de las 11 aplicaciones. 2. Para las 4 HU, combinar I1 + I2 (31 ítems) y calcular p_j por HU. 3. Calcular media y desviación estándar de p sobre las 4 HU. 4. Graficar p_j contra los límites de control (ver 5.3). Las aplicaciones únicas (I3, I4, I5) se reportan como índice sin gráfico de control. | Jhoselin Bello y revisores (aplicación); Anthonny Baladi (cálculo y control estadístico). |
| M3 | **Eficiencia de revisión** (Proceso). ER_j = defectos detectados_j / horas-persona de revisión_j (defectos/hora), por aplicación j. | Evaluar la eficiencia del proceso de revisión estática y comparar su comportamiento entre instrumentos y revisores. | 1. Cada revisor registra hora de inicio y fin de cada aplicación. 2. Calcular horas-persona por aplicación. 3. Calcular ER_j. 4. Comparar por instrumento y por revisor. | Revisores (registro de tiempo); Anthonny Baladi (cálculo). |
| M4 | **Cobertura de revisión** (Proceso). CR = (aplicaciones de instrumento completadas / aplicaciones planificadas) x 100. Planificadas: 11 (tabla 5.0). | Verificar que la fase estática cubra la totalidad de las especificaciones incluidas en el alcance del PACS con todos sus instrumentos. | 1. Tomar el plan de revisiones como lista de aplicaciones planificadas. 2. Marcar cada una como completada al cerrar su lista. 3. Calcular CR en cada corte. | Devony Ramírez (plan de revisiones); Anthonny Baladi (cálculo). |
| M5 | **Cumplimiento del cronograma SQA** (Proyecto). CC = (actividades SQA completadas en la fecha planificada / actividades SQA planificadas a la fecha de corte) x 100. | Controlar el cumplimiento de plazos del plan de aseguramiento hasta la entrega del 26/10/2026. | 1. Tomar las actividades del Cronograma de SQA (sección 6). 2. En cada corte, comparar fecha real contra fecha planificada. 3. Calcular CC. | Devony Ramírez (seguimiento del cronograma); Anthonny Baladi (cálculo). |

Fuentes de clasificación y base de cada métrica:
- M1: herramienta de Pareto y hojas de verificación o listas de chequeo [II7 Control estadístico].
- M2: gráfico p para proporciones de unidades defectuosas [II7]; densidad de defectos [II6; plantilla, sección IEEE 730].
- M3: métricas de proceso: "eficiencia, tasas de defectos" [II6].
- M4: cobertura de requisitos evaluados [II6].
- M5: métricas de proyecto: "cumplimiento de plazos, costos y alcance" [II6].

### 5.2 Ficha IEEE 1061 de cada métrica

| N | Tipo | Entidad de medición | Atributo de calidad | Escala | Método de recolección |
| --- | --- | --- | --- | --- | --- |
| M1 | Producto | Conjunto de aplicaciones de un instrumento | Calidad de la especificación por dimensión | Conteo (entero) y porcentaje (0-100 %) | Listas de chequeo aplicadas |
| M2 | Producto | Aplicación de un instrumento sobre una especificación | Conformidad con los atributos del instrumento | Razón 0-1 | Listas de chequeo aplicadas |
| M3 | Proceso | Aplicación de un instrumento (sesión de revisión) | Eficiencia del proceso de revisión | Defectos/hora (razón >= 0) | Listas de chequeo + registro de tiempo |
| M4 | Proceso | Plan de revisiones | Completitud de la revisión | Porcentaje 0-100 % | Plan de revisiones + estado de listas |
| M5 | Proyecto | Cronograma SQA | Cumplimiento de plazos | Porcentaje 0-100 % | Cronograma SQA (sección 6) |

### 5.3 Umbrales

| N | Umbral | Base |
| --- | --- | --- |
| M1 | Las dimensiones que acumulan hasta el 80 % de los defectos de un instrumento se declaran prioritarias y deben tener recomendación explícita en el informe de revisiones. | Regla 80/20 [II7] |
| M2 | Gráfico p sobre las 4 HU. Límite superior: p_j > media(p) + 2 desv. estándar -> HU fuera de control (defectos anormalmente altos). Límite inferior: p_j < media(p) - 1 desv. estándar -> revisar (posible revisión superficial o HU sobresaliente). Adicional (propuesto): ICE_j >= 0,80 como nivel aceptable para toda aplicación. | Criterio del gráfico p [II7]; meta absoluta a acordar por el equipo |
| M3 | Mismos límites de control que M2 aplicados a ER_j sobre las 11 aplicaciones. | Criterio de control [II7] |
| M4 | 100 % al cierre de la fase estática. | Alcance del PACS |
| M5 | (propuesto) >= 90 % en cada corte; < 90 % activa acción correctiva del Líder General. | A acordar por el equipo |

### 5.4 Comparaciones y correlaciones planificadas

**Comparaciones**
- C1: ICE (M2) entre las 4 HU. Cada HU tiene un autor distinto en la ERS (Leonardo García, Edgar Paz, Alejandra Teixeira y Javier Delmoral). Pregunta: ¿la conformidad varía entre las HU?
- C2: Dimensiones comunes entre instrumentos. "Completitud" aparece en I1 y en I4; "Coherencia/Coherente" aparece en I3 y en I4. Pregunta: ¿el defecto aparece tanto a nivel de HU como a nivel de ERS?
- C3: ICE según I1 (29148 + INVEST) contra ICE según I2 (buenas prácticas ágiles) sobre las mismas HU. Pregunta: ¿los dos instrumentos coinciden en su diagnóstico?
- C4: Eficiencia de revisión (M3) entre revisores y entre instrumentos.

**Correlaciones** (diagrama de dispersión y coeficiente de Pearson [II7: dispersión]):
- R1: horas-persona de revisión contra defectos detectados, por aplicación (n = 11). Pregunta: ¿se encuentran más defectos cuando se revisa más tiempo?
- R2: ICE según I1 contra ICE según I2, por HU (n = 4). Complementa a C3.

Limitación declarada: con n = 4 HU y n = 11 aplicaciones, los límites de control y los coeficientes de correlación son indicativos y no concluyentes. Se complementan con juicio experto [II6: "complementar métricas con juicio experto"].

### 5.5 Gobernanza de los datos de medición

| Aspecto | Regla |
| --- | --- |
| Fuente única | Un solo registro de datos de medición en el espacio compartido: <HERRAMIENTA A DEFINIR CON EL LÍDER TECNOLÓGICO>. No se calculan métricas fuera de esa fuente. |
| Campos mínimos | id_aplicación, instrumento (I1-I5), especificación, revisor, fecha, hora_inicio, hora_fin, dimensión, ítem, resultado (Sí/No/N/A), observación. |
| Captura | Cada revisor registra sus propios resultados al aplicar la lista. |
| Validación | La Escriba (Valentina Izquierdo) verifica completitud y consistencia del registro antes de cada corte; se eliminan duplicados e inconsistencias [II6: recolección y análisis]. |
| Cálculo | Solo el Líder de Métricas calcula y publica resultados. |
| Versionado | El registro y los resultados se versionan en el espacio compartido; cada corte queda con fecha en la sección 9.1. |
| Acceso | Edición: equipo. Lectura: profesor (Entregable 2). |
| Trazabilidad | Cada valor en 9.1 enlaza a la lista de chequeo aplicada y a la especificación de origen. |

### 5.6 Cortes de medición

- Corte 1: al completar I1, I2 e I3 (historias de usuario).
- Corte 2: al completar I4 e I5 (ERS completa y DAS), que es el cierre de la fase estática.
- M5 se mide en ambos cortes.

---

## Parte C. Sección 9.1 - Registros de Calidad: Métricas (estructura a llenar)

No contiene datos todavía. Se llena con los resultados reales de cada corte.

| Fecha | Métrica | Resultado | Observaciones |
| --- | --- | --- | --- |
| dd/mm/aa | M1 Distribución de defectos por dimensión (I1, I2, I3) | | Corte 1 |
| dd/mm/aa | M2 ICE por HU y gráfico p | | Corte 1 |
| dd/mm/aa | M3 Eficiencia de revisión | | Corte 1 |
| dd/mm/aa | M4 Cobertura de revisión | | Corte 1 |
| dd/mm/aa | M5 Cumplimiento del cronograma SQA | | Corte 1 |
| dd/mm/aa | M1 a M5 (incluye I4 e I5) | | Corte 2 (cierre) |

---

## Pendientes y supuestos (no van al PAC)

1. **Marcas en la imagen de I4**: la imagen recibida ya trae X marcadas (Sí en Completitud, Pertinente y Correcto; No en Coherente). Confirmar si es el ejemplo de la muestra del profesor o una aplicación del equipo. No se usan como datos hasta confirmarlo.
2. **I4 completo**: confirmar que la imagen tiene la lista entera y que termina en "Coherente b".
3. **I4 y casos de uso**: varios ítems de I4 hablan de "casos de uso" y del "diagrama de casos de uso". La ERS trabaja con historias de usuario y diagramas de actividades. Si esos ítems se marcan N/A cambia el denominador de M2. Lo decide el Líder Funcional.
4. **I2 sin columnas Sí/No/N/A**: se supone que se aplica con la misma escala que las demás listas.
5. **I5 Lista del DAS**: no existe todavía.
6. **Herramienta de métricas**: definirla con Aarón Bastado (Líder Tecnológico).
7. **Umbrales propuestos** (ICE >= 0,80 y CC >= 90 %): validarlos con el equipo.
8. **Objetivos SMART** (sección 1, Líder General): cada objetivo debe apuntar a M1-M5 para el Apéndice 3.
9. **Supuesto**: la Fase 1 tiene una sola iteración de revisión, por eso el control estadístico usa las HU como muestras.
