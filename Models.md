# Modelos entrenados

Este directorio contiene los modelos resultantes del entrenamiento realizado en el proyecto **CNN vs Transfer Learning for Image Classification**.

## 📁 Contenido

- `mi_modelo_TL.h5`  
  Modelo de clasificación basado en Transfer Learning utilizando MobileNetV2 como modelo base preentrenado en ImageNet.

- `mi_modelo_TL.keras`  
  Versión del mismo modelo guardada en el formato nativo de Keras.

📌 Nota sobre los archivos del repositorio

Debido a su gran tamaño, el modelo CNN entrenado desde cero no se incluye directamente en el repositorio.
El modelo de Transfer Learning sí se proporciona, ya que representa una solución más práctica y eficiente.

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
