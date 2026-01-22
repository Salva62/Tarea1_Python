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

## 📝 Contenido del análisis (paso a paso)

### 1) Carga del DataFrame (FBref)
- Acceso a la tabla de FBref y guardado local con **Ctrl+S → “Página web, completa”**
- Lectura del HTML con **pandas.read_html()**
- Selección de la **tabla 0** y verificación de dimensiones (20 equipos, 32 columnas)

### 2) Limpieza y preparación
- Aplanado de cabeceras (MultiIndex) y eliminación de columnas auxiliares tipo **“Unnamed”**
- Configuración de visualización para mostrar todas las columnas (`display.max_columns`)
- Detección del problema de **columnas duplicadas** (totales vs métricas por 90)
- Renombrado automático de duplicados añadiendo sufijo **/90** a la segunda aparición  
  (ej: `xG` → `xG/90`, `Gls` → `Gls/90`, etc.)

### 3) Exploración y análisis descriptivo
- Visualización inicial: `head()`
- Estructura y tipos: `info()`
- Distribución de plantilla: `value_counts()` sobre `# Pl` (jugadores usados)
- Estadística descriptiva enfocada en métricas ofensivas:
  `describe()` sobre `Gls`, `Ast`, `G+A`, `xG`, `xAG`

### 4) Calidad del dato
- Comprobación de valores nulos con `isna()`:
  - total de NaN = 0 (dataset limpio)
- Eliminación de duplicados de filas con `drop_duplicates()`:
  - duplicados eliminados = 0

### 5) Ranking y comparación de eficacia ofensiva
- Top 20 equipos por **goles totales (Gls)** y comparación con **xG**
- Top 20 por **xG/90** y comparación con **Gls/90**
- Interpretación final: equipos que convierten por encima / por debajo de lo esperado

## 👤 Autor
Salvador Álvarez Sánchez