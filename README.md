# 📊 Predicción de Costes de Seguros Médicos

Proyecto de análisis exploratorio de datos (EDA) y Machine Learning utilizando PySpark para predecir los costes médicos de asegurados a partir de variables demográficas y de salud.

## 🎯 Objetivo

Analizar un conjunto de datos de seguros médicos mediante PySpark y construir un modelo de Machine Learning capaz de estimar los gastos médicos (`charges`) de una persona en función de sus características.

---

## 🛠 Tecnologías utilizadas

* Python 3
* PySpark
* Pandas API on Spark
* Spark MLlib
* Matplotlib
* Jupyter Notebook

---

## 📂 Dataset

Se utiliza el dataset **Medical Cost Personal Dataset**, que contiene información sobre:

* Edad (`age`)
* Sexo (`sex`)
* Índice de masa corporal (`bmi`)
* Número de hijos (`children`)
* Hábito de fumar (`smoker`)
* Región (`region`)
* Costes médicos (`charges`)

---

## 📊 Análisis Exploratorio de Datos (EDA)

Durante el análisis se realizaron las siguientes tareas:

### Limpieza de datos

* Comprobación de valores nulos.
* Validación de tipos de datos.
* Revisión de la calidad general del dataset.

### Análisis univariante

Variables categóricas:

* Sexo
* Fumador
* Región

Variables numéricas:

* Edad
* BMI
* Número de hijos
* Costes médicos

### Análisis bivariante

Relaciones estudiadas:

* Fumador vs Costes médicos
* Edad vs Costes médicos
* Correlación entre variables numéricas

### Visualizaciones

* Histogramas
* Boxplots
* Scatter plots
* Matriz de correlación

---

## 🤖 Machine Learning

Se construyó un modelo de:

### Regresión Lineal

Pipeline implementado con Spark ML:

1. Conversión de variables categóricas.
2. Indexación y codificación.
3. Creación del vector de características.
4. Escalado de variables.
5. Entrenamiento del modelo.
6. Predicción sobre conjunto de prueba.
7. Evaluación mediante RMSE.

---

## 📈 Resultados

El modelo obtuvo:

* RMSE ≈ 6548

Esto indica que, de media, las predicciones presentan un error aproximado de 6548 unidades monetarias respecto al valor real.

---

## 🔍 Principales conclusiones

* No se encontraron valores nulos.
* El hábito de fumar es la variable con mayor impacto en los costes médicos.
* La edad presenta una correlación positiva con los gastos sanitarios.
* El BMI también influye en los costes, aunque en menor medida.
* El número de hijos tiene una relación débil con los gastos médicos.

---

## 📁 Estructura del proyecto

```text
pyspark-insurance-ml/
│
├── data/
│   └── insurance.csv
│
├── notebooks/
│   └── PySpark_ML.ipynb
│
├── images/
│   ├── histograma_charges.png
│   ├── boxplot_smoker.png
│   └── scatter_age_charges.png
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## 🚀 Instalación

Clonar el repositorio:

```bash
git clone https://github.com/usuario/pyspark-insurance-ml.git
```

Acceder al proyecto:

```bash
cd pyspark-insurance-ml
```

Instalar dependencias:

```bash
pip install -r requirements.txt
```

---

## ▶️ Ejecución

Abrir el notebook:

```bash
jupyter notebook
```

Ejecutar:

```text
PySpark_ML.ipynb
```
