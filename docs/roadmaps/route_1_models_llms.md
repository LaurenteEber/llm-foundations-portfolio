# Ruta 1: modelos, deep learning y llms

## 0. Cambios clave tras la auditoría

- Se añadió una fase explícita de **búsqueda/planificación y aprendizaje por refuerzo** (brecha B) para cubrir pilares de IA más allá de llms y conectar con RLHF.
- Se reforzó el bloque de **evaluación** (más allá de una métrica) y el bloque de **eficiencia** (coste y serving), que suelen ser puntos débiles en portafolios.
- Se incluyó un módulo opcional de **generativos más allá de texto** (difusión/multimodal) para amplitud académica.

## 1. Propósito y criterio de diseño

Esta ruta prepara dos cosas a la vez:

- **Base amplia de IA aplicada** (ML, DL, búsqueda/planificación, RL, NLP).
- **Especialización moderna en llms** (transformers, ajuste fino, evaluación, alineamiento y sistemas con recuperación).

La optimización prioriza:
- Cobertura de pilares que suelen aparecer en maestrías en IA (ML, DL, RL, planificación/razonamiento bajo incertidumbre, NLP).
- Material “columna vertebral” por fase (pocos recursos, bien elegidos).
- Enfoque práctico: cada fase debe producir código, experimentos y un informe técnico (vía plan integral y repos).

> Nota de integración: la formalización matemática vive en la ruta 2; la ingeniería y operacionalización viven en la ruta 3.

## 2. Mapa de fases

- **Fase 0:** fundamentos prácticos de ML moderno (supervisado + evaluación).
- **Fase 1:** deep learning general (entrenamiento estable, regularización, diagnóstico).
- **Fase 2:** búsqueda, planificación y aprendizaje por refuerzo (fundamentos para IA “no-llm” y para entender RLHF).
- **Fase 3:** NLP moderno pre-transformer (representaciones, embeddings, LMs clásicos).
- **Fase 4:** transformers y modelos de lenguaje autorregresivos (comprensión de arquitectura).
- **Fase 5:** llms prácticos (preentrenamiento, SFT, PEFT, evaluación, eficiencia).
- **Fase 6:** alineamiento, seguridad y sistemas avanzados (RLHF/DPO, RAG, agentes, evaluación robusta).

---

## 3. Fase 0: fundamentos prácticos de aprendizaje automático moderno

**Objetivo:** dominar el ciclo end-to-end de ML supervisado: datos → entrenamiento → validación → métricas → reporte.

### Temas clave
- Regresión y clasificación; métricas y selección de modelo.
- Validación (train/valid/test, CV, leakage).
- Pipelines, preprocesamiento, baselines y “error analysis”.
- Modelos base: regresión/logística, árboles, random forest, gradient boosting.
- Calibración (si clasificación) y noción básica de incertidumbre predictiva.

### Recursos núcleo (elige 1)
- Aurélien Géron — *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow* (3.ª ed.).  
  Lectura sugerida por temas: workflow y validación; regresión/clasificación; árboles/ensembles; pipelines y tuning.

### Complementos recomendados
- Documentación de scikit-learn: pipelines, CV, métricas, calibration.

---

## 4. Fase 1: deep learning general con foco en entrenamiento estable

**Objetivo:** construir intuición práctica de redes neuronales y dominar “diagnóstico de entrenamiento”.

### Temas clave
- MLP, backprop y optimización (SGD, momentum, Adam).
- Regularización: weight decay, dropout, batch norm.
- Inicialización, normalización, schedulers, early stopping.
- Diagnóstico: under/overfitting, curvas, ablations, control de semillas.
- CNN y RNN solo como contexto (por qué transformers dominan).

### Recursos núcleo (elige 1 “principal” + 1 de apoyo)
- Aston Zhang et al. — *Dive into Deep Learning* (D2L).  
  Enfoque: implementaciones didácticas + entrenamiento.
- Ian Goodfellow, Yoshua Bengio, Aaron Courville — *Deep Learning*.  
  Lectura selectiva: redes feed-forward, entrenamiento y regularización.

### Complementos recomendados
- Simon J. D. Prince — *Understanding Deep Learning* (si prefieres un texto moderno y unificado).

---

## 5. Fase 2: búsqueda, planificación y aprendizaje por refuerzo (fundamentos)

**Objetivo:** cubrir pilares clásicos de IA (planning/search/reasoning y RL) y conectar con RLHF.

### Temas clave (búsqueda y planificación)
- Formulación de problemas: estados, acciones, costos, objetivos.
- Búsqueda no informada e informada: BFS/DFS/UCS/A*, heurísticas.
- Planificación básica (visión general) y grafos.
- Razonamiento bajo incertidumbre (visión conceptual): Bayes, MDP/POMDP.

### Temas clave (aprendizaje por refuerzo)
- Multi-armed bandits (exploración vs explotación).
- MDP: value iteration, policy iteration.
- TD learning, Q-learning, SARSA.
- Policy gradients (nivel conceptual) y conexión con RLHF.

### Recursos núcleo
- Stuart Russell, Peter Norvig — *Artificial Intelligence: A Modern Approach* (4.ª ed.).  
  Lectura sugerida por temas: search, planificación, incertidumbre, MDPs.
