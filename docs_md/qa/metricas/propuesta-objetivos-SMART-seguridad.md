# Propuesta: Objetivos de Calidad SMART con enfoque en Seguridad

Para: Devony Ramírez (Líder General) y equipo
De: Anthonny Baladi (Líder de Métricas)
Fecha: 11/10/2026
Destino en el PAC: Sección 1 "Objetivos de Calidad" (y ajustes a la Sección 5 "Métricas")

---

## 1. Por qué enfocar en Seguridad

1. Es la característica de ISO/IEC 25010 que elegimos en clases, y el curso trae un instrumento propio para ella (`guias/insumos para seguridad.md`). Ese instrumento ya incluye una métrica (ISEP) y una escala de interpretación, así que los umbrales salen del material del curso y no hay que inventarlos.
2. El sistema objeto tiene contenido de seguridad en los tres artefactos de la Fase 1:
   - **ERS, RNF 2.4.1 Confidencialidad**: "Cada transacción realizada en el sistema debe completarse correctamente y proteger la información sensible de los usuarios contra accesos no autorizados."
   - **ERS, las 4 historias de usuario**: todas declaran un alcance restringido a "usuarios autenticados con rol" (Administrador o cliente).
   - **DAS, secciones 1.1 y 1.3**: autenticación por correo y contraseña validada contra MySQL, y la afirmación de que la API RESTful "garantiza la seguridad en la red con el cliente".
3. El rol del Líder Tecnológico en el PAC ya incluye "su respectiva seguridad", así que hay un responsable natural para aplicar el instrumento.

El enfoque **no reemplaza** la revisión general. El proyecto exige una lista de chequeo por tipo de especificación (HU, RF, RNF y DAS) [proyecto.md, Entregable 5]. Lo que se agrega es una capa de seguridad sobre las especificaciones que tienen relevancia de seguridad.

## 2. Alcance propuesto

| Revisión | Aplicaciones de instrumento | Total |
| --- | --- | --- |
| General (listas de chequeo del equipo) | Lista por HU x 4 + lista ágil x 4 + conjunto de HU x 1 + lista RF/RNF sobre la ERS x 1 + lista del DAS x 1 | 11 |
| Seguridad (instrumento ISEP adaptado) | 4 HU + RNF 2.4.1 Confidencialidad + DAS | 6 |

## 3. Objetivos SMART propuestos

| N | Objetivo | Específico | Medible (métrica / umbral) | Alcanzable | Relevante | Plazo |
| --- | --- | --- | --- | --- | --- | --- |
| O1 | Completar el 100 % de las 11 aplicaciones de las listas generales y el 100 % de las 6 aplicaciones del instrumento de seguridad. | Aplicaciones listadas en la sección 2 | M4 Cobertura de revisión = 100 % | 17 aplicaciones sobre una ERS de 8 páginas y un DAS de 16 | Sin cobertura completa no se puede concluir sobre la calidad del producto | 21/10/2026 |
| O2 | Determinar el Índice de Seguridad Estructural Preventiva (ISEP) de cada una de las 6 especificaciones de seguridad y clasificarlas en la escala del instrumento. | 6 especificaciones, 3 dimensiones de seguridad | M2 ISEP (%). Escala: >= 90 % Blindado; 75-89 % Aceptable con advertencia; 60-74 % Vulnerable; < 60 % Inseguro | El instrumento y su escala ya existen en el material del curso | Mide directamente la característica elegida | 23/10/2026 |
| O3 | Identificar las dimensiones de seguridad que concentran el 80 % de los defectos detectados y emitir al menos una recomendación por cada dimensión prioritaria. | Dimensiones: Confidencialidad e Integridad; Autenticación y Autorización; Responsabilidad y No Repudio | M1 Pareto: % acumulado <= 80 % = prioritaria | Se calcula con los mismos datos de O2 | Orienta las recomendaciones del informe de revisiones | 24/10/2026 |
| O4 | Registrar el tiempo del 100 % de las sesiones de revisión y analizar la causa del 100 % de las sesiones con eficiencia fuera de los límites de control. | Sesiones de revisión de la Fase 1 | M3 Eficiencia de revisión (defectos/hora). Fuera de control: > media + 2 desv. o < media - 1 desv. [II7] | Basta con registrar hora de inicio y fin | Evalúa el proceso, no solo el producto | 21/10/2026 |
| O5 | Completar al menos el 90 % de las actividades del cronograma SQA en su fecha planificada, en cada corte de medición. | Actividades de la sección 6 del PAC | M5 Cumplimiento del cronograma >= 90 % (propuesto) | Cronograma interno del equipo | Garantiza la entrega del 26/10/2026, 23:55 | Cortes del 18/10 y 24/10/2026 |

Nota sobre O2: el objetivo es **medir y clasificar** la seguridad de las especificaciones, no que salgan "Blindadas". El ERS y el DAS no son nuestros, así que no controlamos su resultado. Sí controlamos medirlo bien y reportarlo.

## 4. Cómo se ajustan las métricas de la Sección 5

| N | Antes (general) | Ahora (enfoque seguridad) |
| --- | --- | --- |
| M1 | Pareto por dimensión de la lista general | Pareto por dimensión de seguridad (3 dimensiones del instrumento) |
| M2 | Índice de conformidad Sí / (Sí + No) | ISEP adaptado: escala 0/1/2 por ítem, puntaje obtenido / puntaje máximo x 100 |
| M3 | Eficiencia de revisión | Sin cambio |
| M4 | Cobertura sobre 11 aplicaciones | Cobertura doble: general (11) y seguridad (6) |
| M5 | Cumplimiento del cronograma | Sin cambio |

Correlación nueva: el índice de conformidad general de cada especificación contra su ISEP. Pregunta: ¿las especificaciones mejor escritas en general también son más seguras? Con n = 6 el resultado es indicativo.

## 5. Decisiones que necesitamos como equipo

1. **Confirmar el enfoque en Seguridad** como característica prioritaria del PACS.
2. **Adaptar el instrumento de código a especificaciones.** El instrumento del curso evalúa "el texto del código fuente" y tiene 12 ítems en 4 áreas de código. La Fase 1 revisa Brief, ERS y DAS. Propongo conservar las 3 dimensiones, la escala 0/1/2 y la escala de interpretación, y reformular los ítems para especificaciones. Por ejemplo, "Consultas Parametrizadas" se convierte en "¿La especificación exige protección contra inyección en el acceso a datos?". La adaptación la redactarían Aarón (seguridad) y Valentina (estándares), y yo la reviso para que la métrica siga siendo calculable. Hay que documentarla en el PACS como racionalización del instrumento.
3. **Aprobar el umbral de O5** (90 %).
4. **Asignar responsables**: Aarón aplica el instrumento de seguridad; Jhoselin, la lista general; Anthonny calcula y analiza.
5. **Lista de chequeo para el DAS**: hoy no está en la carpeta del equipo.
