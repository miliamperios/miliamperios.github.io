---
title: De 3.3 a 5v sin despeinarse
author: Kokuma
tags: circuitos
---

Convierte una señal de 3.3v en otra de 5v de manera sencilla.

Las nuevas hornadas de microcontroladores ([WeMos D1 mini PRO](https://wiki.wemos.cc/products:d1:d1_mini_pro), [Adafruit Huzzah](https://learn.adafruit.com/adafruit-huzzah-esp8266-breakout?view=all)...) utilizan un valor menor de voltaje en sus salidas digitales (3.3v en vez de los 5v de un Arduino) Esto supone un problema cuando tenemos que manejar dispositivos que requieren los 5v para funcionar adecuadamente.

Uno de los ejemplos más comunes son los [NeoPixel](https://learn.adafruit.com/adafruit-neopixel-uberguide/the-magic-of-neopixels): podemos alimentarlos con 3.3v y controlarlos con una señal de 3.3v, pero brillarán lo justo. Si los alimentamos con 5v y la señal es de 3.3v, el comportamiento será errático, así que no nos queda otra que alimentarlos a 5v y amplificar la señal a 5v.

Para amplificar una señal de 3.3v a 5v se utiliza un chip llamado "level shifter" (aunque el nombre oficial es "74HTC245 - Octal bus transceiver", que da más respeto) Es un chip al que por un lado se conectan las señales de 3.3v y por el otro, tecnimágicamente, aparecen convertidas en señales de 5v. El montaje es muy sencillo:

{% include image.html
  img="assets/2018-05-26-levelshifter.png"
  title="Esquema level shifter"
  caption="Conexionado del chip para amplificar dos señales de un WeMos mini"
 %}

En este ejemplo estamos amplificando las señales de las salidas D1 y D2 de 3.3v a 5v. Podemos amplificar hasta 8 señales, pero ojo, que el chip está pensado para amplificar señales, no es un convertidor de voltaje para alimentar otros dispositivos.

### Referencias

Data sheet del 74HTC245:
: <http://www.ti.com/general/docs/lit/getliterature.tsp?genericPartNumber=SN74HCT245&&fileType=pdf>
