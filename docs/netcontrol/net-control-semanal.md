---
title: 🎛️ Net Control Semanal
description: Explicación del Net Control Semanal de Quixote Network.
sidebar_position: 2
---

# 🎛️ Net Control Semanal de Quixote Network

*Todos los Miércoles a las 19:00 UTC utilizando el programa JS8Call.*

:::info
📡 **JS8Call: (grupo @QXTNET)** 

**HORARIO INVIERNO:** 20:00 Horas Península - UTC +1 (Del 25 de Octubre al 28 de Marzo)
- 80m: 3.578 MHz USB
- 11m: 27.265 MHz

**HORARIO VERANO:** 21:00 Horas Península - UTC +2 (Del 28 de Marzo al 25 de Octubre)
- 40m: 7.078 MHz
- 11m: 27.265 MHz
- 
:::

### 🕒 Secuencia Horaria del Net Control

| Hora UTC        | Operador TX | Mensaje |
|-----------------|-------------|---------|
| 19:00           | Organizador envía | `@QXTNET QXTMSG1 INICIO NET CONTROL` |
| 19:01           | Organizador envía | `@QXTNET SNR?` |
| 19:05           | Organizador envía | `@QXTNET QXTMSG2 EA1ABC EA2DEF EA3GHI` (Estaciones Rxs y Órden Tx) |
| 19:08           | Est. Lejana envía | `@QXTNET QXTMSG3 EA6AND EA9CEU` (Estaciones Rxs faltantes) |
| 19:12           | Organizador envía | `@QXTNET QXTMSG3-1 ENVIAD REGISTRO` |
| 19:15 – 19:20   | Cada Estación envía | `@QXTNET REGISTRO [TU GRID]` |
| 19:21           | Organizador envía | `@QXTNET QXTMSG4 ENVIAD SITREP` |
| 19:22 – 19:25   | Cada Estación envía|  `@QXTNET E:0 I:0 A:0 M:0 AE:2` (Ejemplo SITREP) |
| 19:26           | Organizador envía | `@QXTNET INFO?` |
| 19:30           | Organizador envía | `@QXTNET QXTMSG5 FIN NET CONTROL` |


### 📡 ¿Cómo se elije un Organizador de un Net Control?
Cada semana, entre **30 y 15 minutos antes del inicio del NetControl**, las estaciones interesadas en actuar como organizadoras realizarán intercambios de informes de señal (SNR?) a través del grupo @QXTNET, con el objetivo de determinar cuáles disponen de mayor cobertura y capacidad de recepción. En función de los resultados, se seleccionará como organizadora la estación que pueda alcanzar al mayor número de participantes y cubrir la mayor área posible. Si existen estaciones que quedan fuera de su cobertura, podrá designarse **una segunda estación organizadora** para atenderlas, de modo que todas puedan participar en el SITREP.

Una vez finalizado el NetControl, las estaciones organizadoras intercambiarán la relación de indicativos de las estaciones que hayan participado en sus respectivas sesiones, así como cualquier información o novedad relevante comunicada durante los SITREP. Finalmente, esta información se compartirá en el grupo @QXTNET, para que **todas las estaciones tengan conocimiento de los participantes, las novedades y la situación general de la red**.

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
