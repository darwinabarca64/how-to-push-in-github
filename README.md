<img src="https://git-scm.com//images/logos/downloads/Git-Logo-2Color.png" width="150">

# GUIA BÁSICA DE GIT Y GITHUB 
*HECHO POR DARWIN_ABARCA*

Esta guía ha sido creada para ayudar a los nuevos alumnos de Oscar a entender el flujo de trabajo esencial con el control de versiones.

## 2. INTRODUCCIÓN.

*   **¿Qué es Git?**: Es un sistema de control de versiones distribuido. Sirve para llevar un registro de los cambios en los archivos de un proyecto y permitir que varias personas trabajen juntas.

*   **¿Qué es GitHub?**: Es una plataforma en la nube que aloja repositorios de Git. Permite guardar tus proyectos de forma remota y colaborar con otros desarrolladores.

## 3. COMANDOS BÁSICOS DE GIT.

Son los comandos que más usarás en tu día a día:

```bash
# Inicializar un nuevo repositorio local
git init

# Mostrar el estado de los archivos
git status

# Añadir todos los cambios al área de preparación
git add .

# Guardar los cambios con un mensaje descriptivo
git commit -m "mensaje"

# Conectar el repositorio local con uno remoto
git remote add origin URL

# Subir los cambios locales a GitHub
git push -u origin main
```

## 3.1. Comandos adicionales de Git.

Para llevar el manejo de Git a otro nivel, estos son los comandos que usarás en proyectos colaborativos reales:

### Gestión de Ramas (Branches)
Las ramas permiten trabajar en nuevas funciones sin romper el código principal.

```bash
# Listar todas las ramas del proyecto
git branch

# Crear una nueva rama
git branch nombre

# Cambiar a la rama indicada
git checkout nombre

# Crear una rama y moverse a ella en un solo paso
git checkout -b nombre

# Fusionar la rama indicada con la actual
git merge nombre
```

### Inspección y Comparación
Para entender qué ha pasado en el historial del proyecto.

```bash
# Historial de cambios resumido y limpio
git log --oneline

# Comparar cambios realizados antes del add
git diff

# Ver quién escribió cada línea de un archivo
git blame archivo
```

### Deshacer y Corregir
Comandos útiles para cuando algo sale mal.

```bash
# Modificar el último commit (mensaje o archivos)
git commit --amend

# Deshacer cambios locales en un archivo
git restore archivo

# Borrar el último commit y sus cambios permanentemente
git reset --hard HEAD~1
```

### Utilidades Profesionales

```bash
# Guardar cambios temporalmente sin hacer commit
git stash

# Recuperar los cambios guardados en el stash
git stash pop

# Listar las conexiones con repositorios remotos
git remote -v
```

## 4. FLUJO DE TRABAJO.

Para trabajar correctamente, sigue estos pasos:

1.  **Crear repositorio**: Inicia tu proyecto con `git init`.
2.  **Añadir archivos**: Usa `git add .` para preparar los archivos que quieras guardar.
3.  **Hacer commit**: Registra los cambios con un mensaje claro usando `git commit`.
4.  **Subir a GitHub**: Envía tus commits al servidor remoto con `git push`.

## 5. EJEMPLO PRACTICO.

Ejemplo de cómo se vería una secuencia de comandos en la terminal:

```bash
# 1. Configuración inicial del proyecto
mkdir mi-proyecto
cd mi-proyecto
git init

# 2. Creación de contenido y guardado local
git add .
git commit -m "Primer commit: Estructura inicial"

# 3. Conexión y subida al repositorio remoto
git remote add origin https://github.com/(adiciona_tu_link)
git branch -M main
git push -u origin main
```

## Comandos Extra.

*   `git clone [URL]`: Descarga una copia exacta de un repositorio remoto a tu ordenador.
*   `git pull`: Trae los cambios más recientes desde GitHub a tu equipo local.

## Errores Comunes.

*   **Olvidar el `git add .`**: Si no añades los archivos antes del commit, estos no se guardarán.
*   **Mensajes de commit poco claros**: Evita usar "cambios" o "fix", sé descriptivo.
*   **Trabajar en la rama incorrecta**: Asegúrate de estar en `main` o en la rama de trabajo asignada.

## bonus.

Podemos subir el archivo de imagenes mediante enlace

## 5. CLONAR REPOSITORIO.

En la terminal:

```bash
git clone https://github.com...
cd how-to-push-in-github
```

## 6. Actualizar tu repositorio cuando has hecho cambios locales y, al mismo tiempo, el repositorio remoto .

```bash
git add .
git commit -m "Mis cambios locales"

git pull origin main --rebase

git push origin main
```
¿Qué pasa si hay un conflicto?Si modificaste la misma línea de un archivo que también se cambió en GitHub, el proceso se detendrá. Deberás abrir el archivo, elegir qué código dejar, guardar y luego ejecutar

```bash
git add .
git rebase --continue
```

## 6. Para un nuevo archivo en blanco.

```bash
git init
git remote add origin https://github.com
git branch -M main
git pull origin main
git add .
git commit -m "Initial commit"
git push -u origin main
```
---

*FIN_PARTE_1_SALU2/PARTE 2 CREARÉ LAS CARPETAS PARA SUBIR ESTE ARCHICO A GITHUB*