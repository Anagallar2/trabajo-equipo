---
title: "\U0001F4CB Listado de Comandos CMD (Símbolo del sistema de Windows)"
created: '2025-06-25T07:55:17.431Z'
modified: '2025-06-25T08:00:52.135Z'
---

# 📋 Listado de Comandos CMD (Símbolo del sistema de Windows)

## 🔧 Comandos Básicos del Sistema
| Comando     | Descripción                                            |
|-------------|--------------------------------------------------------|
| `help`      | Muestra ayuda de comandos disponibles.                |
| `cls`       | Limpia la pantalla.                                   |
| `exit`      | Cierra la ventana del símbolo del sistema.            |
| `echo`      | Muestra mensajes o activa/desactiva el eco de comandos. |
| `ver`       | Muestra la versión del sistema operativo.             |
| `hostname`  | Muestra el nombre del equipo.                         |
| `systeminfo`| Muestra información detallada del sistema.            |

## 📁 Comandos de Directorios y Archivos
| Comando                         | Descripción                                          |
|---------------------------------|------------------------------------------------------|
| `dir`                           | Lista archivos y carpetas del directorio actual.     |
| `cd [ruta]`                     | Cambia el directorio actual.                         |
| `md [nombre]` / `mkdir`         | Crea un nuevo directorio.                            |
| `rd [nombre]` / `rmdir`         | Elimina un directorio vacío.                         |
| `del [archivo]`                 | Elimina un archivo.                                  |
| `copy [origen] [destino]`       | Copia archivos.                                      |
| `xcopy [origen] [destino] /s /e`| Copia carpetas con subcarpetas.                      |
| `move [origen] [destino]`       | Mueve archivos o carpetas.                           |
| `ren [archivo viejo] [nuevo]`   | Renombra archivos.                                   |
| `attrib`                        | Muestra o cambia atributos de archivos.              |

## 🌐 Comandos de Red
| Comando         | Descripción                                               |
|-----------------|-----------------------------------------------------------|
| `ipconfig`      | Muestra configuración de red.                             |
| `ping [ip/url]` | Verifica conectividad de red.                             |
| `tracert [url]` | Muestra la ruta de los paquetes hacia un host.            |
| `netstat`       | Muestra conexiones de red activas y puertos abiertos.     |
| `nslookup`      | Consulta servidores DNS.                                  |
| `netsh`         | Configura interfaces de red y configuración avanzada.     |
| `arp -a`        | Muestra la tabla ARP.                                     |
| `net use`       | Conecta a recursos compartidos.                           |
| `ftp [host]`    | Inicia una sesión FTP.                                    |

## 👤 Gestión de Usuarios
| Comando                                      | Descripción                            |
|----------------------------------------------|----------------------------------------|
| `net user`                                   | Lista los usuarios del sistema.        |
| `net user [nombre] [contraseña] /add`        | Crea un nuevo usuario.                 |
| `net user [nombre] /delete`                  | Elimina un usuario.                    |
| `net localgroup`                             | Lista grupos locales.                  |
| `net localgroup [grupo] [usuario] /add`      | Agrega un usuario a un grupo.          |

## ⚙️ Mantenimiento y Diagnóstico
| Comando                  | Descripción                                       |
|--------------------------|---------------------------------------------------|
| `chkdsk [unidad]:`       | Escanea y repara errores del disco.              |
| `sfc /scannow`           | Repara archivos corruptos del sistema.           |
| `tasklist`               | Lista procesos activos.                          |
| `taskkill /im [proceso] /f`| Finaliza un proceso por nombre.               |
| `shutdown /r /t 0`       | Reinicia el sistema inmediatamente.              |
| `shutdown /s /t 0`       | Apaga el sistema inmediatamente.                 |
| `diskpart`               | Abre la herramienta de gestión de discos.        |

## 🧪 Otros Comandos Útiles
| Comando                    | Descripción                                         |
|----------------------------|-----------------------------------------------------|
| `assoc`                    | Muestra asociaciones de extensiones de archivos.   |
| `fc [archivo1] [archivo2]` | Compara el contenido de dos archivos.              |
| `set`                      | Muestra o modifica variables de entorno.           |
| `pause`                    | Pausa la ejecución del script.                     |
| `timeout /t [segundos]`    | Espera un tiempo determinado antes de continuar.   |

---

> ✅ Este archivo contiene un resumen útil de comandos CMD para tareas comunes en Windows.
