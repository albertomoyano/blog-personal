+++
author = "Alberto Moyano"
title= "Edición literada"
date= "2021-12-29"
description = "Pequeña reflexión sobre la edición literada"
tags = ["LaTeX", "edición", "academia",]
pin = true
+++

Creo que es posible decir que la edición es íntegramente digital desde comienzo de los noventa, ya que los diferentes intervinientes del proceso editorial, han terminado incorporando a las computadoras en su uso diario para escribir y producir, así también podemos asegurar que hoy las imprentas (por dar un ejemplo del proceso) solo reciben trabajos en formato digital.

<!--more-->

Sin embargo, también es posible observar que la tradición editorial no ha sabido captar --al menos hasta ahora-- que este cambio en la forma de producir, no refiere solo al hecho de utilizar nuevas técnicas, herramientas o dispositivos, sino también a la pérdida de los fundamentos básicos que existen en el proceso de edición.

En este posteo pretendo exponer de manera resumida, una posible mirada a las problemáticas actuales de la edición profesional.

La idea que propongo consiste en trabajar sobre un modelo de edición estandarizada, automatizada, multiformato y multisoporte, o como es conocida: **edición literada**. Para lograr esto es necesario evitar cualquier tipo de enfoque [WYSIWYG](https://es.wikipedia.org/wiki/WYSIWYG) para dar lugar a un enfoque [WYSIWYM](https://es.wikipedia.org/wiki/WYSIWYM).

[Brian Kernighan](blank:#https://es.wikipedia.org/wiki/Brian_Kernighan) dijo alguna vez que el problema con el WYSIWYG (*lo que ves es lo que obtienes*) es que en realidad *lo que ves es **TODO** lo que obtienes*.  Las interfaces gráficas son excelentes para muchas cosas y yo las utilizo de manera constante. Pero también uso la consola con un *Shell* cuando necesito elasticidad, ya que es mucho más conveniente para algunas tareas, ahí entra el WYSIWYM.

## Edición cíclica

Podemos observar en la figura a continuación que la edición cíclica se concentra en la posibilidad de producir al mismo tiempo para varios soportes de salida (un inicio A, deriva en un destino B, C, etc.), tratando de conservar la idea de que la publicación (en nuestro caso un libro) tiene un solo camino a seguir. Este método de trabajo está arraigado en la idea de que el *software* de alguna multinacional haga el trabajo milagroso de hacerlo posible, otorgándonos tranquilidad al concebir la conversión a diferentes formatos. Solo cuando se toma conciencia *real* de la pérdida en la calidad técnica y editorial, se hace patente que la edición cíclica no es el método más óptimo para una producción multiformato y multisoporte.

![](https://albertomoyano.github.io/blog-gbtexpublisher/images/ciclos.png)

Pero es entendible que esto haya pasado, si observamos como era el modelo de producción editorial antes de la era digital.

![](https://albertomoyano.github.io/blog-gbtexpublisher/images/gutenberg.png)

## Edición literada

Cambiemos la perspectiva. ¿Si en lugar de concentrarnos en los diferentes formatos finales, realizamos un ejercicio de pensamiento lateral?[^1] La idea es simple: **no nos concentremos en los formatos de salida, sino en los caminos que conducen a ellos**. La conclusión se hace evidente: a múltiples formatos, múltiples caminos.

Para realizar este modelo de trabajo se utiliza un lenguaje de marcas, es la mejor forma de codificar un documento, ya que se pueden incorporar las marcas que contienen las indicaciones adicionales acerca de la estructura y el diseño necesarios para la representación del texto en la salida deseada.

La figura a continuación nos muestra un posible modelo de edición literada, donde no existe una secuencia de A con B, sino un inicio de (A) con diversos caminos (B, C, D, etc.), algunos pueden frenar su andar (llegar a su destino final), otros se pueden desprender y convertirse en el inicio de otros nuevos caminos.

![](https://albertomoyano.github.io/blog-gbtexpublisher/images/completo.png)

Este es un posible camino, que tiene su base en el lenguaje de marcas [Markdown](blank:#https://es.wikipedia.org/wiki/Markdown), pero también existen otros lenguajes como [asciidoc](blank:#https://asciidoc-py.github.io/index.html) y [Org Mode](blank:#https://orgmode.org/) por ejemplo.

La principal consigna de este método es ir de lo simple a lo complejo. Cada formato de salida tiene sus propias particularidades. Para el PDF de imprenta se requieren ajustes por cuestiones ortotipográficas y de diseño; en el ePub a veces es necesario ordenar figuras o cuadros para una correcta visualización, en una lectura *on line* se puede sacar provecho de la visualización interactiva y así un largo etcétera. Por consiguiente, lo que se hace imperioso es **evitar la herencia de características**, que es el principal problema que tiene la metodología cíclica, a diferencia de esta, la edición literada se inicia con un documento simple de [texto plano](blank:#https://es.wikipedia.org/wiki/Archivo_de_texto) que **contiene solo las marcas** de los elementos estructurales y de diseño, para luego con ajustes automatizados según los diferentes destinos se pueda obtener una salida sin errores.

Ejemplo conceptual de la lógica a seguir, supongamos que tengo una marca de cita:[^cita]

[^cita]: Puede ser cualquier valor de la estructura: título, referencia, fórmula, etcétera.

1. Si la salida es a PDF se aplica «Q» diseño y valor de estructura.
2. Si la salida es a ePub se aplica «X» diseño y valor de estructura.
3. Si la salida es a XML se aplica «Y» diseño y valor de estructura.
4. Si la salida es a HTML se aplica «Z» diseño y valor de estructura.

Cada salida tiene su propia lógica para su destino, subordinada a un solo patrón de diseño estructural.

Furtado[^2] plantea que en una primera aproximación, las ediciones se diferencian entre ellas por la predominancia que tienen las actividades primarias en la transformación físico-técnica del contenido, esto implica que, desde el punto de vista de la edición, el *diseño estructural* goza de muchísimo valor.

## El tiempo y la portabilidad de los contenidos

Scolari[^3] se plantea si podremos leer un PDF dentro de 100 años, su análisis arranca de una premisa equivocada, es equivalente a pensar que alguien en la década del sesenta se preguntara lo mismo sobre el *cassette*. Estos errores de análisis son comunes de encontrar y obedecen a que están atrapados (o enamorados) de las herramientas que utilizan. En 1838 Samuel Morse realizó la invención que hoy nos sigue mostrando cuál es el camino que se debe seguir en las tecnologías digitales.

La edición científica necesita una transformación --esencialmente enriquecedora-- sobre su modelo de producción, a efectos de poder garantizar --sin fechas de vencimiento-- su capacidad de poder mantenerse en el tiempo asegurando el procesamiento y la difusión de sus contenidos. El método elegido para la edición científica, es en gran medida responsable de la calidad de las fuentes de información que produce. Los variados saberes involucrados, le otorgan a esta profesión un desempeño interdisciplinario complejo dentro del campo de la producción del conocimiento.

Me arriesgo a pensar que en esta nueva etapa del desarrollo de los procesos de edición, su reproducción, distribución y conservación, el profesional de la edición seguirá siendo un *cliente* si no adquiere las habilidades necesarias para convertirse en su propio arquitecto.

Matthew Carter en una exposición en el 2014 lo planteó en términos muy simples:

> La pregunta es, ¿una restricción obliga a un compromiso? Aceptando una restricción, ¿estás trabajando a un nivel inferior? (...). La distinción entre una restricción y un compromiso es, obviamente, muy sutil, pero es muy central en mi actitud hacia el trabajo (min. 4:57).

{{< youtube xjxyEwjG2Es >}}

[^1]: De Bono, Edward (1967). [*New Think: The Use of Lateral thinking*](https://books.google.com.ar/books/about/El_pensamiento_lateral_pr%C3%A1ctico.html?id=ir_PDOmfHBwC&printsec=frontcover&source=kp_read_button&hl=es-419&redir_esc=y#v=onepage&q&f=false), Avon Books.

[^2]: Furtado, José Afonso (2014). [*La edición de libros y la gestión estratégica*](https://www.eduvim.com.ar/libro/9789876991735-la-edicion-de-libros-y-la-gestion-estrategica), Córdoba: EDUVIM.

[^3]: Scolari, Carlos (2010) [*¿Podremos leer un PDF dentro de 100 años?*](https://hipermediaciones.com/2010/11/11/%c2%bfpodremos-leer-un-pdf-dentro-de-100-anos/).
