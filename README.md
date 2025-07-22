# Lectura y análisis de archivos de imágenes Metafluor

Este repositorio contiene un conjunto de notebooks y funciones en Python para la lectura, visualización y análisis de archivos de imágenes provenientes del software **Metafluor**, utilizado en microscopía de fluorescencia. El foco principal está en el análisis cuantitativo de secuencias de imágenes adquiridas en dos longitudes de onda (W1 y W2), que permiten calcular relaciones de fluorescencia relativas como W1/W2, una métrica clave en estudios de señalización intracelular, pH, calcio y otros procesos fisiológicos.

## Acerca del formato y el software original

Metafluor es un software privativo desarrollado por **Molecular Devices**, diseñado para el control de cámaras y adquisición de imágenes en experimentos de microscopía de fluorescencia. Sus archivos típicamente se guardan como secuencias de imágenes TIFF en carpetas separadas por canal.

Más información sobre el software original:

* Sitio oficial de Molecular Devices: [https://www.moleculardevices.com](https://www.moleculardevices.com)

Si bien Metafluor permite visualización y análisis de forma integrada, su naturaleza cerrada, la falta de interoperabilidad con otras herramientas y las limitaciones de automatización han llevado a la necesidad de desarrollar alternativas abiertas.

## Motivación del proyecto

Este proyecto nace de la necesidad de contar con una herramienta **libre, reproducible y personalizable**, que permita trabajar con imágenes de Metafluor fuera del ecosistema propietario. La idea central es reemplazar progresivamente las funciones básicas del software oficial con scripts en Python accesibles para toda la comunidad científica.

## Funcionalidades incluidas

* Lectura y organización de imágenes TIFF desde carpetas separadas.
* Visualización comparativa por frame (W1, W2 y W1/W2).
* Binarización por umbral e identificación de regiones intensas.
* Generación de videos 2D convencionales y videos 3D con mapas de superficie.
* Filtros de suavizado (Non-local Means) para mejorar la calidad visual.
* Interfaz preparada para ejecutarse directamente en Jupyter Lab.

## Requisitos

El código está diseñado para funcionar en un entorno de Python 3.8+ con las siguientes librerías instaladas:

* `numpy`
* `matplotlib`
* `opencv-python`
* `imageio`
* `seaborn`
* `tqdm`
* `ipywidgets`

La mayoría de las funciones fueron probadas en notebooks ejecutados localmente en Jupyter Lab sobre Linux.

## Instrucciones de descarga

Cloná este repositorio ejecutando el siguiente comando en tu terminal:

```bash
git clone https://github.com/juanjosecas/metafluor-analysis.git
```

Luego abrí el notebook principal (`Lectura_Archivos_Metafluor.ipynb`) en Jupyter Lab o VS Code y seguí las instrucciones comentadas en cada celda.

## Uso

1. Modificá las rutas a las carpetas que contienen las imágenes de W1 y W2.
2. Ejecutá las celdas de carga, visualización, análisis y exportación según necesidad.
3. Adaptá o extendé el código para nuevas métricas o automatización experimental.

## Licencia

Este proyecto se distribuye bajo la licencia MIT. Podés utilizarlo, modificarlo y adaptarlo para tus propios experimentos sin restricciones.
