# 🔉 Generación de Señales con Series de Fourier

Este proyecto demuestra cómo utilizar **series de Fourier** para generar señales periódicas a partir de múltiples armónicos. Se implementa en Python y se visualizan tres señales diferentes con distintas cantidades de términos de Fourier.

---

## 📌 ¿Qué hace este proyecto?

- Implementa una función que suma armónicos senoidales para construir una señal.
- Visualiza cómo afecta el número de términos (armónicos) a la forma de la señal.
- Grafica tres señales con 10, 20 y 30 términos respectivamente.

---

## 📈 Resultado esperado

El programa genera una figura con tres gráficos apilados mostrando señales generadas por series de Fourier con diferente cantidad de armónicos:

- Señal 1: 10 términos
- Señal 2: 20 términos
- Señal 3: 30 términos

Esto permite observar cómo la señal se vuelve más compleja y rica a medida que se agregan más términos.

---

## ⚙️ Requisitos

Este script utiliza solo bibliotecas estándar de análisis y visualización de datos en Python:

- `numpy`
- `matplotlib`

Puedes instalarlas con:

```bash
pip install numpy matplotlib
