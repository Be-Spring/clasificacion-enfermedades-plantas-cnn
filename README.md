# Clasificación de enfermedades en plantas mediante CNN

## Descripción
Proyecto de Deep Learning desarrollado en Google Colab para clasificar enfermedades en hojas de plantas utilizando el dataset PlantVillage.

Se implementaron y compararon dos arquitecturas de redes neuronales convolucionales (CNN) para identificar 15 categorías de hojas sanas y enfermas.

## Dataset
Se trabajó con una muestra de 4.200 imágenes, distribuidas en:
- Entrenamiento: 3.000 imágenes.
- Validación: 600 imágenes.
- Prueba: 600 imágenes.

Las imágenes fueron redimensionadas a 64 × 64 píxeles y normalizadas.

## Modelos implementados
- **CNN base:** arquitectura inicial con dos capas convolucionales.
- **CNN mejorada:** arquitectura con tres capas convolucionales, Batch Normalization, Dropout, regularización L2 y Global Average Pooling.

## Resultados

| Métrica | CNN base | CNN mejorada |
|---|---:|---:|
| Accuracy | 69,50 % | 79,67 % |
| Precision macro | 63,42 % | 83,96 % |
| Recall macro | 61,71 % | 72,95 % |
| F1-score macro | 60,52 % | 75,24 % |

La segunda arquitectura obtuvo mejores resultados generales en el conjunto de prueba, aunque todavía presentó dificultades para reconocer algunas categorías.

## Tecnologías
Python, TensorFlow, Keras, NumPy, Pandas, Matplotlib, Seaborn y Scikit-learn.

## Entorno de ejecución
Google Colab.

Para reproducir el proyecto se requiere descargar el dataset PlantVillage y configurar las rutas de acceso a los archivos utilizados en el notebook.

## Autoras
- Betsabé Spring
- María
