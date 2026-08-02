# Comandos básicos de Unix

Esta hoja resume los comandos utilizados durante la primera práctica.

## Navegación

### `pwd`

Muestra la ruta del directorio de trabajo actual.

```bash
pwd
```

### `ls`

Lista los archivos y directorios.

```bash
ls
```

Listado detallado:

```bash
ls -l
```

Listado detallado con tamaños legibles:

```bash
ls -lh
```

### `cd`

Permite cambiar de directorio.

```bash
cd nombre_directorio
```

Subir un nivel:

```bash
cd ..
```

Regresar al directorio personal:

```bash
cd ~
```

---

## Creación de directorios

### `mkdir`

Crear un directorio:

```bash
mkdir resultados
```

Crear varios directorios:

```bash
mkdir datos scripts resultados
```

Crear directorios anidados:

```bash
mkdir -p proyecto/datos/crudos
```

---

## Manipulación de archivos

### `cp`

Copiar un archivo:

```bash
cp archivo_original.txt copia.txt
```

Copiar un archivo a otro directorio:

```bash
cp archivo.txt resultados/
```

### `mv`

Mover un archivo:

```bash
mv archivo.txt resultados/
```

Renombrar un archivo:

```bash
mv archivo.txt nuevo_nombre.txt
```

### `rm`

Eliminar un archivo:

```bash
rm archivo.txt
```

Eliminar un directorio y su contenido:

```bash
rm -r nombre_directorio
```

> ⚠️ Utiliza `rm -r` con precaución.

---

## Descarga de archivos

### `wget`

```bash
wget URL
```

### `curl`

```bash
curl URL -O
```

---

## Obtener ayuda

```bash
comando --help
```

```bash
man comando
```

Ejemplo:

```bash
man ls
```

---

## Estructura general de un comando

```text
comando [opciones] [argumentos]
```

Ejemplo:

```bash
ls -lh datos
```

Donde:

- `ls` es el comando;
- `-lh` contiene las opciones;
- `datos` es el argumento.
