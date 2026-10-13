<!-- Fuente: insumos para mantenibilidad.docx -->
<!-- Convertido: 2026-10-11T19:51:52 -->

Aquí tienes el desarrollo metodológico completo para la característica de **Mantenibilidad** (una de las características de calidad más críticas de la ISO/IEC 25010), estructurado bajo el mismo enfoque estático, preventivo y adaptado para el análisis del artefacto.

**1. Lo que capta**

Este instrumento capta **resistencia estructural del código frente a modificaciones futuras**.

Evalúa la facilidad, velocidad y seguridad con la que el artefacto puede ser comprendido, corregido, adaptado o mejorado por cualquier desarrollador (no solo por su autor). Capta el riesgo latente de que un cambio menor en el código genere un "efecto dominó" que rompa otras partes del sistema.

**2. El Instrumento de Inspección (Lista de Chequeo Estática)**

Diseñado para la revisión analítica del texto del código fuente centrado en la arquitectura, acoplamiento y legibilidad.

| **Dimensiones (Filas)** | **Área 1: Estructuras de Control y Lógica Algorítmica** | **Área 2: Capa de Datos y Persistencia (I/O)** | **Área 3: Gestión del Estado y Variables** | **Área 4: Interfaces de Comunicación y Frontera** |
| --- | --- | --- | --- | --- |
| **Dimensión 1: Modularidad y Reutilización** *(¿Está acoplado?)* | [ ] **Principio de Responsabilidad Única:** ¿Cada función o clase del artefacto resuelve una única tarea lógica bien definida, evitando componentes "Dios" que hacen de todo? | [ ] **Aislamiento de la Persistencia:** ¿El acceso a la base de datos está confinado en componentes específicos (ej. Repositorios/DAOs), evitando consultas directas esparcidas en la lógica del negocio? | [ ] **Encapsulamiento del Estado:** ¿Las variables y estructuras internas protegen su estado, exponiendo métodos de acceso controlados en lugar de permitir modificaciones externas globales? | [ ] **Inversión de Dependencias:** ¿Las fronteras del código dependen de abstracciones (interfaces) y no de implementaciones concretas, facilitando el intercambio de componentes externos? |
| **Dimensión 2: Analizabilidad y Comprensión** *(¿Se entiende?)* | [ ] **Complejidad Ciclomática Controlada:** ¿Las estructuras de control evitan anidamientos excesivos (if/else o switch masivos) que dificulten seguir el hilo mental del flujo? | [ ] **Transparencia en el Modelo:** ¿Los nombres de las tablas, campos y entidades en el código reflejan con total claridad el dominio del negocio, evitando abreviaturas crípticas o confusas? | [ ] **Auto-documentación y Semántica:** ¿Los nombres de las variables y funciones describen explícitamente su propósito técnico o de negocio, minimizando la necesidad de comentarios explicativos? | [ ] **Estandarización de Contratos:** ¿Las interfaces de comunicación (APIs/Mensajería) siguen un estándar de diseño uniforme y predecible en toda la extensión del artefacto? |
| **Dimensión 3: Modificabilidad y Evaluabilidad** *(¿Se puede cambiar/probar?)* | [ ] **Código Limpio de Duplicaciones:** ¿Se evita la repetición de fragmentos de código idénticos o muy similares, abstrayéndolos en funciones reutilizables (*Don't Repeat Yourself*)? | *No se asociaron ítems originales a esta celda específica.* | [ ] **Cohesión de Datos:** ¿Las variables relacionadas que viajan juntas a través del sistema se agrupan en estructuras o componentes limpios en lugar de pasarse como largas listas de parámetros? | [ ] **Diseño para la Testeabilidad:** ¿La estructura de las fronteras permite aislar los componentes mediante dobles de prueba (*mocks/stubs*) para realizar pruebas unitarias automatizadas? |

**3. La Métrica**

La métrica establece el **Índice de Mantenibilidad Estructural ($IME$)**. Evalúa la presencia de buenas prácticas de diseño y la ausencia de deuda técnica mediante la escala politómica aplicada a los 12 ítems:

* **2 puntos:** Cumplimiento Total (El artefacto es altamente modular, limpio y fácil de mantener).
* **1 punto:** Cumplimiento Parcial (Hay indicios de acoplamiento leve o problemas aislados de legibilidad).
* **0 puntos:** No Cumple (Presencia explícita de código espagueti, alta rigidez o nula testeabilidad).

$$IME = \left( \frac{\sum \text{Puntaje Obtenido}}{24} \right) \times 100$$

*(Donde 24 es el puntaje máximo ideal: 12 ítems $\times$ 2 puntos cada uno).*

**4. Unidad de Medida**

* **Unidad:** **Porcentaje de Salud de la Arquitectura ($\%$)**.
* **Significado operativo:** Representa la proporción en la que el artefacto está libre de factores de resistencia al cambio. Un puntaje alto indica que modificar o extender el software en el futuro requerirá un esfuerzo mínimo de tiempo, dinero y personal técnico.

**5. Escala de Interpretación**

Permite traducir el resultado porcentual en un diagnóstico de viabilidad sobre la evolución a largo plazo del sistema:

| **Rango Porcentual** | **Nivel de Mantenibilidad** | **Significado Técnico / Decisión Operativa** |
| --- | --- | --- |
| **90% a 100%** | **Código Limpio / Sostenible** | Diseño altamente modular. Excelente legibilidad y bajo riesgo de regresiones ante cambios. **Aprobado sin objeciones.** |
| **75% a 89%** | **Estable con Deuda Leve** | El software es mantenible, pero posee pequeños focos de acoplamiento o nombres mejorables. **Aprobado; registrar observaciones en el backlog.** |
| **60% a 74%** | **Rígido (Deuda Técnica Alta)** | El artefacto empieza a convertirse en "código espagueti". Cualquier cambio tiene alta probabilidad de romper otra funcionalidad. **Rechazado; requiere refactorización.** |
| **Menos de 60%** | **Inmanejable (Legado Tóxico)** | El diseño es monolítico, confuso e imposible de probar de forma aislada. Alto riesgo de abandono del código por inviabilidad económica. **Rechazado totalmente.** |

**6. El Instrumento de Walkthrough**

Diseñado para cuando el artefacto es analizado colectivamente mediante la exposición oral del programador (informante clave). El evaluador rastrea la salud del diseño a través de la narrativa del autor.

📋 **Guía de Escucha y Conducción:** Sigue la narrativa del autor mientras despliega la estructura del proyecto. Intervén con preguntas operacionales sobre el impacto del cambio.

* **[ ] Propiedad de Independencia (La Modularidad):** Al explicar el autor el mapa de archivos y carpetas, ¿el artefacto muestra una separación de responsabilidades clara o se observa que cambiar una regla de negocio obliga a modificar la base de datos y la interfaz en simultáneo?
* **[ ] Propiedad de Legibilidad (La Analizabilidad):** Cuando el autor lee y narra el flujo de una función compleja línea por línea, ¿el código proyectado es lo suficientemente intuitivo como para que un tercero lo entienda sin que el autor tenga que explicar "lo que quiso decir"?
* **[ ] Propiedad de Localización (El Impacto):** Ante la pregunta operacional *“Si el cliente pide mañana cambiar el proveedor de este servicio externo, ¿en cuántas partes del código tendríamos que meter la mano?”*, ¿el artefacto evidencia que el cambio está confinado en un solo componente o interfaz aislada?
* **[ ] Propiedad de Aislamiento (La Testeabilidad):** Al observar las uniones entre componentes explicadas por el autor, ¿el diseño del artefacto permite "desenchufar" la lógica para probarla de manera solitaria, o está tan soldada que es imposible probar una función sin encender todo el sistema?
* **[ ] Propiedad de Simplicidad (Ausencia de Duplicación):** A lo largo de la exposición de las diferentes áreas del código, ¿se constata que el autor reutiliza abstracciones existentes o se evidencia que el artefacto clona lógicas similares en múltiples archivos?

**7. Comentario Final**

Medir preventivamente la Mantenibilidad es un ejercicio de **sostenibilidad financiera y técnica**. Mientras que la Adecuación Funcional y la Eficiencia miran el éxito del software en el *presente* (que funcione hoy y corra rápido), la Mantenibilidad es la única característica que protege el *futuro* del artefacto. Utilizar este instrumento en un *walkthrough* permite captar de forma temprana si el equipo está construyendo una solución ágil o si está fabricando silenciosamente su propia trampa de deuda técnica.