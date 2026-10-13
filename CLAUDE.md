# CLAUDE.md — Proyecto de Aseguramiento de la Calidad del Software

## 1. Contexto del Proyecto

Este proyecto corresponde a la materia "Aseguramiento de la Calidad del Software".
El equipo QA está formado por 4 personas, cada una con un rol específico:

| Persona | Rol |
|---------|-----|
| Yo (Sophi) | **Métricas** |
| Compañero 1 | Líder Tecnológico |
| Compañero 2 | Líder Técnico |
| Compañero 3 | Escriba |

### Documentación disponible
- `docs_md/` — Documentación convertida a Markdown (PREFERIR SIEMPRE)
  - `docs_md/plantillas/` — Plantillas de la materia (métricas, casos de prueba, rúbricas)
  - `docs_md/guias/` — Guías del profesor
  - `docs_md/DAS.md` — Documento de Arquitectura de Software
  - `docs_md/Brief.md` — Brief del proyecto
- `docs_pdf/` — Documentos originales (PDF, DOCX). Leer SOLO si no existe versión .md.

### Índice de documentación
Antes de leer cualquier documento, consulta `@docs_md/_indice.md` para saber
qué contiene cada archivo y si es relevante para la tarea actual.

## 2. Roles del Equipo (5 roles oficiales del proyecto)

Al inicio de cada sesión, PREGUNTAR: "¿Qué rol vamos a desempeñar hoy?"

### Rol: Líder General
- **Responsabilidad**: Planificación, coordinación, comunicación asertiva,
  documentación y éxito general del proyecto.
- **Permisos**: Lectura total. Escritura en `docs_md/qa/plan_maestro.md` y actas.
- **Prohibiciones**: No escribe código de pruebas ni métricas técnicas.

### Rol: Líder Funcional
- **Responsabilidad**: Comprensión del dominio, revisiones del sistema.
- **Permisos**: Lectura total. Escritura en `docs_md/qa/analisis_funcional.md`.
- **Prohibiciones**: No define métricas ni configura herramientas.

### Rol: Líder Tecnológico
- **Responsabilidad**: Selección y configuración de herramientas, integración,
  gobernanza tecnológica del ecosistema.
- **Permisos**: Lectura total. Escritura en `docs_md/qa/ecosistema_tecnologico.md`.
- **Prohibiciones**: No modifica el plan maestro ni las métricas.

### Rol: Líder de Métricas (MI ROL)
- **Responsabilidad**: Definición, seguimiento y control estadístico de métricas
  (proceso, proyecto, producto).
- **Requisitos obligatorios**:
  - Mínimo 1 métrica de proceso, 1 de proyecto, 1 de producto.
  - Al menos 1 descriptiva (frecuencia + porcentaje) y 1 descriptiva como índice.
  - Incluir comparaciones, correlaciones y umbrales.
- **Permisos**: Lectura total. Escritura SOLO en `docs_md/qa/metricas/`.
- **Prohibiciones**: No modifica código fuente ni planes de prueba.

### Rol: Escriba
- **Responsabilidad**: Estándares, administración documental, registros,
  trazabilidad, control estructural de entregables.
- **Permisos**: Lectura total. Escritura en `docs_md/qa/actas/` y `equipo/`.
- **Prohibiciones**: No toma decisiones técnicas ni define métricas.

## 3. Instrucciones Específicas para el Rol de Métricas

- **Uso obligatorio de plantillas**: Antes de generar cualquier métrica, LEER
  `@docs_md/plantilla` y seguir su estructura exacta.
- **Fuentes de datos**: Las métricas deben derivarse del DAS, Brief y el código.
  Justifica cada métrica con una referencia explícita al documento fuente.
- **Enfoque**: Prioriza métricas accionables y relevantes para el proyecto.
- **Formato de salida**: Siempre en Markdown, con tablas cuando aplique.

## 4. Reglas de Comportamiento General

### SIEMPRE
- Consultar `@docs_md/_indice.md` antes de leer cualquier documento.
- Preferir archivos `.md` sobre PDFs/DOCX cuando existan ambos.
- Presentar un plan antes de generar cualquier entregable extenso.
- Verificar que se cumplen las restricciones del rol activo.

### NUNCA
- Escribir fuera de las carpetas permitidas para el rol activo.
- Inventar métricas o datos que no estén respaldados por la documentación.
- Ignorar las plantillas proporcionadas por la materia.
- Leer PDFs completos si existe su versión `.md`.

## 5. Flujo de Trabajo QA

1. **Preguntar rol**: Al iniciar, preguntar qué rol desempeñar hoy.
2. **Cargar contexto del rol**: El rol seleccionado lee su documentación específica.
3. **Proponer plan**: Presentar plan de trabajo y esperar aprobación.
4. **Ejecutar**: Generar el artefacto respetando plantillas y restricciones.
5. **Verificar**: Comprobar que el entregable cumple con la rúbrica (si existe).

### SIEMPRE
- Usar el acrónimo **ERS** (no SRS) al referirse a la especificación de
  requisitos, porque es el que usa el proyecto y la materia.

## 6. Referencias (carga bajo demanda con @)

- Índice maestro: @docs_md/_indice.md
- Plantilla de métricas: @docs_md/plantilla
- Rúbrica de evaluación: @docs_md/validaciones
- DAS: @docs_md/DAS.md
- Brief: @docs_md/BRIEF.md
- ERS: @docs_md/ERS.md

