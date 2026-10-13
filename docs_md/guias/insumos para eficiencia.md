<!-- Fuente: insumos para eficiencia.docx -->
<!-- Convertido: 2026-10-11T19:51:51 -->

Si lo reducimos a su significado conceptual más estricto dentro de la teoría de la medición, este instrumento, aplicando esa fórmula y escala, lo que capta es:

**El nivel de vulnerabilidad arquitectónica del software frente al hardware.**

En términos métricos, no capta el comportamiento del sistema, sino la **calidad de su diseño lógico**. Capta en qué medida el texto escrito por el desarrollador introduce o no factores de riesgo que sabotearán el rendimiento físico de la máquina cuando el programa sea ejecutado.

Al pasar la lista de chequeo por la matriz, lo que captas numéricamente es un **perfil de madurez estructural**.

Al colocar las **Dimensiones en las filas** y las **Áreas de Manifestación en las columnas**, cruzamos el constructo teórico (el "qué") con el sustrato físico del código (el "dónde").

Aquí tienes la tabla de doble entrada con los **12 ítems originales de eficiencia de desempeño**, distribuidos de forma exacta según su correspondencia metodológica:

| **Dimensiones (Encabezado de Fila)** | **Área 1: Estructuras de Control y Lógica Algorítmica** | **Área 2: Capa de Datos y Persistencia (I/O)** | **Área 3: Gestión del Estado y Variables** | **Área 4: Interfaces de Comunicación y Frontera** |
| --- | --- | --- | --- | --- |
| **Dimensión 1: Comportamiento Temporal** *(¿Cuánto tarda?)* | [ ] **Complejidad Algorítmica en Bucles:** ¿Se evita el uso de bucles anidados innecesarios que eleven la complejidad temporal a niveles críticos (por ejemplo, operaciones $O(n^2)$ o superiores sobre colecciones grandes)? | [ ] **Estrategia de Carga de Datos (Lazy vs. Eager Loading):** En las relaciones de bases de datos o instanciación de objetos, ¿se cargan los datos bajo demanda (*lazy*) en lugar de traer toda la estructura a memoria de golpe si no se va a utilizar de inmediato? | [ ] **Operaciones de Cadena (String Manipulation):** En bucles de alta iteración, ¿se utilizan estructuras eficientes (como StringBuilder o equivalentes según el lenguaje) en lugar de la concatenación tradicional que genera múltiples objetos inmutables en memoria? | [ ] **Procesamiento Asíncrono / No Bloqueante:** ¿Las operaciones pesadas o de larga duración (como I/O de archivos, llamadas a APIs externas o envío de correos) se ejecutan de forma asíncrona para no bloquear el hilo principal (*main thread*)? |
| **Dimensión 2: Utilización de Recursos** *(¿Qué consume?)* | [ ] **Instanciación Eficiente de Objetos:** ¿Se evita la creación repetitiva de objetos pesados dentro de bucles o funciones de alta frecuencia? ¿Se aplican patrones como *Singleton* o *Flyweight* donde corresponda? | [ ] **Uso de Pools de Conexiones:** ¿Las interacciones con bases de datos o servicios externos reutilizan conexiones activas a través de un *Pool* en lugar de abrir y cerrar una conexión física nueva en cada petición?    [ ] **Paginación de Datos:** Al realizar consultas que retornan grandes volúmenes de registros, ¿se implementa paginación o límites estructurales (LIMIT / OFFSET) para evitar saturar el canal de red y la memoria del servidor? | [ ] **Control de Fugas de Memoria (Memory Leaks):** ¿El código garantiza la liberación de memoria o la desuscripción de eventos/observadores, especialmente en entornos donde el recolector de basura (*Garbage Collector*) no actúa de forma automática?    [ ] **Manejo de Streams para Archivos Grandes:** Al leer o escribir archivos de gran tamaño (o subidas de usuarios), ¿se procesan los datos por fragmentos (*buffers/streams*) en lugar de cargar el archivo completo en la memoria RAM? | [ ] **Tamaño de Carga Útil (Payload Optimization):** ¿Los datos que viajan por la red (JSON, XML) están optimizados, enviando únicamente los campos necesarios y evitando redundancias que consuman ancho de banda innecesario? |
| **Dimensión 3: Capacidad** *(¿Cuánto aguanta?)* | [ ] **Gestión de Concurrencia y Bloqueos (Locking):** Al trabajar con múltiples hilos o procesos concurrentes, ¿los bloqueos de recursos (*locks*) son lo más granulares y cortos posible para evitar hilos en espera (*thread starvation*) o bloqueos mutuos (*deadlocks*)? | *No se asociaron ítems originales a esta celda específica.* | *No se asociaron ítems originales a esta celda específica.* | [ ] **Estrategias de Caché:** ¿Se almacenan en una memoria intermedia (como Redis o caché en memoria local) aquellos datos que tienen alta frecuencia de lectura y baja tasa de modificación, reduciendo el estrés en la base de datos? |

Para que este instrumento funcione con total rigor metodológico en el plano de la medición estática y preventiva, la fórmula, la unidad y la escala deben medir **atribuciones de cumplimiento estructural** (puntos de control superados) y no variables físicas en movimiento (como segundos o megabytes).

Aquí tienes la estructura métrica exacta para tu matriz de 12 ítems:

### 1. Fórmula de Cálculo

La métrica central mide el **Índice de Eficiencia Estructural Preventiva ($IEEP$)**. Se calcula mediante la relación porcentual entre los puntos obtenidos tras la inspección visual y el puntaje máximo alcanzado por el diseño ideal.

Cada uno de los 12 ítems se evalúa con una escala politómica:

