---
title: Comandos Comunes de la Terminal de Linux
created: '2025-06-25T07:57:34.647Z'
modified: '2025-06-25T07:57:49.719Z'
---



# Comandos Comunes de la Terminal de Linux

Este documento presenta una lista de comandos esenciales utilizados en la terminal de Linux, junto con una breve descripción de su función.

---

## Navegación y Gestión de Archivos y Directorios

* **`ls`**: Lista el contenido del directorio actual.
    * `ls -l`: Muestra detalles (permisos, propietario, tamaño, fecha) en formato largo.
    * `ls -a`: Muestra todos los archivos, incluyendo los ocultos (que empiezan por `.` ).
    * `ls -lh`: Muestra el tamaño de los archivos en un formato legible para humanos (ej. KB, MB).
* **`cd`**: Cambia de directorio.
    * `cd ..`: Sube un nivel en la jerarquía de directorios.
    * `cd ~`: Va al directorio de inicio del usuario actual.
    * `cd /`: Va al directorio raíz del sistema de archivos.
    * `cd /ruta/a/directorio`: Va a la ruta especificada.
* **`pwd`**: Imprime el directorio de trabajo actual (Print Working Directory).
* **`mkdir`**: Crea un nuevo directorio.
    * `mkdir nombre_directorio`: Crea un directorio con el nombre especificado.
    * `mkdir -p ruta/a/nuevos/directorios`: Crea directorios anidados si no existen.
* **`rmdir`**: Elimina un directorio vacío.
* **`cp`**: Copia archivos y directorios.
    * `cp archivo_origen archivo_destino`: Copia un archivo.
    * `cp -r directorio_origen directorio_destino`: Copia un directorio y su contenido de forma recursiva.
* **`mv`**: Mueve o renombra archivos y directorios.
    * `mv origen destino`: Mueve un archivo o directorio.
    * `mv archivo_antiguo_nombre nuevo_nombre`: Renombra un archivo.
* **`rm`**: Elimina archivos y directorios.
    * `rm archivo`: Elimina un archivo.
    * `rm -r directorio`: Elimina un directorio y su contenido de forma recursiva (¡usar con precaución!).
    * `rm -f archivo`: Fuerza la eliminación de un archivo sin pedir confirmación.
    * `rm -rf directorio`: Elimina un directorio y su contenido de forma recursiva y forzada (¡extrema precaución!).
* **`touch`**: Crea un nuevo archivo vacío o actualiza la fecha de modificación de un archivo existente.
* **`ln`**: Crea enlaces (duros o simbólicos).
    * `ln -s origen enlace_simbolico`: Crea un enlace simbólico (acceso directo).

## Visualización y Edición de Archivos

* **`cat`**: Concatena archivos e imprime su contenido en la salida estándar.
    * `cat archivo.txt`: Muestra el contenido de `archivo.txt`.
* **`less`**: Muestra el contenido de un archivo página por página, permitiendo el desplazamiento.
* **`more`**: Similar a `less`, pero con menos funcionalidades de navegación.
* **`head`**: Muestra las primeras líneas de un archivo (por defecto 10).
    * `head -n 20 archivo.txt`: Muestra las primeras 20 líneas.
* **`tail`**: Muestra las últimas líneas de un archivo (por defecto 10).
    * `tail -n 20 archivo.txt`: Muestra las últimas 20 líneas.
    * `tail -f archivo.log`: Muestra las últimas líneas de un archivo y sigue añadiendo nuevas líneas a medida que se escriben (útil para logs).
* **`nano`**: Un editor de texto simple y fácil de usar para la terminal.
* **`vi`** / **`vim`**: Editores de texto potentes y versátiles (Vim es la versión mejorada de Vi), con una curva de aprendizaje más pronunciada.

## Búsqueda y Filtrado

* **`grep`**: Busca patrones de texto dentro de archivos.
    * `grep "patron" archivo.txt`: Busca "patron" en `archivo.txt`.
    * `grep -i "patron" archivo.txt`: Busca ignorando mayúsculas/minúsculas.
    * `grep -r "patron" directorio`: Busca de forma recursiva en todos los archivos de un directorio.
    * `grep -l "patron" *.txt`: Muestra solo los nombres de los archivos que contienen el patrón.
* **`find`**: Busca archivos y directorios en una jerarquía de directorios.
    * `find . -name "mi_archivo.txt"`: Busca un archivo llamado `mi_archivo.txt` en el directorio actual y subdirectorios.
    * `find /home -type d -name "docs"`: Busca directorios llamados "docs" en `/home`.
    * `find /var/log -size +10M`: Busca archivos de más de 10MB en `/var/log`.
* **`locate`**: Busca archivos rápidamente utilizando una base de datos preconstruida (necesita ser actualizada regularmente con `sudo updatedb`).
* **`wc`**: Cuenta líneas, palabras y caracteres en un archivo.
    * `wc -l archivo.txt`: Cuenta solo las líneas.

## Gestión de Procesos

* **`ps`**: Muestra una instantánea de los procesos en ejecución.
    * `ps aux`: Muestra todos los procesos de todos los usuarios con información detallada.
