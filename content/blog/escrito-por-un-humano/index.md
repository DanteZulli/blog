+++
date = '2026-08-08'
draft = false
layout = "single"
title = 'Este post fue escrito por un humano'
description = '(y todos los demás también)'
author = "Dante Zulli"
tags = []
+++

## La des-inteligencia artificial

Si leen habitualmente en internet (cómo yo) y son observadores, quizá se hayan encontrado con la "no tan leve" sensación de que en los últimos años, cada artículo, blog, nota, o publicación pareciera haber sido escrito por la misma persona. Me creerían si les digo que de cierta forma, es verdad?

Desde la normalización del consumo y uso de la inteligencia artificial, la cantidad de textos escritos _en su totalidad_ por humanos fue cayendo en picado, mientras que los escritos por inteligencia artificial aumentaron brutalmente, a tal punto de que hoy en día [se revirtió la tendencia](https://graphite.io/five-percent/research/ai-now-writes-as-many-online-articles-as-humans-do), volviendo complicado, difícil (y hasta extraño) encontrar algo para leer que haya escrito un humano **real**.

{{< img src="images/graph.png" alt="Gráfico de contenido generado por IA vs contenido generado por humanos" >}}

No soy muy fanático de las teorías conspirativas, pero he de admitir que esto no hace más que convertir a la [teoría del internet muerto](https://en.wikipedia.org/wiki/Dead_Internet_theory) en realidad. De hecho, Mark Zuckerberg ya confirmó que comenzará a [introducir (o reemplazar) usuarios de sus redes sociales más utilizadas por "bots"](https://www.rollingstone.com/culture/culture-news/meta-ai-users-facebook-instagram-1235221430/). Esto, sumado a su reciente compra de [la red social para IA's](https://gizmodo.com/mark-zuckerberg-decides-meta-needs-more-slop-buys-the-social-network-for-ai-agents-2000731931) pareciera confirmar que cada vez importa menos el aspecto social (y humano) del contenido que nos encontramos en internet.

Sin ir más lejos, foros muy conocidos como Medium [están teniendo inconvenientes](https://www.wired.com/story/ai-generated-medium-posts-content-moderation/) para moderar y evitar esta cantidad excesiva de ["AI Slop"](https://en.wikipedia.org/wiki/AI_slop) debido a la frecuencia y cantidad con la que este mismo contenido se produce y publica en sus plataformas.

La afectación va más allá de lo que nos podemos encontrar en distintas redes sociales o foros, ya que también se descubrió recientemente que existen ["editoriales IA" que producen libros en masa](https://www.insidehook.com/books/ai-generated-books-amazon-authors-publishing-industry), con contenido basura, generado en su totalidad por un LLM, y que se vuelve casi indistinguible para el lector promedio.

No me malentiendan. No estoy en contra de la inteligencia artificial como tecnología, y no considero que sea buena o mala per-sé. \
Es el uso que se le da a esta lo que la puede volver "malvada" o "perjudicial" para el usuario.

>  Recordemos la primera ley de la tecnología de Kranzberg: "La tecnología no es buena ni mala, ni es neutral."

## Que podemos hacer?

{{< img src="images/meme.png" alt="Meme sobre reducción de inteligencia humana" >}}

Soy completamente consciente de que este "mini-post" no va a ser capaz de revertir esta tendencia, y tampoco es lo que busco al escribirlo. \
Mi intención es generar consciencia en el lector, y brindarle algunas herramientas que yo fui recolectando con el tiempo para evitar caer en esto.

> PD: O mejor dicho, caer lo mínimo posible. A veces es inevitable.

### Foros, comunidades gestionadas y/o moderación online

Sé que va a sonar "arcaico", y de cierta forma lo es, pero la mejor manera de asegurarnos de que la inteligencia artificial no esté infectando lo que leemos es volver a lo básico; filtrar y controlar nuestras fuentes de información.

Y cómo podemos hacer eso hoy en día se preguntarán? Yo considero que es una tarea complicada, más no imposible. Sólo tenemos que aprender a identificar las comunidades y "rinconcitos" de internet que aún sean "auténticos".

Por ejemplo, mientras que [XDA Developers](https://www.xda-developers.com/) está completamente [infestado de publicaciones generadas con IA](https://www.facebook.com/groups/linux.fans.group/posts/33045005475114485/), [XDA Forums](https://xdaforums.com/f/artificial-intelligence-ai-general-discussion.12757/) mantiene [estrictas reglas de moderación](https://xdaforums.com/t/using-ai-to-generate-post-content-in-the-forums-is-not-permitted.4704288/) respecto al contenido que allí se publica. \
Dentro de otros ejemplos similares, se pueden encontrar los subreddits, muchas veces (auto)moderados sobre diferentes temas de interés, o páginas que se mantienen fieles a sus raíces, cómo por ejemplo mi querido y amado (Q.E.P.D) [StackOverflow](https://stackoverflow.com/questions).

> PD: Sé que compartí un post de Facebook, no me juzguen :P. \
> Los "grupos" de redes sociales suelen ser también lugares dónde cada publicación se somete a un "escrutinio público" inmediato que filtra contenido basura o generado vagamente con LLM's

En resumen, cualquier comunidad **humana** con la que compartan intereses y también posea este deseo de filtrar este tipo de contenido, en pos de favorecer la **interacción social real**.

> PD 2: Si en algún momento están en duda de si esto es así, pregúntense quién modera el contenido que les está llegando -> Si la respuesta es "un algoritmo", o es incierta, muy probablemente se los haya servido un LLM.

### Aprender a identificar los patrones uno mismo

Puede parecer una tarea imposible, pero con un poco de práctica uno comienza a volverse más habilidoso en el arte de detectar este contenido basura.\
Los modelos de inteligencia artificial funcionan de una forma [muy particular](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), bien definida (aunque no lo parezca), y bajo un sistema de incentivos que los premia por responder o articular "ideas" con ciertas frases, generar explicaciones de cierta forma, o por ejemplo, representar ejemplos usando paralelismos (del tipo "No es X, es Y").

A esto se le suele llamar "tropos" (o "tropes" en inglés), y son fácilmente detectables! \
En [tropes.fyi](https://tropes.fyi/directory) se van a encontrar con un directorio dinámico que lista muchos de estos, además de otras herramientas útiles:

- **AI;DR:** Una herramienta del estilo "mucho texto, no lo leí" (TLDR por sus siglas en inglés) que extrae la idea básica detrás de las pila de textos basura.
- **AI Vetter:**: Un "juez" de IA en publicaciones.

En esta sección también vale la pena mencionar los detectores de contenido IA (cómo pueden ser [GPTZero](https://gptzero.me/) o [Pangram](https://www.pangram.com/)), aunque yo considero que lo mejor es [entrenar](https://en.wikipedia.org/wiki/Wikipedia:AI_or_not_quiz) las habilidades de detección de cada uno.

> Nota: Esto va más allá de textos y publicaciones en internet. Se está poniendo de "moda" usar la IA para responder o chatear entre personas. Por favor, no sean [esta clase de personas](https://stopsloppypasta.ai/en/).

### Fuentes de confianza

> Esta sección de cierta forma solo va a ahondar en la primera, así que perdón si les parece repetitivo (todavía no redacto como IA xD).

La *mejor y única* forma de asegurarnos que el contenido que estamos consumiendo es de confianza, es **confiar** en las fuentes del mismo.\
Sé que parece que estoy haciendo una joda, o que intento explicar "lo obvio", pero en esta era de algoritmos, de "scrollear", de recibir recomendaciones teledirigidas y de consumir sólo lo que nos ponen en frente, nos olvidamos fácilmente que quienes tenemos la potestad de **decidir qué contenido consumimos** o dejamos de consumir somos nosotros mismos!

Esto aplica a todo (ya vimos que ningún sector se salva), así que lo más sencillo es empezar a seleccionar *a conciencia* aquellas fuentes en las que nosotros depositamos nuestra seguridad, y someterlas o auditarlas día tras día!

Una lista de autores de libros que sabemos son de nuestro agrado, un grupo de marcadores con distintos blogs de escritores que estamos seguros son auténticos, recomendaciones de pares en lugar de recomendaciones de algoritmos, litas RSS o feeds Atom para noticias de medios en los que confiemos, etc. \
A esto me refiero cuándo digo la frase "volver a lo básico"; literalmente a las raíces, a cómo se hacía todo, no sólo antes de la IA, sino antes de la normalización de los algoritmos, antes de la estandarización de las redes sociales, y mucho antes de acostumbrarnos a consumir más que a crear.

> Nota: Esta sección final quedó más "reflexiva" (si a esto se le puede llamar reflexión) y no brindé ninguna herramienta nueva, así que, a modo de dejarles algo, les dejo mi página de [contacto](/contacto) por si algún día desean debatir, compartir o reflexionar al respecto <3