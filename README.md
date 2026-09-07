# Laboratorio 6 — Análisis de redes sociales (YouTube)

CC3084 Data Science — Universidad del Valle de Guatemala, Semestre II 2026

## Integrantes

- Javier Eduardo España (23361)
- Angel Esteban Esquit (23221)
- Roberto Jose Barreda (23354)

## Estructura del Repositorio

El proyecto se encuentra organizado en las siguientes carpetas:

- `notebooks/`: Cuadernos interactivos Jupyter con la secuencia completa del análisis.
- `data/`: Datos crudos de entrada (`youtube_videos.csv`, `youtube_comments.csv`) y datos derivados/procesados generados por los notebooks.
- `report/`: Código fuente en LaTeX (`reporte.tex`), figuras de alta resolución (`figures/`) e informe final compilado (`reporte.pdf`).
- `docs/`: Documentación del laboratorio y copia del informe final en PDF.

## Contenido de los Notebooks

Los notebooks se ejecutan secuencialmente; cada uno lee los archivos procesados que deja el notebook anterior en `data/`:

| Notebook | Secciones del enunciado |
|---|---|
| `notebooks/01_carga_calidad_limpieza.ipynb` | 1. Carga, comprensión e integración · 2. Calidad, limpieza y preprocesamiento |
| `notebooks/02_analisis_exploratorio.ipynb` | 3. Análisis exploratorio |
| `notebooks/03_red_bipartita.ipynb` | 4. Red bipartita autor-video |
| `notebooks/04_proyecciones_topologia.ipynb` | 5. Proyecciones · 6. Topología y fragmentación |
| `notebooks/05_comunidades_centralidad.ipynb` | 7. Comunidades · 8. Nodos centrales y participantes puente |
| `notebooks/06_contenido_sentimiento.ipynb` | 9. Análisis de contenido y sentimiento · 10. Interpretación, limitaciones y conclusiones |

### Datos de entrada y salida (`data/`)
- **Entrada:** `youtube_videos.csv` (293 videos) y `youtube_comments.csv` (406 comentarios).
- **Salida / Procesados:**
  - `videos_procesado.csv`, `comments_procesado.csv` (limpieza y normalización NLP)
  - `red_nodos.csv`, `red_aristas.csv` (red bipartita)
  - `proj_autor_autor.csv`, `proj_video_video.csv` (proyecciones ponderadas)
  - `centralidad.csv` (métricas de grado, betweenness, PageRank, cercanía)
  - `sentimiento_comments.csv` (análisis de sentimiento en español)
  - `fig_comunidades.png` (gráfico de comunidades de Louvain)

## Informe Final

El informe completo se elaboró en LaTeX con todas las figuras, tablas, justificaciones metodológicas y conclusiones integradas:
- **PDF:** `report/reporte.pdf` (también disponible en `docs/reporte.pdf` y en la raíz `reporte.pdf`).
- **Código fuente:** `report/reporte.tex`

## Dependencias e Instalación

Requisitos: Python 3.12+ y TeX Live (para compilar LaTeX).

Instalación de dependencias de Python:
```bash
pip install -r requirements.txt
```

## Cómo ejecutar

### 1. Ejecutar todos los notebooks
Desde la raíz del repositorio:
```bash
jupyter nbconvert --to notebook --execute --inplace notebooks/*.ipynb
```

O abriendo Jupyter:
```bash
jupyter notebook
```

### 2. Compilar el reporte en LaTeX
```bash
cd report
pdflatex -interaction=nonstopmode reporte.tex
pdflatex -interaction=nonstopmode reporte.tex
```
