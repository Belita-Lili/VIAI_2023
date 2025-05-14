# 🔭 Detección de Estrellas Azules en Imágenes Astronómicas

Este script detecta y cuenta estrellas azules en una imagen astronómica (`stars.png`) usando técnicas de visión por computadora con OpenCV. También calcula el flujo (área) total de las estrellas detectadas y visualiza el resultado con rectángulos y círculos.

---

## 🧠 ¿Qué hace este proyecto?

- Convierte una imagen BGR a HSV para una mejor segmentación por color.
- Crea una **máscara binaria** para detectar estrellas dentro de un rango de azul específico.
- Detecta contornos, filtra por área mínima, y calcula:
  - 🔢 Cantidad de estrellas
  - 📐 Flujo total (suma de áreas)
  - 📊 Porcentaje de flujo respecto a la imagen
- Visualiza:
  - La máscara en escala de grises
  - La imagen original con rectángulos y círculos sobre las estrellas detectadas

---

## 📸 Ejemplo visual

| Máscara generada | Imagen original con detecciones |
|------------------|----------------------------------|
| ![image](https://github.com/user-attachments/assets/5144dd68-990c-43e6-b47b-1bc4509286b9)|(![image](https://github.com/user-attachments/assets/5c4d4486-40a0-44ab-adce-e0dac93049df)



---

## ⚙️ Requisitos

Este script requiere Python 3 y las siguientes librerías:

- `opencv-python`
- `numpy`
- `matplotlib`

Instalación rápida:

```bash
pip install opencv-python numpy matplotlib
