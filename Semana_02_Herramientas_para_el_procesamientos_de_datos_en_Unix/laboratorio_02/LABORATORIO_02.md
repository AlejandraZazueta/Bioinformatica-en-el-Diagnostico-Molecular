
# Laboratorio 2 | Procesamiento de datos biomoleculares con Unix

## Bioinformática en el Diagnóstico Molecular

En el ejemplo guiado aprendiste a inspeccionar y procesar una tabla utilizando comandos de Unix.

En este laboratorio aplicarás esos mismos comandos sobre un nuevo conjunto de datos correspondiente a muestras procesadas en un laboratorio de diagnóstico molecular.

> **Objetivo:** utilizar la terminal Unix para inspeccionar, organizar y obtener información relevante a partir de una tabla de muestras biomoleculares.

---

# Archivo de trabajo

Utilizaremos:

```text
datos/muestras_moleculares.csv
```

La tabla contiene las siguientes variables:

| Variable | Descripción |
|---|---|
| `muestra` | Identificador de la muestra |
| `paciente` | Identificador anonimizado del paciente |
| `tipo_muestra` | Tipo de muestra biológica |
| `gen` | Gen analizado |
| `resultado` | Resultado del análisis |

---

# Parte 1 | Reconocimiento del archivo

Abre el repositorio utilizando GitHub Codespaces.

Desde la terminal, ingresa a la carpeta correspondiente a la Semana 2.

Comprueba que puedes localizar el archivo:

```text
datos/muestras_moleculares.csv
```

### Actividad 1

Utilizando los comandos aprendidos:

1. Determina en qué directorio te encuentras.
2. Lista los archivos disponibles.
3. Visualiza las primeras líneas de `muestras_moleculares.csv`.
4. Visualiza las últimas líneas.
5. Determina cuántas líneas contiene el archivo.

### Comandos que pueden ayudarte

```text
pwd
ls
head
tail
wc
```

### Pregunta 1

¿Cuántas muestras contiene la tabla?

**Importante:** recuerda considerar la existencia del encabezado.

---

# Parte 2 | Selección de información

Para algunos análisis no necesitamos trabajar con todas las columnas de una tabla.

### Actividad 2

Genera una tabla que contenga solamente:

```text
muestra
gen
resultado
```

Guarda el resultado con el nombre:

```text
muestras_resultados.csv
```

### Pistas

Piensa en:

```text
cut
-d
-f
>
```

Comprueba que el archivo fue creado correctamente y visualiza sus primeras líneas.

### Pregunta 2

¿Qué columnas seleccionaste para generar `muestras_resultados.csv`?

---

# Parte 3 | Distribución de los genes analizados

Ahora queremos conocer qué genes aparecen en el conjunto de muestras.

### Actividad 3

Utilizando una **tubería**, genera un flujo de comandos que permita:

1. seleccionar únicamente la columna `gen`;
2. eliminar el encabezado;
3. ordenar los genes alfabéticamente;
4. contar cuántas veces aparece cada gen.

El resultado debería tener una estructura similar a:

```text
3 GEN_A
2 GEN_B
1 GEN_C
```

### Comandos que pueden ayudarte

```text
cut
tail
sort
uniq
```

y el operador:

```text
|
```

### Pregunta 3

¿Qué gen fue analizado con mayor frecuencia?

---

# Parte 4 | Resultados del análisis molecular

Ahora queremos conocer la distribución global de los resultados.

### Actividad 4

Construye una tubería que permita contar cuántas muestras presentan cada tipo de resultado.

Para ello deberás:

1. seleccionar la columna `resultado`;
2. eliminar el encabezado;
3. ordenar los valores;
4. contar sus apariciones.

### Pregunta 4

Completa:

```text
Resultados positivos: ______

Resultados negativos: ______
```

### Pregunta 5

¿Existe la misma cantidad de resultados positivos y negativos?

---

# Parte 5 | Crear un archivo de resumen

Hasta ahora los resultados se han mostrado en la terminal.

Ahora guarda el conteo de genes obtenido en la Parte 3 en un archivo llamado:

```text
resumen_genes.txt
```

No es necesario escribir manualmente el resultado.

Utiliza una **redirección** para que la salida de tu tubería quede almacenada directamente en el archivo.

Comprueba su contenido utilizando:

```bash
cat resumen_genes.txt
```

---

# Parte 6 | Interpretación

Observa los resultados que obtuviste y responde brevemente.

### Pregunta 6

¿Por qué podría ser útil conocer cuántas muestras están asociadas a cada gen antes de realizar un análisis bioinformático?

### Pregunta 7

¿Qué ventaja tiene procesar una tabla utilizando comandos de Unix en lugar de revisar manualmente cada fila?

Responde considerando qué ocurriría si el archivo tuviera:

```text
10 muestras
100 muestras
10.000 muestras
1.000.000 de muestras
```

---

# Parte 7 | Desafío

Ahora realiza el análisis con menor cantidad de instrucciones.

Genera un archivo llamado:

```text
resumen_resultados.txt
```

que contenga el número de resultados positivos y negativos presentes en la tabla.

### Condiciones

Debes:

- utilizar una tubería;
- utilizar al menos tres comandos;
- utilizar una redirección;
- no escribir manualmente los conteos.

Al finalizar comprueba el contenido utilizando:

```bash
cat resumen_resultados.txt
```

---

# Archivos que deberías haber generado

Al terminar el laboratorio deberías tener:

```text
muestras_resultados.csv
resumen_genes.txt
resumen_resultados.txt
```

Puedes comprobarlo utilizando:

```bash
ls
```

---

# Reflexión final

En este laboratorio partimos de una tabla de muestras y realizamos un pequeño flujo de procesamiento:

```text
muestras_moleculares.csv
          ↓
     inspección
          ↓
selección de columnas
          ↓
    ordenamiento
          ↓
      conteo
          ↓
 generación de archivos
          ↓
    interpretación
```

En un análisis bioinformático real, los archivos pueden contener miles o millones de registros.

La combinación de comandos mediante tuberías permite construir flujos de procesamiento reproducibles sin necesidad de modificar manualmente los datos.

---

## Antes de finalizar

Comprueba que puedes explicar qué función cumplen:

```text
head
tail
wc
cut
sort
uniq
>
|
```

Estos conceptos serán necesarios para desarrollar la **Tarea 2**.
