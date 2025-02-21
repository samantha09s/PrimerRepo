# 🖥️ Mi Primer Repositorio con Git

## Fundamentos de Python 2025 - SoftServe Academy

Este repositorio forma parte de mi aprendizaje en **Git y GitHub** dentro del curso **Fundamentos de Python 2025** de SoftServe Academy. Aquí documentaré los comandos utilizados, los desafíos que enfrenté y cómo logré solucionarlos.

---

## 📌 Objetivo

El propósito de esta actividad fue:

- Clonar un repositorio desde GitHub a mi máquina local.
- Modificar un archivo (`Zen.txt`) agregando una línea del **Zen de Python**.
- Resolver problemas cuando Git no detectaba cambios en `Zen.txt`.
- Subir los cambios al repositorio remoto en GitHub.
- Revisar el historial de cambios en Git.

---

## ⚙️ Comandos Git Utilizados

### 1️⃣ Clonar un repositorio desde GitHub
```bash
git clone https://github.com/samantha09s/PrimerRepo.git
```
- **Objetivo:** Descargar el repositorio a mi computadora para poder trabajar con él.

### 2️⃣ Acceder a la carpeta del repositorio
```bash
cd PrimerRepo
```
- **Objetivo:** Moverse dentro del directorio del repositorio clonado.

### 3️⃣ Verificar los archivos en la carpeta del repositorio
```bash
dir
```
- **Objetivo:** Comprobar que `Zen.txt` está presente en el repositorio local.

### 4️⃣ Agregar un archivo al index stage
```bash
git add Zen.txt
```
- **Objetivo:** Mover `Zen.txt` al área de preparación (*staging area*), indicando que está listo para ser *commiteado*.

### 5️⃣ Verificar el estado del repositorio
```bash
git status
```
- **Objetivo:** Comprobar si hay archivos nuevos, modificados o si todo está actualizado.

> [!NOTE]  
> Si `git status` muestra _"nothing to commit, working tree clean"_, significa que no hay cambios pendientes.

### 6️⃣ Guardar los cambios en el repositorio local (commit)
```bash
git commit -m "Añade Zen.txt con la línea del Zen de Python."
```
- **Objetivo:** Guardar el estado actual del archivo con un mensaje descriptivo.

### 7️⃣ Obtener los cambios más recientes del repositorio remoto
```bash
git pull origin main --rebase
```
- **Objetivo:** Descargar y aplicar los cambios más recientes del repositorio en GitHub para evitar conflictos antes de subir nuevos cambios.

### 8️⃣ Subir cambios al repositorio remoto en GitHub
```bash
git push origin main
```
- **Objetivo:** Enviar los cambios confirmados (commit) al repositorio en GitHub.

> [!IMPORTANT] 
> Git pedirá autenticación si es la primera vez que se usa.

### 9️⃣ Ver el historial de commits
```bash
git log --oneline
```
- **Objetivo:** Revisar los cambios registrados en el repositorio de manera resumida.

---

## 🚨 Problema Encontrado: Git no detectaba cambios en `Zen.txt`

### Situación
Cuando intenté hacer `git add Zen.txt`, seguido de `git commit`, Git indicaba que no había cambios en `Zen.txt`, aunque lo había editado.

```bash
nothing to commit, working tree clean
```

### 🔎 Solución aplicada
1. Verificamos si realmente había modificaciones:
   ```bash
   git diff Zen.txt
   ```
   - El comando mostró que **no había diferencias** en el contenido del archivo.

2. Para forzar la detección de cambios, agregamos una nueva línea al archivo:
   ```bash
   "Añade Zen.txt con la línea del Zen de Python." >> Zen.txt
   ```

3. Luego, forzamos la adición del archivo al *staging area*:
   ```bash
   git add Zen.txt --force
   ```

4. Confirmamos los cambios con un commit:
   ```bash
   git commit -m "Forzar cambio en Zen.txt"
   ```

5. Finalmente, subimos el archivo al repositorio remoto:
   ```bash
   git push origin main
   ```

> **Resultado:** `Zen.txt` fue detectado correctamente y los cambios se reflejaron en GitHub.

---

## 📸 Capturas de Pantalla del Proceso

### Clonación del repositorio y verificación de archivos
📌 Se verificó que `Zen.txt` estaba presente en el repositorio local.  
![Clonación del repositorio](https://github.com/user-attachments/assets/e54d90d3-5c37-4c3b-a2a4-11ef2ee4643b)

---

### Intento de agregar cambios sin éxito
📌 Git no detectaba cambios en `Zen.txt`.  
![Error al agregar cambios](https://github.com/user-attachments/assets/7e6fc9d4-46de-453b-abde-3c8744c6a8e0)

---

### Solución aplicada: Forzar la detección de cambios
📌 Se usaron `git add --force` y `git commit` para resolver el problema.  
![Solución aplicada](https://github.com/user-attachments/assets/372ebaef-2bfe-4c7f-bf64-dfc7aa43c473)

---

### Subida del archivo corregido a GitHub
📌 Se verificó que el cambio se reflejaba en el repositorio remoto.  
![Subida a GitHub](https://github.com/user-attachments/assets/66a15a38-14aa-4d8a-96b0-5c28f9191caf)

📌 Confirmación de la actualización en `Zen.txt`.  
![Archivo Zen.txt](https://github.com/user-attachments/assets/a4dba0ba-01ba-4278-9ab8-fc447a0132be)

---

## 🎯 Reflexiones

Este ejercicio fue una excelente introducción a Git y GitHub. Mis principales aprendizajes fueron:

- **Cómo clonar un repositorio** y configurar un entorno local para trabajar con Git.
- **La importancia del staging (`git add`)** antes de confirmar cambios con `git commit`.
- **Cómo manejar errores comunes**, como cuando Git no detecta cambios en un archivo.
- **La estructura del flujo de trabajo en Git** (_working directory_ → _staging area_ → _local repository_ → _remote repository_).
- **Cómo evitar conflictos** usando `git pull --rebase` antes de `git push`.
- **Cómo revisar el historial de cambios** con `git log`.

También aprendí que Git es muy estricto en cuanto a detectar cambios, y que a veces es necesario forzar su reconocimiento cuando el archivo parece sin modificaciones.

Este proyecto me permitió aplicar comandos básicos y solucionar errores de principiante en un entorno real, lo cual me da confianza para seguir aprendiendo y enfrentando desafíos más avanzados.

---

## 🔗 Referencias y Recursos

- 📖 [Documentación oficial de Git](https://git-scm.com/doc)
- 📖 [Guía de Markdown para README](https://www.markdownguide.org/basic-syntax/)

---

### 🚀 ¡Gracias por visitar este repositorio!
Este fue mi primer acercamiento con **Git y GitHub** dentro de mi formación en **SoftServe Academy**.
¡Espero seguir mejorando y documentando mi aprendizaje! Si tienes sugerencias o comentarios, ¡estaré feliz de escucharlos!
