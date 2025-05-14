# 📡 Visualización del Espectro en Microondas

Este proyecto permite visualizar datos en formato de espectro en microondas obtenidos mediante una antena de medición. A partir de un archivo `.txt` con lecturas de **hora**, **azimut**, **elevación** e **intensidad de señal**, se genera un gráfico de dispersión con colores que representan la intensidad.

---

## 🌐 ¿Qué hace este proyecto?

- Lee datos de azimut, elevación y potencia desde un archivo `.txt`
- Usa la potencia como intensidad para asignar colores gradientes
- Genera un **scatter plot** que representa la distribución angular y de potencia de la señal
- Visualiza cómo cambia la intensidad en función de la orientación de la antena

---

## 📄 Formato del archivo de entrada

El archivo debe tener el siguiente formato (sin encabezado o con una línea inicial que se ignora):

hora azimuth elevación potencia
08:30:00 120.0 45.0 -35.6
08:30:10 125.0 43.5 -36.0
...

Ejemplo de nombre de archivo: `NE-F1_28-jun-2023_091642.txt`

---

## 🎯 Resultado esperado

Un gráfico como este:

![image](https://github.com/user-attachments/assets/7b8c1d43-2c27-4231-bdca-e148ca0eb8a0)


> *Colores desde morado hasta rojo representan potencias desde más bajas hasta más altas.*

---

## ⚙️ Requisitos

Este proyecto está hecho en Python 3 e incluye dependencias comunes:

- `matplotlib`
- `numpy`

Instalación:

```bash
pip install matplotlib numpy
```
🚀 Cómo ejecutar
Asegúrate de tener un archivo .txt con el formato adecuado.

Coloca el archivo en el mismo directorio que el script.

Modifica el nombre del archivo en el código si es necesario:

```bash
with open("NE-F1_28-jun-2023_091642.txt", "r") as file:
```
Ejecuta el script:
```bash
python visualizar_espectro.py
```
Se mostrará un gráfico con azimut vs elevación, coloreado por intensidad.

---

##🎨 Colormap
El código usa un gradiente de colores desde morado (baja intensidad) hasta rojo (alta intensidad):

```
colormap = mcolors.LinearSegmentedColormap.from_list("", 
    ["purple", "blue", "turquoise", "green", "yellow", "red"])
```
---

##🛠️ Posibles mejoras
Incluir la hora como etiqueta o animación para mostrar el cambio temporal.

Exportar el gráfico como imagen con plt.savefig().

Ajustar dinámicamente el tamaño del punto basado en la intensidad.

---

##👩‍🚀 Autora
Liliana Becerril Tapia
Desarrollado como parte del programa VIAI en INAOE – Verano 2023
