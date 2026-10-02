
# Semana 09 — Métodos de secuenciación masiva y control de calidad

## Bioinformática en el Diagnóstico Molecular

Durante esta semana revisaremos cómo los datos generados mediante secuenciación masiva son inspeccionados antes de continuar con un análisis bioinformático.

Trabajaremos con archivos **FASTQ** y utilizaremos **R** para explorar características básicas de las secuencias, evaluar la calidad de las reads e interpretar posibles problemas en los datos.

---

## Contenidos

- Introducción a la secuenciación masiva
- Reads y secuenciación paired-end
- Archivos FASTQ
- Puntajes de calidad Phred
- Inspección de longitud de reads
- Calidad por posición
- Calidad promedio por read
- Contenido GC
- Identificación de problemas de calidad
- Trimming
- Comparación antes y después del procesamiento

---

##  Práctico 2.4 — Control de calidad de secuencias

Práctico guiado para explorar datos de secuenciación y evaluar su calidad utilizando R.

El notebook incluye código y preguntas de interpretación que trabajaremos durante la clase.

### Abrir en Google Colab

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AlejandraZazueta/Bioinformatica-en-el-Diagnostico-Molecular/blob/main/Semana_09/Practico_2_4_Control%20de%20calidad%20de%20secuencias.ipynb)

**Archivo:** `Practico_2_4_Control de calidad de secuencias.ipynb`

---

## 📝 Tarea 9 — Control de calidad de secuencias

Actividad individual en la que deberán aplicar los procedimientos trabajados durante el práctico guiado.

Pueden utilizar el código del práctico como referencia, pero deberán identificar qué análisis realizar y adaptar el código a las muestras de la tarea.

### Abrir en Google Colab

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AlejandraZazueta/Bioinformatica-en-el-Diagnostico-Molecular/blob/main/Semana_09/Tarea_9_Control%20de%20calidad%20de%20secuencias.ipynb)

**Archivo:** `Tarea_9_Control de calidad de secuencias.ipynb`

---

##  Al finalizar esta semana deberías ser capaz de:

1. Reconocer la estructura básica de un archivo FASTQ.
2. Interpretar los puntajes de calidad Phred.
3. Comparar la calidad de reads R1 y R2.
4. Identificar problemas de calidad a lo largo de una secuencia.
5. Evaluar métricas como longitud, calidad y contenido GC.
6. Comprender el propósito del trimming.
7. Comparar datos antes y después del procesamiento.
8. Fundamentar si los datos son adecuados para continuar con un análisis bioinformático.

---

### Importante

El control de calidad no consiste únicamente en obtener un valor de **Q30** o clasificar una muestra como "buena" o "mala".

La decisión debe considerar **múltiples métricas en conjunto** y el contexto del experimento.
