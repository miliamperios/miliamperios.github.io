---
title: El relé biestable
author: Arnauti
tags: componentes prototipo
---

El relé biestable no gasta energía mientras mantiene el contacto.

Un relé es un elemento mecánico que sustituye a un interruptor:
Le mandas una señal de control (los voltajes varían, pero para prototipos con microcontroladores pequeños suelen ser de __5v__) y enclava un electroimán que produce un contacto que aguanta voltajes y cargas muy superiores.

Es decir, que puedes _encender_ y _apagar_ cosas que funcionan con otros voltajes y consumen bastante potencia con tu pequeño microcontrolador.

Los relés suelen ser mandados por una sola señal de control: si está activa, el relé comunica una entrada común con la entrada que normalmente está abierta (_normally open_, NO) y si está inactiva, el contacto es entre la entrada común y la que normalmente está cerrada (_normally closed_, NC).

Eso quiere decir que para mantener algo encendido con la ayuda de un relé, tienes que mantener la señal de control activa, y el relé consumirá corriente para mantener el electroimán energizado.

Y aquí aparecen los relés biestables (_latching relay_). Son relés que funcionan como un balancín: una vez los empujas hacia una posición, se quedan ahí sin consumir energía, hasta la próxima vez que vuelvas a decirle que cambie su estado.


{% include image.html
  img="assets/2018-05-31-el-rele-biestable.jpg"
  title="El relé biestable"
  caption="Esto es un relé biestable. Suele ser algo mayor que los relés sencillos, y tiene dos entradas de control además de la entrada de voltaje positiva y negativa."
 %}

Los relés biestables tienen dos entradas: __SET__ y __RESET__. Cada una de ellas cambia la entrada activa, y una vez hecho, deja de consumir energía. Las señales de control son temporales: basta medio segundo para cambiar el estado del relé, y después puedes desactivar la señal de nuevo.

Los relés biestables son ideales para prototipos que mantienen contactos o dispositivos apagados o encendidos durante mucho tiempo, o precisan ahorrar energía o ser tolerantes a cortes de corriente, por ejemplo.



### Referencias

What is Latching Relay?:
: <http://www.omron.com.au/service_support/FAQ/FAQ02822/index.asp>

Grove - 2- Coil Latching relay:
: <https://www.seeedstudio.com/Grove-2-Coil-Latching-Relay-p-1446.html>
