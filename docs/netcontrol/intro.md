---
title: 🎛️ Net Control Semanal
description: Explicación del Net Control Semanal de Quixote Network.
sidebar_position: 1
---

# 🎛️ Net Control Semanal

*Todos los Miércoles a las 20:00 horas invierno / 21:00 horas verano, horario peninsular (19:00 UTC).*

:::info
📡 JS8Call: (grupo @QXTNET) 
- 40m: 7.078 MHz
- 11m: 27.265 MHz

📶 Meshtastic: canal Iberia
:::

### 🕒 Secuencia Horaria del Net Control

| Hora UTC        | Operador TX | Mensaje |
|-----------------|-------------|---------|
| 19:00           | Organizador envía | `@QXTNET QXTMSG1 INICIO NET CONTROL` |
| 19:01           | Organizador envía | `@QXTNET SNR?` |
| 19:04           | Organizador envía | `@QXTNET QXTMSG2 ENVIAD REGISTRO` |
| 19:05 – 19:14   | Cada Estación envía | `@QXTNET REGISTRO [TU GRID]` |
| 19:15           | Organizador envía | `@QXTNET QXTMSG3 ENVIAD SITREP` |
| 19:16 – 19:29   | Cada Estación envía|  `@QXTNET E:0 I:0 A:0 M:0 AE:2` (EJEMPLO SITREP) |
| 19:30           | Organizador envía | `@QXTNET QXTMSG4 FIN NET CONTROL` |


### 📡 Ejemplo Formato SITREP
Ejemplo de SITREP (Informe de Situación) enviado por una Estación:
```
E:0 I:0 A:0 M:0 AE:2
```
Significado: Electriciad Normal, Internet Normal, Agua Normal, Meteorología Normal y Autonomía Energética de 2 horas.

Más información sobre los SITREP: [Explicación detallada SITREP](https://quixote.info/docs/netcontrol/sitrep)

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
