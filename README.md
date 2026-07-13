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



## 🛠️ Requisitos e Instalación (Entorno Windows)

El proyecto ha sido diseñado para ejecutarse en un entorno aislado usando **Miniconda/Anaconda** con **Python 3.10+**. 
Para configurar el entorno y ejecutar los notebooks, abre `Anaconda Prompt` y sigue estos pasos:

1. **Clonar el repositorio y navegar a la carpeta raíz:**
   ```cmd
   git clone <URL_DEL_REPOSITORIO>
   cd proyecto-bi-techstore


conda create -n bi_techstore python=3.10 -y
conda activate bi_techstore


pip install -r requirements.txt

jupyter notebook



🚀 Orden de Ejecución
Para garantizar que los datos fluyan correctamente a través de los modelos, los notebooks deben ejecutarse estrictamente en orden numérico:

Ejecutar 00_generacion_datos.ipynb para poblar la carpeta data/raw/.

Ejecutar 01_datamart_etl.ipynb para limpiar la data y llenar data/processed/.

Ejecutar los notebooks del 02 al 06 para generar el EDA, los modelos y los archivos analíticos finales (predicciones_abandono.csv, segmentacion_clientes.csv, reglas_asociacion.csv, predicciones_regresion_ventas.csv).

Una vez ejecutados todos los scripts, se debe abrir el archivo TechStore.pbix y actualizar los orígenes de datos apuntando a la carpeta local data/processed/ para visualizar los resultados en el tablero de control.
