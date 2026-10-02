# Semana 09 — Control de calidad de secuencias

## Bioinformática en el Diagnóstico Molecular

Durante esta semana trabajaremos con datos de secuenciación masiva y revisaremos cómo evaluar su calidad antes de continuar con un análisis bioinformático.

Utilizaremos archivos **FASTQ** y el lenguaje **R** en Google Colab para inspeccionar distintas características de las secuencias, identificar posibles problemas de calidad y evaluar el efecto del procesamiento de las reads.

---

## Contenidos

- Reads y secuenciación *paired-end*
- Archivos FASTQ
- Puntajes de calidad Phred
- Longitud de las reads
- Calidad por posición
- Calidad promedio por read
- Contenido GC
- Identificación de problemas de calidad
- *Trimming*
- Comparación antes y después del procesamiento

---

## 🧪 Práctico 2.4 — Control de calidad de secuencias

Práctico guiado para explorar datos de secuenciación y evaluar su calidad utilizando **R**.

Durante el práctico trabajaremos juntos siguiendo la lógica:

**observar → interpretar → diagnosticar → procesar → reevaluar**

El notebook contiene el código y las respuestas guiadas que utilizaremos durante la clase.

### Abrir en Google Colab

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AlejandraZazueta/Bioinformatica-en-el-Diagnostico-Molecular/blob/main/Semana_09%20%7C%20Control%20de%20calidad%20de%20secuencias/Practico_2_4_Control_de_calidad_de_secuencias.ipynb)

**Archivo:** `Practico_2_4_Control_de_calidad_de_secuencias.ipynb`

---

## 📝 Tarea 9 — Control de calidad de secuencias

Actividad individual para aplicar los procedimientos trabajados durante el práctico guiado.

En esta actividad deberán utilizar el **código del práctico como referencia**, identificar qué análisis necesitan realizar y adaptar el código para inspeccionar nuevas muestras de secuenciación.

El objetivo no es memorizar los comandos de R, sino utilizarlos para **interpretar la calidad de los datos y fundamentar sus decisiones**.

### Abrir en Google Colab

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AlejandraZazueta/Bioinformatica-en-el-Diagnostico-Molecular/blob/main/Semana_09%20%7C%20Control%20de%20calidad%20de%20secuencias/Tarea_9_Control%20de%20calidad%20de%20secuencias.ipynb)

**Archivo:** `Tarea_9_Control de calidad de secuencias.ipynb`

---

## 🎯 Al finalizar esta semana deberías ser capaz de:

1. Reconocer la estructura básica de un archivo FASTQ.
2. Interpretar los puntajes de calidad Phred.
3. Comparar reads R1 y R2 de una secuenciación *paired-end*.
4. Explorar la longitud de las reads.
5. Interpretar la calidad a lo largo de una secuencia.
6. Evaluar la calidad promedio de las reads.
7. Explorar la distribución del contenido GC.
8. Identificar posibles problemas de calidad.
9. Comprender el propósito del *trimming*.
10. Comparar los datos antes y después del procesamiento.

---

## 💡 Importante

El control de calidad no consiste en evaluar una única métrica.

Para decidir si los datos son adecuados para continuar con un análisis bioinformático debemos integrar diferentes evidencias, como:

**calidad por posición + calidad promedio + longitud + contenido GC + contexto del experimento**

Una alerta o un valor de calidad no determina automáticamente que una muestra deba ser descartada.
