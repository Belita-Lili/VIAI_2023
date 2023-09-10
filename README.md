# VIAI_2023
Este programa está escrito en Python utilizando la biblioteca OpenCV (cv2) y NumPy para el procesamiento de imágenes y la biblioteca Matplotlib para la visualización. Su función es procesar una imagen llamada 'stars.png' que contiene objetos con tonos de azul y calcular ciertas métricas, como el número de objetos azules, el área total de los objetos y el porcentaje de área ocupada por los objetos azules en la imagen.

Aquí hay una descripción detallada de lo que hace cada parte del programa:

## 1. Importación de bibliotecas:

Se importan las bibliotecas necesarias: cv2 para OpenCV, numpy como np y matplotlib.pyplot para la manipulación y visualización de imágenes.
## 2. Lectura de la imagen original:

original = cv2.imread('stars.png')

La imagen 'stars.png' se carga en la variable original utilizando la función cv2.imread.

## 3. Obtención de las dimensiones de la imagen:

alto, ancho, canales = original.shape

Se obtienen las dimensiones de la imagen, incluyendo su altura (alto), ancho (ancho) y el número de canales de color (canales).

## 4. Definición de rangos de color azul:

azulClaro = np.array([270, 10, 20], dtype=np.uint8)
azulOscuro = np.array([310, 255, 255], dtype=np.uint8)
Se definen dos valores de color en formato HSV que representan el rango de tonos de azul que se buscarán en la imagen.
## 5. Conversión a espacio de color HSV:

frameHSV = cv2.cvtColor(original, cv2.COLOR_BGR2HSV)
La imagen original se convierte del espacio de color BGR (RGB en OpenCV) al espacio de color HSV para facilitar la detección de tonos de azul.

## 6. Creación de una máscara:

mask = cv2.inRange(frameHSV, azulClaro, azulOscuro)
Se crea una máscara utilizando cv2.inRange que identifica los píxeles en el rango de colores azules especificados y los asigna a la máscara.

## 7. Detección de contornos:

contornos, _ = cv2.findContours(mask, cv2.RETR_EXTERNAL, cv2.CHAIN_APPROX_SIMPLE)
Se encuentran los contornos en la máscara. Los contornos externos se seleccionan con cv2.RETR_EXTERNAL, y se utiliza cv2.CHAIN_APPROX_SIMPLE para aproximar los contornos con una representación mínima de puntos.

## 8. Análisis de contornos:

El programa itera a través de los contornos encontrados y realiza las siguientes acciones:
Calcula el área de cada contorno con cv2.contourArea.
Dibuja un rectángulo alrededor de los contornos con cv2.rectangle.
Dibuja un círculo mínimo que rodea cada contorno con cv2.minEnclosingCircle.

## 9. Cálculo de métricas:

Se calcula el número total de estrellas encontradas (counter), el flujo total (suma de las áreas de los contornos) y el porcentaje de flujo en relación con el número total de píxeles de la imagen.

## 10. Visualización de la máscara y la imagen original:

Se utilizan Matplotlib para mostrar la máscara y la imagen original.

## 11. Espera de entrada del usuario:

cv2.waitKey(0)
El programa espera hasta que el usuario presione una tecla antes de cerrar las ventanas.

## 12. Limpieza y cierre de ventanas:

cv2.destroyAllWindows()
Se cierran todas las ventanas abiertas por OpenCV.
En resumen, este programa procesa una imagen en busca de objetos con tonos de azul, calcula diversas métricas relacionadas con esos objetos y muestra la máscara resultante y la imagen original con los contornos detectados dibujados en ellas.
