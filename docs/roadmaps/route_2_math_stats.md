# Ruta 2: matemática y estadística para IA y llms (versión auditada y optimizada)

## 0. Cambios clave tras la auditoría

- Se añadió una fase explícita de **Markov y MDPs** para soportar planificación/RL (brecha B).
- Se reforzó la parte de **estadística aplicada a evaluación**: bootstrap, comparaciones pareadas y comparaciones múltiples.
- Se incluyó un bloque más explícito de **inferencia bayesiana práctica** como apoyo a razonamiento bajo incertidumbre.

## 1. Propósito y criterio de diseño

Esta ruta cubre el mínimo “profesional” de matemática y estadística para:

- Entender con rigor entrenamiento y evaluación de modelos (incluyendo llms).
- Leer papers sin que la notación sea una barrera.
- Diseñar experimentos y comparaciones con criterio estadístico.

Libros “columna vertebral” (pocos y consistentes):
- Deisenroth et al. — *Mathematics for Machine Learning*.
- Blitzstein & Hwang — *Introduction to Probability*.
- Wasserman — *All of Statistics*.
- Boyd & Vandenberghe — *Convex Optimization* (lectura selectiva).
- Cover & Thomas — *Elements of Information Theory* (capítulos selectivos).
- Vershynin — *High-Dimensional Probability* (intro selectivo).
- Shalev-Shwartz & Ben-David — *Understanding Machine Learning* (selectivo).

---

## 2. Fase 0: cálculo y álgebra operativos (mínimo necesario)

**Objetivo:** evitar bloqueos por falta de cálculo/algebra básica.

### Temas clave
- Derivadas, regla de la cadena, optimización en 1 variable.
- Derivadas parciales y gradiente (noción operativa).
- Notación de vectores y matrices.

### Recursos recomendados
- Stewart — *Calculus: Early Transcendentals* (lectura operativa).
- Deisenroth — cálculo vectorial como puente a ML (lectura selectiva).

---

## 3. Fase 1: álgebra lineal y geometría de representaciones

**Objetivo:** dominar la matemática de embeddings, capas lineales y atención.

### Temas clave
- Espacios vectoriales, bases, proyecciones, ortogonalidad.
- Normas y productos internos.
- Autovalores/autovectores (intuición geométrica).
- SVD y PCA (herramientas de análisis).

### Recursos núcleo
- Strang — *Introduction to Linear Algebra*.
- Deisenroth — álgebra lineal + descomposiciones + PCA (lectura selectiva).

---

## 4. Fase 2: probabilidad para modelos de lenguaje y ML

**Objetivo:** comprender modelos probabilísticos, log-verosimilitud y muestreo.

### Temas clave
- Probabilidad condicional, independencia, Bayes.
- Variables aleatorias, distribuciones conjuntas, transformaciones.
- Esperanza, varianza, covarianza.
- LLN y TCL (intuición y uso).

### Recursos núcleo
- Blitzstein & Hwang — lectura selectiva orientada a fundamentos y ejercicios.

---

## 5. Fase 3: procesos estocásticos básicos y Markov (para planificación y RL)

**Objetivo:** cubrir lo mínimo de Markov para MDPs/RL y razonamiento bajo incertidumbre.

### Temas clave
- Cadenas de Markov: transición, estacionariedad (nivel conceptual).
- MDP: ecuaciones de Bellman, valores y políticas.
- POMDP: solo para ubicar el tema.

### Recursos recomendados
- Sutton & Barto — capítulos de MDP y DP (como puente práctico).
- Murphy — *Probabilistic Machine Learning: An Introduction* (lectura selectiva sobre Markov).

---

## 6. Fase 4: estadística e inferencia para evaluación de modelos

**Objetivo:** comparar modelos y experimentos con rigor, más allá de una métrica puntual.

### Temas clave
- Estimación: sesgo/varianza, MSE.
- Intervalos de confianza y tests de hipótesis.
- Bootstrap y métodos no paramétricos (muy útiles en ML).
- Diseño experimental aplicado:
  - Comparación pareada (win-rate) y tests sobre diferencias.
  - Noción práctica de comparaciones múltiples.

### Recursos núcleo
- Wasserman — *All of Statistics* (estimación e inferencia, lectura selectiva).
- Casella & Berger — *Statistical Inference* (opcional).

---

## 7. Fase 5: optimización y estabilidad numérica (para entrenamiento de redes)

**Objetivo:** entender “por qué funciona o falla” el entrenamiento.

### Temas clave
- Gradiente, Hessiana, puntos críticos (intuición).
- Convexidad vs no convexidad (lo mínimo).
- Descenso de gradiente y variantes (conexión con Adam).
- Lagrange/KKT (conceptual).
- Estabilidad numérica: log-sum-exp, underflow/overflow, exploding/vanishing.

### Recursos núcleo
- Deisenroth — optimización continua (lectura selectiva).
- Boyd & Vandenberghe — convexidad y formulación (lectura selectiva).

---

## 8. Fase 6: teoría de la información y divergencias (entropía, KL, perplexity)

**Objetivo:** entender la pérdida de llms con claridad.

### Temas clave
- Entropía, entropía condicional.
- KL y relación con entropía cruzada.
- Información mutua (intuición).
- Perplexity y limitaciones.

### Recursos núcleo
- Cover & Thomas — capítulos del núcleo (lectura selectiva).

---

## 9. Fase 7: alta dimensión y generalización (lectura selectiva)

**Objetivo:** intuiciones para scaling laws, sobreparametrización y generalización en DL.

### Temas clave
- Concentración (conceptual).
- Vectores y matrices aleatorias (intuición).
- Fundamentos de teoría de aprendizaje (VC, generalización) a nivel conceptual.

### Recursos núcleo
- Vershynin — introducción selectiva.
- Shalev-Shwartz & Ben-David — fundamentos selectivos.

---

## 10. Integración con las rutas 1 y 3

- Con ruta 1: fases 1–2 alimentan transformers/embeddings; fase 3 alimenta RL/planning; fases 6–7 alimentan pérdidas, evaluación y scaling.
- Con ruta 3: fase 4 sustenta evaluación experimental; fase 5 sustenta tuning/diagnóstico; fase 6 sustenta métricas y criterios de aceptación.
