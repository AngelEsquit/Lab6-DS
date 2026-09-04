# Laboratorio 6 — Análisis de redes sociales (YouTube)

CC3084 Data Science — Universidad del Valle de Guatemala, Semestre II 2026

## Integrantes

- Javier Eduardo España (23361)
- Angel Esteban Esquit (23221)
- Roberto Jose Barreda (23354)

## Contenido

Los notebooks se ejecutan en orden; cada uno lee los archivos que deja el anterior en `data/`.

| Notebook | Secciones del enunciado |
|---|---|
| `01_carga_calidad_limpieza.ipynb` | 1. Carga e integración · 2. Calidad y limpieza |
| `02_analisis_exploratorio.ipynb` | 3. Análisis exploratorio |
| `03_red_bipartita.ipynb` | 4. Red bipartita autor-video |
| `04_proyecciones_topologia.ipynb` | 5. Proyecciones · 6. Topología y fragmentación |

Datos de entrada: `data/youtube_videos.csv` y `data/youtube_comments.csv`. Los demás archivos de `data/` son generados por los notebooks.

## Dependencias

Python 3.12+ y:

```bash
pip install pandas numpy matplotlib seaborn networkx nltk spacy emoji wordcloud jupyter
python -m spacy download es_core_news_sm
```

El notebook 01 descarga por su cuenta el corpus `stopwords` de `nltk` en su primera ejecución; el modelo `es_core_news_sm` de spaCy (usado para lematizar) sí debe instalarse con el comando anterior.

## Cómo ejecutar

Desde la raíz del repositorio (las rutas a `data/` son relativas):

```bash
jupyter notebook
```

o, para ejecutar todo sin abrir la interfaz:

```bash
jupyter nbconvert --to notebook --execute --inplace 0*.ipynb
```
