# Índice de Documentación — Proyecto PACS

Este índice rige la navegación de Claude dentro del proyecto. **Consultarlo SIEMPRE antes de leer cualquier archivo.** Si un documento no aparece aquí, preguntar antes de leerlo.

---

## 🎯 Contexto del Proyecto

**Materia**: Aseguramiento de la Calidad del Software (UCAB, 2026-2)
**Profesor**: Ernesto Suárez
**Proyecto**: Ecosistema de Aseguramiento de la Calidad del Software — Fase 1 (técnicas estáticas)
**Entrega**: Único PDF, máx. 30 páginas, en M7 del aula virtual, antes del **26 de octubre de 2026, 23:55**.

⚠️ **Regla crítica del proyecto**: Las alucinaciones anulan el proyecto de inmediato. Toda afirmación debe estar sustentada en documentación real.

---

## 👥 Roles del Equipo (5 roles oficiales)

| Rol | Responsabilidad clave |
|-----|----------------------|
| **Líder General** | Planificación, coordinación, comunicación, documentación, éxito del proyecto. |
| **Líder Funcional** | Comprensión del dominio, revisiones del sistema objeto. |
| **Líder Tecnológico** | Selección y configuración de herramientas, integración, gobernanza. |
| **Líder de Métricas** ⭐ | Definición, seguimiento y control estadístico de métricas. |
| **Escriba** | Estándares, administración documental, registros, trazabilidad. |

> El proyecto lista 5 roles. **No confundir con las configuraciones previas de 4 roles.**

---

## 📚 Documentación de la Materia

### 📁 `plantillas/`
Carpeta con esquemas de estándares. Contiene: estándares para pruebas y estructura base de documentos.

### 📁 `validaciones/`
Carpeta de apoyo para validar lo que se está haciendo en los documentos (checklists auxiliares, guías de verificación).

### 📁 `guias/`
Teoría general de la materia. **Carpeta de alta importancia**. Contiene material sobre:
- Métricas
- Prevención
- Construcción de calidad
- Especificaciones libres
- Otras técnicas estáticas

### 📁 `equipo/`
Lista de chequeos refinada por el escriba. Incluye:
- Lista de chequeo por historia de usuario individual
- Lista de chequeo para requerimientos funcionales
- Chequeador para revisión de historias de usuario
- Otros instrumentos de verificación

---

## 📄 Documentos del Proyecto

### `proyecto.md` ⭐ (uso constante)
Especificaciones completas del proyecto del semestre. **Es el documento rector.** Define:
- Objetivo general y descripción
- Los 5 roles y sus responsabilidades
- Los 6 entregables
- Los 5 estándares internacionales aplicables
- La rúbrica de evaluación (30 puntos, mín. 15)
- Reglas de entrega y fechas

**Regla**: cada decisión debe poder trazarse a una sección de `proyecto.md`.

### `DAS.md`
Documento de Arquitectura del Software. **Clave para métricas de producto y evaluación de arquitectura** (ISO/IEC/IEEE 42010).

### `BRIEF.md`
Contexto del cliente, alcance y objetivos de negocio. **Clave para métricas de proyecto.**

### `ERS.md`
Especificación de Requisitos de Software (ERS/SRS). **Documento central para las técnicas estáticas de la Fase 1.** Base para evaluar:
- Requerimientos funcionales
- Requerimientos no funcionales
- Historias de usuario
- Aplicación de ISO/IEC/IEEE 29148 como estándar de referencia.

⚠️ **Nomenclatura**: en este proyecto se usa el acrónimo en español **ERS**. No buscar ni referenciar como "SRS" en los entregables.

---

## 📏 Estándares Internacionales Aplicables

Todo el trabajo debe alinearse con:

| Estándar | Uso en el proyecto |
|---|---|
| **ISO/IEC 25010** | Modelo de calidad del producto software (base para métricas de producto). |
| **ISO/IEC 12207** | Procesos del ciclo de vida del software (base para métricas de proceso). |
| **ISO/IEC/IEEE 29148** | Requisitos de sistemas y software (base para lista de chequeo de reqs). |
| **IEEE 730** | Plan de Aseguramiento de la Calidad (estructura del PACS). |
| **ISO/IEC/IEEE 42010:2011** | Descripción de arquitectura (base para evaluar el DAS). |

---

## 📦 Entregables del Proyecto (6)

1. **Infograma del Ecosistema Tecnológico** — Visualización de herramientas + integración.
2. **Invitación al Espacio de Trabajo Compartido** — Acceso del docente con trazabilidad por rol.
3. **Lista de Chequeo Refinada** — Basada en muestra del docente, justificada por estándares.
4. **Plan de Aseguramiento de la Calidad del Software (PACS)** — Según IEEE 730.
5. **Evidencia de Ejecución de la Fase Estática** — Aplicación de listas + informe de revisiones + métricas.
6. **Reflexión sobre el Ecosistema Tecnológico** — Análisis crítico (ventajas, límites, IA).

**Apéndices obligatorios del PACS**:
- Informe de revisiones (gestión, instrumentos, aplicación, métricas, recomendaciones).
- Infograma + análisis del ecosistema.
- Resolución del alcance de objetivos SMART con evidencias y métricas.

---

## 📊 Requisitos Específicos del Rol de Métricas ⭐

El **Líder de Métricas** debe garantizar **mínimo 3 métricas** con las siguientes características:

| Tipo | Obligatorio | Característica exigida |
|------|-------------|------------------------|
| **Métrica de proceso** | Sí | Al menos una. |
| **Métrica de proyecto** | Sí | Al menos una. |
| **Métrica de producto** | Sí | Al menos una. |
| **Descriptiva (frecuencia + porcentaje)** | Sí | Al menos una. |
| **Descriptiva como índice** | Sí | Al menos una. |

**Además obligatorio**:
- **Comparaciones** entre métricas.
- **Correlaciones** entre métricas.
- **Umbrales** definidos explícitamente.
- **Trazabilidad** con el ecosistema integrado.
- **Gobernanza de los datos** involucrados.

---

## 🔗 Herramientas del Ecosistema (referencia)

Categorías mínimas exigidas:
- Aplicación de técnicas estáticas
- Métricas
- Automatización
- Reportes
- Gestión documental y del proyecto
- IA para apoyo del proceso

Ejemplos sugeridos por el docente:
- **Gestión documental**: Google Drive, Notion, Confluence, SharePoint
- **Inspección estática**: SonarQube, CodeScene, Review Board, GitHub Issues
- **Métricas**: Excel, Power BI, Grafana, JIRA Metrics
- **Automatización**: Python + Pandas, Jupyter, Google Apps Script
- **Control de versiones**: Git, GitHub, GitLab
- **Comunicación**: Slack, Discord, Teams

---

## 📋 Reglas de Navegación

1. **Consultar este índice ANTES de leer cualquier archivo.**
2. **Preferir `.md` sobre PDFs/DOCX** cuando existan ambos.
3. Si un documento no está listado aquí, **preguntar antes de leerlo**.
4. Toda afirmación en entregables debe poder **trazarse** a `proyecto.md` o a un estándar.
5. **Nunca inventar**: las alucinaciones anulan el proyecto.