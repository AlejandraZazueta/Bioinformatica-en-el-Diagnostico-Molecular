# Laboratorio 1 | Primeros pasos en Linux utilizando GitHub Codespaces

## Objetivo

Familiarizarse con el entorno de trabajo Linux mediante GitHub Codespaces y aplicar comandos básicos para navegar por el sistema de archivos, crear directorios, organizar información y descargar archivos desde Internet.

---

# Antes de comenzar

En este laboratorio utilizarás GitHub Codespaces.

Si aún no has abierto tu entorno de trabajo:

1. Ingresa al repositorio del curso.
2. Haz clic en **Code → Codespaces → Create codespace on main**.
3. Espera a que cargue Visual Studio Code.
4. Abre la terminal.

---

# Parte 1. Conociendo el entorno

### 1. ¿Dónde estoy?

Ejecuta:

```bash
pwd
```

**Pregunta**

¿Qué información entrega este comando?

---

### 2. ¿Qué contiene mi directorio?

```bash
ls
```

Ahora prueba:

```bash
ls -lh
```

**Pregunta**

¿Cuál es la diferencia entre ambos comandos?

---

### 3. Explora el repositorio

Navega hasta la carpeta de la Semana 1.

Utiliza únicamente los comandos aprendidos en clases.

Cuando llegues, verifica tu ubicación con:

```bash
pwd
```

---

# Parte 2. Organización de un proyecto

Imagina que comenzarás un nuevo proyecto de bioinformática.

Crea la siguiente estructura de carpetas:

```
Proyecto_Bioinformatica
│
├── datos
├── resultados
├── scripts
└── documentos
```

No copies la estructura.

Construye cada carpeta utilizando los comandos aprendidos.

Cuando termines ejecuta:

```bash
tree
```

Si `tree` no funciona, utiliza varios comandos `ls`.

---

# Parte 3. Descargar un archivo

Ingresa al directorio

```
datos
```

Descarga el siguiente archivo utilizando **wget** o **curl**.

```bash
[https://raw.githubusercontent.com/AlejandraZazueta/Bioinformatica-en-el-Diagnostico-Molecular/refs/heads/main/Semana_01_Introduccion_Unix/Datos/bienvenida_bioinformatica.txt ]
```

Comprueba que el archivo fue descargado utilizando

```bash
ls -lh
```

---

# Parte 4. Organización de archivos

Realiza las siguientes acciones.

- Cambia el nombre del archivo descargado por

```
muestra.txt
```

- Copia el archivo al directorio

```
documentos
```

- Verifica que ambos archivos existan.

---

# Parte 5. Limpieza del proyecto

El investigador te informa que ya no utilizará la carpeta

```
documentos
```

Elimínala junto con su contenido.

Antes de ejecutar el comando verifica tu ubicación utilizando

```bash
pwd
```

---

# Parte 6. Resultado final

La estructura final debe ser similar a:

```
Proyecto_Bioinformatica
│
├── datos
│      muestra.txt
│
├── resultados
│
└── scripts
```

Compruébalo utilizando

```bash
tree
```

---

# Preguntas de reflexión

Responde brevemente.

1. ¿Para qué sirve el comando `pwd`?

2. ¿Cuál es la diferencia entre `cp` y `mv`?

3. ¿Qué diferencia existe entre una ruta absoluta y una ruta relativa?

4. ¿Por qué es importante verificar la ubicación actual antes de utilizar `rm`?

---

# Evidencia de aprendizaje

Sube a Canvas:

- una captura de pantalla donde se observe la estructura final del proyecto;
- las respuestas a las preguntas de reflexión.
