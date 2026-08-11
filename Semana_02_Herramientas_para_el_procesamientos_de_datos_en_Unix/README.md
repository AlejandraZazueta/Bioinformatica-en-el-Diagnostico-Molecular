# Tarea 2 | Aplicación de Unix al diagnóstico molecular

## Bioinformática en el Diagnóstico Molecular

### Contexto

En un laboratorio de diagnóstico molecular se dispone de un panel de genes asociados a diferentes condiciones de interés clínico.

Antes de realizar análisis bioinformáticos posteriores, es necesario inspeccionar los datos, identificar la información relevante y recuperar desde una base de datos pública la secuencia de referencia correspondiente a uno de los genes.

En esta tarea aplicarás los comandos aprendidos durante la Semana 2 para realizar este proceso utilizando la terminal Unix.

---

# Objetivo

Aplicar comandos de Unix para:

- inspeccionar archivos de datos biomoleculares;
- seleccionar y organizar información;
- combinar comandos mediante tuberías;
- generar nuevos archivos mediante redirecciones;
- identificar una secuencia de interés;
- recuperar una secuencia de referencia desde NCBI;
- documentar de manera reproducible el procedimiento realizado.

---

# Archivos de trabajo

Utiliza los archivos disponibles en:

```text
datos/
```

principalmente:

```text
panel_diagnostico.csv
muestras_moleculares.csv
```

---

# Parte 1 | Inspección de los datos

Utiliza la terminal para examinar:

```text
muestras_moleculares.csv
```

Determina:

1. ¿Cuántas muestras contiene el archivo?
2. ¿Qué información representa cada columna?
3. ¿Qué genes aparecen en la tabla?

No es necesario revisar manualmente todas las filas.

Utiliza los comandos de Unix aprendidos durante la clase.

---

# Parte 2 | Generación de una tabla de trabajo

A partir de:

```text
muestras_moleculares.csv
```

genera un nuevo archivo que contenga únicamente:

```text
muestra
gen
resultado
```

Guarda el archivo como:

```text
tabla_trabajo.csv
```

El archivo debe ser generado utilizando comandos de la terminal y no mediante Excel u otro editor de tablas.

---

# Parte 3 | Resumen de los genes analizados

Construye una tubería que permita determinar cuántas veces aparece cada gen en el conjunto de muestras.

Guarda el resultado en:

```text
frecuencia_genes.txt
```

A partir de este análisis responde:

**¿Qué gen aparece con mayor frecuencia en el conjunto de muestras?**

---

# Parte 4 | Control básico de los datos

Ahora utiliza:

```text
panel_diagnostico.csv
```

El panel contiene intencionalmente un registro duplicado.

Utilizando comandos de Unix:

1. identifica qué gen se encuentra duplicado;
2. determina cuántas veces aparece;
3. registra el procedimiento utilizado.

### Pregunta

¿Por qué sería importante detectar registros duplicados antes de realizar un análisis bioinformático?

Responde en un máximo de 3–4 líneas.

---

# Parte 5 | Selección de un gen

Selecciona **un gen del panel diagnóstico**.

Puedes escoger cualquiera de los genes presentes en:

```text
panel_diagnostico.csv
```

Registra:

```text
Gen seleccionado:
Aplicación:
Accession:
```

> No utilices una secuencia diferente a la indicada en el archivo `panel_diagnostico.csv`.

---

# Parte 6 | Recuperación de una secuencia desde NCBI

Utilizando la accession correspondiente al gen seleccionado, recupera su secuencia en formato FASTA desde NCBI utilizando `curl`.

La estructura general del comando es:

```bash
curl -s "https://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi?db=nuccore&id=ACCESION&rettype=fasta&retmode=text" > GEN.fasta
```

Debes reemplazar:

```text
ACCESION
```

por el número de acceso correspondiente y:

```text
GEN.fasta
```

por el símbolo del gen seleccionado.

Por ejemplo, si seleccionaras un gen llamado `GENX`, el archivo debería llamarse:

```text
GENX.fasta
```

---

# Parte 7 | Verificación del archivo FASTA

Una vez descargada la secuencia:

1. comprueba que el archivo fue creado;
2. visualiza sus primeras líneas;
3. identifica el encabezado FASTA;
4. determina cuántas líneas contiene el archivo.

Responde:

### Pregunta 1

¿Qué información puedes reconocer en el encabezado FASTA?

### Pregunta 2

¿Qué carácter permite reconocer el comienzo del encabezado de una secuencia FASTA?

---

# Parte 8 | Registro reproducible del análisis

Uno de los objetivos de esta actividad es que otra persona pueda reproducir el procedimiento que realizaste.

Crea un archivo llamado:

```text
comandos_tarea2.txt
```

Este archivo debe contener, en el orden en que fueron utilizados, **los comandos necesarios para realizar tu análisis**.

Puedes consultar el historial de la terminal utilizando:

```bash
history
```

Selecciona únicamente los comandos relevantes para resolver la tarea.

> No es necesario incluir comandos repetidos, errores de escritura ni intentos fallidos.

---

# Parte 9 | Respuestas

Crea un archivo:

```text
respuestas_tarea2.txt
```

Incluye:

```text
Nombre:

1. Número de muestras:

2. Genes presentes en el archivo:

3. Gen más frecuente:

4. Gen duplicado en panel_diagnostico.csv:

5. Importancia de detectar duplicados:

6. Gen seleccionado:

7. Aplicación:

8. Accession:

9. Información observada en el encabezado FASTA:

10. Carácter que identifica el encabezado FASTA:
```

---

# Archivos finales

Al finalizar deberías tener al menos:

```text
tabla_trabajo.csv

frecuencia_genes.txt

comandos_tarea2.txt

respuestas_tarea2.txt

GEN.fasta
```

donde `GEN.fasta` corresponde al gen que seleccionaste.

---

# Entrega en Canvas

Sube los siguientes archivos:

1. `tabla_trabajo.csv`
2. `frecuencia_genes.txt`
3. `comandos_tarea2.txt`
4. `respuestas_tarea2.txt`
5. archivo FASTA del gen seleccionado

Además, incluye **una captura de pantalla de la terminal** donde se observe la ejecución de una tubería (`|`) utilizada durante la actividad.

---

# Criterios de evaluación

| Criterio | Ponderación |
|---|---:|
| Uso correcto de comandos Unix | 30 % |
| Procesamiento y generación correcta de archivos | 25 % |
| Uso de tuberías y redirecciones | 15 % |
| Recuperación y verificación de la secuencia FASTA | 15 % |
| Respuestas e interpretación | 10 % |
| Orden y reproducibilidad del procedimiento | 5 % |
| **Total** | **100 %** |

---

# Comandos disponibles

Puedes resolver esta tarea utilizando los comandos y operadores trabajados durante la Semana 2:

```text
pwd
ls
cd

less
head
tail
cat
wc

cut
sort
uniq

curl

>
>>
|
```

También puedes utilizar:

```bash
man comando
```

o:

```bash
comando --help
```

para consultar la ayuda de un comando.

---

## Importante

El objetivo de la tarea no es memorizar comandos.

Debes demostrar que eres capaz de seleccionar y combinar las herramientas apropiadas para resolver un problema sencillo de procesamiento de datos biomoleculares.
