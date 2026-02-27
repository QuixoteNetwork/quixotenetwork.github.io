---
title: 🎛️ Net Control Semanal
description: Net Control Semanal.
sidebar_position: 1
---

# 🎛️ Net Control Semanal

*Todos los Miércoles a las 20:00 horas peninsular (19:00 UTC).*

:::info
📡 JS8Call: 40m (70.078 MHz) (grupo @QXTNET) 

📶 Meshtastic: canal Iberia
:::

### 🕒 Secuencia Horaria del Net Control

| Hora            | Acción |
|-----------------|--------|
| 20:00           | El organizador envía **QXTMSG1: Inicio Net Control** |
| 20:01 – 20:04   | El organizador envía: `@QXTNET SNR?` |
| 20:05 – 20:15   | Envío de cada estación: **REGISTRO [GRID]** |
| 20:16 – 20:30   | Envío de cada estación: **Reporte de Situación (SITREP)** |


### 📡 Ejemplo Formato SITREP
```
E:0 I:0 A:0 M:0 AE:2
```

### 📡 ¿Qué es un SITREP en Quixote Network?

Un SITREP (Situation Report) o Informe de Situación, es un informe estructurado y periódico que cada estación participante envía durante el Net Control semanal, con el objetivo de comunicar de forma breve y estandarizada el estado de su entorno e infraestructura básica.

En el contexto de Quixote Network, el SITREP no es solo un “check-in”, sino una fotografía operativa de la situación local de cada nodo, incluyendo:

- Estado del suministro eléctrico
- Conectividad a Internet
- Disponibilidad de agua
- Condiciones meteorológicas dominantes
- Autonomía energética de la estación

Este formato permite:

- Obtener una visión global distribuida de la situación en distintas zonas geográficas
- Evaluar la resiliencia de la red
- Practicar comunicaciones estructuradas en modo digital (JS8Call)
- Fomentar la preparación técnica y la autonomía operativa

El SITREP está diseñado para ser compacto, claro y transmisible en condiciones de señal débil, permitiendo mantener coordinación incluso en escenarios de infraestructura degradada.
