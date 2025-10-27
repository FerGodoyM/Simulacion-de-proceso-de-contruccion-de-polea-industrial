## Avance — Simulación del proceso de construcción de poleas (Maestranza Faremin)

Este repositorio contiene el avance del proyecto final de la asignatura *Simulación*. El objetivo es modelar y simular el proceso de fabricación de poleas en la maestranza Faremin para analizar la situación actual: medir tiempos de ciclo, variabilidad y utilización de recursos.

## Información del curso

- Asignatura: Simulación
- Profesora: Lucy Bugueño Guajardo
- Carrera: Ingeniería Civil En Computación e Informatica
- Universidad: Universidad Central (UCEN)

## Artefactos principales en este repositorio

- `simulacion.ipynb` — Notebook con el modelo, la simulación y los análisis (celdas ejecutables).
- `simulacion_eventos_gantt.doe` — Registro detallado de eventos (formato CSV / .doe) usado para el diagrama de Gantt.
- `simulacion_resumen_estadistico.csv` — Resumen estadístico de tiempos de ciclo y métricas calculadas.
- `1_histograma_tiempos_ciclo.png`, `2_grafico_utilizacion_recursos.png`, `4_diagrama_gantt_poleas.png` — Gráficos generados por la simulación.

> Nota: El notebook es el punto de partida recomendado para reproducir los resultados y explorar parámetros.

## Tecnologías y librerías (usadas o recomendadas)

El proyecto fue desarrollado en Python. En el notebook se utilizan (entre otras):

- Python 3.8+ (recomendado)
- Jupyter Notebook / JupyterLab
- simpy (simulación de eventos discretos)
- pandas, numpy (manipulación y análisis de datos)
- matplotlib / seaborn (visualización)

Puedes instalar las dependencias mínimas con pip. En PowerShell (Windows):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install jupyterlab jupyter simpy pandas numpy matplotlib seaborn
```

Si prefieres usar un entorno conda:

```powershell
conda create -n simulacion python=3.10 -y
conda activate simulacion
pip install jupyterlab simpy pandas numpy matplotlib seaborn
```

## Cómo reproducir la simulación (rápido)

1. Clona o descarga este repositorio.
2. Activa tu entorno virtual e instala dependencias (ver arriba).
3. Abre el notebook:

```powershell
jupyter notebook simulacion.ipynb
# o
jupyter lab
```

4. Ejecuta las celdas del notebook de arriba hacia abajo. El notebook contiene secciones para:

- Definición del modelo (recursos, procesos y parámetros).
- Ejecución de la simulación y recolección de datos.
- Análisis y generación de gráficos.

5. Al finalizar, el notebook genera los artefactos: los archivos `.png` con gráficos y los CSV/DOE con resultados (`simulacion_resumen_estadistico.csv`, `simulacion_eventos_gantt.doe`).

## Resultado esperado

- Histogramas de tiempos de ciclo.
- Gráficos de utilización de recursos (identificación de cuellos de botella).
- Diagrama de Gantt para las primeras ordenes/poleas.
- CSV con resumen estadístico y archivo `.doe` con el log de eventos para entrega.

## Estructura del repositorio

```
.
├─ simulacion.ipynb
├─ simulacion_eventos_gantt.doe
├─ simulacion_resumen_estadistico.csv
├─ 1_histograma_tiempos_ciclo.png
├─ 2_grafico_utilizacion_recursos.png
└─ 4_diagrama_gantt_poleas.png
```

## Autor

Fernando Godoy Marín
