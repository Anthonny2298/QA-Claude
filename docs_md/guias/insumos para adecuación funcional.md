<!-- Fuente: insumos para adecuación funcional.docx -->
<!-- Convertido: 2026-10-11T19:51:51 -->

Aquí tienes el desarrollo metodológico completo para la característica de **Adecuación Funcional** estructurado exactamente bajo los componentes solicitados, manteniendo el enfoque estático y preventivo sobre el artefacto.

**1. Lo que capta**

Este instrumento capta **el nivel de alineación estructural entre la lógica escrita en el código fuente y los requisitos estipulados por el negocio**.

Evalúa la presencia de omisiones, errores de cálculo latentes o rigideces en el texto del artefacto que impedirán que el sistema cumpla con las tareas, objetivos y reglas solicitadas por el usuario.

**2. El Instrumento de Inspección (Lista de Chequeo Estática)**

Diseñado para la revisión analítica y directa del texto del código fuente a la luz de los requerimientos técnicos y de negocio.

| **Dimensiones (Filas)** | **Área 1: Estructuras de Control y Lógica Algorítmica** | **Área 2: Capa de Datos y Persistencia (I/O)** | **Área 3: Gestión del Estado y Variables** | **Área 4: Interfaces de Comunicación y Frontera** |
| --- | --- | --- | --- | --- |
| **Dimensión 1: Completitud Funcional** *(¿Está todo?)* | [ ] **Cobertura de Excepciones de Negocio:** ¿El flujo lógico del código implementa todos los caminos alternativos y restricciones estipulados en las reglas de negocio? | [ ] **Persistencia Completa de Entidades:** ¿Las operaciones de guardado o actualización impactan a la totalidad de los campos obligatorios exigidos por el modelo de datos del cliente? | [ ] **Validación de Casos de Borde:** ¿Se controla en las variables la existencia de valores nulos, vacíos o fuera de rango permitidos por el negocio antes de procesar? | [ ] **Trazabilidad del Requisito:** ¿Los endpoints o firmas de los métodos hacen referencia explícita o mapeable al requerimiento o historia de usuario que los originó? |
| **Dimensión 2: Corrección Funcional** *(¿Es exacto?)* | [ ] **Manejo Estructural del Error:** ¿El código captura las excepciones de forma controlada para evitar estados corruptos y asegurar una salida limpia estipulada por el diseño? | [ ] **Integridad de Transacciones:** ¿Las operaciones compuestas en la base de datos aplican reversiones (*rollbacks*) si un paso intermedio falla, garantizando la exactitud de los datos? | [ ] **Precisión de Tipos de Datos:** ¿Se utilizan tipos de datos numéricos adecuados para cálculos críticos (ej. evitar decimales flotantes en operaciones financieras) evitando errores de redondeo? | [ ] **Idoneidad en payloads de Salida:** ¿Los datos que el componente devuelve hacia el exterior se corresponden con la estructura matemática y formal esperada por el contrato del servicio? |
| **Dimensión 3: Pertinencia Funcional** *(¿Es oportuno?)* | [ ] **Ausencia de Pasos Redundantes:** ¿La estructura lógica ejecuta estrictamente las operaciones necesarias para cumplir la tarea del usuario, omitiendo burocracia algorítmica innecesaria? | *No se asociaron ítems originales a esta celda específica.* | [ ] **Parametrización de Reglas (No Hardcoding):** ¿Los valores sujetos a cambios del negocio (tasas, impuestos, límites) están parametrizados en variables de configuración externas en lugar de estar soldados en texto plano? | [ ] **Semántica en Mensajes de Error:** ¿Los textos y códigos de respuesta generados por las fronteras del software emplean el lenguaje conceptual del dominio del usuario y no jerga técnica interna? |

**3. La Métrica**

La métrica establece el **Índice de Adecuación Funcional Preventiva ($IAFP$)**. Evalúa formalmente la presencia de aciertos o la ausencia de defectos mediante una escala politómica aplicada a los 12 ítems de la matriz:

