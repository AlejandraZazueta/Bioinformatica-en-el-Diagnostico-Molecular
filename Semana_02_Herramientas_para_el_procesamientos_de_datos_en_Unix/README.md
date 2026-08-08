# Semana 2 | Procesamiento de datos en Unix

## Bioinformática en el Diagnóstico Molecular

Durante esta semana utilizaremos la terminal Unix para inspeccionar,
organizar y procesar archivos utilizados en bioinformática.

Los comandos aprendidos serán aplicados al manejo de archivos de texto,
tablas y secuencias biológicas.

---

## Resultados de aprendizaje

Al finalizar esta semana serás capaz de:

1. Utilizar comandos básicos de Unix para inspeccionar y manipular archivos.
2. Procesar archivos de texto y tablas mediante la terminal.
3. Aplicar redirecciones y tuberías para combinar comandos.
4. Manipular archivos CSV, TSV y FASTA.
5. Recuperar secuencias biológicas desde bases de datos públicas utilizando `curl`.

---

## Contenidos

- Navegación y manipulación de archivos.
- Inspección de archivos de texto.
- `less`, `head`, `tail`, `cat` y `wc`.
- Redirección de entrada y salida.
- Tuberías (`|`).
- Comodines (`*` y `?`).
- Compresión y descompresión.
- Procesamiento de tablas.
- `cut`, `sort`, `uniq`, `paste` y `echo`.
- Archivos FASTA.
- Recuperación de secuencias desde NCBI.

---

## Actividades de la semana

### 1. Ejemplo guiado

Procesamiento de un panel de genes asociado a diagnóstico molecular.

➡️ [Ir al ejemplo guiado](./ejemplo_guiado/EJEMPLO_GUIADO.md)

### 2. Laboratorio 2

Aplicación de comandos Unix para inspeccionar y procesar datos biomoleculares.

➡️ [Ir al Laboratorio 2](./laboratorio_02/LABORATORIO_02.md)

### 3. Tarea 2

Procesamiento de datos biomoleculares y recuperación de una secuencia desde NCBI.

➡️ [Ir a la Tarea 2](./tarea_02/TAREA_02.md)

---

## Archivos de trabajo

Los archivos necesarios para desarrollar las actividades se encuentran en:

📁 [`datos/`](./datos/)

---

## Comandos principales

```bash
pwd
ls
cd
mkdir

less
head
tail
cat
wc

cut
sort
uniq
paste

curl
wget

gzip
gunzip
tar
