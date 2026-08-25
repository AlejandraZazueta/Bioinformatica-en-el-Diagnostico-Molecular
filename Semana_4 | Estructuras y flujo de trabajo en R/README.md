# Semana 4 | Estructuras y flujo de trabajo en R

Durante esta semana continuaremos trabajando con **R**, utilizando **Google Colab** como entorno para ejecutar y documentar nuestros análisis.

Avanzaremos desde los principales **tipos y estructuras de datos en R** hacia la construcción de un **flujo de trabajo organizado y reproducible**.

---

## Objetivos de la semana

Al finalizar esta semana serás capaz de:

- Reconocer los principales tipos de datos en R.
- Diferenciar entre vectores, matrices, data frames, factores y listas.
- Explorar objetos utilizando `typeof()`, `class()` y `str()`.
- Acceder a información mediante indexación.
- Utilizar funciones y reconocer sus argumentos.
- Comprender cómo se utilizan paquetes en R.
- Diferenciar entre instalar, cargar y utilizar un paquete.
- Importar y explorar archivos `.csv`.
- Organizar código, resultados e interpretaciones en Google Colab.
- Reconocer las características básicas de un flujo de análisis reproducible.

---

# Clase 1.6 | Viaje a través de las estructuras en R

En esta clase revisaremos cómo R almacena y organiza la información.

## Contenidos

- Tipos de datos:
  - `character`
  - `double`
  - `integer`
  - `logical`
- Creación y asignación de objetos.
- Funciones y argumentos.
- Vectores.
- Matrices.
- Data frames.
- Factores.
- Listas.
- Exploración de objetos con:
  - `typeof()`
  - `class()`
  - `str()`
- Indexación:
  - `[ ]`
  - `[fila, columna]`
  - `$`

Durante la clase resolveremos **mini desafíos en Google Colab** para aplicar inmediatamente los contenidos revisados.

###  Mini desafíos Clase 1.6

 [[Abrir Mini desafíos Clase 1.6 en Google Colab](Clase_1.6_Mini_Desafios_Colab.ipynb)](https://colab.research.google.com/github/AlejandraZazueta/Bioinformatica-en-el-Diagnostico-Molecular/blob/main/Semana_4%20%7C%20Estructuras%20y%20flujo%20de%20trabajo%20en%20R/Clase_1.6_Mini_Desafios_Colab.ipynb)

---

#  Clase 1.7 | Flujo de trabajo en R: código, paquetes y documentos

En esta clase avanzaremos desde las estructuras de datos hacia la organización de un **flujo de análisis en R**.

## Contenidos

- Funciones integradas en R.
- Argumentos de una función.
- Importancia del orden de los argumentos.
- Paquetes de R.
- Diferencia entre:
  - instalar;
  - cargar;
  - utilizar un paquete.
- Importación de archivos `.csv`.
- Verificación de los datos.
- Scripts y notebooks.
- Organización del código.
- Documentación del análisis.
- Reproducibilidad.

###  Mini desafíos Clase 1.7

Durante la clase trabajaremos con pequeños desafíos para practicar:

- funciones integradas;
- argumentos;
- paquetes;
- importación de datos;
- exploración de un archivo;
- organización de un análisis reproducible.

 [[Abrir Mini desafíos Clase 1.7 en Google Colab](Clase_1.7_Mini_Desafios_Colab.ipynb)](https://colab.research.google.com/github/AlejandraZazueta/Bioinformatica-en-el-Diagnostico-Molecular/blob/main/Semana_4%20%7C%20Estructuras%20y%20flujo%20de%20trabajo%20en%20R/Clase_1.7_Mini_Desafios_Colab.ipynb)

---

#  Práctico 1.4 | Estructuras y flujo de trabajo en R

El práctico será **demostrativo y guiado**.

Integraremos los principales contenidos de las clases 1.6 y 1.7 siguiendo un flujo sencillo:

**Tipos de datos → Funciones → Estructuras → Indexación → Paquetes → Importación → Verificación → Análisis → Documentación**

Las operaciones estarán separadas para poder observar claramente el resultado producido por cada instrucción.

###  Notebook del práctico

[ [Abrir Práctico 1.4](Practico_1.4_Colab.ipynb)](https://colab.research.google.com/github/AlejandraZazueta/Bioinformatica-en-el-Diagnostico-Molecular/blob/main/Semana_4%20%7C%20Estructuras%20y%20flujo%20de%20trabajo%20en%20R/Practico_1_4_Colab.ipynb)

###  Archivo necesario

Para realizar una parte del práctico utilizaremos:

`datos/muestras_practico_1_4.csv`

Antes de ejecutar esa sección:

1. Descarga el archivo desde este repositorio.
2. Abre el notebook en Google Colab.
3. Selecciona **Archivos** en el panel lateral.
4. Sube `muestras_practico_1_4.csv`.
5. Continúa con las instrucciones del notebook.

---

#  Tarea 4 | Aplicación individual

La **Tarea 4 es individual** y deberá desarrollarse en Google Colab.

En esta actividad aplicarás los contenidos trabajados durante las clases y el práctico.

La tarea incluye ejercicios relacionados con:

- tipos de datos;
- estructuras de datos;
- funciones;
- argumentos;
- data frames;
- exploración de objetos;
- indexación;
- interpretación de resultados;
- documentación del código;
- organización de un flujo reproducible.

###  Tarea 4

 [Abrir Tarea 4](Tarea_4_.ipynb)

>  **Importante:** esta actividad debe ser desarrollada de manera individual.

La entrega se realizará a través de **Canvas**, siguiendo las instrucciones indicadas para la actividad.

---

#  Punto extra para el control

Al final de la Tarea 4 encontrarás un **desafío adicional**.

Este ejercicio:

- es individual;
- integra contenidos trabajados durante la semana;
- requiere interpretar el problema antes de escribir el código;
- permite obtener un **punto extra para el control**, de acuerdo con las instrucciones entregadas en clase.

El objetivo no es utilizar funciones que no hemos revisado, sino **combinar correctamente herramientas que ya conoces**.

---

#  Archivos de la semana

La carpeta de la Semana 4 está organizada de la siguiente manera:

    Semana_04_Estructuras_y_flujo_de_trabajo_en_R/
    │
    ├── README.md
    │
    ├── 01_Clase_1.6_Mini_Desafios_Colab.ipynb
    │
    ├── 02_Clase_1.7_Mini_Desafios_Colab.ipynb
    │
    ├── 03_Practico_1.4_Estructuras_y_flujo_de_trabajo_en_R.ipynb
    │
    ├── 04_Tarea_4_Individual.ipynb
    │
    └── datos/
        ├── muestras.csv
        └── muestras_practico_1_4.csv

---

#  Importar datos en Google Colab

Durante esta semana utilizaremos archivos `.csv`.

Para trabajar con ellos en Google Colab:

1. Descarga el archivo desde GitHub.
2. Abre el notebook correspondiente.
3. En Google Colab, selecciona el ícono ** Archivos**.
4. Selecciona **Subir al almacenamiento de la sesión**.
5. Sube el archivo `.csv`.
6. Verifica que el nombre coincida exactamente con el utilizado en el código.

Por ejemplo:

```r
datos <- read.csv("muestras.csv")
