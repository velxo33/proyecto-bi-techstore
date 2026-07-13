# Proyecto Grupal de Inteligencia de Negocios: TechStore Perú S.A.C. 🛒📊

**Universidad Nacional Mayor de San Marcos (UNMSM)**  
**Facultad de Ingeniería de Sistemas e Informática**  
**Escuela Profesional de Ingeniería de Software**  
**Asignatura:** Inteligencia de Negocios (Ciclo 2026-1)  
**Docente:** Mg. Juan Gamarra Moreno  

---

## 📌 Descripción del Proyecto
Este repositorio contiene el desarrollo integral de una solución de Inteligencia de Negocios para la empresa ficticia **TechStore Perú S.A.C.**, un retailer tecnológico omnicanal. El proyecto abarca todo el ciclo de vida de los datos: desde la generación sintética de transacciones comerciales, pasando por la construcción de un pipeline ETL y un Datamart en estrella, hasta la aplicación de técnicas avanzadas de Machine Learning (Clasificación, Segmentación, Asociación y Regresión) y su posterior integración en un Dashboard interactivo en Power BI.

## 📂 Estructura del Repositorio
El proyecto sigue una arquitectura estandarizada para garantizar la reproducibilidad y el orden de los datos:

```text
proyecto-bi-techstore/
│
├── data/
│   ├── raw/                  # Datos sintéticos crudos con problemas de calidad inyectados
│   └── processed/            # Datos limpios y salidas de los modelos de ML para Power BI
│
├── notebooks/
│   ├── 00_generacion_datos.ipynb   # Generador de DW (Semilla 42)
│   ├── 01_datamart_etl.ipynb       # Pipeline ETL y modelo dimensional
│   ├── 02_visualizacion.ipynb      # Análisis Exploratorio de Datos (EDA)
│   ├── 03_clasificacion.ipynb      # Predicción de Abandono (Churn) - Random Forest
│   ├── 04_segmentacion.ipynb       # Segmentación RFM y K-Means
│   ├── 05_asociacion.ipynb         # Market Basket Analysis - Algoritmo Apriori
│   └── 06_regresion.ipynb          # Pronóstico de Ventas - Gradient Boosting
│
├── powerbi/
│   └── TechStore.pbix              # Dashboard final interactivo
│
├── informe/
│   ├── img/                        # Gráficos generados por los notebooks
│   └── Informe_Final_Inteligencia_de_Negocios_TechStore.pdf  # Reporte gerencial y técnico
│
├── prompts/
│   └── registro_prompts.md         # Bitácora de asistencia de IA (Ingeniería de Prompts)
│
├── requirements.txt                # Dependencias del proyecto
└── README.md                       # Documentación principal
