---
slug: inicio-blog
title: Configuración con direwolf de iGate / Digipeater APRS
authors: [quixote]
tags: [quixote_network][aprs][direwolf]
---
# Configuración con direwolf de iGate / Digipeater APRS

Aquí os pegamos un archivo de configuración listo para usar tanto en Linux (Ubuntu, Debian, Raspbian...) como en Windows. Sólo tendréis que cambiar:
- Puerto de comunicación de vuestro dispositivo
- Indicativo de vuestro Digipeater / iGate
- Passcode de vuestro Indicativo

Este es el archivo direwolf.conf que tendréis que usar en vuestro dispositivo Raspberry Pi, Mini-Pc o cualquier otro dispositivo:

```ini
# Si se pone ADEVICE = ADEVICE0
# Linux: er la salida de los comandos 'aplay -l' y 'arecord -l' para ver el dispositivo y subdispositivo. En vez de poner el numero (que pu>
ADEVICE0 plughw:Device,0

# ACHANNELS es 1 para canal unico o mono. Es 2 para canal estereo.
ACHANNELS 1

# Ver la guia de usuario de Direwolf, capitulo 9.1 Audio Device. 
CHANNEL 0

# Como SSID se puede poner xxxxx-0. Segun la documentacion: -0 Your primary station usually fixed and message capable
MYCALL CALLSIGN-0

MODEM 1200

# Se puede activar FIX_BITS para que intente corregir tramas con errores
# FIX_BITS 1 APRS
FIX_BITS 0

# AGWPORT y KISSPORT para conectividad de aplicaciones AGW y TCP-KISSPORT
# Si no se usan se ponen a 0
# AGWPORT 8000
# KISSPORT 8001

##### APRS RF #####
# Baliza de posicion fija para APRS RF
# Aqui poner la el intervalo de tiempo que se quiera la Baliza. La posicion GPS y el texto que enviara. Potencia y Ganancia de la Antena:
PBEACON delay=0:30 every=20:00 symbol=/# lat=39.999999 long=-4.000000 power=25 height=21 gain=5 comment="CALLSIGN-0 APRS iGate Digipeater"

# Otros parametros para VHF. Puede no ser necesario activar algunos o todos.
# FX25TX 1
# RETRY 5
# FRACK 3
# MAXFRAME 7
# EMAXFRAME 14
# PACLEN 128
# DWAIT 0
# TXDELAY: Retardo en ms antes de TX (el valor es x10, p.e. TXDELAY 50 son 500 ms). Por defecto es 30. Puede ser muy util para contro>
# Con 120 funciona el envio de varios paquetes seguidos
TXDELAY 120
# TXTAIL: Retardo en ms despues de TX antes de cortar el audio (el valor es x10). Por defecto es 10. Puede ser muy util para controla>
# Con 5 funciona muy bien cuando hay varios mensajes que repetir
TXTAIL 5
# MAXV22 2
# FULLDUP OFF
# SLOTTIME 10
# PERSIST 63

##### APRS-IS #####
# Baliza de posicion fija para APRS-IS
# Simbolo anterior Digipeater: /#
PBEACON sendto=IG delay=0:30 every=30:00 symbol=I& overlay=T lat=39.842668 long=-4.050211 power=25 height=21 gain=8 comment="CALLSIGN-0 comentario"

# iGate para mandar el RX entrante a internet (pasarela)
IGSERVER euro.aprs2.net
# Hay que generar un "passcode" para nuestro indicativo (SIN el SSID, es decir, solo el indicativo).
# Para generarlo: https://www.iz3mez.it/aprs-passcode/ codigo en: https://github.com/DO3SWW/web-aprs-passcode
# Como SSID para iGates se suele aconsejar xxxxx-10. Segun la documentacin: -10 internet, Igates, echolink, winlink, AVRS, APRN, etc
# Sustituir 11111 por el Passcode de tu Indicativo
IGLOGIN CALLSING-0 11111

# IGTXVIA 0 WIDE1-1
# Reenvia a APRS-IS tambien la info que recibe los Digipeaters
#IGFILTER *
# Reenvia a APRS-IS todo lo recibido en canal 0
IGTXVIA 0

##### --- REGLAS DIGIPEATER --- #####

# Habilita el digipeater
# WIDE1-1 como fill-in digipeater
DIGIPEAT 0 0 ^WIDE1-1$ ALIAS

# Soporte para rutas WIDEn-N, y TRACE para hacer "trazabilidad"
DIGIPEAT 0 0 ^WIDE[2-7]-[1-7]$ TRACE
DIGIPEAT 0 0 ^TRACE[1-7]-[1-7]$ TRACE

# IMPORTANTE: admite errores comunes en moviles
DIGIPEAT 0 0 ^WIDE[1-7]-[1-7]$ ALIAS

# Esta regla la he encontrado en varias fuentes y parece ser muy comun
# DIGIPEAT 0 0 ^WIDE[3-7]-[1-7]$|^TEST$ ^WIDE[12]-[12]$ TRACE

```
