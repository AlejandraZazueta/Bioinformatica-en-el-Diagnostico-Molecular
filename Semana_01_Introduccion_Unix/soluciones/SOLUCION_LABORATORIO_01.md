# Solución | Laboratorio 1
## Primeros pasos en Linux utilizando GitHub Codespaces

Esta pauta presenta una posible forma de resolver el Laboratorio 1.

> En algunos ejercicios pueden existir diferentes comandos o rutas que conduzcan al mismo resultado.

---

# Parte 1 | Conociendo el entorno

## 1. ¿Dónde estoy?

### Comando

```bash
pwd
```

### ¿Qué información entrega este comando?

`pwd` significa **print working directory** y muestra la ruta del directorio en el que estamos trabajando actualmente.

En GitHub Codespaces, al iniciar el entorno, el resultado puede ser similar a:

```text
/workspaces/Bioinformatica-en-el-Diagnostico-Molecular
```

La ruta exacta puede variar dependiendo del repositorio y del entorno de trabajo.

---

## 2. ¿Qué contiene mi directorio?

### Comando

```bash
ls
```

`ls` muestra los archivos y directorios presentes en la ubicación actual.

Ahora ejecutamos:

```bash
ls -lh
```

### ¿Cuál es la diferencia?

`ls` muestra los nombres de los archivos y directorios.

`ls -lh` muestra información adicional, como:

- permisos;
- propietario;
- tamaño;
- fecha de modificación;
- nombre del archivo o directorio.

La opción `-h` presenta los tamaños en un formato más fácil de interpretar, por ejemplo:

```text
1.2K
5.4M
2.1G
```

en lugar de mostrar únicamente el número de bytes.

---

## 3. Explorar el repositorio

Primero podemos observar el contenido:

```bash
ls
```

Luego ingresamos a la carpeta de la Semana 1:

```bash
cd Semana_01_Introduccion_Unix
```

Comprobamos nuestra ubicación:

```bash
pwd
```

Podemos volver al directorio anterior utilizando:

```bash
cd ..
```

---

# Parte 2 | Organización de un proyecto

Debíamos construir:

```text
Proyecto_Bioinformatica
│
├── datos
├── resultados
├── scripts
└── documentos
```

Primero creamos el directorio principal:

```bash
mkdir Proyecto_Bioinformatica
```

Ingresamos:

```bash
cd Proyecto_Bioinformatica
```

Creamos las cuatro carpetas:

```bash
mkdir datos resultados scripts documentos
```

Comprobamos:

```bash
ls
```

Resultado esperado:

```text
datos
documentos
resultados
scripts
```

También podemos comprobar la estructura utilizando:

```bash
tree
```

Resultado:

```text
Proyecto_Bioinformatica
├── datos
├── documentos
├── resultados
└── scripts
```

> Si `tree` no está disponible, `ls` permite comprobar los directorios creados.

---

# Parte 3 | Descargar un archivo

Primero ingresamos a:

```bash
cd datos
```

Comprobamos nuestra ubicación:

```bash
pwd
```

## Opción A | Utilizando wget

```bash
wget https://raw.githubusercontent.com/AlejandraZazueta/Bioinformatica-en-el-Diagnostico-Molecular/refs/heads/main/Semana_01_Introduccion_Unix/Datos/bienvenida_bioinformatica.txt
```

## Opción B | Utilizando curl

```bash
curl -O https://raw.githubusercontent.com/AlejandraZazueta/Bioinformatica-en-el-Diagnostico-Molecular/refs/heads/main/Semana_01_Introduccion_Unix/Datos/bienvenida_bioinformatica.txt
```

No es necesario utilizar ambos comandos. Cualquiera de las dos alternativas permite realizar la actividad.

Comprobamos:

```bash
ls -lh
```

Debería aparecer:

```text
bienvenida_bioinformatica.txt
```

---

# Parte 4 | Organización de archivos

## 1. Cambiar el nombre

El archivo:

```text
bienvenida_bioinformatica.txt
```

debe llamarse:

```text
muestra.txt
```

Utilizamos:

```bash
mv bienvenida_bioinformatica.txt muestra.txt
```

Comprobamos:

```bash
ls
```

---

## 2. Copiar el archivo a `documentos`

Actualmente estamos dentro de:

```text
Proyecto_Bioinformatica/datos
```

