---
title: 📡 Informe de Situación
description: Explicación en Detalle del Informe de Situación o SITREP.
sidebar_position: 2
---

## 📡 Estructura Oficial del SITREP de Quixote Network

SITREP: significa Situation Report, en castellano Informe de Situación, que es un Informe donde cada Estación anuncia la situación que tiene, en nuestro caso sobre:
- Suministro eléctrico
- Estado del Internet
- Suministro de Agua corriente
- Meteorología
- Autonomnía eléctrica en caso de corte eléctrico

**Ejemplo de transmisión:**

Emisión: ``` E:0 I:0 A:0 M:03 AE:2 ```
Significado: Red Eléctrica Operativa, Internet Normal, Suministro Agua Normal, Meteorología Tomenta y Autonomía Energética de 2 horas sin electricidad.

---

### 1️⃣ Electricidad (E)

Estado del suministro eléctrico doméstico.

| Estado                              | Código |
|-------------------------------------|--------|
| Red eléctrica operativa             | 0      |
| Intermitente                        | 1      |
| Sin red                             | 2      |
| Funcionando con generador           | 3      |

---

### 2️⃣ Internet (I)

Estado de conectividad IP.

| Estado                                      | Código |
|---------------------------------------------|--------|
| Conectividad normal (Cable y Móvil)         | 0      |
| Sólo datos móviles                          | 1      |
| Cortes intermitentes / Baja velocidad       | 2      |
| Sin Internet de ningún tipo                 | 3      |

---

### 3️⃣ Agua (A)

Estado del suministro de agua.

| Estado              | Código |
|---------------------|--------|
| Normal              | 0      |
| Baja presión        | 1      |
| Sin suministro      | 2      |

---

### 4️⃣ Meteorología (M)

Condición dominante relevante.

| Estado    | Código |
|----------|--------|
| Normal   | 0      |
| Lluvia   | 1      |
| Viento   | 2      |
| Tormenta | 3      |
| Nieve    | 4      |
| Calor    | 5      |
| Frío     | 6      |

> Solo indicar la condición dominante más relevante.

---

### 5️⃣ Autonomía Energética (AE)

Capacidad sin red eléctrica.

| Autonomía          | Código |
|--------------------|--------|
| Sin batería (0H)   | 0      |
| 2 horas            | 2      |
| 6 horas            | 6      |
| 12 horas           | 12     |
| 24 horas o más     | 24     |
