+++
author = "Alberto Moyano"
title= "¿Cómo cierran los pliegos?"
date= "2017-06-07"
description = "¿Cómo cierran los pliegos?"
tags = ["LaTeX", "edición", "artes gráficas",]
pin = true
+++

Tiempo atrás, debatía con un colega sobre el inconveniente que existe a la hora de producir libros con programas convencionales de armado en lo referente a la cantidad de páginas.

<!--more-->

Hay libros en donde al terminarlos sobran más de 2 páginas, o que terminan bien en páginas, pero mal a la vista (por la compresión o expansión de caracteres o líneas), o capítulos que tienen todas las notas o pies de página apuntadas en su final (situación aceptable solo cuando son pocas y no molesta a la lectura del texto central).}}

Entonces, frente a la pregunta, ¿qué hacer para solucionarlo?, la respuesta es **nada**, a menos que el editor esté dispuesto a pagar el trabajo de armado nuevamente.

Como le gusta decir a mi socio, por suerte nosotros usamos San LaTeX.

Todos los que armamos libros sabemos que cuando se coloca la última corrección, la primer pregunta que surge es: ¿cómo cierran los pliegos?

No es un detalle menor. El aumento del costo del libro es directo, hay más papel, impresión y encuadernación.

Usando LaTeX la situación cambia al momento de solucionar el inconveniente. Con instrucciones directas del lenguaje se puede formatear el diseño de la página. Pero un muchacho japonés --Hideo Umeki-- escribió el paquete [geometry](https://ctan.org/pkg/geometry) (¡que es impresionante!) que simplifica todo el trabajo. Al momento de formatear opciones en la página, es difícil imaginar que no se puede hacer con él. Yo no utilizo ni el 30% de las opciones que posee y con eso me basta para solucionar gran parte de los inconvenientes al momento de reformatear el libro. El código que dejo a continuación es el que utilizo usualmente:

{{< highlight latex >}}
\usepackage[paperwidth=155mm,
    paperheight=230.00mm,
    textwidth=115.00mm,
    centering,
    includehead,
    includefoot,
    headsep=15pt,
    top=15mm,
    bottom=20mm,
    footskip=0mm,
    footnotesep=5mm plus 4pt minus 4pt]{geometry}
{{< /highlight >}}

Una vez terminado el libro, con solo modificar los valores de ancho (textwidth) se puede formatear íntegramente el texto del libro hasta conseguir la cantidad de páginas que necesitamos para que cierren los pliegos. Existen más opciones con las cuales también se puede llegar a obtener el mismo resultado, esta solo es la más rápida.

Como ejemplo puedo decir que en un trabajo reciente, una corrección de 0.4 mm en el ancho de la caja de texto, permitió llevar un libro de 226 páginas a 224. De más está decir que todas las condiciones estructurales y condicinales del texto se actualizan íntegramente. Nos podemos despreocupar de las llamadas a pie de página, de las referencias cruzadas y los índices entre otras cosas.

