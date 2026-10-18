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

---

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

Prepara el archivo `perfil.md` para ser guardado.

```bash
git commit -m "Crea el perfil en Markdown"
```

Guarda una versión definitiva del proyecto con un mensaje descriptivo.

---

## 3. Revisar Estado y Cambios (`status` / `diff`)

```bash
git status
```

Te dice en qué punto está tu trabajo y qué archivos han cambiado.

```bash
git diff
```

Te muestra línea por línea exactas las modificaciones que aún no has preparado para guardar.

---

## 4. Deshacer Cambios (`restore`)

```bash
git restore --staged perfil.md
```

Saca el archivo del área de preparación sin borrar el trabajo que hiciste en él.

```bash
git restore perfil.md
```

Descarta los cambios no guardados y vuelve el archivo a la última versión registrada.

---

## 5. Eliminar y Mover Archivos (`rm` / `mv`)

```bash
git rm perfil.md
```

Elimina el archivo del disco y avisa a Git para que prepare su borrado.

```bash
git mv perfil.md nuevo_nombre.md
```

Cambia el nombre o la ubicación del archivo guardando el rastro del cambio.

---

## 6. Historial

```bash
git log --oneline
```

Muestra la lista de versiones guardadas de forma resumida en una sola línea por cada una.

```bash
git show
```

Detalla exactamente qué cambió en el último guardado realizado.
