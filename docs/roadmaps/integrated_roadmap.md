# Plan integral de estudio – roadmap por trimestres

## 0. Cambios clave tras la auditoría

- Se añadió explícitamente:
  - **Brecha A:** cs fundamentals (estructuras de datos, algoritmos, complejidad) con un repo de evidencia.
  - **Brecha B:** RL y planificación/búsqueda con un micro-proyecto.
  - **Brecha C:** responsible AI (ética y gobernanza) como entregable transversal en informes.
- Se mantuvo el foco en llms, pero se mejoró la cobertura de IA “general” para que el portafolio sea convincente ante admisión y útil académicamente.

## 1. Supuestos generales del plan

- **Opción estándar:** 6 trimestres (≈ 18 meses).
- **Opción acelerada:** 4 trimestres (≈ 12 meses), compactando términos (ver sección 8).
- **Dedicación semanal de referencia:** 4 sesiones a la semana, 2 horas cada una.
- **Rutas en paralelo:**
  - Ruta 1: modelos, deep learning, RL/planning y llms.
  - Ruta 2: matemática y estadística para IA/llms.
  - Ruta 3: cs fundamentals + ingeniería y mlops/llmops.
- **Orden dentro de cada sesión (recomendado):**
  1) Ruta 2 (20–40 min).  
  2) Ruta 1 (40–60 min).  
  3) Ruta 3 (20–40 min).

## 2. Entregables transversales (portafolio)

Para cada repo de proyecto (incluyendo micro-proyectos):
- README en inglés (problema, método, resultados, cómo ejecutar).
- Informe técnico en inglés (`docs/report.md` o `report.pdf`, 3–8 páginas).
- Tests básicos (pytest) + scripts reproducibles.
- Sección “responsible AI” con:
  - contexto de uso, riesgos, mitigaciones, limitaciones, y criterios de monitoreo.

---

## 3. Plantillas de sesión, semana y mes

### 3.1 Sesión tipo (2 horas)
- Ruta 2 (30–40 min): teoría + 1–3 ejercicios.
- Ruta 1 (45–60 min): concepto + implementación/lectura.
- Ruta 3 (20–30 min): avance tangible en repo (código/tests/docs).
- Cierre (5–10 min): 3 bullets + siguiente paso.

### 3.2 Semana tipo (4 sesiones)
- Sesión 1: fundación teórica (peso ruta 2).
- Sesión 2: teoría → código (peso ruta 1 + ruta 3).
- Sesión 3: matemática aplicada (ruta 2 conectada a experimento).
- Sesión 4: proyecto semanal (peso ruta 3 + resultados + documentación).

### 3.3 Mes tipo (4 semanas)
- Semana 1: exploración y setup.
- Semana 2: profundización.
- Semana 3: proyecto parcial.
- Semana 4: consolidación (mini examen + cierre de entregables).

---

## 4. Visión global por trimestres (opción estándar 6 trimestres)

- **Trimestre 1 – base ML + cs fundamentals (brecha A) + cálculo mínimo**
- **Trimestre 2 – deep learning + álgebra lineal + arquitectura de código + RL/planning (brecha B)**
- **Trimestre 3 – nlp moderno + probabilidad/Markov + datos de texto**
- **Trimestre 4 – transformers + optimización + gpu**
- **Trimestre 5 – llms prácticos + evaluación estadística + mlops**
- **Trimestre 6 – alineamiento + rag + llmops + ética aplicada (brecha C)**

---

## 5. Trimestre 1 – base ML + cs fundamentals + cálculo mínimo

### Objetivo del trimestre
- Probar dominio del flujo ML clásico y capacidad de ingeniería básica.
- Cubrir cs fundamentals para cursos de IA (brecha A).
- Asegurar cálculo/álgebra operativos (ruta 2) para no bloquear.

### Mes 1
- Ruta 1: ML clásico (workflow, regresión y clasificación).
- Ruta 2: derivadas/regla de la cadena + notación vectorial.
- Ruta 3: setup de repos + git + tests básicos.

**Sesión 4 de cada semana (recomendada):** 30–40 min de cs fundamentals (Big-O y estructuras básicas).

### Mes 2
- Ruta 1: modelos y evaluación (ensembles, CV, métricas).
- Ruta 2: inicio álgebra lineal (vectores, matrices, proyecciones).
- Ruta 3: cs fundamentals intensivo (grafos y búsqueda).

**Entregable del mes:** cerrar `cs-fundamentals-for-ai` (BFS/DFS/Dijkstra/A* + tests + README).

### Mes 3
- Ruta 1: consolidación con un caso real (dataset económico/política pública + uno estándar).
- Ruta 2: repaso aplicado (gradiente como intuición).
- Ruta 3: refactor, tests y documentación.

**Proyecto del trimestre:** `ml-classic-portfolio`.

---

## 6. Trimestre 2 – deep learning + arquitectura + RL/planning (brecha B)

### Objetivo del trimestre
- Dominar redes neuronales y entrenamiento estable.
- Reforzar álgebra lineal (PCA/SVD como herramienta).
- Introducir RL/planning básico para cubrir pilares de IA.

### Mes 1
- Ruta 1: MLP y entrenamiento (pérdidas, regularización).
- Ruta 2: álgebra lineal (bases, ortogonalidad).
- Ruta 3: arquitectura limpia (capas, configuración YAML).

