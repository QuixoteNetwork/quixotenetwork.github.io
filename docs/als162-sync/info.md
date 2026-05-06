---
title: 📘 Introducción
description: Introducción a ALS162 Sync.
sidebar_position: 1
---

# 📡 ALS162 Sync

ALS162 Sync es una herramienta diseñada para decodificar la señal horaria de radio [ALS162](https://en.wikipedia.org/wiki/ALS162_time_signal) y utilizarla para sincronizar el reloj del ordenador sin necesidad de conexión a internet.

El programa recibe audio desde una tarjeta de sonido, un receptor SDR o una radio externa, analiza la señal recibida y detecta automáticamente tramas válidas de ALS162 para extraer la fecha y hora transmitidas por radio.

Una vez decodificada correctamente la información, el sistema puede comparar esa referencia temporal con el reloj local y sincronizar el equipo utilizando únicamente la señal de radio.

## ✨ Características

- Multiplataforma: Windows, MacOS, Linux...
- Decodificación de la señal horaria ALS162
- Precisión aproximada de ±1 segundo
- Compatible con SDR, radios HF/LF y entradas de audio estándar
- Detección de tonos y análisis a nivel de bit
- Búsqueda automática de tramas válidas
- Extracción de fecha y hora desde la señal recibida
- Sincronización del reloj del sistema de manera automática
- Funciona completamente offline
- Diseñado para radioaficionados, laboratorios y experimentación con señales de baja frecuencia

## 📟 Interfaces disponibles

ALS162 Sync dispone de dos versiones:

### 🖥️ GUI (Graphical User Interface)
Versión gráfica con interfaz visual sencilla e intuitiva para monitorizar el estado de la decodificación y facilitar la interacción con el programa.

<img width="332" height="445" alt="gui" src="https://github.com/user-attachments/assets/592d50eb-9c20-4909-a3d6-9c04e3b8f15e" />

### 💻 TUI (Terminal User Interface)
Versión ligera basada en terminal, ideal para sistemas de bajos recursos, acceso remoto mediante SSH o entornos sin interfaz gráfica.

<img width="422" height="452" alt="tui" src="https://github.com/user-attachments/assets/1f496bc7-81f9-4dee-af15-56d59a149b1e" />

---
## 🎯 Objetivo del proyecto

El objetivo de ALS162 Sync es ofrecer una forma sencilla y autónoma de sincronizar un ordenador utilizando una referencia horaria transmitida por radio, especialmente útil en escenarios offline, experimentación técnica y entornos donde no se dispone de acceso a servicios de tiempo por internet.

Además de su utilidad práctica, el proyecto sirve como herramienta educativa para comprender el funcionamiento de las señales horarias de baja frecuencia y las técnicas de decodificación digital aplicadas a radio.

## Instala y Descarga 

Puedes descargar la herramienta tanto en su versión GUI como TUI desde el repositiorio de Github: https://github.com/QuixoteNetwork/als162-sync/

## Más info:
- Grupo de Telegrma de Quixote Network: https://t.me/quixotenetwork

---

## ❤️ Apoya el proyecto

Si este proyecto te resulta útil:

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/M4M81CV1EX)
