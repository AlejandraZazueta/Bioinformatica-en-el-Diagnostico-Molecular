
# Semana 12 | Metagenómica: análisis de secuencias 16S con DADA2

## Objetivo de la semana

Aplicar un pipeline bioinformático para el procesamiento de secuencias del gen ARNr 16S mediante **DADA2**, desde la evaluación de calidad de las lecturas hasta la construcción de un objeto `phyloseq`, que será utilizado para los análisis de diversidad y composición de la microbiota en la siguiente semana.

## Material de trabajo

### Práctico 3.1 – Pipeline DADA2

**[Abrir Práctico 3.1 en Google Colab](https://colab.research.google.com/github/AlejandraZazueta/Bioinformatica-en-el-Diagnostico-Molecular/blob/main/Semana_12%20%7C%20Metagenomica/Pactico_3.1_Pipeline_DADA2.ipynb)**

Durante el práctico se revisarán las principales etapas del análisis:

1. Preparación del entorno de trabajo y carga de datos.
2. Evaluación de la calidad de las secuencias.
3. Filtrado y recorte de lecturas.
4. Estimación de errores e inferencia de variantes de secuencia (ASV).
5. Ensamblaje de lecturas paired-end y eliminación de quimeras.
6. Asignación taxonómica y construcción del objeto `phyloseq`.

### Tarea 11 – Pipeline DADA2

**[Abrir Tarea 11 en Google Colab](https://colab.research.google.com/github/AlejandraZazueta/Bioinformatica-en-el-Diagnostico-Molecular/blob/main/Semana_12%20%7C%20Metagenomica/Tarea_11_Pipeline_DADA2.ipynb)**

En esta actividad deberán aplicar el pipeline DADA2 a un conjunto de secuencias públicas y responder las preguntas de interpretación incorporadas en el notebook.

**Opciones para trabajar con los datos:**

- **Opción A:** descargar las secuencias mediante el código proporcionado.
- **Opción B:** cargar directamente los archivos FASTQ previamente descargados, para optimizar el tiempo de ejecución.

Ejecuten solamente una de las dos opciones.

## Recomendaciones importantes

- Abran los notebooks desde Google Colab y guarden una copia en su Google Drive.
- Ejecuten las celdas en el orden indicado.
- Revisen los resultados obtenidos en cada etapa antes de continuar.
- Guarden los archivos y objetos intermedios para evitar repetir el procesamiento si se interrumpe la sesión.
- Conserven el objeto `phyloseq` generado al finalizar la tarea.

## Continuidad del trabajo

**Semana 13:** utilizaremos el objeto `phyloseq` para realizar la visualización de datos, los análisis de diversidad alfa y beta y la caracterización de la composición taxonómica de las comunidades microbianas.
