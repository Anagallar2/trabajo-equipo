---
title: Zsh
created: '2025-06-25T07:55:42.650Z'
modified: '2025-06-25T08:31:59.171Z'
---

# Zsh
Aquí tienes una **tabla con comandos útiles de Zsh**, clasificados por categoría, para ayudarte a dominar este shell:

---

### 🧭 **Navegación**

| Comando Zsh              | Descripción                                  |
| ------------------------ | -------------------------------------------- |
| `cd`                     | Cambiar de directorio                        |
| `cd -`                   | Ir al directorio anterior                    |
| `cd ~` o simplemente `~` | Ir al directorio home                        |
| `pushd [dir]`            | Añade un directorio al stack y se mueve a él |
| `popd`                   | Vuelve al último directorio del stack        |

---

### 🔍 **Autocompletado y corrección**

| Comando Zsh      | Descripción                                     |
| ---------------- | ----------------------------------------------- |
| `ls <TAB>`       | Autocompleta archivos/directorios               |
| `setopt correct` | Activa corrección de errores de tipeo           |
| `setopt autocd`  | Permite cambiar de directorio sin escribir `cd` |

---

### 🔁 **Alias y funciones**

| Comando Zsh                         | Descripción      |
| ----------------------------------- | ---------------- |
| `alias ll='ls -lah'`                | Crea un alias    |
| `unalias ll`                        | Elimina un alias |
| `function saludar() { echo Hola; }` | Crea una función |

---

### 🔧 **Variables y configuración**

| Comando Zsh        | Descripción                          |
| ------------------ | ------------------------------------ |
| `export VAR=valor` | Define una variable de entorno       |
| `echo $VAR`        | Muestra el valor de una variable     |
| `printenv`         | Lista todas las variables de entorno |
| `source ~/.zshrc`  | Recarga la configuración             |

---

### 🔎 **Búsqueda y historial**

| Comando Zsh  | Descripción                                         |
| ------------ | --------------------------------------------------- |
| `history`    | Muestra historial de comandos                       |
| `!n`         | Ejecuta el comando número `n` del historial         |
| `!palabra`   | Ejecuta el último comando que empieza con “palabra” |
| `<Ctrl> + R` | Buscar comandos anteriores interactivamente         |

---

### 🌈 **Estética y personalización**

| Comando Zsh                             | Descripción                  |
| --------------------------------------- | ---------------------------- |
| `autoload -Uz promptinit && promptinit` | Inicia el sistema de temas   |
| `prompt -p`                             | Lista temas disponibles      |
| `PROMPT='%n@%m %~ %# '`                 | Define el prompt manualmente |

---

### ⚡ **Plugins y frameworks**

| Comando Zsh                               | Descripción                          |
| ----------------------------------------- | ------------------------------------ |
| `oh-my-zsh`                               | Framework de configuración y plugins |
| `zinit`, `antigen`, `zplug`, `zsh4humans` | Gestores de plugins para Zsh         |

---

### 💥 **Ejecutar scripts**

| Comando Zsh                          | Descripción                           |
| ------------------------------------ | ------------------------------------- |
| `zsh script.zsh`                     | Ejecuta un script en Zsh              |
| `#!/bin/zsh` (al inicio del archivo) | Shebang para usar Zsh como intérprete |
| `chmod +x script.zsh`                | Da permisos de ejecución al script    |



