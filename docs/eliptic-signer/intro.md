---
title: 📘 Introducción
description: Introducción a Eliptic Signer como aplicación ligera diseñada para firmar y verificar mensajes digitales
sidebar_position: 1
---

# 🔐 Eliptic Signer  
### Firma y Verificación de Mensajes con Ed25519 para Comunicaciones y Radiocomunicaciones 

---

## 🧭 ¿Qué es Eliptic Signer?

**Eliptic Signer** es una herramienta ligera diseñada para **firmar y verificar mensajes digitales** usando criptografía moderna (**Ed25519**), especialmente pensada para:

- 📡 Comunicaciones por radio (HF / VHF / UHF / Mesh)
- 🌐 Entornos sin internet
- 🚨 Situaciones de emergencia o seguridad
- 🧩 Redes descentralizadas

Permite demostrar **quién eres realmente**, incluso cuando no hay infraestructura.

---

## 🚀 ¿Qué puedes hacer con él?


✔️ Firmar mensajes de texto  
✔️ Verificar la autenticidad de un mensaje  
✔️ Generar tus propias claves criptográficas  
✔️ Compartir tu identidad de forma segura  
✔️ Integrarlo en el uso con sistemas como APRS, MeshFest, VARA o JS8Call  


---

## 📡 Casos reales en radio


🔹 Autenticación de estaciones en el **Net Control**  
🔹 Evitar suplantaciones en enlaces de Radio (HF, VHF, UHF...)  
🔹 Validación de mensajes en emergencias  
🔹 Identificación en redes Mesh distribuidas  
🔹 Comunicación autenticada en modos digitales (APRS, JS8Call, VARA...)

:::tip
**Filosofía**

> “En radio, cualquiera puede hablar…  
> pero no cualquiera puede demostrar quién es.”

**Eliptic Signer hace eso posible.**
:::

---

## 📄 Ejemplo real

```
MSG: 070426 START NET CONTROL EA1ABC
SIG: RnZ5ts8cFnPUwy9bkqmUuX2RZ4RTVF57r6jUdnzC1iD6boM1VXynW+vWWJa4ooJ2XhuhTdzriuF5OiEMjk19Cw==
```

👉 Cualquier estación puede verificar que ese mensaje ha sido enviado por quien dice ser.

---

## 🔐 ¿Por qué usar Ed25519?

<div>

⚡ Muy rápido y eficiente  
🔒 Criptografía moderna y segura  
📏 Firmas pequeñas (64 bytes)  
🔁 Determinista (mismo mensaje → misma firma)  

:::tip
💡 Ideal para comunicaciones de **bajo ancho de banda como HF**
:::
---

## 🧩 Compatibilidad

Funciona perfectamente con:

- 📡 **VARA HF**
- 📡 **JS8Call**
- 📡 **MeshFest**
- 🔜 Integraciones futuras en desarrollo

---


## ⚠️ Importante (Legal)

❌ No utiliza cifrado para el texto(no permitido en radioafición)  
✔️ Solo firma digital del texto (sí permitido)  
✔️ El contenido del texto siempre es visible  


---


## ❤️ Apoya el proyecto

Si este proyecto te resulta útil:

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/M4M81CV1EX)

Tu apoyo ayuda a seguir desarrollando herramientas para la comunidad de radio 🙌