- Richard S. Sutton, Andrew G. Barto — *Reinforcement Learning: An Introduction* (2.ª ed.).  
  Lectura sugerida por temas: bandits, MDP, DP, TD, Q-learning.

### Complementos recomendados
- David Silver (UCL): lecturas de RL (para consolidar intuición).
- OpenAI Spinning Up (guía práctica introductoria, opcional).

---

## 6. Fase 3: NLP moderno y representación del lenguaje (pre-transformer)

**Objetivo:** entender el camino hacia transformers: representaciones, embeddings y LMs clásicos.

### Temas clave
- Bag-of-words y tf-idf (como baseline).
- Modelos de lenguaje n-gram y suavizado (contexto histórico).
- Semántica distribuida: word2vec, GloVe.
- Modelos neuronales pre-transformer (RNN/LSTM/GRU) a nivel conceptual.
- Limitaciones: paralelismo, dependencia larga, estabilidad.

### Recursos núcleo
- Jurafsky & Martin — *Speech and Language Processing* (3.ª ed., borrador).  
  Lectura por temas: n-grams, embeddings, neural language models.
- Yoav Goldberg — *Neural Network Methods for Natural Language Processing* (como puente).

---

## 7. Fase 4: transformers y modelos de lenguaje autorregresivos

**Objetivo:** comprender la arquitectura transformer “sin caja negra”.

### Temas clave
- Scaled dot-product attention, multi-head attention.
- Encoder/decoder vs decoder-only (GPT-style).
- Positional encodings y variantes (visión conceptual).
- Objetivos: masked LM vs causal LM.
- Complejidad y motivación de optimizaciones.

### Recursos núcleo
- Vaswani et al. — “Attention Is All You Need”.
- Lewis Tunstall, Leandro von Werra, Thomas Wolf — *Natural Language Processing with Transformers*.  
  Enfoque: anatomía + práctica con modelos preentrenados.
- D2L — capítulos de attention/transformers (refuerzo práctico).

### Complementos recomendados
- “The Annotated Transformer” (implementación comentada).
- Lecturas selectivas sobre eficiencia (por ejemplo FlashAttention), solo si necesitas optimizar.

---

## 8. Fase 5: llms prácticos (entrenamiento, ajuste fino, PEFT y evaluación)

**Objetivo:** operar llms: entrenar/afinar, evaluar con criterio y entender trade-offs de coste/calidad.

### Temas clave
- Tokenización (BPE/SentencePiece): efectos en longitud y coste.
- Preentrenamiento causal: dataset mixture y calidad de datos.
- Scaling laws: compute/data/model (intuición práctica).
- Fine-tuning (SFT) y adaptación por dominio.
- PEFT: LoRA/adapters y PEFT+cuantización (por ejemplo QLoRA).
- Eficiencia: batching, KV cache, cuantización (conceptual), distilación (conceptual).
- Evaluación:
  - Intrínseca: loss, perplexity.
  - Extrínseca: benchmarks/suites, win-rate pareado.
  - Robustez: sensibilidad a prompts/decoding.

### Recursos núcleo
- Jay Alammar, Maarten Grootendorst — *Hands-On Large Language Models*.
- *Natural Language Processing with Transformers* (Tunstall et al.).
- Documentación de Hugging Face: Transformers + PEFT + datasets/tokenizers.

### Papers esenciales (lectura selectiva)
- Scaling: Kaplan et al. y “compute-optimal” (Hoffmann/Chinchilla).
- Modelos base: GPT-3, LLaMA (para recetas de entrenamiento y trade-offs).
- PEFT: LoRA y QLoRA (para entrenamiento realista con recursos limitados).

---

## 9. Fase 6: alineamiento, seguridad y sistemas avanzados basados en llms

**Objetivo:** I+D aplicada: preferencias, seguridad, RAG, agentes y evaluación robusta.

### Temas clave
- Preferencias:
  - SFT → reward model → RLHF (visión general).
  - DPO y variantes (visión general).
- Seguridad:
  - Jailbreaks, toxicidad, alucinaciones, over-refusal.
  - Mitigación: guardrails, filtros, evaluación adversarial.
- RAG:
  - Chunking, retrieval, reranking (conceptual), grounding.
  - Evaluación: faithfulness, citation accuracy, retrieval metrics.
- Agentes/herramientas:
  - Tool calling, planificación simple, ejecución multi-paso.
  - Observabilidad y control (coordinación con ruta 3).

### Recursos núcleo
- Christiano et al. — “Deep Reinforcement Learning from Human Preferences”.
- Ouyang et al. — “Training Language Models to Follow Instructions with Human Feedback” (InstructGPT).
- Lewis et al. — “Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks”.
- *Hands-On Large Language Models* (para integración con sistemas).

---

## 10. Módulo complementario (opcional): generativos más allá de texto y multimodalidad

**Objetivo:** ampliar “IA moderna” más allá de llms, sin perder el foco principal.

### Temas sugeridos
- Autoencoders / VAEs (conceptual).
- Difusión (conceptual y práctica ligera).
- Visión con transformers (ViT) y embeddings multimodales (CLIP) a alto nivel.

### Recurso sugerido
- Kevin P. Murphy — *Probabilistic Machine Learning* (lectura selectiva).
