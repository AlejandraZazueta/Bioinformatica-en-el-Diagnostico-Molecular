# Semana 2 | Herramientas para el procesamiento de datos en Unix

## Bioinformática en el Diagnóstico Molecular

Durante esta semana aprenderemos a utilizar la terminal Unix para inspeccionar, organizar y procesar archivos utilizados en bioinformática.

A partir de archivos de texto y tablas con información biomolecular, utilizaremos comandos de Unix para seleccionar información, combinar operaciones mediante tuberías y generar nuevos archivos. Finalmente, aplicaremos estas herramientas para recuperar una secuencia biológica desde NCBI en formato FASTA.

---

## Resultados de aprendizaje

Al finalizar la semana, serás capaz de:

1. Utilizar comandos básicos de Unix para inspeccionar y manipular archivos.
2. Procesar archivos de texto y tablas desde la terminal.
3. Seleccionar y organizar información utilizando comandos de Unix.
4. Combinar comandos mediante tuberías (`|`) y redirecciones (`>`, `>>`).
5. Reconocer la estructura básica de archivos CSV y FASTA.
6. Recuperar una secuencia biológica desde NCBI utilizando `curl`.

---

## Contenidos

Durante esta semana trabajaremos con:

### Inspección de archivos

```bash
less
head
tail
cat
wc
```

### Procesamiento de tablas

```bash
cut
paste
sort
uniq
```

### Redirecciones y tuberías

```bash
>
>>
|
```

### Comodines

```bash
*
?
```

### Compresión y descompresión

```bash
gzip
gunzip
tar
zip
unzip
```

### Recuperación de información

```bash
curl
wget
```

---

#  Actividades de la semana

Te recomendamos realizar las actividades en el siguiente orden.

##  Ejemplo guiado

Primero realizaremos un ejemplo paso a paso utilizando un pequeño panel de genes asociados a diferentes aplicaciones de diagnóstico molecular.

Aprenderás a:

- inspeccionar una tabla;
- seleccionar columnas;
- ordenar información;
- detectar registros duplicados;
- utilizar tuberías;
- identificar una accession;
- recuperar una secuencia desde NCBI;
- reconocer un archivo FASTA.

 **[Comenzar ejemplo guiado](./ejemplo_guiado/EJEMPLO_GUIADO.md)**

---

##  Laboratorio 2

Ahora aplicarás los comandos aprendidos sobre un nuevo conjunto de datos correspondiente a muestras de un laboratorio de diagnóstico molecular.

A diferencia del ejemplo guiado, en esta actividad deberás decidir qué comandos utilizar y cómo combinarlos.

 **[Comenzar Laboratorio 2](./laboratorio_02/LABORATORIO_02.md)**

---

##  Tarea 2 | Aplicación al diagnóstico molecular

Finalmente, aplicarás lo aprendido para resolver de manera más autónoma un problema sencillo de procesamiento de datos biomoleculares.

Deberás integrar:

```text
Tabla de muestras
       ↓
Procesamiento con Unix
       ↓
Selección de un gen
       ↓
Identificación de accession
       ↓
Consulta a NCBI
       ↓
Secuencia FASTA
```

 **[Ver Tarea 2](./tarea_02/TAREA_02.md)**

---

#  Archivos de trabajo

Los datos necesarios para las actividades están disponibles en:

 **[Carpeta de datos](./datos/)**

Contiene:

| Archivo | Uso |
|---|---|
| `panel_diagnostico.csv` | Ejemplo guiado y Tarea 2 |
| `muestras_moleculares.csv` | Laboratorio 2 y Tarea 2 |

---

#  Trabajar en GitHub Codespaces

Las actividades deben realizarse utilizando la terminal de GitHub Codespaces.

Desde la página principal del repositorio:

1. Haz clic en **Code**.
2. Selecciona la pestaña **Codespaces**.
3. Haz clic en **Create codespace on main**.
4. Espera a que se abra el entorno de trabajo.
5. Abre la terminal.

Comprueba dónde te encuentras utilizando:

```bash
pwd
```

y observa el contenido del repositorio:

```bash
ls
```

---

#  Acceder a Semana 2 desde la terminal

Desde la raíz del repositorio puedes ingresar utilizando:

```bash
cd Semana_02_Herramientas_para_el_procesamientos_de_datos_en_Unix
```

Comprueba el contenido:

```bash
ls
```

Deberías encontrar:

```text
datos
ejemplo_guiado
laboratorio_02
tarea_02
README.md
```

---

#  ¿Necesitas ayuda con un comando?

Puedes consultar el manual:

```bash
man comando
```

Por ejemplo:

```bash
man cut
```

También puedes utilizar:

```bash
comando --help
```

Por ejemplo:

```bash
cut --help
```

Antes de preguntar cómo resolver una actividad, intenta identificar:

1. ¿Qué información necesito obtener?
2. ¿Qué comando realiza esa operación?
3. ¿Necesito combinarlo con otro comando?
4. ¿Necesito guardar el resultado en un archivo?

---

#  ¿Por qué utilizamos Unix en Bioinformática?

Los datos biomoleculares pueden contener miles o millones de registros y frecuentemente se almacenan en archivos de texto.

La terminal permite inspeccionar, seleccionar, transformar y organizar estos archivos sin necesidad de abrirlos manualmente.

Durante esta semana comenzaremos con archivos pequeños para comprender los principios fundamentales. Más adelante, estos mismos conceptos podrán aplicarse al procesamiento de conjuntos de datos bioinformáticos de mayor tamaño.

---

##  Antes de continuar

Asegúrate de poder acceder a GitHub Codespaces y localizar la carpeta de la Semana 2.

Cuando estés listo:

###  [Comenzar el Ejemplo guiado](./ejemplo_guiado/EJEMPLO_GUIADO.md)
