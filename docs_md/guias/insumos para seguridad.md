<!-- Fuente: insumos para seguridad.docx -->
<!-- Convertido: 2026-10-11T19:51:52 -->

Aquí tienes el desarrollo metodológico completo para la característica de **Seguridad** (una de las características más críticas y transversales de la ISO/IEC 25010), estructurado bajo el mismo enfoque estático, preventivo y diseñado para captar las vulnerabilidades en el diseño lógico del artefacto antes de su ejecución.

**1. Lo que capta**

Este instrumento capta **el nivel de exposición de diseño estructural que comprometen la protección de la información y los recursos del sistema**.

No busca ataques en tiempo real ni evalúa la infraestructura de red; capta en qué medida el texto del código fuente implementa defensas nativas para garantizar que los datos no autorizados sean inaccesibles, que las acciones queden registradas y que las identidades sean verificadas de forma segura.

**2. El Instrumento de Inspección (Lista de Chequeo Estática)**

Diseñado para la revisión analítica del texto del código fuente enfocado en los pilares de la seguridad de la información.

| **Dimensiones (Filas)** | **Área 1: Estructuras de Control y Lógica Algorítmica** | **Área 2: Capa de Datos y Persistencia (I/O)** | **Área 3: Gestión del Estado y Variables** | **Área 4: Interfaces de Comunicación y Frontera** |
| --- | --- | --- | --- | --- |
| **Dimensión 1: Confidencialidad e Integridad** *(¿Los datos están protegidos?)* | [ ] **Sanitización de Entradas:** ¿El código limpia y valida de forma estricta todo dato externo antes de procesarlo, previniendo ataques lógicos o alteraciones de flujo? | [ ] **Consultas Parametrizadas:** ¿Se prohíbe la concatenación directa de variables en las consultas de base de datos, usando obligatoriamente parámetros lógicos para neutralizar inyecciones (ej. SQLi)? | [ ] **Cifrado de Datos Sensibles:** ¿El código garantiza que los datos críticos (contraseñas, tokens, datos personales) se procesen y almacenen usando algoritmos de hash fuerte o cifrado, evitando texto plano? | [ ] **Control de Exposición en Fronteras:** ¿Las API o interfaces filtran los payloads de salida para asegurar que solo viajen los campos autorizados, evitando la fuga accidental de datos internos? |
| **Dimensión 2: Autenticación y Autorización** *(¿Quién entra y qué hace?)* | [ ] **Principio de Menor Privilegio:** ¿Las funciones de control verifican explícitamente los permisos o roles del contexto antes de dar paso a la ejecución de acciones críticas? | [ ] **Seguridad a Nivel de Registro (Row-Level):** ¿Las consultas a la persistencia restringen los datos asegurando que el usuario en sesión solo pueda leer o modificar los registros que legítimamente le pertenecen? | [ ] **Manejo Seguro de Sesiones y Tokens:** ¿La lógica del artefacto gestiona los identificadores de sesión de forma efímera, invalidándolos ante cierres o expiraciones sin reutilizar estados? | [ ] **Blindaje de Endpoints:** ¿Todos los puntos de entrada externos del código cuentan con un interceptor o mecanismo de control de acceso que bloquee de forma nativa las peticiones anónimas? |
| **Dimensión 3: Responsabilidad y No Repudio** *(¿Hay rastro de las acciones?)* | [ ] **Trazabilidad de Acciones Críticas:** ¿El código invoca funciones de registro (logs) inmediatamente antes o después de que ocurra un evento sensible del negocio (mutaciones, borrados)? | [ ] **Logs Libres de Datos Sensibles:** ¿La estructura de los mensajes de auditoría en el código omite deliberadamente contraseñas, tokens o secretos, evitando la contaminación del registro? | *No se asociaron ítems originales a esta celda específica.* | [ ] **Inmutabilidad del Contexto de Auditoría:** ¿Los datos que identifican al autor de una acción (IDs, IPs) se toman de variables seguras del sistema y no de parámetros modificables enviados por el cliente? |

**3. La Métrica**

La métrica establece el **Índice de Seguridad Estructural Preventiva ($ISEP$)**. Evalúa formalmente la presencia de blindajes y la ausencia de vulnerabilidades mediante la escala politómica aplicada a los 12 ítems:

