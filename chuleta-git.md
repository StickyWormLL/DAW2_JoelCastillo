# Guía Básica de Git

## 1. Instalar y Configurar

* **Windows:** Descarga desde [git-scm.com](https://git-scm.com).
* **macOS:** Ejecuta `git --version` en la terminal e instala las herramientas si las pide.
* **Ubuntu/Debian:** Instala ejecutando `sudo apt install git`.

```bash
git --version
```

Comprueba si Git está instalado correctamente en tu equipo.

```bash
git config --global user.name "Tu Nombre"
```

Guarda tu nombre para identificar quién hace los cambios.

```bash
git config --global user.email "tu@email.com"
```

Guarda tu correo electrónico asociado a los cambios.

## 2. Iniciar y Guardar Cambios

* **Carpeta de trabajo:** Donde creas o modificas tus archivos.
* **Staging:** El área donde preparas los archivos antes de guardarlos.
* **Repositorio:** El historial donde se guardan las versiones de tu proyecto.

```bash
cd ruta/de/la/carpeta
```

Entra en la carpeta de tu proyecto.

```bash
git init
```

Inicializa Git dentro de la carpeta actual.

```bash
git add perfil.md
```

Prepara el archivo `perfil.md` para ser guardado en el próximo commit.

```bash
git commit -m "Crea el perfil en Markdown"
```

Guarda una versión definitiva del proyecto con un mensaje explicativo.

## 3. Revisar Estado y Cambios

```bash
git status
```

Muestra qué archivos han cambiado y en qué rama te encuentras.

```bash
git diff
```

Muestra las diferencias exactas línea por línea que aún no están preparadas.

## 4. Deshacer Cambios

```bash
git restore --staged perfil.md
```

Saca el archivo del área de preparación sin perder tus modificaciones.

```bash
git restore perfil.md
```

Descarta los cambios locales y vuelve el archivo a la última versión guardada.

## 5. Eliminar y Mover Archivos

```bash
git rm perfil.md
```

Borra el archivo del disco y prepara su eliminación en Git.

```bash
git mv perfil.md nuevo_nombre.md
```

Renombra o mueve un archivo manteniendo el seguimiento de su historial.

## 6. Trabajar con Ramas (`branches`)

```bash
git branch
```

Muestra la lista de ramas creadas y marca con un asterisco en la que estás situado.

```bash
git branch rama-nueva
```

Crea una nueva rama de trabajo a partir de la actual sin cambiarte a ella.

```bash
git branch -M main
```

Cambia el nombre de la rama actual a `main`.

```bash
git switch -c rama-nueva
```

Crea una nueva rama y se cambia a ella en un solo paso.

```bash
git switch master
```

Cambia a la rama especificada (por ejemplo, a la principal `master`).

```bash
git checkout rama-nueva
```

Comando clásico para cambiarte de rama (equivalente a `git switch`).

```bash
git checkout -
```

Vuelve a la última rama en la que estuviste antes.

```bash
git branch -d rama-feature
```

Elimina una rama de forma segura, solo si sus cambios ya han sido fusionados.

```bash
git branch -D rama-feature
```

Fuerza la eliminación de una rama aunque contenga cambios no fusionados.

## 7. Fusionar Cambios (`merge`)

```bash
git merge rama-feature
```

Incorpora en la rama actual los cambios guardados en la rama indicando su nombre.

## 8. Repositorios Remotos (GitHub)

```bash
git remote add origin URL_DEL_REPOSITORIO
```

Conecta tu repositorio local con la dirección del repositorio remoto en GitHub.

```bash
git remote -v
```

Muestra la lista de repositorios remotos vinculados y sus direcciones URL.

```bash
git push -u origin main
```

Envía los commits locales a la rama `main` remota y establece el enlace de seguimiento.

## 9. Ver el Historial

```bash
git log --oneline
```

Muestra la lista de commits de forma resumida en una sola línea.

```bash
git show
```

Detalla los cambios exactos guardados en el último commit realizado.

```bash
git log --oneline --graph --all
```

Muestra un gráfico visual sencillo del historial con todas las ramas y fusiones.

```bash
git log rama1 rama2 archivo.md
```

Compara el historial de commits entre dos ramas enfocado en un archivo específico.
