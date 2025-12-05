
Este repositorio contiene los desafíos y proyectos completados durante el curso de Procesamiento de Lenguaje Natural (PLN). Los trabajos abarcan desde técnicas fundamentales de clasificación y vectorización, 
hasta la implementación de modelos avanzados de lenguaje y traducción con arquitecturas recurrentes (RNN/LSTM).

## 👨‍🏫 Equipo del Curso

| Rol | Nombre | Periodo |
| :--- | :--- | :--- |
| **Alumno** | Lic. Juan Manuel Calabia | 
| **Profesor** | Dr. Rodrigo Cardenas Szigety | 
| **Profesor** | Dr. Nicolás Vattuone | 
| **Profesor** | Esp. Ing. Hernán Contigiani | 


# 🌟 Resumen General de la Materia: Procesamiento de Lenguaje Natural (PLN)

Esta materia ofrece una visión integral de las técnicas y modelos utilizados para que las máquinas procesen y entiendan el lenguaje humano. El curso se divide en tres pilares fundamentales:

## 1. Fundamentos y Representación del Lenguaje

Se establecen las bases del PLN, enseñando a la computadora a "leer":
* **Vectorización:** Técnicas para convertir texto en números (ej. TF-IDF).
* **Embeddings:** Construcción de representaciones vectoriales semánticas (**Word2Vec, CBOW, Skip-Gram**) que capturan el significado de las palabras.
* **Aplicación:** Uso de estas herramientas en la construcción de **Information Retrieval Bots** (Clases 1-3).

## 2. Modelos de Secuencia Profunda (*Deep Learning*)

Se cubren las arquitecturas neuronales diseñadas para procesar secuencias de texto:
* **Redes Recurrentes (RNN/LSTM):** Estudio de modelos para manejar dependencias en el tiempo, aplicados a la predicción de la próxima palabra y el **Análisis de Sentimiento** (Clases 4-5).
* **Sequence-to-Sequence (Seq2Seq):** Arquitectura Encoder-Decoder, pilar de los **Traductores Automáticos** y los **Bots Conversacionales** (Clase 6).

## 3. PLN de Vanguardia y Producción

Se exploran los modelos más avanzados y se enseña a llevarlos al mundo real:
* **Attention y Transformers:** Introducción al mecanismo de **Attention** y el modelo **Transformer** (la base de los LLMs modernos).
* **Modelos Pre-entrenados:** Uso de modelos avanzados como **BERT** y **ELMo** mediante **Fine Tuning** (Clase 7).
* ***Deployment*** **Industrial:** Cierre práctico con el **Deployment de Servicios NLP** usando herramientas como **Flask**, **Docker** y **Tensorflow Serving (TFX)** (Clase 8).

  
# 🚀 Resumen de Proyectos

## Desafío 1: Clasificación de Textos con Naïve Bayes

### Vectorización de texto y Clasificación Naïve Bayes

* **Objetivo:** Clasificar documentos del dataset **20 newsgroups** después de convertirlos a una representación vectorial.
* **Metodología Clave:**
    * **Vectorización:** Uso de **TF-IDF** para la representación numérica de documentos.
    * **Clasificación:** Implementación y optimización de modelos **Multinomial Naïve Bayes** y **Complement Naïve Bayes**.
* **Resultado Destacado:**
    * El modelo **ComplementNB** demostró ser la **solución de mejor desempeño**, alcanzando un **F1-macro de 0.704**.

---

## Desafío 2: Custom Embeddings con Word2Vec

### Creación de Embeddings Personalizados con Gensim

* **Objetivo:** Generar representaciones vectoriales (*embeddings*) de palabras basadas en un contexto temático específico.
* **Corpus Utilizado:** Letras de canciones de **Jimi Hendrix**, para capturar el lenguaje lírico y simbólico del artista.
* **Metodología Clave:**
    * Entrenamiento de un modelo **Word2Vec** con arquitectura **Skip-Gram** sobre el corpus de letras.
    * Análisis de similitud entre palabras clave (ej. 'love', 'fire', 'power').
    * Visualización del espacio vectorial mediante **t-SNE**.
* **Conclusión:**
    * El modelo capturó la esencia semántica, revelando núcleos temáticos claros: emocional, vital y conceptual (libertad/poder). El espacio vectorial refleja una constelación de **amor, energía y conciencia**.

---

## Desafío 3: Modelo de Lenguaje a Nivel de Carácter (RNN)

### Implementación de un Modelo de Lenguaje Recurrente

* **Objetivo:** Construir un modelo de lenguaje con redes neuronales recurrentes (**RNN**) que opere a nivel de carácter para generar nuevas secuencias de texto.
* **Metodología Clave:**
    * **Tokenización por caracteres** del corpus seleccionado.
    * Implementación de la arquitectura recurrente para predecir el siguiente carácter.
    * Exploración de técnicas de decodificación para la generación de texto.
* **Estrategias de Generación Exploradas:**
    * **Greedy Search**
    * **Beam Search** (determinístico y estocástico, analizando el impacto de la temperatura en la diversidad de las salidas).

---

## Desafío 4: Traductor Secuencia a Secuencia (LSTM Seq2Seq)

### Traducción Automática Neuronal con LSTM Encoder-Decoder

* **Objetivo:** Construir un sistema de Traducción Automática Neuronal (NMT) utilizando la arquitectura fundamental **Sequence-to-Sequence (Seq2Seq)** con redes **LSTM**.
* **Metodología Clave:**
    * Uso de un dataset de traducciones de Anki.
    * Diseño del modelo **Encoder-Decoder** en una *framework* de *deep learning*.
* **Estrategias de Decodificación y Muestreo Exploradas:**
    * **Greedy Search**
    * **Sampling**
    * **Top-K Sampling**
    * **Top-P (Nucleus) Sampling**
    * **Beam Search**
* **Foco:** El trabajo se centró en la comparación de estas estrategias para mejorar tanto la calidad como la diversidad de las traducciones generadas.
