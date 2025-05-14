# 🌌 Proyectos de Análisis y Visualización Científica en Python

Este repositorio contiene una colección de proyectos realizados durante el programa de verano VIAI en el INAOE (2023), enfocados en el procesamiento de datos astronómicos, análisis de señales y generación de visualizaciones. Todos los proyectos están escritos en Python y utilizan herramientas estándar como `numpy`, `matplotlib` y `opencv`.

---

## 📁 Estructura del Repositorio
```bash
astro-science-projects/
│
├── fourier-series-signals/
│ ├── fourier-series-signals.py
│ ├── fourier-series-signals.ipynb
│ └── README.md
│
├── star-localization-from-image/
│ ├── stars.png
│ ├── star-localization-from-image.py
│ ├── star-localization-from-image.ipynb
│ └── README.md
│
├── telescope-site-mapper/
│ ├── telescope-site-mapper.py
│ ├── telescope-site-mapper.ipynb
│ ├── NE-F1_28-jun-2023_091642.txt
│ └── README.md
│
└── README.md (este archivo)
```

---

## 📌 Descripción de Proyectos

### 1. [`fourier-series-signals`](fourier-series-signals/)

Este proyecto genera señales periódicas utilizando **series de Fourier** y grafica el resultado con diferentes cantidades de armónicos. Es ideal para comprender cómo se construyen las señales complejas a partir de componentes sinusoidales.

📊 Tecnologías: `numpy`, `matplotlib`

---

### 2. [`star-localization-from-image`](star-localization-from-image/)

Un script de visión por computadora que detecta y cuenta objetos brillantes (como estrellas) en una imagen astronómica (`stars.png`) utilizando el espacio de color HSV y detección de contornos con OpenCV.

📊 Tecnologías: `opencv`, `numpy`, `matplotlib`

---

### 3. [`telescope-site-mapper`](telescope-site-mapper/)

Este script analiza datos provenientes de una antena en ondas de radio para representar la potencia recibida en función del azimut y la elevación. Se utiliza una escala de colores para visualizar los patrones de intensidad espacial.

📊 Tecnologías: `numpy`, `matplotlib`, `colors`

---

## 🚀 Cómo usar este repositorio

1. Clona el repositorio:

```bash
git clone https://github.com/tu-usuario/astro-science-projects.git
cd astro-science-projects
```
2. Instala los requisitos si los deseas agrupar:
```bash
pip install -r requirements.txt
```
3. Dirígete a cada carpeta de proyecto y ejecuta el script correspondiente.

## 🧪 Requisitos Generales
Python 3.x

numpy

matplotlib

opencv-python (solo para el proyecto de detección de estrellas)

Puedes instalarlos con:

```bash
pip install numpy matplotlib opencv-python
```