La carpeta `documentos` se encuentra un nivel arriba.

Podemos copiar el archivo utilizando una ruta relativa:

```bash
cp muestra.txt ../documentos/
```

---

## 3. Verificar los archivos

Comprobamos que el original continúa en `datos`:

```bash
ls
```

Deberíamos encontrar:

```text
muestra.txt
```

Comprobamos la copia:

```bash
ls ../documentos
```

También debería aparecer:

```text
muestra.txt
```

Por lo tanto, existen dos copias:

```text
Proyecto_Bioinformatica
│
├── datos
│   └── muestra.txt
│
└── documentos
    └── muestra.txt
```

---

# Parte 5 | Limpieza del proyecto

Debemos eliminar:

```text
documentos
```

junto con su contenido.

Primero comprobamos nuestra ubicación:

```bash
pwd
```

Si estamos dentro de `datos`, regresamos al directorio principal del proyecto:

```bash
cd ..
```

Comprobamos nuevamente:

```bash
pwd
```

Ahora podemos eliminar el directorio y su contenido:

```bash
rm -r documentos
```

Comprobamos:

```bash
ls
```

La carpeta `documentos` ya no debería aparecer.

> ⚠️ `rm` elimina archivos y `rm -r` puede eliminar directorios completos junto con su contenido. Por eso es importante comprobar la ubicación antes de ejecutarlo.

---

# Parte 6 | Resultado final

Ejecutamos:

```bash
tree
```

La estructura final debería ser:

```text
Proyecto_Bioinformatica
├── datos
│   └── muestra.txt
├── resultados
└── scripts
```

---

# Preguntas de reflexión

## 1. ¿Para qué sirve el comando `pwd`?

`pwd` muestra la ruta completa del directorio de trabajo actual.

Permite saber exactamente en qué ubicación del sistema de archivos nos encontramos.

---

## 2. ¿Cuál es la diferencia entre `cp` y `mv`?

`cp` **copia** un archivo o directorio.

Por ejemplo:

```bash
cp muestra.txt ../documentos/
```

El archivo original permanece en su ubicación.

En cambio, `mv` permite **mover** un archivo a otra ubicación o **cambiar su nombre**.

Por ejemplo:

```bash
mv bienvenida_bioinformatica.txt muestra.txt
```

cambia el nombre del archivo.

---

## 3. ¿Qué diferencia existe entre una ruta absoluta y una ruta relativa?

Una **ruta absoluta** indica la ubicación completa de un archivo o directorio desde la raíz del sistema.

Por ejemplo:

```text
/workspaces/Bioinformatica-en-el-Diagnostico-Molecular/Semana_01_Introduccion_Unix
```

Una **ruta relativa** indica una ubicación tomando como referencia el directorio en el que estamos actualmente.

Por ejemplo:

```text
../documentos/
```

En este caso, `..` representa el directorio inmediatamente superior.

---

## 4. ¿Por qué es importante verificar la ubicación actual antes de utilizar `rm`?

Porque `rm` elimina archivos y, cuando se utiliza con opciones como `-r`, puede eliminar directorios completos y su contenido.

Comprobar previamente:

```bash
pwd
```

y:

```bash
ls
```

reduce el riesgo de eliminar información desde una ubicación incorrecta.

---

# Resumen de comandos utilizados

| Comando | Función |
|---|---|
| `pwd` | Mostrar el directorio actual |
| `ls` | Listar archivos y directorios |
| `ls -lh` | Listar archivos mostrando información adicional y tamaños legibles |
| `cd` | Cambiar de directorio |
| `cd ..` | Ir al directorio superior |
| `mkdir` | Crear directorios |
| `wget` | Descargar archivos |
| `curl` | Transferir/descargar contenido |
| `mv` | Mover o cambiar el nombre de un archivo |
| `cp` | Copiar archivos |
| `rm -r` | Eliminar un directorio y su contenido |
| `tree` | Visualizar la estructura de directorios |

---

## Flujo realizado en el laboratorio

```text
Navegar por Linux
       ↓
Crear un proyecto
       ↓
Organizar directorios
       ↓
Descargar un archivo
       ↓
Renombrar y copiar
       ↓
Verificar las rutas
       ↓
Eliminar archivos/directorios
       ↓
Comprobar estructura final
```

Estos comandos constituyen la base para comenzar a trabajar con archivos de datos mediante Unix.