* **2 puntos:** Cumplimiento Total (El artefacto cuenta con mecanismos defensivos explícitos y correctos).
* **1 punto:** Cumplimiento Parcial (Existe intención defensiva, pero es inconsistente o delegada a librerías sin validación).
* **0 puntos:** No Cumple (Presencia de una vulnerabilidad crítica directa o exposición severa de datos).

*![](data:image/png;base64...) (Donde 24 es el puntaje máximo ideal: 12 ítems $\times$ 2 puntos cada uno).*

**4. Unidad de Medida**

* **Unidad:** **Porcentaje de Robustez Defensiva ($\%$)**.
* **Significado operativo:** Representa la proporción en la que el diseño del código está protegido de forma nativa contra la explotación de fallos lógicos elementales (como los descritos en estándares como OWASP).

**5. Escala de Interpretación**

Permite traducir el resultado porcentual en un dictamen sobre el nivel de riesgo de seguridad incrustado en el software:

| **Rango Porcentual** | **Nivel de Robustez** | **Significado Técnico / Decisión Operativa** |
| --- | --- | --- |
| **90% a 100%** | **Blindado (Riesgo Mínimo)** | El artefacto implementa defensas nativas robustas. La superficie de ataque a nivel de código es mínima. **Aprobado.** |
| **75% a 89%** | **Aceptable con Advertencia** | Existen controles de acceso y cifrado, pero hay descuidos menores (como logs demasiado verbosos o validaciones laxas). **Aprobado con correcciones inmediatas.** |
| **60% a 74%** | **Vulnerable (Riesgo Alto)** | Faltan controles de autorización críticos o hay consultas propensas a inyección. El software es explotable fácilmente desde el código. **Rechazado de forma tajante.** |
| **Menos de 60%** | **Inseguro / Expuesto** | El diseño ignora los pilares de la seguridad. Datos sensibles en texto plano o endpoints totalmente abiertos. **Rechazado y catalogado como peligroso.** |

**6. El Instrumento de Walkthrough**

Diseñado para cuando el artefacto es analizado colectivamente mediante la exposición oral del programador (informante clave). El evaluador utiliza la narrativa para rastrear cómo el código se defiende.

📋 **Guía de Escucha y Conducción:** Sigue el viaje de los datos que el autor describe. Intervén para validar el comportamiento del artefacto en escenarios de desconfianza.

* **[ ] Propiedad de Desconfianza Nativa (La Sanitización):** Cuando el autor describe cómo entran los datos desde el exterior, ¿el artefacto muestra filtros que validan la forma y el tipo de dato antes de que toque la lógica interna, o el código asume que el dato viene limpio?
* **[ ] Propiedad de Confinamiento (El Acceso):** Al exponer el autor un proceso sensible o una consulta, ¿el código evidencia que se valida la identidad y los privilegios del usuario en ese punto exacto, o se confía en que "la pantalla anterior ya validó"?
* **[ ] Propiedad de Opacidad (El Cifrado):** Al pasar por las variables que manejan secretos, credenciales o datos personales en el discurso del autor, ¿se observa en la pantalla que el artefacto los enmascara, hashea o cifra de inmediato, o viajan expuestos en memoria?
* **[ ] Propiedad de Evidencia (La Auditoría):** Ante la pregunta operacional: *“Si un usuario con malas intenciones intenta alterar este registro de forma maliciosa, ¿qué rastro imborrable deja el artefacto en los logs del sistema?”*, ¿la explicación y el código muestran la invocación automática de un registro seguro?
* **[ ] Propiedad de Hermeticidad (La Salida):** Al revisar las respuestas que el código envía de vuelta hacia el cliente o API, ¿el artefacto demuestra un diseño que entrega exclusivamente lo mínimo necesario, o devuelve objetos completos de la base de datos con campos ocultos expuestos?

**7. Comentario Final**

Diseñar e implementar este instrumento para la Seguridad desde un enfoque preventivo y estático cambia por completo el paradigma del desarrollo. Tradicionalmente, la seguridad se evalúa al final mediante costosas pruebas de penetración (*pentesting*) cuando el software ya está construido. Al captar estas debilidades en el *walkthrough* directamente sobre el artefacto, los fallos estructurales y lógicos (los más difíciles y caros de solucionar más adelante) se neutralizan en la mesa de diseño, garantizando un código inherentemente seguro desde su concepción.