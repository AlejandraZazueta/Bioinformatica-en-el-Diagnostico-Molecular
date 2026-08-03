# Clase 1.2: Introducción a la línea de comandos Unix

## Propósito de la clase

Aprender a interactuar con un sistema Linux mediante la terminal y utilizar comandos básicos para navegar por directorios y manipular archivos.

---

## Resultados de aprendizaje

Al finalizar esta clase, el estudiante será capaz de:

- reconocer los componentes básicos de una terminal;
- identificar la diferencia entre una ruta absoluta y una ruta relativa;
- navegar por el sistema de archivos;
- crear directorios;
- copiar, mover, renombrar y eliminar archivos;
- descargar archivos desde internet;
- utilizar la ayuda disponible para consultar comandos.

---

## Contenidos

### Conceptos fundamentales

- Linux
- Unix
- terminal
- shell
- comandos
- opciones
- argumentos
- rutas
- directorios
- archivos

### Comandos de la clase

| Comando | Función |
|---|---|
| `pwd` | Mostrar el directorio actual |
| `ls` | Listar archivos y directorios |
| `cd` | Cambiar de directorio |
| `mkdir` | Crear directorios |
| `cp` | Copiar archivos o directorios |
| `mv` | Mover o renombrar archivos |
| `rm` | Eliminar archivos o directorios |
| `curl` | Descargar archivos desde internet |
| `wget` | Descargar archivos desde internet |
| `man` | Consultar el manual de un comando |

---

## Reglas de seguridad

Antes de ejecutar un comando:

1. confirma en qué directorio estás utilizando `pwd`;
2. revisa los archivos disponibles utilizando `ls`;
3. lee cuidadosamente las rutas;
4. evita utilizar `rm -r` si no comprendes qué carpeta eliminará;
5. recuerda que los archivos eliminados desde la terminal pueden no pasar por la papelera.

---

## Ejercicio final

Al terminar la práctica deberás ser capaz de construir esta estructura:

```text
ejercicios/
└── leccion_1/
    └── bioinformatica.txt
```

Para lograrlo deberás emplear comandos de navegación, creación de directorios, descarga, cambio de nombre, copia y eliminación.

---