* **2 puntos:** Cumplimiento Total (El artefacto refleja con total fidelidad el requerimiento).
* **1 punto:** Cumplimiento Parcial (Hay indicios de omisión menor o rigidez en el diseño).
* **0 puntos:** No Cumple (Brecha explícita con la regla de negocio o error latente).

*![](data:image/png;base64...) (Donde 24 es el puntaje máximo ideal: 12 ítems x2 puntos cada uno).*

**4. Unidad de Medida**

* **Unidad:** **Porcentaje de Conformidad Funcional (%)**.
* **Significado operativo:** Representa la proporción en la que el diseño lógico del código se encuentra blindado contra desviaciones funcionales respecto al pliego de requisitos de la aplicación.

**5. Escala de Interpretación**

Permite traducir el resultado porcentual obtenido en un dictamen sobre la viabilidad del software para responder a las necesidades del negocio:

| **Rango Porcentual** | **Nivel de Madurez Funcional** | **Significado Técnico / Decisión Operativa** |
| --- | --- | --- |
| **90% a 100%** | **Fiel / Conforme** | Alta fidelidad con el negocio. El artefacto cubre las reglas de forma precisa y flexible. **Aprobado para pruebas con usuarios.** |
| **75% a 89%** | **Aceptable con Deuda** | El software cumple la tarea macro, pero posee rigideces (como *hardcoding*) o descuido en casos borde menores. **Aprobado con observaciones.** |
| **60% a 74%** | **Deficiente (Brecha Alta)** | Existen omisiones graves en las reglas de negocio o un manejo de errores precario que corromperá los datos. **Rechazado; requiere corrección.** |
| **Menos de 60%** | **Inviabilidad Funcional** | El código no se corresponde con las necesidades del cliente o ignora los flujos de excepción críticos del negocio. **Rechazado totalmente.** |

**6. El Instrumento de Walkthrough**

Diseñado para cuando el artefacto es analizado de forma colectiva e informal a través de la exposición oral del programador (informante clave). El evaluador utiliza el discurso técnico para rastrear la presencia de las variables en el código proyectado.

📋 **Guía de Escucha y Conducción:** Sigue la narrativa del autor sobre el flujo del programa. Intervén para validar si el artefacto posee las siguientes propiedades.

* **[ ] Propiedad de Completitud (La Cobertura):** A medida que el autor explica la lógica, ¿el código proyectado evidencia que se consideraron todos los caminos de excepción y restricciones del negocio, o se asumió únicamente el "camino feliz"?
* **[ ] Propiedad de Consistencia (Los Límites):** Al mostrar las funciones de entrada, ¿se observa en el artefacto que los parámetros están protegidos estructuralmente contra valores nulos o vacíos que inhabilitarían la función del negocio?
* **[ ] Propiedad de Exactitud (El Cálculo):** Cuando el autor detalla las operaciones matemáticas o lógicas del negocio, ¿las variables y estructuras del artefacto garantizan que el resultado intermedio y final conserve la precisión exigida?
* **[ ] Propiedad de Flexibilidad (La Configuración):** Al exponer los puntos donde se aplican políticas comerciales o de negocio, ¿el artefacto muestra que dichas reglas están parametrizadas o se encuentran incrustadas de forma rígida en las líneas de texto?
* **[ ] Propiedad de Blindaje (El Control):** Ante la pregunta operacional *“¿qué ocurre con los datos guardados si el proceso se interrumpe aquí?”*, ¿la arquitectura expuesta por el autor demuestra poseer mecanismos para evitar la pérdida de integridad funcional?

**7. Comentario Final**

Este enfoque metodológico para la Adecuación Funcional cierra un ciclo preventivo indispensable. Al evaluar de forma estática la correspondencia con el negocio —tanto en solitario con la matriz como guiados por el autor en el *walkthrough*— se mitiga el tipo de error más costoso en la ingeniería de software: **construir perfectamente un producto equivocado**. El instrumento asegura que el plano lógico sea fiel al cliente mucho antes de que se escriban las pruebas funcionales dinámicas o de aceptación.