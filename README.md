# Análisis Estadístico del Desempeño Académico Universitario

Estudio estadístico sobre los factores que influyen en el rendimiento académico de estudiantes universitarios, desarrollado para la Dirección de Asuntos Estudiantiles como parte de la Evaluación 03.

---

## Preguntas de investigación

1. ¿Existe evidencia de que dedicar más horas de estudio semanal mejore el desempeño académico global?
2. ¿En qué medida afecta el nivel de estrés en las calificaciones finales?

---

## Archivos del proyecto

| Archivo | Descripción |
|---------|-------------|
| `SabinaRomeroRodriguez.ipynb` | Notebook principal con el análisis completo |
| `Students_Grading_Dataset.csv` | Dataset con 5.000 registros de estudiantes |
| `WPC300_M3_Sabina_Romero.docx` | Informe en Word con los resultados |
| `README.md` | Este archivo |

---

## Requisitos

- Python 3.8+
- Jupyter Notebook o JupyterLab

Instalar dependencias:

```bash
pip install pandas numpy matplotlib seaborn scipy
```

---

## Cómo ejecutar

1. Clonar o descargar el repositorio
2. Colocar `Students_Grading_Dataset.csv` en el mismo directorio que el notebook
3. Abrir y ejecutar `SabinaRomeroRodriguez.ipynb` celda por celda

---

## Estructura del Notebook

| Sección | Contenido |
|---------|-----------|
| 1. Importación de librerías | pandas, numpy, matplotlib, seaborn, scipy |
| 2. Carga e inspección | Dimensiones, tipos de datos, vista previa |
| 3. Limpieza | Eliminación de registros con valores nulos |
| 4. Estadística descriptiva | Media, desviación estándar, cuartiles, asimetría |
| 5. Visualización | Histogramas, scatter plots, heatmap de correlación |
| 6. Correlación | Matriz de Pearson, ranking por variable objetivo |
| 7. Pruebas de hipótesis | Pearson, Spearman, Kruskal-Wallis con justificación |
| 8. Análisis por grupos | Cuartiles de estudio, grupos de estrés |
| 9. Integridad del dataset | Verificación de consistencia Grade vs Total_Score |
| 10. Conclusiones | Respuestas a las hipótesis y recomendaciones |

---

## Resultados principales

Ambas hipótesis fueron evaluadas con α = 0.05. En ningún caso se encontró evidencia estadísticamente significativa:

| Hipótesis | Pearson p | Spearman p | Kruskal p | Decisión |
|-----------|-----------|------------|-----------|----------|
| Study_Hours vs Total_Score | 0.740 | 0.776 | 0.910 | No se rechaza H₀ |
| Stress_Level vs Final_Score | 0.280 | 0.306 | 0.902 | No se rechaza H₀ |

> **Nota importante:** El análisis reveló que el dataset es de naturaleza sintética — las variables fueron generadas de forma independiente y aleatoria, lo que explica la ausencia de correlaciones significativas. La variable `Grade` no presenta relación monotónica con `Total_Score` (un estudiante con D tiene mayor puntaje promedio que uno con A), lo cual confirma este diagnóstico.

---

## Librerías utilizadas

- **pandas** — manipulación y análisis de datos tabulares
- **numpy** — operaciones numéricas
- **matplotlib** — visualización base
- **seaborn** — visualización estadística (heatmaps, boxplots, violin plots)
- **scipy.stats** — pruebas estadísticas (pearsonr, spearmanr, kruskal)