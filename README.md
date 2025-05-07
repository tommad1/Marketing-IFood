# 🧠 Predictive Marketing Analysis - iFood Dataset

Este proyecto utiliza modelos de machine learning para analizar y predecir el comportamiento de clientes, con foco en su respuesta a campañas y su nivel de ingreso, basado en el dataset `marketing_campaign.csv`.

---

## 📌 Objetivos del proyecto

- Clasificar clientes según su **probabilidad de responder a una campaña** (`Response`)
- Predecir el **nivel de ingreso (`Income`)** de los clientes mediante regresión
- Utilizar técnicas de limpieza, transformación y selección de variables

---

## 🗂️ Contenido del repositorio

- `marketing_campaign.csv`: Dataset original
- `IFood_TM.ipynb`: Notebook principal con análisis exploratorio y modelos
- `IFood_TM_Regressor.ipynb`: Notebook complementario con mejoras en clasificación y regresión
- `README.md`: Este archivo

---

## 📊 Dataset

El dataset contiene información de más de 2.200 clientes, incluyendo:

- Edad, estado civil, educación
- Ingreso (`Income`)
- Compras por tipo de producto
- Canales utilizados (web, catálogo, tienda)
- Respuesta a campañas anteriores

---

## ⚙️ Técnicas aplicadas

- Limpieza de datos y tratamiento de nulos
- Detección de outliers con **MAD**
- Discretización de ingresos con `qcut`
- Codificación de variables categóricas (`LabelEncoder`, `get_dummies`)
- Modelos usados:
  - `RandomForestClassifier` para predecir `Response`
  - `LinearRegression` para predecir `Income`
  - `RandomForestRegressor` + `GridSearchCV` para optimizar predicción de `Income`

---

## 📈 Principales resultados

### Clasificación (`Response`)
- Modelo: `RandomForestClassifier`
- Accuracy: **87%**
- F1-score clase positiva (1): 0.36
- Observación: el modelo requiere balanceo por desbalance de clases

### Regresión (`Income`)
- `LinearRegression`: R² ≈ 0.73
- `RandomForestRegressor` (GridSearchCV): R² ≈ 0.75

---

## 🚀 Cómo ejecutar

1. Cloná el repositorio:
```bash
git clone https://github.com/tu_usuario/tu_repo.git
cd tu_repo
