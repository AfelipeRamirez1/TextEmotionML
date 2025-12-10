# 🤖 TextEmotionML: Clasificación Automática de Emociones en Texto

## 🌟 Resumen del Proyecto

**TextEmotionML** es un proyecto de **Clasificación Automática de Emociones** en lenguaje natural (NLP). El objetivo principal es construir un sistema capaz de identificar la emoción predominante en frases o mensajes escritos, utilizando un enfoque comparativo de Machine Learning.

Este trabajo se centra en el análisis riguroso de las decisiones de preprocesamiento y modelado, clasificando textos en seis categorías emocionales fundamentales: **sadness, joy, love, anger, fear,** y **surprise**.

---

## 🛠️ Enfoque y Tareas Abordadas

El proyecto combina técnicas avanzadas de **Procesamiento de Lenguaje Natural (NLP)** y **Aprendizaje Automático (ML)**, abordando las siguientes tareas clave:

* **Limpieza y Preprocesamiento:** Normalización del texto, tokenización y eliminación de *stopwords*.
* **Representación Vectorial:** Transformación del texto a formato numérico mediante **TF-IDF** (Term Frequency-Inverse Document Frequency).
* **Manejo de Desbalanceo:** Aplicación de **Random Over-Sampling (ROS)** para mitigar el desequilibrio natural de las clases minoritarias en el *dataset*.
* **Entrenamiento y Comparación de Modelos:** Evaluación exhaustiva de dos arquitecturas fundamentales:
    * **Naive Bayes (Probabilístico)**
    * **Perceptrón Multicapa (MLPClassifier)**, cumpliendo con el requisito de introducción a Redes Neuronales.

### 📊 Métricas y Análisis

La evaluación se basa en métricas esenciales (**Accuracy, Precision, Recall, F1-score**), complementadas con **Matrices de Confusión** y **Gráficos comparativos** para un análisis profundo del rendimiento por clase.

---

## 🎯 Objetivo de la Evaluación

El propósito central del proyecto es evaluar distintas estrategias de Machine Learning para la clasificación emocional y analizar empíricamente:

1.  **Impacto del Desbalanceo:** Cómo afecta la distribución desigual de clases a los modelos base.
2.  **Efecto del Oversampling (ROS):** La contribución real de la técnica de balanceo a la generalización del modelo.
3.  **Comparación de Arquitecturas:** Las diferencias de rendimiento, robustez y capacidad de generalización entre modelos **probabilísticos (Naive Bayes)** y **neuronales (MLP)**.

### 📂 Contenido del Notebook

Este cuaderno incluye el flujo completo para la generación y evaluación de **cuatro modelos clave**:

| Estrategia de Modelado | Modelo | Datos de Entrenamiento |
| :--- | :--- | :--- |
| **Línea Base** | Naive Bayes | Sin ROS (Original) |
| **Estrategia A** | Naive Bayes | Con ROS (Balanceado) |
| **Línea Neuronal** | **MLPClassifier** | Sin ROS (Original) |
| **Estrategia B** | **MLPClassifier** | Con ROS (Balanceado) |

---

## 🚨 Requisito Indispensable: Acceso al Dataset de Kaggle

El proyecto utiliza el **Emotion Dataset** de Kaggle. Para la descarga automática en Google Colab, es **obligatorio** contar con el archivo de configuración de la API de Kaggle.

📌 **Dataset:** [Emotion Dataset – Kaggle](https://www.kaggle.com/datasets/parulpandey/emotion-dataset)

### Pasos para la Descarga Automática

1.  Obtener el archivo `kaggle.json` (API Token) desde tu cuenta de Kaggle (`Account` → `API` → `Create New API Token`).
2.  Subir el archivo `kaggle.json` a la ruta en Colab: `~/.kaggle/`
3.  Asignar permisos de lectura al archivo: `!chmod 600 ~/.kaggle/kaggle.json`

⚠️ **Advertencia:** Sin este archivo, la primera celda de descarga fallará y el proyecto no podrá ejecutarse.