
# Semana 1: Introducción a Unix y GitHub Codespaces

## Objetivos de aprendizaje

Al finalizar esta semana serás capaz de:

- Comprender qué es Unix y por qué se utiliza en bioinformática.
- Acceder a un entorno Linux mediante GitHub Codespaces.
- Navegar entre directorios utilizando la terminal.
- Crear, copiar, mover y eliminar archivos y carpetas.
- Reconocer la estructura básica de un proyecto bioinformático.

---

# Antes de la clase

Antes de asistir al laboratorio debes:

- Crear una cuenta en GitHub.
- Ingresar al repositorio del curso.
- Leer esta guía.
- Tener acceso a Canvas.

---

# Actividad 1: Abrir GitHub Codespaces

1. Ingresa al repositorio del curso.
2. Haz clic en **Code**.
3. Selecciona la pestaña **Codespaces**.
4. Haz clic en **Create codespace on main**.
5. Espera unos minutos mientras se prepara el entorno.

Cuando finalice la carga, verás una ventana similar a Visual Studio Code con una terminal Linux.

---

# Actividad 2: Conociendo la terminal

Ejecuta los siguientes comandos uno por uno.

## ¿Dónde estoy?

```bash
pwd
```

---

## ¿Qué archivos existen?

```bash
ls
```

---

## Crear una carpeta

```bash
mkdir Proyecto_Bioinformatica
```

---

## Entrar a la carpeta

```bash
cd Proyecto_Bioinformatica
```

---

## Crear un archivo

```bash
touch notas.txt
```

---

## Ver el contenido de la carpeta

```bash
ls
```

---

## Volver al directorio anterior

```bash
cd ..
```

---

# Desafío

Crea la siguiente estructura utilizando únicamente la terminal.

```
Proyecto_Bioinformatica/

├── datos/

├── resultados/

└── scripts/
```

---

# Entrega

Al finalizar la actividad deberás mostrar la estructura creada al docente utilizando el comando:

```bash
ls
```

---

# Material complementario

Durante la próxima clase aprenderemos a visualizar y manipular archivos de texto utilizando comandos de Unix.
