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

El proyecto fue desarrollado en **Google Colab**, utilizando Python y aceleración GPU T4.

### Instrucciones de ejecución

1. Descargar el notebook `Clasificacion_Enfermedades_Plantas_EP2.ipynb` desde este repositorio y abrirlo en Google Colab.
2. Acceder a la **[carpeta de archivos del proyecto](https://drive.google.com/drive/folders/1h-jr0FMvQoXV4rhqVqV2qUPpWTdk0xFY?usp=drive_link)**, que contiene:
   - `PlantVillage.zip`: dataset de imágenes.
   - `division_datos.csv`: división de entrenamiento, validación y prueba.
   - `clases.json`: identificación de las 15 categorías.
   - `modelo_cnn_base.keras`: primer modelo entrenado.
   - `modelo_cnn_2.keras`: segundo modelo entrenado.
3. Agregar la carpeta compartida como acceso directo a **Mi unidad** de Google Drive, con el nombre `Prueba2_DeepLearning`.
4. En Google Colab, conectar Google Drive y comprobar que las rutas del notebook correspondan a la ubicación de los archivos.
5. Seleccionar **Entorno de ejecución → Cambiar tipo de entorno de ejecución → GPU T4**, si está disponible.
6. Ejecutar las celdas del notebook en orden para reproducir el proyecto. Si solo se desea revisar la comparación, pueden cargarse los modelos previamente entrenados desde Google Drive, sin repetir el entrenamiento.

**Nota:** Los modelos entrenados se encuentran disponibles en Google Drive para facilitar su carga y comparación sin necesidad de entrenarlos nuevamente.

### Consideraciones

- El notebook utiliza una muestra de 4.200 imágenes del dataset PlantVillage.
- Los archivos `division_datos.csv` y `clases.json` permiten conservar la división de los datos y el orden de las categorías.
- Los modelos `.keras` corresponden a las arquitecturas entrenadas y deben estar disponibles para ejecutar las celdas que los cargan.
- Si se desea entrenar nuevamente los modelos, se deben ejecutar las celdas correspondientes al entrenamiento.
- Los resultados pueden variar ligeramente al repetir el entrenamiento.

## Autoras
- Betsabé Spring
- María
