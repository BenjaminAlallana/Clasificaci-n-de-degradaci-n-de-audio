# Descripción del proyecto

El objetivo de este trabajo es clasificar distintos tipos de degradación acústica aplicados de forma sintética a señales de audio ambiental. Para ello, se utilizan grabaciones de audio limpio como base, a las cuales se les aplican degradaciones controladas que permiten un etiquetado automático y un conjunto de datos balanceado.

Las degradaciones consideradas son:
- Ruido blanco
- Ruido de fondo
- Clipping (saturación de amplitud)
- Compresión con pérdida simulada

Las señales de audio son transformadas en espectrogramas Mel en escala logarítmica, los cuales se utilizan como entrada para un modelo de clasificación basado en CNN.

## Conjunto de datos

Se utiliza el dataset público **ESC-50 (Environmental Sound Classification)** únicamente como fuente de señales base. Las etiquetas originales del dataset no se emplean en este experimento.

El dataset puede descargarse desde Kaggle en el siguiente enlace:
https://www.kaggle.com/datasets/mmoreaux/environmental-sound-classification-50

## Experimento

Todo el experimento se encuentra contenido en un único Jupyter Notebook:

- `audio_degradation_classification.ipynb`

El notebook incluye:
- Preprocesamiento de audio
- Generación de degradaciones
- Extracción de espectrogramas Mel
- Entrenamiento del modelo CNN
- Evaluación mediante accuracy, precision, recall, F1-score y matriz de confusión

## Resultados

El modelo propuesto obtiene un desempeño sólido, destacando una alta capacidad de clasificación para degradaciones como el ruido blanco y la compresión. Se observa cierta confusión entre clipping y ruido de fondo, atribuible a similitudes espectrales entre estas degradaciones.

## Notas

- El conjunto de datos no está incluido en este repositorio y debe descargarse de forma independiente desde Kaggle.
- Este proyecto tiene fines académicos y de investigación.
