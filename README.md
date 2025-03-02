# Análisis Empírico del Problema de Alquiler de Canoas 🛶

Este repositorio contiene el código, datos y resultados de un estudio empírico sobre diferentes algoritmos para resolver el problema de alquiler de canoas. El objetivo es comparar la eficiencia (tiempo de ejecución y uso de memoria) de tres enfoques algorítmicos: fuerza bruta, recursión con memoización y programación dinámica.

## Descripción del Problema

El problema de alquiler de canoas consiste en encontrar la forma más económica de alquilar una canoa para viajar entre *n* puertos a lo largo de un río.  Existe un costo por alquilar una canoa entre cualquier par de puertos, y el objetivo es minimizar el costo total del viaje desde el puerto 1 hasta el puerto *$n$*. No es posible viajar río arriba. Se asume que no es más barato ir directo que hacer escalas.

## Algoritmos Implementados

Se implementaron y compararon los siguientes algoritmos:

1.  **Fuerza Bruta (Recursivo):** Explora todas las posibles combinaciones de alquileres de forma recursiva.  Tiene una complejidad temporal exponencial, $O(2^n).$
2.  **Recursión con Memoización (Top-Down):**  Utiliza una tabla de memoización para almacenar los resultados de subproblemas ya calculados, evitando recálculos innecesarios.  Tiene una complejidad temporal de $O(n^2).$
3.  **Programación Dinámica (Bottom-Up):**  Resuelve el problema de forma iterativa, construyendo la solución desde los subproblemas más pequeños hasta el problema completo.  Tiene una complejidad temporal de $O(n^2)$.

## Estructura del Repositorio

proyecto-alquiler-canoas/
├── data/
│ ├── raw/
│ │ ├── seeds.txt
│ │ └── instancias.json
│ └── processed/
│ ├── resultados_optimizados.csv
│ └── resultados_optimizados2.csv
├── notebooks/
│ └── proyecto_canoas_analisis.ipynb
├── docs/
│ ├── proyecto_canoas_analisis.html
│ └── proyecto_canoas_analisis.pdf
└── README.md


## Cómo Ejecutar el Código

1.  **Descargar repositorio:**
Los archivos se pueden descargar desde el repositorio
   
2.  **Abrir el notebook:**
    ```bash
    jupyter notebook notebooks/proyecto_canoas_analisis.ipynb
    ```
   (o `jupyter lab` si usas JupyterLab)

3.  **Ejecutar las celdas del notebook** en orden. El notebook contiene el código para generar las instancias, ejecutar los algoritmos, medir el tiempo y la memoria, y realizar el análisis estadístico.

## Resultados Principales


*   La programación dinámica ($DP$) y la recursión con memoización son significativamente más rápidas que la fuerza bruta, como se esperaba teóricamente ($O(n^2)$ vs. $O(2^n)$).
*   La programación dinámica es ligeramente más rápida que la recursión con memoización y usa menos memoria.
*   (Incluye aquí tus resultados específicos, con números y comparaciones).
*   (Incluye una breve discusión sobre las diferencias entre `psutil` y `tracemalloc`).

## Herramientas y Librerías

*   **Lenguaje:** Python 3.11
*   **Librerías:**
    *   `numpy`: Para operaciones numéricas y manejo de arreglos.
    *   `pandas`: Para manejo y análisis de datos.
    *   `matplotlib`: Para visualización de datos (gráficos).
    *   `seaborn`: Para visualización de datos (gráficos estadísticos).
    *   `plotly`: Para visualización de datos (gráficos interactivos).
    *   `scipy`: Para computación científica (estadísticas).
    *   `statsmodels`: Para modelos estadísticos (ANOVA).
    *   `psutil`: Para monitorizar el uso de CPU y memoria.
    *   `tracemalloc`: Para rastrear asignaciones de memoria.
    *   `joblib`: Para ejecución en paralelo.
    *   `unittest`: Para pruebas unitarias.
    *   `time`: Para medir los tiempos de ejecución
    *   `json`: Formato de los archivos de entrada
    * `sklearn`: Modelado predictivo (regresiones, machine learning)

## Cómo Citar


Si utilizas este código o los resultados en tu trabajo, por favor cítalo de la siguiente manera:


## Autores

*   Hervin D. Rodríguez C. - HervinY- daniel26rodriguez@gmail.com

---