* **`top`**: Muestra los procesos en ejecución de forma interactiva y en tiempo real, ordenados por uso de CPU.
* **`htop`**: Una alternativa a `top` con una interfaz más amigable y características adicionales.
* **`kill`**: Envía una señal a un proceso para terminarlo.
    * `kill PID`: Termina un proceso por su ID de proceso (PID).
    * `kill -9 PID`: Fuerza la terminación de un proceso (señal SIGKILL).
* **`killall`**: Termina procesos por su nombre.
    * `killall nombre_proceso`: Termina todas las instancias de un proceso con el nombre especificado.
* **`bg`**: Pone un proceso en segundo plano.
* **`fg`**: Trae un proceso de segundo plano al primer plano.
* **`jobs`**: Lista los procesos que se están ejecutando en segundo plano en la sesión actual.

## Información del Sistema

* **`uname`**: Muestra información del sistema.
    * `uname -a`: Muestra toda la información del sistema (nombre del kernel, versión, etc.).
* **`df`**: Muestra el espacio en disco utilizado y disponible en los sistemas de archivos montados.
    * `df -h`: Muestra la información en un formato legible para humanos.
* **`du`**: Estima el uso de espacio en disco por archivos o directorios.
    * `du -sh directorio`: Muestra el tamaño total de un directorio en formato legible para humanos.
* **`free`**: Muestra la cantidad de memoria libre y usada en el sistema.
    * `free -h`: Muestra la información en un formato legible para humanos.
* **`whoami`**: Muestra el nombre de usuario actual.
* **`id`**: Muestra información sobre el usuario y los grupos a los que pertenece.
* **`history`**: Muestra un historial de los comandos ejecutados previamente.
* **`date`**: Muestra la fecha y hora actuales del sistema.
* **`cal`**: Muestra un calendario.

## Red y Conectividad

* **`ping`**: Envía paquetes ICMP a un host para verificar la conectividad de la red.
* **`ip addr`** / **`ifconfig`** (obsoleto en algunas distribuciones): Muestra información de la interfaz de red (direcciones IP, MAC, etc.).
* **`ss`** / **`netstat`** (obsoleto en algunas distribuciones): Muestra información sobre las conexiones de red (puertos abiertos, conexiones activas, etc.).
* **`ssh`**: Cliente para iniciar sesiones seguras en máquinas remotas.
* **`scp`**: Copia archivos de forma segura entre hosts.
* **`wget`**: Descarga archivos desde la web.
* **`curl`**: Herramienta para transferir datos con sintaxis de URL, soporta muchos protocolos.

## Gestión de Usuarios y Permisos

* **`sudo`**: Ejecuta un comando como superusuario (root).
* **`su`**: Cambia al usuario root o a otro usuario.
* **`chmod`**: Cambia los permisos de archivos y directorios.
    * `chmod +x archivo`: Otorga permiso de ejecución al archivo.
    * `chmod 755 directorio`: Establece permisos (lectura, escritura, ejecución para propietario; lectura, ejecución para grupo y otros).
* **`chown`**: Cambia el propietario de archivos y directorios.
* **`chgrp`**: Cambia el grupo de archivos y directorios.
* **`adduser`**: Añade un nuevo usuario al sistema.
* **`deluser`**: Elimina un usuario del sistema.
* **`passwd`**: Cambia la contraseña de un usuario.

## Compresión y Descompresión

* **`tar`**: Herramienta para archivar y comprimir archivos (Tape ARchiver).
    * `tar -cvf archivo.tar directorio`: Crea un archivo `.tar` sin comprimir.
    * `tar -xvf archivo.tar`: Extrae un archivo `.tar`.
    * `tar -czvf archivo.tar.gz directorio`: Crea un archivo `.tar.gz` (comprimido con gzip).
    * `tar -xzvf archivo.tar.gz`: Extrae un archivo `.tar.gz`.
    * `tar -cjvf archivo.tar.bz2 directorio`: Crea un archivo `.tar.bz2` (comprimido con bzip2).
    * `tar -xjvf archivo.tar.bz2`: Extrae un archivo `.tar.bz2`.
* **`gzip`**: Comprime o descomprime archivos con el algoritmo gzip.
* **`gunzip`**: Descomprime archivos comprimidos con gzip.
* **`zip`**: Comprime archivos en formato .zip.
* **`unzip`**: Descomprime archivos .zip.

## Misceláneos y Utilidades

* **`man`**: Muestra las páginas del manual de un comando (información detallada sobre su uso).
    * `man ls`: Muestra el manual del comando `ls`.
* **`apropos`**: Busca en las descripciones de las páginas del manual.
    * `apropos network`: Busca comandos relacionados con "network".
* **`echo`**: Muestra texto en la salida estándar.
    * `echo "Hola Mundo"`: Imprime "Hola Mundo".
* **`alias`**: Crea un atajo para un comando o una secuencia de comandos.
    * `alias ll='ls -lh'`: Crea el alias `ll` para `ls -lh`.
* **`unalias`**: Elimina un alias.
* **`clear`**: Limpia la pantalla de la terminal.
* **`exit`**: Sale de la sesión actual de la terminal.
* **`reboot`**: Reinicia el sistema (requiere permisos de superusuario).
* **`shutdown`**: Apaga el sistema (requiere permisos de superusuario).
    * `shutdown -h now`: Apaga el sistema inmediatamente.
    * `shutdown -r now`: Reinicia el sistema inmediatamente.

---
