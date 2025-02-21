# 🖥️ Mi Primer Repositorio con Git

## Fundamentos de Python 2025 - SoftServe Academy

Este repositorio forma parte de mi aprendizaje en **Git y GitHub** dentro del curso **Fundamentos de Python 2025** de SoftServe Academy. Aquí documentaré los comandos utilizados, el proceso realizado y los aprendizajes adquiridos mientras trabajaba con mi primer repositorio.

---

## 📌 Objetivo

El propósito de esta actividad fue:

- Clonar un repositorio desde GitHub a mi máquina local.
- Modificar un archivo (`Zen.txt`) agregando una línea del **Zen de Python**.
- Agregar cambios al *index stage* y realizar un *commit*.
- Sincronizar los cambios con el repositorio remoto en GitHub.
- Verificar el historial de cambios en Git.

---

## ⚙️ **Comandos Git Utilizados**

A continuación, se documentan los comandos utilizados y su propósito:

### 1️⃣ **Clonar un repositorio desde GitHub**
```
git clone https://github.com/samantha09s/PrimerRepo.git
```
- **Objetivo:** Descargar el repositorio a mi computadora para poder trabajar con él.

### 2️⃣ **Acceder a la carpeta del repositorio**
```
cd PrimerRepo
```
- **Objetivo:** Moverse dentro del directorio del repositorio clonado.

### 3️⃣ **Verificar los archivos en la carpeta del repositorio**
```
dir
```
- **Objetivo:** Comprobar que `Zen.txt` está presente en el repositorio local.

### 4️⃣ **Agregar un archivo al index stage**
```
git add Zen.txt
```
- **Objetivo:** Mover `Zen.txt` al área de preparación (*index stage*), indicando que está listo para ser *commiteado*.

### 5️⃣ **Verificar el estado del repositorio**
```
git status
```
- **Objetivo:** Comprobar si hay archivos nuevos, modificados o si todo está actualizado.

> [!NOTE]
> Si `git status` muestra _"nothing to commit, working tree clean"_, significa que no hay cambios pendientes.

### 6️⃣ **Guardar los cambios en el repositorio local (commit)**
```
git commit -m "Añade Zen.txt con la línea del Zen de Python."
```
- **Objetivo:** Guardar el estado actual del archivo con un mensaje descriptivo.

### 7️⃣ **Obtener los cambios más recientes del repositorio remoto**
```
git pull origin main --rebase
```
- **Objetivo:** Descargar y aplicar los cambios más recientes del repositorio en GitHub para evitar conflictos antes de subir nuevos cambios.

### 8️⃣ **Subir cambios al repositorio remoto en GitHub**
```
git push origin main
```
- **Objetivo:** Enviar los cambios confirmados (`commit`) al repositorio en GitHub.

> [!IMPORTANT]
> Git pedirá autenticación si es la primera vez que se usa.

### 9️⃣ **Ver el historial de commits**
```
git log --oneline
```
- **Objetivo:** Revisar los cambios registrados en el repositorio de manera resumida.  

---

## 📸 Capturas de Pantalla

Aquí se incluyen capturas del proceso en la terminal:

1. 📌 **Clonación del repositorio y verificación de archivos**  
   ![image](https://github.com/user-attachments/assets/e54d90d3-5c37-4c3b-a2a4-11ef2ee4643b)

2. 📌 **Edición y agregado de `Zen.txt`**  
   ![image](https://github.com/user-attachments/assets/4bcab76e-8b99-429c-9315-a7b9e37fb506)

3. 📌 **Commit y sincronización con GitHub**
   ![image](https://github.com/user-attachments/assets/feb53248-877d-477b-af4e-8a28f6849421)

---

## 🎯 **Reflexiones**

Durante este ejercicio, aprendí lo siguiente:

- **Cómo clonar un repositorio desde GitHub** y trabajar con él en mi máquina local.
- **La importancia del index stage** (`git add`) y cómo preparar archivos para un commit.
- **La estructura de trabajo en Git** (_working directory_ → _staging area_ → _local repository_ → _remote repository_).
- **Cómo evitar conflictos usando `git pull --rebase`** antes de hacer un `git push`.
- **Cómo revisar el historial de cambios** con `git log`.

Este proyecto me permitió comprender el flujo de trabajo básico en Git y GitHub, sentando las bases para proyectos más avanzados.

---

## 🔗 Referencias y Recursos

- 📖 [Documentación oficial de Git](https://git-scm.com/doc)
- 📖 [Guía de Markdown para README](https://www.markdownguide.org/basic-syntax/)

---

### 🚀 **Gracias por visitar este repositorio!**
Este fue mi primer acercamiento con **Git y GitHub** dentro de mi formación en **SoftServe Academy**. ¡Espero seguir mejorando y documentando mi aprendizaje! Si tienes sugerencias o comentarios, ¡estaré feliz de escucharlos!
