# Semana 06 | Introducción al aprendizaje automático

Durante esta semana comenzaremos a trabajar con **modelos de predicción** y **regresión lineal simple**.

El objetivo es comprender cómo podemos utilizar datos para estudiar la relación entre variables cuantitativas, construir un modelo lineal, interpretar sus principales resultados y utilizarlo para realizar predicciones.

---

##  Contenidos de la semana

Durante esta semana trabajaremos con:

- Introducción a los modelos de predicción
- Variable respuesta y variable predictora
- Gráficos de dispersión
- Correlación
- Valores observados y predichos
- Residuos
- Método de mínimos cuadrados
- Regresión lineal simple
- Intercepto y pendiente
- Construcción de modelos con `lm()`
- Interpretación de `summary()`
- Error estándar y p-value
- Coeficiente de determinación R²
- Predicción con `predict()`
- Asociación y causalidad

---

##  Clase 2.1 | Introducción al aprendizaje automático

En esta clase revisaremos qué es un modelo de predicción y cómo podemos representar la relación entre una **variable predictora X** y una **variable respuesta Y**.

---

##  Clase 2.2 | Modelos de regresión lineal

Estudiaremos cómo se construye e interpreta un modelo de regresión lineal simple.

Seguiremos el flujo:

**Observar → Correlacionar → Modelar → Interpretar → Predecir**

---

##  Desafíos Clase 2.2 | Regresión lineal

Durante la clase resolveremos pequeños desafíos en R para aplicar progresivamente los conceptos estudiados.

Trabajaremos con la relación entre:

**IMC → Presión arterial sistólica**

###  Abrir en Google Colab

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AlejandraZazueta/Bioinformatica-en-el-Diagnostico-Molecular/blob/main/Semana_06%7CIntroducci%C3%B3n%20al%20aprendizaje%20autom%C3%A1tico/Desafios_Clase_2_2_Regresion_Lineal.ipynb)

 **Archivo de datos:** `datos_salud.csv`

> Recuerda subir `datos_salud.csv` a Google Colab antes de ejecutar el análisis.

---

##  Práctico 2.1 | Correlación y regresión lineal simple

En este práctico aplicaremos el flujo completo de análisis utilizando un conjunto de datos biomédicos.

Trabajaremos con la relación entre:

**lcavol → lpsa**

Durante el práctico deberán:

1. Explorar los datos.
2. Construir e interpretar un gráfico de dispersión.
3. Calcular e interpretar la correlación.
4. Construir un modelo de regresión lineal.
5. Identificar e interpretar sus coeficientes.
6. Interpretar el error estándar y el p-value.
7. Interpretar R².
8. Utilizar el modelo para realizar una predicción.

###  Abrir en Google Colab

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AlejandraZazueta/Bioinformatica-en-el-Diagnostico-Molecular/blob/main/Semana_06%7CIntroducci%C3%B3n%20al%20aprendizaje%20autom%C3%A1tico/Practico_2_1_Regresion_lineal_.ipynb)

 **Archivo de datos:** `pros_data.csv`

> Recuerda subir `pros_data.csv` a Google Colab antes de ejecutar el práctico.

---

##  Tarea 6 | Regresión lineal simple

En esta actividad aplicarán de manera más autónoma los conceptos trabajados durante la semana utilizando un nuevo conjunto de datos.

Trabajaremos con la relación entre:

**radius_mean → concavity_mean**

El objetivo no es solamente ejecutar el código, sino también **interpretar correctamente los resultados obtenidos**.

###  Abrir en Google Colab

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AlejandraZazueta/Bioinformatica-en-el-Diagnostico-Molecular/blob/main/Semana_06%7CIntroducci%C3%B3n%20al%20aprendizaje%20autom%C3%A1tico/Tarea_6_Regresion_lineal_.ipynb)

 **Archivo de datos:** `data_breast.csv`

> Recuerda subir `data_breast.csv` a Google Colab antes de comenzar la tarea.

---

## Al finalizar esta semana deberías ser capaz de:

- Reconocer la variable predictora y la variable respuesta.
- Explorar gráficamente la relación entre dos variables cuantitativas.
- Calcular e interpretar una correlación.
- Construir un modelo de regresión lineal simple en R.
- Interpretar el intercepto y la pendiente.
- Interpretar el error estándar y el p-value de un coeficiente.
- Interpretar R².
- Utilizar un modelo para realizar una predicción.
- Diferenciar entre **asociación** y **causalidad**.

---

### 💡 Recuerda

> **El objetivo no es memorizar la salida de R, sino comprender qué nos dice el modelo sobre los datos.**
