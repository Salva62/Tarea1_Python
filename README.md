# M9 – Tarea 1 Python

Análisis de datos de fútbol a partir de estadísticas oficiales de **FBref** utilizando Python y la librería **pandas**.

## 📌 Objetivo
Cargar un DataFrame desde una fuente web (FBref), realizar una limpieza básica de datos y aplicar análisis descriptivo y comparativo sobre métricas ofensivas de la Premier League.

## 📊 Fuente de datos
https://fbref.com/en/comps/9/stats/Premier-League-Stats

La página fue guardada localmente en formato HTML para garantizar la reproducibilidad del análisis.

## 🧰 Tecnologías utilizadas
- Python 3
- pandas
- numpy
- Jupyter Notebook
- Visual Studio Code
- Git & GitHub

## 📁 Archivos del repositorio
- **Tarea1.ipynb** → Notebook con el desarrollo completo del ejercicio
- **Tarea1.pdf** → Exportación a PDF del notebook
- **Premier_League_Player_Stats _ FBref.com.html** → Página FBref guardada localmente
- **fbref_laliga21.csv / premier_standard_stats.csv** → Datasets auxiliares

## 📝 Contenido del análisis
- Carga de datos desde HTML
- Exploración del DataFrame (`head`, `info`, `describe`)
- Tratamiento de valores nulos y duplicados
- Renombrado de columnas duplicadas
- Ranking Top 20 de equipos según:
  - Goles anotados
  - Goles esperados (xG)
  - Métricas normalizadas por 90 minutos

## 👤 Autor
Salvador Álvarez Sánchez