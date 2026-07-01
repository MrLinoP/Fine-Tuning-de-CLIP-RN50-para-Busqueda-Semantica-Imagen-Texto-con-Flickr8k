# Fine-Tuning de CLIP-RN50 para Búsqueda Semántica Imagen-Texto

Este proyecto implementa el **fine-tuning del modelo CLIP-RN50 (OpenAI)** utilizando el dataset **Flickr8k** para mejorar la alineación entre imágenes y descripciones en lenguaje natural mediante aprendizaje contrastivo.

El objetivo es entrenar un modelo capaz de representar imágenes y textos en un mismo espacio vectorial, permitiendo realizar búsquedas semánticas imagen-texto y texto-imagen con alta precisión.

## Características

- Fine-tuning de CLIP-RN50 preentrenado.
- Uso del dataset Flickr8k.
- Entrenamiento mediante pérdida contrastiva.
- Validación y evaluación del modelo.
- Configuración reproducible mediante semillas aleatorias.
- Implementación en Python utilizando PyTorch y OpenCLIP.

## Dataset

Se utiliza **Flickr8k**, un conjunto de datos compuesto por:

- 8,000 imágenes
- 5 descripciones por imagen
- División estándar:
  - 6,000 imágenes para entrenamiento
  - 1,000 imágenes para validación
  - 1,000 imágenes para prueba

El dataset es ampliamente utilizado para tareas de recuperación imagen-texto y generación de descripciones.

## Tecnologías utilizadas

- Python
- PyTorch
- OpenCLIP
- Hugging Face Datasets
- Transformers
- Pillow
- NumPy
- Pandas
- Matplotlib

## Estructura del proyecto

```
.
├── BIMODAL-IMAGE-TEXT.ipynb
├── README.md
└── requirements.txt (opcional)
```

## Flujo del proyecto

1. Configuración del entorno.
2. Definición de hiperparámetros.
3. Descarga y preparación del dataset Flickr8k.
4. Preprocesamiento de imágenes y texto.
5. Fine-tuning del modelo CLIP-RN50.
6. Validación del entrenamiento.
7. Evaluación del modelo.
8. Obtención de embeddings para recuperación semántica.

## Modelo utilizado

- Arquitectura: **CLIP RN50**
- Pesos preentrenados: **OpenAI**

El modelo aprende representaciones conjuntas de imágenes y texto para maximizar la similitud entre pares correctos y minimizar la de pares incorrectos.

## Resultados esperados

Al finalizar el entrenamiento, el modelo es capaz de:

- Recuperar imágenes a partir de una descripción.
- Recuperar descripciones a partir de una imagen.
- Generar embeddings multimodales de alta calidad.
- Mejorar el rendimiento respecto al modelo base en el dominio de Flickr8k.

## Cómo ejecutar

1. Clonar el repositorio.

```bash
git clone https://github.com/usuario/nombre-del-repositorio.git
cd nombre-del-repositorio
```

2. Instalar dependencias.

```bash
pip install -r requirements.txt
```

3. Abrir el notebook.

```bash
jupyter notebook BIMODAL-IMAGE-TEXT.ipynb
```

o ejecutarlo desde Google Colab.

## Autores

Julian Hilton Lino Pariona
Diego Alonso Reátegui Gonzales
Jim Navarrete Cáceres
Flavio Roberto Pujay Angeles

## Licencia

Este proyecto tiene fines académicos.
