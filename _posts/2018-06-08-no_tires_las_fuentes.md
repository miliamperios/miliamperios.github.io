---
title: No tires las fuentes
author: Arnauti
tags: hack
synopsis: Nunca tires una fuente de alimentación.
---

Cuando un aparato se estropea, no suele ser porque la fuente de alimentación falle.

La mayoría de las veces la fuente de alimentación se tira junto con el resto del cadáver.

Actualmente hay en realidad tres o cuatro tensiones de alimentación para casi todos los aparatos, así que suele ser una buena idea mirar si la fuente de alimentación aún funciona antes de tirarla.

En la parte posterior de las fuentes de alimentación (cuando van separadas del aparato) suelen estar escritos los dos datos que suelen interesarnos más para poder reaprovecharlas: la tensión de operación y la corriente máxima que pueden proporcionar.

Para que te hagas una idea, una Raspberry Pi no funcionará contenta con menos de 5v y 2A (los últimos modelos). Con 5V y 500mA puedes alimentar muchos pequeños microcontroladores, porque muchos de ellos llevan regulador de voltaje y se comen 5V aunque usen 3.3V o incluso 2.8V.

{% include image.html
  img="assets/2018-06-08-no_tires_las_fuentes.jpg"
  title="Una fuente de alimentación"
  caption="Esta fuente de alimentación era de un portátil viejo. Da sus buenos 2A y dos voltajes diferentes: 5V y 12V. así puede alimentar unos cuantos relés y una Particle Photon."
 %}
{% include image.html
  img="assets/2018-06-08-no_tires_las_fuentes-2.jpg"
  title="Una fuente de alimentación"
  caption="Esta fuente de alimentación proporciona 5v y 2A. Era de un cargador de móvil. Es muy fácil abrirla y montarla en un prototipo, y ocupa muy poco espacio."
 %}
