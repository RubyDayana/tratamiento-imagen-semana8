# Tratamiento de imagen: diagnóstico y corrección con OpenCV

**Universidad de Cundinamarca** · **CADI:** Percepción Computacional · Experiencia IMAGEN · Semana 8
**Estudiante:** Ruby Dayana Cárdenas Gómez

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RubyDayana/tratamiento-imagen-semana8/blob/main/Semana8_Tratamiento_Imagen_RCardenas.ipynb)

## ¿De qué trata?

Cinco fotos de un mismo objeto (un gato de cerámica) tomadas en condiciones distintas: referencia, baja iluminación, desenfoque, fondo complejo y cambio de ángulo. Con Python y OpenCV se mide resolución, canales, brillo, contraste, nitidez (varianza del Laplaciano) y tamaño de archivo, se identifica la imagen problemática y se le aplica un tratamiento justificado, comparando antes y después con números e imágenes.

## Resultado

| Imagen | Brillo | Contraste | Nitidez |
|---|---|---|---|
| Referencia | 149.7 | 73.5 | 94.0 |
| Baja iluminación | 116.2 | 62.4 | 80.4 |
| **Desenfoque** | 147.2 | 71.6 | **5.5** |
| Fondo complejo | 117.2 | 58.8 | 256.6 |
| Cambio de ángulo | 151.2 | 72.8 | 258.4 |

Problema seleccionado: **desenfoque** (nitidez al 6 % de la referencia). Tratamiento: **máscara de desenfoque (unsharp mask)**, fuerza 1.5 y radio 5. La nitidez pasó de 5.5 a 34.5 sin alterar brillo ni contraste, pero quedó lejos de la referencia y con halos en los bordes: el realce recupera parte del detalle, no el que la cámara no capturó.

## Archivos

| Archivo | Descripción |
|---|---|
| `Semana8_Tratamiento_Imagen_RCardenas.ipynb` | Cuaderno con todo el análisis y sus salidas |
| `referencia.jpg`, `baja_luz.jpg`, `desenfoque.jpg`, `fondo_complejo.jpg`, `angulo.jpg` | Las cinco capturas |
| `Informe_Tratamiento_Imagen_Semana8_RCardenas.pdf` | Informe de resultados |
| `README.md` | Este archivo |
