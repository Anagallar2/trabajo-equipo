---
title: 'Comparativa de Comandos de Terminal (Windows, Linux, macOS)'
created: '2025-06-25T08:04:41.686Z'
modified: '2025-06-25T08:04:48.317Z'
---

# Comparativa de Comandos de Terminal (Windows, Linux, macOS)

Este documento compara comandos comunes utilizados en las terminales de Windows (Símbolo del sistema/CMD y PowerShell), Linux (Bash) y macOS (Bash/Zsh).

---

## I. Navegación y Gestión de Archivos y Directorios

| Propósito                  | Windows (CMD)      | Windows (PowerShell) | Linux (Bash)      | macOS (Bash/Zsh)   | Explicación                                                  |
| :------------------------- | :----------------- | :------------------- | :---------------- | :----------------- | :----------------------------------------------------------- |
| **Listar contenido** | `dir`              | `Get-ChildItem` (gci, dir, ls) | `ls`              | `ls`               | Muestra los archivos y directorios en el directorio actual. |
| **Cambiar directorio** | `cd`               | `Set-Location` (cd, chdir, sl) | `cd`              | `cd`               | Navega a un directorio diferente.                            |
| **Directorio actual** | `cd`               | `Get-Location` (pwd, gl) | `pwd`             | `pwd`              | Muestra la ruta del directorio de trabajo actual.            |
| **Crear directorio** | `mkdir`            | `New-Item -ItemType Directory` (ni) | `mkdir`           | `mkdir`            | Crea un nuevo directorio.                                    |
| **Eliminar directorio (vacío)** | `rmdir`         | `Remove-Item -Recurse` (rmdir) | `rmdir`           | `rmdir`            | Elimina un directorio vacío.                                 |
| **Eliminar directorio (no vacío)** | `rmdir /s`     | `Remove-Item -Recurse` (rm -r) | `rm -r`           | `rm -r`            | Elimina un directorio y su contenido de forma recursiva.     |
| **Copiar archivos** | `copy`             | `Copy-Item` (cp, copy, cpi) | `cp`              | `cp`               | Copia archivos de un lugar a otro.                           |
| **Mover/Renombrar archivos** | `move`            | `Move-Item` (mv, move, mi) | `mv`              | `mv`               | Mueve o renombra archivos y directorios.                     |
| **Eliminar archivos** | `del` / `erase`    | `Remove-Item` (rm, del, erase, ri) | `rm`              | `rm`               | Elimina uno o más archivos.                                  |
| **Crear archivo vacío** | `type nul > archivo.txt` | `New-Item -ItemType File` | `touch`           | `touch`            | Crea un archivo vacío o actualiza su fecha de modificación.  |

---

## II. Visualización y Edición de Archivos

| Propósito                  | Windows (CMD)      | Windows (PowerShell) | Linux (Bash)      | macOS (Bash/Zsh)   | Explicación                                                  |
| :------------------------- | :----------------- | :------------------- | :---------------- | :----------------- | :----------------------------------------------------------- |
| **Mostrar contenido** | `type`             | `Get-Content` (cat, type, gc) | `cat`             | `cat`              | Muestra el contenido de un archivo en la consola.            |
| **Ver contenido paginado** | `more`             | `Get-Content | More` | `less` / `more`   | `less` / `more`    | Muestra el contenido de un archivo página por página.        |
| **Ver inicio de archivo** | N/A                | `Get-Content -Head N` | `head -n N`       | `head -n N`        | Muestra las primeras N líneas de un archivo.                 |
| **Ver final de archivo** | N/A                | `Get-Content -Tail N` | `tail -n N`       | `tail -n N`        | Muestra las últimas N líneas de un archivo.                  |
| **Seguir archivo (logs)** | N/A                | `Get-Content -Wait`  | `tail -f`         | `tail -f`          | Muestra las últimas líneas y sigue añadiendo nuevas (útil para logs). |
| **Editor de texto** | `edit` (en versiones antiguas) | `notepad` (abre en GUI) / Integración con VS Code/otros editores CLI | `nano` / `vim` / `emacs` | `nano` / `vim` / `emacs` | Abre un editor de texto en la terminal o una interfaz gráfica. |

---

## III. Búsqueda y Filtrado

| Propósito                  | Windows (CMD)      | Windows (PowerShell) | Linux (Bash)      | macOS (Bash/Zsh)   | Explicación                                                  |
| :------------------------- | :----------------- | :------------------- | :---------------- | :----------------- | :----------------------------------------------------------- |
| **Buscar texto en archivos** | `findstr`          | `Select-String` (sls) | `grep`            | `grep`             | Busca patrones de texto dentro de archivos.                  |
| **Buscar archivos** | `dir /s` / `where` | `Get-ChildItem -Recurse` | `find`            | `find`             | Busca archivos y directorios en una jerarquía.               |
| **Comparar archivos** | `fc`               | `Compare-Object` (compare, diff) | `diff`            | `diff`             | Muestra las diferencias entre dos archivos.                  |
| **Contar líneas/palabras** | N/A                | `Get-Content | Measure-Object -Line -Word -Character` | `wc`              | `wc`               | Cuenta líneas, palabras y/o caracteres en un archivo.        |

---

## IV. Gestión de Procesos

| Propósito                  | Windows (CMD)      | Windows (PowerShell) | Linux (Bash)      | macOS (Bash/Zsh)   | Explicación                                                  |
| :------------------------- | :----------------- | :------------------- | :---------------- | :----------------- | :----------------------------------------------------------- |
| **Listar procesos** | `tasklist`         | `Get-Process` (gps, ps) | `ps` / `top` / `htop` | `ps` / `top` / `htop` | Muestra los procesos en ejecución.                            |
| **Terminar un proceso** | `taskkill`         | `Stop-Process` (spps, kill) | `kill`            | `kill`             |
