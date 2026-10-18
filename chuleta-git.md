# Guía Básica de Git

## Instalar y Configurar

* **Windows:** Descarga desde [git-scm.com](https://git-scm.com).
* **macOS:** Ejecuta `git --version` en la terminal e instala las herramientas si te las pide.
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

---

## Iniciar y Guardar Cambios

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
git status
```

Muestra qué archivos se han creado, modificado o preparado.

```bash
git add perfil.md
```

Prepara el archivo `perfil.md` para ser guardado.

```bash
git commit -m "Crea el perfil en Markdown"
```

Guarda una versión definitiva del proyecto con un mensaje descriptivo.

---

## Ver Cambios e Historial

```bash
git diff
```

Enseña las líneas concretas que has cambiado pero aún no has preparado.

```bash
git log --oneline
```

Muestra la lista de versiones guardadas en una sola línea por cada una.

```bash
git show
