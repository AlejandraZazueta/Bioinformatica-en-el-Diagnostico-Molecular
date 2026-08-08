# Ejemplo guiado | Procesamiento de datos biomoleculares con Unix

## Semana 2 | Bioinformática en el Diagnóstico Molecular

En este ejemplo utilizaremos comandos de Unix para inspeccionar y procesar un pequeño panel de genes asociados a diferentes aplicaciones de diagnóstico molecular.

El objetivo es comenzar a utilizar la terminal como una herramienta para trabajar con datos biomoleculares.

---

## Archivo de trabajo

Utilizaremos el archivo:

```text
datos/panel_diagnostico.csv
```

Este archivo contiene tres columnas:

- `gen`: símbolo del gen.
- `aplicacion`: contexto clínico o diagnóstico asociado.
- `accesion`: número de acceso de la secuencia de referencia.

---

# 1. Preparar el entorno de trabajo

Abre el repositorio utilizando GitHub Codespaces.

Desde la terminal, comprueba en qué directorio te encuentras:

```bash
pwd
```

Lista el contenido del repositorio:

```bash
ls
```

Ingresa a la carpeta de la Semana 2:

```bash
cd Semana_02_Herramientas_para_el_procesamientos_de_datos_en_Unix
```

Comprueba su contenido:

```bash
ls
```

Deberías observar las carpetas:

```text
datos
ejemplo_guiado
laboratorio_02
tarea_02
```

---

# 2. Inspeccionar el archivo

Primero, observa el contenido de la carpeta `datos`:

```bash
ls datos
```

Visualiza las primeras líneas de la tabla:

```bash
head datos/panel_diagnostico.csv
```

Ahora observa las últimas líneas:

```bash
tail datos/panel_diagnostico.csv
```

También puedes visualizar el archivo completo utilizando:

```bash
cat datos/panel_diagnostico.csv
```

### Pregunta

¿Qué información contiene cada fila del archivo?

---

# 3. Contar las líneas del archivo

Utiliza:

```bash
wc -l datos/panel_diagnostico.csv
```

El resultado debería indicar:

```text
11 datos/panel_diagnostico.csv
```

¿Por qué aparecen 11 líneas si existen solamente 10 registros?

Porque la primera línea corresponde al encabezado de la tabla.

---

# 4. Seleccionar columnas

El archivo utiliza comas como delimitador.

Podemos seleccionar solamente las columnas `gen` y `accesion` utilizando:

```bash
cut -d ',' -f 1,3 datos/panel_diagnostico.csv
```

La opción:

```text
-d ','
```

indica que las columnas están separadas por comas.

La opción:

```text
-f 1,3
```

indica que queremos seleccionar las columnas 1 y 3.

---

# 5. Guardar el resultado en un nuevo archivo

Hasta ahora los resultados se han mostrado directamente en la terminal.

Podemos redirigir la salida a un nuevo archivo utilizando `>`:

```bash
cut -d ',' -f 1,3 datos/panel_diagnostico.csv > genes_accesiones.csv
```

Comprueba que el archivo fue creado:

```bash
ls
```

Visualízalo:

```bash
cat genes_accesiones.csv
```

> `>` crea un archivo nuevo o sobrescribe su contenido si ya existe.

---

# 6. Ordenar los genes

Extraigamos solamente la primera columna:

```bash
cut -d ',' -f 1 datos/panel_diagnostico.csv
```

Ahora combinaremos varios comandos.

Queremos:

1. seleccionar la columna de genes;
2. eliminar el encabezado;
3. ordenar los nombres alfabéticamente.

Utilizaremos:

```bash
cut -d ',' -f 1 datos/panel_diagnostico.csv | tail -n +2 | sort
```

El símbolo:

```text
|
```

se denomina **pipe** o tubería.

Permite utilizar la salida de un comando como entrada del siguiente.

En este caso:

```text
cut
 ↓
tail
 ↓
sort
```

Cada comando realiza una pequeña operación sobre los datos.

---

# 7. Buscar genes repetidos

Ahora agregaremos el comando `uniq`.

Ejecuta:

```bash
cut -d ',' -f 1 datos/panel_diagnostico.csv | tail -n +2 | sort | uniq -c
```

`uniq -c` cuenta cuántas veces aparece cada valor.

Observa el resultado.

### Pregunta

¿Qué gen aparece más de una vez?

El archivo contiene intencionalmente un registro duplicado.

Este tipo de revisión representa un ejemplo sencillo de **control de calidad de datos antes de realizar un análisis**.

---

# 8. Seleccionar información de un gen de interés

Supongamos que queremos trabajar con el gen **HBB**.

Podemos localizar visualmente su información en la tabla:

```bash
cat datos/panel_diagnostico.csv
```

Encontraremos:

```text
HBB,hemoglobinopatias,NM_000518.5
```

El número:

```text
NM_000518.5
```

corresponde al identificador de la secuencia de referencia que utilizaremos en el siguiente paso.

---

# 9. Recuperar una secuencia desde NCBI

Podemos utilizar `curl` para recuperar una secuencia directamente desde NCBI.

Ejecuta:

```bash
curl -s "https://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi?db=nuccore&id=NM_000518.5&rettype=fasta&retmode=text" > HBB.fasta
```

Comprueba que el archivo fue creado:

```bash
ls
```

Ahora observa sus primeras líneas:

```bash
head HBB.fasta
```

Deberías observar una estructura similar a:

```text
>NM_000518.5 ...
ACATTTGCTTCTGACACAACTGTGTTCACTAGC...
```

---

# 10. Reconocer la estructura de un archivo FASTA

Un archivo FASTA presenta dos componentes principales:

```text
>encabezado
SECUENCIA
```

La primera línea comienza con:

```text
>
```

y contiene información que identifica la secuencia.

Las líneas siguientes contienen la secuencia de nucleótidos.

Cuenta cuántas líneas contiene el archivo:

```bash
wc -l HBB.fasta
```

---

# 11. Guardar los archivos generados

Al finalizar el ejemplo deberías tener al menos:

```text
genes_accesiones.csv
HBB.fasta
```

Compruébalo utilizando:

```bash
ls
```

---

# Desafío final

Sin copiar los comandos anteriores de forma literal, intenta recuperar desde NCBI la secuencia de **otro gen presente en `panel_diagnostico.csv`**.

Para ello deberás:

1. identificar su número de acceso;
2. modificar el comando `curl`;
3. guardar la secuencia utilizando el símbolo del gen como nombre del archivo;
4. comprobar que el archivo FASTA fue creado correctamente.

Por ejemplo:

```text
CFTR.fasta
BRCA1.fasta
PAH.fasta
```

---

## ¿Qué aprendimos?

En este ejemplo utilizamos Unix para realizar un flujo sencillo de procesamiento de datos:

```text
Archivo CSV
     ↓
Inspección
     ↓
Selección de columnas
     ↓
Ordenamiento
     ↓
Detección de duplicados
     ↓
Identificación de una accession
     ↓
Recuperación de una secuencia desde NCBI
     ↓
Archivo FASTA
```

Estos mismos principios se utilizan en bioinformática para trabajar con conjuntos de datos mucho más grandes.
