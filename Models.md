# Modelos entrenados

Este directorio contiene los modelos resultantes del entrenamiento realizado en el proyecto **CNN vs Transfer Learning for Image Classification**.

## 📁 Contenido

- `mi_modelo_CNN.h5`  
  Modelo de red neuronal convolucional entrenado desde cero utilizando únicamente el dataset del proyecto.

  - `mi_modelo_CNN.keras`  
  Versión del mismo modelo guardada en el formato nativo de Keras.

- `mi_modelo_TL.h5`  
  Modelo de clasificación basado en Transfer Learning utilizando MobileNetV2 como modelo base preentrenado en ImageNet.

- `mi_modelo_TL.keras`  
  Versión del mismo modelo guardada en el formato nativo de Keras.

## 🧠 Descripción de los modelos

### CNN desde cero
- Arquitectura convolucional personalizada
- Entrenamiento completo desde pesos aleatorios
- Limitada por el tamaño del dataset

### Transfer Learning
- MobileNetV2 como extractor de características
- Capas del modelo base congeladas
- Cabeza del modelo optimizada para clasificación binaria
- Mejor desempeño y generalización

## 🔄 Cómo cargar un modelo

Ejemplo para cargar cualquiera de los modelos:

```python
import tensorflow as tf

model = tf.keras.models.load_model("ruta_al_modelo")