* **2 puntos:** Cumplimiento Total (No hay indicios de riesgo).
* **1 punto:** Cumplimiento Parcial (Hay indicios leves o aplicación inconsistente).
* **0 puntos:** No Cumple (Presencia explícita del cuello de botella/defecto).

$$IEEP = \left( \frac{\sum \text{Puntaje Obtenido}}{24} \right) \times 100$$

*(Donde 24 representa el puntaje máximo posible: 12 ítems $\times$ 2 puntos máximo cada uno).*

### 2. Unidad de Medida

Dado que estamos ante una medición estática basada en un criterio de conformidad respecto a un estándar (ISO 25010), la unidad de medida no es física, sino un indicador relativo:

* **Unidad:** **Porcentaje de Conformidad Estructural ($\%$)**.
* **Significado operativo:** Representa el grado en que el diseño lógico del código está libre de predictores de fricción con el hardware. Un $80\%$, por ejemplo, significa que el código cumple con el $80\%$ de las pautas óptimas de ingeniería para prevenir el desperdicio de recursos.

### 3. Escala de Interpretación

Al ser una medición preventiva de riesgos antes del despliegue, el resultado porcentual se mapea contra una **escala ordinal de viabilidad o madurez arquitectónica**:

| **Rango Porcentual** | **Nivel de Madurez Preventiva** | **Decisión Operativa / Significado Técnico** |
| --- | --- | --- |
| **90% a 100%** | **Optimizado (Riesgo Mínimo)** | El diseño es maduro. Posee un blindaje estructural excelente contra el desperdicio de recursos. **Aprobado para producción.** |
| **75% a 89%** | **Aceptable (Deuda Técnica Controlada)** | Existen indicios leves de fricción, pero no comprometen la estabilidad global. **Aprobado con observaciones menores.** |
| **60% a 74%** | **Crítico (Riesgo Latente)** | Se detectaron fallos estructurales importantes (ej. bucles $O(n^2)$ o falta de paginación). El software sufrirá bajo estrés. **Rechazado; requiere refactorización obligatoria.** |
| **Menos de 60%** | **Deficiente (Inviabilidad Estructural)** | El diseño lógico ignora casi por completo las pautas de eficiencia. Alto potencial de colapso de infraestructura o fugas masivas. **Rechazado totalmente.** |

En un *walkthrough*, el autor no está siendo evaluado; él es tu **guía turístico y microscopio viviente**. Al conocer las entrañas del sistema, su exposición oral te sirve para "hacer zoom" y alumbrar los rincones del artefacto que a solas te tomaría días entender. El autor es el puente para que tú captes las propiedades estructurales del software.

Para lograr esto, la lista de chequeo deja de evaluar la "solidez de su respuesta" y se convierte en un **rastreador de propiedades del artefacto guiado por el discurso**.

Así se reconfigura el instrumento bajo este enfoque metodológico:

## Lista de Control de Walkthrough: El Autor como Informante del Artefacto

📋 **Instrucciones para el Evaluador:** Escucha la exposición técnica del autor y observa el código proyectado. Utiliza su narrativa para marcar la presencia de las siguientes **propiedades de eficiencia estructural** en el artefacto.

### Dimensión 1: Comportamiento Temporal (El Artefacto en el Tiempo)

* **[ ] Linealidad de la Lógica Algorítmica:** A través de la explicación del flujo de control que hace el autor, ¿se constata que el artefacto ejecuta recorridos directos sobre las colecciones de datos, sin anidamientos que disparen el tiempo de procesamiento?
* **[ ] Desacoplamiento de Operaciones Pesadas (Asincronía):** Al exponer el autor las fronteras del sistema (I/O, APIs), ¿se observa en el artefacto la estructura de hilos independientes o promesas que evitan el bloqueo del hilo principal?
* **[ ] Carga Bajo Demanda:** Cuando el autor describe la instanciación o la consulta de datos, ¿el código muestra mecanismos de exclusión para no traer datos que el flujo actual no requiere?

### Dimensión 2: Utilización de Recursos (El Artefacto ante el Hardware)

* **[ ] Ciclo de Vida Conservador de Objetos:** Cuando el autor muestra dónde se crean y destruyen los componentes en la arquitectura, ¿el artefacto evidencia una política de reutilización (instancias compartidas o patrones de creación controlada)?
* **[ ] Segmentación de Flujos de Datos (Streams):** Al guiar el autor la lectura/escritura de archivos o payloads, ¿el artefacto cuenta con buffers o canales de flujo fragmentado en lugar de asignaciones masivas de memoria RAM?
* **[ ] Mecanismos de Liberación Explícita:** Al cierre del ciclo del proceso expuesto por el autor, ¿se observa en el artefacto que las conexiones, eventos o recursos asignados quedan explícitamente liberados?

### Dimensión 3: Capacidad (El Artefacto bajo Carga)

* **[ ] Aislamiento de la Persistencia (Caché):** Al exponer las zonas de alta demanda, ¿el artefacto cuenta con una capa de retención intermedia que evite que las peticiones idénticas golpeen repetidamente el almacenamiento principal?
* **[ ] Concurrencia Confinada (Bloqueos Mínimos):** Al revisar los puntos de acceso simultáneo explicados por el autor, ¿las secciones críticas del código poseen delimitaciones de exclusión mutua angostas y breves para prevenir bloqueos del sistema?

### ¿Qué capta el instrumento en esta modalidad?

Bajo este enfoque, el instrumento capta exactamente lo mismo que en la revisión en solitario: **los indicadores de riesgo e ineficiencia estructural del artefacto**.

La única diferencia es el **canal de captura**: en lugar de descubrir los indicadores mediante una lectura analítica individual del texto completo, los captas **validando visual y auditivamente las afirmaciones técnicas que el autor hace sobre los componentes clave del código**. El artefacto se mide igual, pero de manera guiada y eficiente.