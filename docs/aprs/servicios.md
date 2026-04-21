---
title: 📡  Comandos Servicios
description: Comandos de Servicios en APRS.
sidebar_position: 3
---

# 📡 Comandos de Servicios en APRS

Esta guía recopila comandos útiles que puedes enviar mediante APRS para acceder a distintos servicios: información, meteorología, búsqueda de estaciones, mensajería, etc.

> ⚠️ Nota: Algunos servicios dependen de la cobertura APRS-IS mediante iGates y Digipeaters activos.

---

## 🔍 Información de Estaciones

| Comando | Sintaxis | Función | Ejemplo |
|---------|---------|--------|--------|
| **WHO-15** | `WHO-15: indicativo` | Información sobre un radioaficionado | `WHO-15: EA1ABC` |
| **FIND** | `FIND: indicativo` | Última posición conocida de una estación | `FIND: EA1ABC` |

---

## 🌦️ Meteorología

| Comando | Sintaxis | Función | Ejemplo |
|--------|---------|--------|--------|
| **WXYO** | `WXYO: periodo [modo] GRID` | Información meteorológica | `WXYO: today full IM89cx` |
|  | `today / tomorrow / 3 / 6 / 12` | Periodo en horas/días | |

---

## 📢 Mensajería y Broadcast

| Comando | Sintaxis | Función | Ejemplo |
|--------|---------|--------|--------|
| **ALL** | `ALL: texto` | Mensaje broadcast | `ALL: alguien me recibe?` |
| **CQ** | `CQ: texto` | Llamada general | `CQ: alguien me recibe?` |
| **EMAIL-2** | `EMAIL-2: email texto` | Enviar email desde APRS | `EMAIL-2: email@email.com Hola` |
| **WTSAP** | `WTSAP: @+teléfono texto` | Enviar WhatsApp | `WTSAP: @+34123456789 Hola` |

---

## 🏔️ Actividades y Avisos (SOTA y POTA)

| Comando | Sintaxis | Función | Ejemplo |
|--------|---------|--------|--------|
| **SOTA** | `SOTA: referencia frecuencia modo` | Publicar activación SOTA en APRS-IS | `SOTA: EA1/A-001 145.500 FM` |
| **APSPOT** | `! POTA referencia frecuencia modo texto` | Spot de activación POTA | `! POTA ES-0951 7.200 USB CQ` |
| **APSPOT** | `! SOTA referencia frecuencia modo texto` | Spot de activación SOTA | `! SOTA EA4/TO-001 7.200 USB CQ` |
---

## 🔁 Pruebas de Red

| Comando | Sintaxis | Función | Ejemplo |
|--------|---------|--------|--------|
| **ECHO** | `ECHO: texto` | Verificar si llegas a un digipeater | `ECHO: test 1` |\

---

## 📡 Repetidores

| Comando | Sintaxis | Función | Ejemplo |
|--------|---------|--------|--------|
| **REPEAT** | `REPEAT: n número banda` | Repetidores cercanos | `REPEAT: n 3 70cm` |


---

## 🌐 #APRSThrusday

| Comando | Sintaxis | Función | Ejemplo |
|--------|---------|--------|--------|
| **ANSRVR** | `CQ HOTG texto` | Canal #APRSThursday (u otros) | `CQ HOTG Hola! 73` |

---
