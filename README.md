# Fine-Tuning de CLIP-RN50 para Recuperación Imagen-Texto

Este proyecto implementa el **fine-tuning del modelo CLIP-RN50 de OpenAI** utilizando el conjunto de datos **Flickr8k** para mejorar la representación conjunta de imágenes y texto mediante aprendizaje contrastivo.

El modelo entrenado permite realizar tareas de **Image-to-Text Retrieval** y **Text-to-Image Retrieval**, aprendiendo un espacio de embeddings compartido donde imágenes y descripciones semánticamente relacionadas quedan cercanas.

---

## Objetivos

- Implementar un modelo multimodal basado en CLIP.
- Ajustar (Fine-Tuning) el modelo preentrenado sobre Flickr8k.
- Evaluar el desempeño mediante métricas de recuperación.
- Generar embeddings conjuntos para imágenes y texto.

---

## Dataset

Se emplea el dataset **Flickr8k**, el cual contiene:

- 8,000 imágenes
- 5 descripciones por imagen
- Aproximadamente 40,000 captions

División utilizada:

- Entrenamiento
- Validación
- Prueba

Cada imagen posee cinco descripciones independientes, lo que permite entrenar modelos de alineación imagen-texto.

---

## Arquitectura

El proyecto utiliza:

- **Modelo:** CLIP RN50
- **Pesos iniciales:** OpenAI
- **Framework:** PyTorch
- **Tokenizer:** OpenCLIP

El entrenamiento consiste en ajustar únicamente los parámetros del modelo para especializarlo en Flickr8k mediante una pérdida contrastiva.

---

## Tecnologías utilizadas

- Python
- PyTorch
- OpenCLIP
- Hugging Face Datasets
- Transformers
- NumPy
- Pandas
- Matplotlib
- Scikit-Learn
- Pillow

---

## Instalación

Clonar el repositorio:

```bash
git clone https://github.com/usuario/nombre-del-repositorio.git

cd nombre-del-repositorio
```

Instalar dependencias:

```bash
pip install -r requirements.txt
```

---

## Estructura del proyecto

```
.
├── BIMODAL-IMAGE-TEXT.ipynb
├── requirements.txt
└── README.md
```

---

## Flujo del proyecto

1. Instalación de dependencias.
2. Configuración del entorno y semillas aleatorias.
3. Descarga automática del dataset Flickr8k.
4. Preprocesamiento de imágenes y captions.
5. Carga del modelo CLIP-RN50 preentrenado.
6. Fine-Tuning del modelo.
7. Validación durante el entrenamiento.
8. Evaluación mediante recuperación semántica.
9. Obtención de embeddings para imágenes y texto.

---

## Métricas de evaluación

El notebook evalúa el modelo utilizando métricas estándar de recuperación:

- Recall@1
- Recall@5
- Recall@10
- Median Rank (MedR)
- Rsum

Estas métricas permiten medir qué tan bien el modelo recupera imágenes a partir de texto y viceversa.

---

## Resultados

Al finalizar el entrenamiento, el modelo puede:

- Buscar imágenes a partir de una descripción.
- Buscar descripciones a partir de una imagen.
- Generar embeddings multimodales alineados.
- Mejorar el desempeño sobre el modelo preentrenado en el dominio de Flickr8k.

---

## Ejecución

Abrir el notebook:

```bash
jupyter notebook BIMODAL-IMAGE-TEXT.ipynb
```

También puede ejecutarse directamente desde **Google Colab**.

---

## Dependencias

Las principales bibliotecas utilizadas son:

- torch
- torchvision
- open_clip_torch
- transformers
- datasets
- huggingface_hub
- numpy
- pandas
- matplotlib
- Pillow
- tqdm
- scikit-learn

---

## Autores

- Julian Hilton Lino Pariona
- Diego Alonso Reátegui Gonzales
- Jim Navarrete Cáceres
- Flavio Roberto Pujay Angeles

---

## Licencia

Este proyecto fue desarrollado con fines académicos y de investigación.
