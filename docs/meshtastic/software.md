---
title: 📱 Software
description: Software para Meshtastic.
sidebar_position: 2
---

# 📡 Software para Meshtastic

Una recopilación de herramientas para usar, visualizar y sacar el máximo partido a mallas **Meshtastic**.

---

## 🌐 Software Oficial

### 📱 Apps móviles

- 📲 Android: https://play.google.com/store/apps/details?id=com.geeksville.mesh
- 🍎 iOS: https://apps.apple.com/us/app/meshtastic/id1586432531

---

### 💻 Cliente Web Oficial

- 🌍 Web Client: https://client.meshtastic.org/

Permite:
- Conectarse por Bluetooth, Serial o TCP
- Ver mapa de nodos
- Enviar mensajes

---

## 📊 Visualización RF Avanzada

### 📡 MeshMonitor

- 👉 Web (Información): https://meshmonitor.org/
- 👉 Repositorio Github (Descarga e Instalación): https://github.com/Yeraze/meshmonitor

Funciones:
- Mapa en tiempo real
- Visualización de enlaces entre nodos
- Datos históricos
- Despliegue con Docker

Ideal para:
- Ver cobertura RF real
- Analizar enlaces y calidad
- Gestionar nodos desde un ordenador

---

## 🧰 CLI (línea de comandos)

- GitHub: https://github.com/meshtastic/meshtastic-python

### 📦 Instalación

```bash
pip install meshtastic
```

---

### 🚀 Uso básico

Consultar información del nodo:

```bash
meshtastic --info
```

---

### 💬 Enviar mensajes

```bash
meshtastic --sendtext "Hola desde Meshtastic"
```

Enviar a un nodo específico:

```bash
meshtastic --dest !abcdef01 --sendtext "Mensaje directo"
```

---

### 🔌 Conexión al dispositivo

#### Por puerto serie (USB)

```bash
meshtastic --port COM3 --info
```

#### Por TCP/IP

```bash
meshtastic --host 192.168.1.50 --info
```

