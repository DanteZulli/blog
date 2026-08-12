+++
date = '2026-06-28'
draft = true
layout = "single"
title = 'Dispositivos Con Propósito'
description = 'Segunda vida para aparatos "obsoletos"'
author = "Dante Zulli"
tags = []
+++

## Contexto

Hace no mucho mi vieja me planteó que le gustaría empezar a darles una introducción al mundo de la tecnología a mis dos hermanas menores. Una especie de _primer vuelo_ en el que aprendan por su cuenta a manejarse con "las máquinas". El plan era sencillo; conseguirle a ambas al menos una tablet que cumpla con "lo básico" para un uso regular, controlado, idealmente sin intervención adulta, sin acceso libre a internet, y lo más importante; que sea lo más económico posible.

Yo no soy fanático de las tablets (de hecho, las detesto). \
Me parecen un punto medio entre un celular y una PC que no termina de satisfacer nunca por completo ninguna de **mis** necesidades. Considero que son el dispositivo por excelencia para definir el concepto de ["obsolescencia programada"](https://es.wikipedia.org/wiki/Obsolescencia_programada), y además, viendo lo que cuesta una de las más básicas (y lo poco que ofrecen), sabía que el camino no era adquirir nada nuevo. Tocaba hacerse de un nuevo plan.

Resulta ser que yo, unos días antes me encontraba ordenando mi "búnker", revisando cajas, muebles y organizadores viejos donde suelo acumular hardware y tecnología ya obsoleta, y me topé con dos anticuadas tablets "chinas" muy primitivas, con especificaciones similares (y paupérrimas) que a fines prácticos, hoy en día no sirven para nada.

{{< img src="images/tablets.jpeg" alt="Las dos Tablets, lado a lado" >}}

Como armar una computadora (por mucho que hubiera querido) no era una opción, ya que las dos son todavía "chicas", y la barrera de entrada generaría más frustración que otra cosa, el camino estaba definido; había que reconvertir esas dos tablets en los dispositivos útiles que alguna vez supieron ser (ponele xD).

Y de eso se trata este artículo, de la travesía que fue responder la pregunta del millón; "Cómo y qué se puede hacer para darle una segunda vida a estas catraminas?"

## Qué se puede hacer con estas cosas?

Originalmente mi intención era *flashearle* alguna ROM modificada mucho más ligera y "vanilla" (de código abierto, obvio) que me permita sacarle provecho al humilde chip y a la escasa memoria que estas tablets traen de fábrica. Ya tenía experiencia con ROMs como [LineageOS](https://lineageos.org/), [crDroid](https://crdroid.net/) y [GrapheneOS](https://grapheneos.org/) a raíz de "cacharrear" con teléfonos viejos míos, o de mi familia, así que no parecía una tarea "difícil".

El inconveniente radica en que proyectos como los antes mencionados, brindan imágenes para ciertos dispositivos y chips **en específico**, y la lista es muy reducida. \
Estas tablets son demasiado "genéricas", y si bien su chip es conocidísimo (el SoC se usó desde tablets hasta TVBox y estéreos), nada te asegura que el paso a paso para flashear la ROM no te deje un hermoso pisapapeles de plástico. No hay un tutorial, una guía, o un "camino ya explorado. No tenía los conocimientos necesarios y no podía arriesgarme aprenderlos esta vez, así que tuve que aplicar todas las otras técnicas de optimización que se me ocurrieron.

> Nota: Les dejo por acá este video; "[Como rootear android efectivo](https://www.youtube.com/watch?v=Dr75djEPJmU)" que grabé hace ya más de 10 años.
> En ese entonces tenía menos miedo (o más ingenuidad) y me animaba más a destripar los aparatos que tenía en mis manos. \
> Nota sobre la nota: El celular que aparece ahí es un [Samsung Galaxy Pocket Neo](https://www.smart-gsm.com/moviles/samsung-galaxy-pocket-neo), al que después le supe flashear [CyanogenMod](https://en.wikipedia.org/wiki/CyanogenMod). Nerd y friki desde la beta se podría decir?

## Especificaciones

Antes de avanzar con lo que se podría decir es el "paso a paso" de este post (y las pequeñas ideas que quiero que se lleven), me gustaría compartirles un pantallazo de las especificaciones de ambas tablets.

### SoC (System on a Chip) / "El proce" para los amigos
El SoC Rockchip RK3126 en la Next y 3126C en la Kanji. Les dejo por acá el [Datasheet](https://rockchip.fr/RK3126%20datasheet%20V1.0.pdf) con toda la información al respecto, además de un [foro interesante](https://www.servicell-arauca.com/foros/showthread.php?tid=28048) en dónde hablan sobre flashear el firmware del mismo en una tablet.

Cómo les mencionaba anteriormente, a día de hoy *se sigue comercializando* Se ve mucho en "Game Sticks" (como [este](https://archive.org/details/gamestick-yx-v3-20231228-rk3126)) o en los "TVBox" (como [este](https://androidpc.es/guia-actualizacion-firmware-android-tvbox-soc-rockchip/)).\
Flashear imágenes en estos casos es "más sencillo", ya que estos dispositivos son más baratos y tienen menos cosas "agregadas" que puedan perder su funcionamiento (cómo en una tablet puede ser la pantalla, la cámara, etc.). Además de que en las tablets las placas de WiFi suelen ser **privativas**, por ende, es difícil que funcionen sin tener que meter mano a posteriori.

> PD: Me hizo acordar a el viejo Debian con esto de no tener drivers para el WiFi xD

Los binarios son de código abierto (creo?) o están publicados bajo [este repositorio](https://github.com/rockchip-linux/rkbin/tree/master) y sospecho que las release notes de este chip están en [este archivo](https://github.com/rockchip-linux/rkbin/blob/master/doc/release/RK3126_EN.md). Del resto no me pidan más, no se chino xD y muy probablemente le esté pifiando a algo.

Para cerrar, la gente de [PostMarketOS](https://postmarketos.org/) tiene [un artículo](https://wiki.postmarketos.org/wiki/Rockchip_RK3126/RK3128/RK3188) hablando al respecto, en dónde menciona algunos dispositivos soportados (reportados funcionando) que tengan este SoC (o uno similar). Cómo ven, la lista es acotadísima, y acá jamás van a aparecer esta clase de tablets importadas en masa y "rebrandeadas" por marcas argentinas, ya que nacen así, sabiendo que más temprano que tarde serán descartables.

### RAM

[~1GB de RAM en cada una.](https://www.youtube.com/watch?v=7bd7TXRY4J0)

### Sistema Operativo



## ADB, el gran salvador

## Y ahora qué? (F-Droid y OSS)

## Un poco de mi perspectiva sobre el libre uso de la tecnología para los niños
