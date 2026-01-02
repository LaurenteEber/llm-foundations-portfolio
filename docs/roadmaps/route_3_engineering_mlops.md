# Ruta 3: ingeniería, sistemas y mlops para IA y llms

## 1. Propósito y criterio de diseño

- Construir proyectos reproducibles, mantenibles y evaluables.
- Operar sistemas basados en llms (RAG/serving/observabilidad) con disciplina de ingeniería.
- Cubrir brechas típicas de admisión para perfiles no-CS: **data structures, algorithms y complejidad**.

---

## 2. Fase 0: fundamentos de ciencias de la computación para IA (brecha A)

**Objetivo:** cubrir prerequisitos típicos de cursos de IA (especialmente planning/search).

### Temas clave
- Estructuras de datos: arrays, stacks/queues, hash tables, heaps, trees.
- Algoritmos: búsqueda, sorting, grafos (BFS/DFS/Dijkstra/A*).
- Complejidad: Big-O, trade-offs espacio/tiempo.
- Técnicas: recursión, programación dinámica.
- Buenas prácticas: testing, debugging, profiling básico.

### Recursos recomendados
- Libro (elige 1):
  - CLRS — *Introduction to Algorithms* (4.ª ed.).
  - Skiena — *The Algorithm Design Manual* (3.ª ed.).
- Curso (elige 1):
  - MIT 6.006 o Princeton Algorithms.

### Entregable mínimo (portafolio)
- Repo `cs-fundamentals-for-ai` con implementaciones + README en inglés + tests.

---

## 3. Fase 1: fundamentos de ingeniería y entorno de trabajo

**Objetivo:** estándar profesional de repo para todos tus proyectos.

### Temas clave
- Git avanzado (ramas, PRs, tags).
- Estructura de repos (`src/`, `tests/`, `configs/`, `notebooks/`, `scripts/`).
- Entornos y dependencias (`pyproject.toml`, `poetry`/`uv`/`pip-tools`).
- Calidad: formatter/linter, tipado, pytest.
- Linux y tooling: CLI, bash básico, make/just (recomendado).
- Contenedores (Docker) como opcional recomendado (para el proyecto final).

### Recursos núcleo
- *Pro Git* (Chacon & Straub).
- *The Pragmatic Programmer* (Hunt & Thomas).
- *Effective Python* (Slatkin).

---

## 4. Fase 2: arquitectura de software para sistemas de ML

**Objetivo:** pasar de notebooks a sistemas modulares.

### Temas clave
- Capas: dominio / aplicación / infraestructura.
- Patrones: puertos y adaptadores, inyección de dependencias.
- Configuración declarativa (YAML + dataclasses/pydantic).
- Testing: tests de datos, tests de entrenamiento corto, tests de métricas.

### Recursos núcleo
- Percival & Gregory — *Architecture Patterns with Python*.
- Chip Huyen — *Designing Machine Learning Systems* (visión de sistemas ML).

---

## 5. Fase 3: data engineering para corpora de texto y llms

**Objetivo:** pipelines de texto con trazabilidad y calidad.

### Temas clave
- Ingesta y limpieza: normalización, filtros, deduplicación (conceptual + práctica).
- Formatos: JSONL/Parquet/Arrow; streaming.
- Gobernanza: linaje, licencias, etiquetado de calidad/riesgo.

### Recursos núcleo
- Reis & Housley — *Fundamentals of Data Engineering*.
- Kleppmann — *Designing Data-Intensive Applications*.

---

## 6. Fase 4: sistemas de cómputo y entrenamiento (GPU y distribuido)

**Objetivo:** entrenar/afinar modelos en GPU con control de memoria/tiempo.

### Temas clave
- Concurrencia y profiling.
- GPU: batch size, mixed precision, profiling.
- Distribuido: DDP (práctico), FSDP/ZeRO (conceptual).
- Checkpointing y reanudación.

### Recursos núcleo
- Gorelick & Ozsvald — *High Performance Python* (profiling).
- Documentación de PyTorch: AMP, profiling, distributed.

---

## 7. Fase 5: mlops general y gestión de experimentos

**Objetivo:** laboratorio reproducible de experimentos.

### Temas clave
- Tracking: config, métricas, artefactos, commit hash.
- Versionado: datos y modelos.
- Pipelines: entrenamiento → evaluación → reporte.
- CI/CD: tests de datos y regresión de métricas.

### Recursos núcleo
- Chip Huyen — *Designing Machine Learning Systems*.
- Lakshmanan et al. — *Machine Learning Design Patterns*.
- Gift & Deza — *Practical MLOps*.

---

## 8. Fase 6: llmops, serving, observabilidad y seguridad (brecha C incluida)

**Objetivo:** operar un sistema basado en llms y evidenciar prácticas de responsible AI.

### Temas clave
- Serving: REST/streaming, batching, límites, cachés.
- Observabilidad: logs estructurados, métricas técnicas y de calidad.
- Evaluación continua: suites de prompts, drift, regresiones.
- Seguridad: filtros, políticas, manejo de incidentes, rollback.
- Responsible AI:
  - Documentación de riesgos, mitigaciones, límites.
  - Sesgo, privacidad, licencias y usos indebidos.

### Recursos recomendados
- Chen et al. — *Reliable Machine Learning*.
- Guías de llmops de herramientas actuales (para prácticas).
- NIST — *AI RMF 1.0* como marco práctico de gestión de riesgos.

---

## 9. Integración con las rutas 1 y 2

- Con ruta 1: convierte modelos en sistemas reproducibles y desplegables.
- Con ruta 2: estadística e inferencia alimentan evaluación; optimización e información alimentan métricas y criterios de aceptación.