### Mes 2
- Ruta 1: regularización y diagnóstico (curvas, ablations).
- Ruta 2: SVD/PCA aplicada a activaciones/embeddings.
- Ruta 3: tests de entrenamiento corto + runner de experimentos.

### Mes 3
- Ruta 1: search/planning + bandits/MDP (fundamentos).
- Ruta 2: Bayes + Markov/MDP a nivel operativo.
- Ruta 3: micro-proyecto RL/planning con repos limpio.

**Entregables del trimestre:**
- Proyecto principal: `dl-systems-basics`.
- Micro-proyecto: `rl-and-planning-foundations`.

---

## 7. Trimestre 3 – nlp moderno + probabilidad/Markov + datos de texto

### Objetivo del trimestre
- Consolidar NLP pre-transformer (embeddings, baselines).
- Probabilidad sólida + Markov como puente a RL.
- Pipeline de datos de texto + tokenizer propio.

### Mes 1
- Ruta 1: n-grams, tf-idf, embeddings.
- Ruta 2: probabilidad básica.
- Ruta 3: arquitectura de datos y diseño de corpus.

### Mes 2
- Ruta 1: modelos neuronales básicos para NLP.
- Ruta 2: distribuciones conjuntas, TCL (intuición).
- Ruta 3: ingesta/limpieza + entrenamiento de tokenizer.

### Mes 3
- Ruta 1: tarea NLP aplicada (clasificación) con análisis de errores.
- Ruta 2: repaso + mini “cheat sheet”.
- Ruta 3: consolidación de pipeline + tests.

**Proyecto del trimestre:** `text-corpus-and-tokenizer`.

---

## 8. Trimestre 4 – transformers + optimización + gpu

### Objetivo del trimestre
- Entender transformer en profundidad y entrenar un LM pequeño.
- Conectar optimización con entrenamiento real.
- Manejar GPU y profiling.

### Mes 1
- Ruta 1: atención y anatomía transformer.
- Ruta 2: optimización (gradiente, estabilidad).
- Ruta 3: GPU basics + profiling.

### Mes 2
- Ruta 1: implementar/entrenar transformer pequeño.
- Ruta 2: convexidad como marco conceptual (selectivo).
- Ruta 3: mixed precision, batch size, checkpoints.

### Mes 3
- Ruta 1: scaling laws (lectura selectiva).
- Ruta 2: análisis de curvas desde optimización.
- Ruta 3: reporte reproducible de tiempos/memoria.

**Proyecto del trimestre:** `mini-transformer-lab`.

---

## 9. Trimestre 5 – llms prácticos + evaluación rigurosa + mlops

### Objetivo del trimestre
- Afinar un llm open-source (PEFT) y evaluarlo con rigor.
- Aplicar inferencia estadística a comparaciones.
- Implementar tracking y versionado.

### Mes 1
- Ruta 1: llms prácticos (tokens, generación, prompts).
- Ruta 2: inferencia (intervalos, tests).
- Ruta 3: experiment tracking.

### Mes 2
- Ruta 1: PEFT (LoRA/QLoRA) en un llm pequeño.
- Ruta 2: teoría de información (entropía, KL, perplexity).
- Ruta 3: versionado de modelos/datos.

### Mes 3
- Ruta 1: alineamiento a alto nivel (RLHF/DPO).
- Ruta 2: tests sobre diferencias y estabilidad.
- Ruta 3: reportes automáticos.

**Proyecto del trimestre:** `llm-experiments-lab`.

---

## 10. Trimestre 6 – alineamiento + rag + llmops + ética aplicada (brecha C)

### Objetivo del trimestre
- Construir un sistema LLM+RAG completo.
- Incorporar observabilidad, seguridad y responsible AI como entregables.
- Conectar generalización/alta dimensión (lectura selectiva) con interpretación de resultados.

### Mes 1
- Ruta 1: RLHF/DPO + RAG (papers y práctica).
- Ruta 2: alta dimensión/generalización (lectura selectiva).
- Ruta 3: llmops (gestión de prompts, evaluaciones continuas).

### Mes 2
- Ruta 1: prototipo RAG sobre dominio concreto.
- Ruta 2: interpretación de resultados con intuiciones de generalización.
- Ruta 3: API + logs + métricas.

### Mes 3
- Ruta 1: agente simple o herramientas (opcional).
- Ruta 2: síntesis final.
- Ruta 3: seguridad, rollback y “responsible AI report”.

**Proyecto final:** `llm-rag-assistant`.

---

## 11. Opción acelerada (12 meses): compactación sugerida

- Trimestre A (meses 1–3): Trimestre 1 completo.
- Trimestre B (meses 4–6): Trimestre 2 completo.
- Trimestre C (meses 7–9): combinar Trimestre 3 y 4 (prioriza transformers).
- Trimestre D (meses 10–12): combinar Trimestre 5 y 6 (prioriza sistema RAG con PEFT + evaluación).

---

## 12. Proyectos (lista final de repos)

**Micro-proyectos**
- `cs-fundamentals-for-ai` (brecha A).
- `rl-and-planning-foundations` (brecha B).

**Proyectos trimestrales**
- `ml-classic-portfolio`
- `dl-systems-basics`
- `text-corpus-and-tokenizer`
- `mini-transformer-lab`
- `llm-experiments-lab`
- `llm-rag-assistant`
