---
title: WSL1
created: '2025-06-25T07:33:28.331Z'
modified: '2025-06-25T08:05:37.193Z'
---

# WSL1

20250625


WSL1 es la **primera versión del Subsistema de Windows para Linux**, una herramienta permite ejecutar distribuciones de Linux directamente en Windows ( como Ubuntu, Debia, etc.) **sin necesidad de usar máquina virtual** o configurar un arranque dua (dual boot).

**Características principales:**

- **Traducción de llamadas de Sistema WSL 1** traduce las llamadas de sistema Linux a llamadas equivalentes a Windows.

- **Sin kernel real de Linux**: A diferencia de WSL2,WSL1 no utiliza núcleo real de Linux.

- **Acceso al sistema de archivos**: Puede accedera los sistemas de Windows desde Linux.

- **Alto rendiemiento o en archivo de Windows**: Las operaciones con archivos que reside en el disco de Windows, suelen ser más rápidas que en WSL2. 


## Ventajas ##

- Arranca más rápido WSL2.
- Mejor rendiemiento al trabajar con archivos del sistema Windows.
- Ideal para scripts.
- Utilidad de línea de comandos y desarrollo liviano. 

## Desventajas ##

- No se puede ejecutar todo el software de Linux.
- No todas las llamadas tiene traducción a Windows.
- No es compatible con Docker de manera nativa.
- No soporta el comando * systemd *ni otros servicios del sistema.
- No se puede usar con aplicaciones que requieran un Kernel del Linux real.

## ¿Cuándo usar WSL1? ##

- Cuando necesitas acceso rápida al sistema de archivos de Linux.
- Si tu equipo no soporta virtualización, necesario para WSL2.
- Si estás trabajando con herramientas simples de desarrollo o scripts.
- Si prefieres un entorno más ligero y rápido ppara tareas básicas.



