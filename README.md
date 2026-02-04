# Predicción de ventas de huevos mediante análisis de series temporales

Este proyecto analiza y modela **30 años de ventas diarias de huevos** de una tienda local en Sri Lanka, con el objetivo de **comprender patrones históricos y predecir las ventas para el año 2022**.

El enfoque combina **análisis exploratorio de datos (EDA)**, **estadística de series temporales** y **modelado ARIMA**, abordando estacionalidad, tendencia y eventos externos.

---

## 🥚 Contexto del problema

Las ventas de productos alimenticios suelen estar influenciadas por:
- estacionalidad
- festividades culturales
- eventos globales inesperados (ej. COVID-19)
- cambios en el comportamiento del consumidor

Este dataset presenta un caso realista de **forecasting**, ideal para estudiar cómo estos factores afectan una serie temporal de largo plazo.

---

## 🎯 Objetivos

- Analizar la evolución histórica de las ventas diarias de huevos
- Detectar tendencia, estacionalidad y fluctuaciones aleatorias
- Identificar eventos atípicos que impactaron las ventas
- Evaluar la estacionariedad de la serie
- Preparar un modelo para la predicción de ventas futuras

---

## 📊 Dataset

El conjunto de datos fue creado originalmente para una competición de forecasting y se basa en datos simulados inspirados en un caso real.

### Archivos
- `train_egg_sales.csv` → ventas históricas (≈30 años)
- `test.csv` → ventas a predecir para 2022
- `sample_submission.csv` → formato esperado de predicción

### Variable principal
- `Sales` → ventas diarias de huevos

---

## 🧹 Preparación de datos

- Conversión de la columna `Date` a formato datetime
- Extracción de variables temporales:
  - año, mes, día
  - semana del año
  - día de la semana
- Renombrado y estandarización de columnas
- Revisión de valores extremos (mínimos y máximos)

---

## 🔍 Análisis exploratorio (EDA)

### Análisis temporal
- Visualización de ventas diarias a lo largo del tiempo
- Identificación de tendencias de largo plazo
- Detección de períodos sin ventas (marzo–abril 2020, COVID-19)

### Estadísticas descriptivas
- Ventas mínimas y máximas
- Distribución de ventas mediante boxplots

### Análisis de autocorrelación
- Función de autocorrelación (ACF)
- Función de autocorrelación parcial (PACF)

Estos análisis permiten definir la estructura del modelo ARIMA.

---

## 📉 Estacionariedad

- Prueba de Dickey-Fuller aumentada (ADF)
- Evaluación de:
  - estadístico ADF
  - valor p
  - valores críticos
- Visualización de la **media móvil** para analizar estabilidad temporal

---

## 🤖 Modelado

- **Tipo de problema:** Forecasting (series temporales)
- **Modelo:** ARIMA
- **Métrica de evaluación:** RMSE (Root Mean Squared Error)

El modelo se entrena sobre los datos históricos y se prepara para generar predicciones diarias para 2022.

---

## 📈 Visualizaciones

- Serie temporal de ventas
- Boxplot de distribución de ventas
- Gráficos ACF y PACF
- Media móvil de ventas

Las visualizaciones ayudan a interpretar **tendencia, estacionalidad y ruido**.

---

## 🛠️ Tecnologías utilizadas

- **Python**
- **pandas, numpy**
- **matplotlib, seaborn**
- **statsmodels**
- **scikit-learn**
- **ydata-profiling**

---

## 📂 Estructura del repositorio

├── train_egg_sales.csv
├── test.csv
├── sample_submission.csv
├── Venta_huevos.py
├── README.md


---

## 🚀 Próximos pasos

- Ajuste fino de parámetros ARIMA
- Validación temporal (train / test split por fecha)
- Comparación con modelos SARIMA
- Incorporación de variables exógenas (festividades)
- Forecasting a largo plazo
- Visualización de predicciones vs valores reales

---

## 👤 Autor

**Flavia Hepp**  
Data Scientist / Time Series en formación  
