+++
author = "Alberto Moyano"
title= "Composición tipográfica"
date= "2013-06-22"
description = "Editores, procesadores, descriptores y armadores"
tags = ["LaTeX", "procesadores", "editores",]
pin = true
+++

En este artículo se leerán términos que si no son entendidos en su correcto valor pueden originar confusiones, por eso me parece oportuno antes que nada aclarar algunos conceptos.

<!--more-->

**¿Qué es un software editor de textos?** Es un programa que permite escribir texto «plano», es decir que no tiene la posibilidad de dar atributos a lo escrito. ¿Sirve para componer texto? No, sirve para tipearlo. Un ejemplo de este tipo de programas es el Notepad de Windows.

**¿Y qué es un procesador de textos?** Es un programa que sí tiene la posibilidad de volcar atributos al texto. Un ejemplo de este tipo de programas son el Word de Microsoft, el Word Perfect, el AbiWord y el Open Office. Pero están cada vez más alejados del concepto de la máquina de escribir (motivo de origen) debido a la gran cantidad de funciones que tienen. ¿Estos procesadores sí permiten componer texto? No, permiten dar atributos de muchísimos tipos, al punto de confundir, pero no sirven para componer textos.

**¿Qué es PostScript?** Es un lenguaje de computación desarrollado por [John Warnock](https://en.wikipedia.org/wiki/John_Warnock) para la empresa Adobe System. ¿Qué hace este lenguaje? ¿Sirve para escribir programas? ¿Sirve para componer textos? No, es un lenguaje descriptivo que sirve para mostrar contenidos, o dicho de otra manera, es un lenguaje descriptor de páginas. Una variante popularizada del uso de este lenguaje es el PDF (Portable Document Format).

InDesign o Quark-Xpress, son los programas más utilizados en el mercado editorial, tampoco son programas de composición tipográfica. Son programas que le permiten al usuario manipular todo tipo de objetos, incluidas las tipografías, y por esto son conocidos como programas de maquetación «o armado» en los que se puede volcar un diseño.

## Entonces ¿qué es componer…?

Si convenimos que la **composición de textos** es la manera de comunicar el conocimiento a través del discurso escrito, tenemos que estar de acuerdo en que la **composición de textos tipográficos** es el modo en que cada letra se coloca con relación a las demás con sus atributos correspondientes. Por consiguiente si en la forma en que se componen las líneas hay errores de armado, también deben ser revisados desde la óptica del error ortográfico y no solo como errores de diseño, que pueden afectar a la estructura del texto.

El sistema de composición TeX no sirve para describir páginas, sino para hacerlas. Para empezar a editar un texto, es necesario haberlo comprendido al punto de poder estructurarlo como documento. Tenemos que saber qué clase de documento queremos editar (artículo, reseña, libro, transparencia, página web…), qué partes va a tener y cómo vamos a trabajar con los distintos elementos que lo componen (capítulos, secciones, tablas, dibujos, notas, enumeraciones…). En definitiva, tenemos que tener un proyecto.

Una vez hecho esto, TeX se encargará automáticamente de que todos estos elementos estén unificados bajo el estándar de edición que le hemos atribuido, reduciendo el margen de error y respetando, si hemos estructurado el documento con un criterio correcto según ciertas pautas de escritura, el verdadero espíritu del texto que vamos a publicar.

## ¿Y qué es TeX?

Lo primero para aclarar es que TeX es un lenguaje. ¿Es como PostScript? No, pero tiene similitudes, en tanto no es un lenguaje descriptor de páginas, sino un **lenguaje de composición de textos** y una de las posibles salidas que tiene son páginas. De aquí que TeX se asimile a los viejos sistemas de composición y fotocomposición tipográfica, pero adicionando todo el potencial que provee el uso de la programación en computadora. Existen lenguajes derivados que usan el motor de TeX, el más popular es LaTeX.

## Haciendo historia

TeX fue creado por [Donald Ervin Knuth](https://es.wikipedia.org/wiki/Donald_Knuth) y sirve para componer textos, trabajar con datos dinámicos (es decir que no se tipean) y fórmulas, fundamentalmente matemáticas. Knuth empezó a escribirlo en 1977 investigando el potencial de los equipos de impresión digital que estaban comenzando a desarrollarse en la industria de la impresión en aquel momento. En concreto él tenía la esperanza de poder invertir la tendencia de calidad tipográfica en declive que existía y que veía afectaba a sus propios libros y artículos técnicos. El lenguaje tal como lo usamos hoy, fue hecho público en 1984, con algunos sutiles cambios agregados en 1989, principalmente para dar soporte a caracteres de 8 bit y a otros alfabetos del mundo. La última gran modificación se hizo en el 2002, para tener soporte nativo al modelo de escritura Unicode. El lenguaje es muy estable, está llevado a casi todos los sistemas operativos conocidos y prácticamente no tiene fallas. El número de versión de TeX converge hacia pi, la versión actual es 3,141592.

> TeX se pronuncia /tej/. La «j» surge del alfabeto griego donde X es la letra «j» o «ji». TeX es la primera sílaba de la palabra griega *texnología* (tecnología).

Knuth es matemático y por consiguiente es natural entender que el lenguaje que desarrolló esté basado en un principio de la matemática que es la lógica. Dicho de otra manera, no existe la intuición como posibilidad de uso. Si calculamos el resultado de la variable tiempo con la variable esfuerzo para medir la obtención de resultados, veríamos que es inversa a la conseguida cuando se utilizan programas más convencionales. Esto al principio frustra a los usuarios (sean autores o editores) cuando comprueban que tienen que esperar un tiempo (en algunos casos, bastante tiempo) hasta aprender, y poder empezar a ver resultados aceptables; pero esta situación se invierte después. Mi experiencia me muestra que, pasado este  proceso. por cierto algo incómodo, la cantidad de tiempo utilizado es mucho menor para una mayor cantidad de producción, comparado con cualquier procesador de textos o programa de armado de páginas.

Pero, ¿cuál es la base de la lógica de uso de este lenguaje? (dicho más simple: ¿qué hay que saber?). Para usar este lenguaje hay que conocer ciertas pautas estructurales de escritura. Bien es sabido que cuando utilizamos alguno de los programas convencionales del mercado para procesar texto o para armar páginas, tenemos un montón de herramientas disponibles a través de menúes o íconos, pero también nos encontramos ante la ausencia de muchas herramientas, que al sumadas a nuestro desconocimiento de esa necesidad, dan como resultado un escrito con errores. Veamos estos dos ejemplos.

1. Cuando un autor escribe o un editor produce un artículo o un libro y empieza a poner las referencias bibliográficas, utiliza por lo general un modelo de referencia dentro del texto que puede ser plain, autor/año o pie de página[^1] ajustado además a un estándar para la representación bibliográfica de ese modelo, es decir, los datos que son necesarios volcar para cada ítem con su pauta tipográfica y de puntuación. Pero, ¿cuáles son todos esos datos?, este es el punto clave. ¿Qué pasa si como autor o editor no tengo un criterio unificado en la anotación de las referencias bibliográficas de un artículo o libro, utilizando programas convencionales? No pasa nada; simplemente tengo un mal escrito y puedo ni siquiera enterarme. Pero usando TeX simplemente no puedo: el lenguaje no lo permite, TeX incita a los autores y a los editores a procesar textos bien estructurados, porque así trabaja. especificando la estructura.

2. El otro ejemplo simple de ver es el uso de las comillas. La introducción de la computadora a la vida cotidiana trajo cambios de hábitos en nuestra escritura; en el español usar en primera instancia las comillas voladas dobles es una situación que sería menos gravosa sino fuera porque estas comillas se emplean en el español, pero en el segundo nivel. Por consiguiente su uso incorrecto debe ser mirado como un error ortográfico con el mismo valor de cuestionamiento que tiene escribir papa (en vez de papá), cuando queremos hablar de nuestro padre. En TeX las comillas no se escriben, «se marcan», y el sistema se encarga de saber a qué nivel pertenecen, controlar que la apertura tenga su correspondiente cierre y qué idioma arrastra la palabra, para así colocar el tipo de comilla correcta.

¿Se vuelve tedioso producir un texto en este lenguaje? Para nada. Una vez adquirido el conocimiento, existen una enorme cantidad de tareas que no se necesitan hacer. En el caso de las referencias bibliográficas por ejemplo, el lenguaje maneja de manera automática el sistema de puntuación, es decir que el autor o editor no necesita preocuparse por si va punto, coma, punto y coma, paréntesis o corchetes al momento de hacer la construcción de la salida final del escrito. En síntesis, no existe la preocupación por el formato de la referencia, ya que el mismo se hará ajustándose al estándar que se haya decidido utilizar.

## ¿Cómo se usa?

Para usar TeX, lo primero es conseguir una distribución, la licencia GPL permite la libre distribución (léase es gratis). Se llama distribución al lenguaje para una cierta plataforma o sistema operativo con una serie de programas y utilidades complementarias. Cada distribución incluye complementos distintos y por lo tanto las hay más o menos completas en función de su objetivo de ser más básicas o más avanzadas, incluso las hay portables.

Las distribuciones no siempre contienen un editor de texto específico y en ese caso conviene tener uno. Las distribuciones más importantes que podemos encontrar al día de hoy son:

1. Multiplataforma: [TeXLive](https://www.tug.org/texlive/)
2. Windows: [MikTeX](https://miktex.org/)
3. MacOS: [MacTeX](https://tug.org/mactex/)

### Los editores de texto mas populares utilizados son:

1. Multiplataforma: [TeXMaker](https://www.xm1math.net/texmaker/), [TeXwork](https://tug.org/texworks/), [TeXstudio](https://www.texstudio.org/)
2. Windows: [TeXnicCenter](https://www.texniccenter.org/)
3. MacOS: [TeXShop](https://pages.uoregon.edu/koch/texshop/)

### Para el manejo de referencias bibliográficas:

1. Multiplataforma: [JabRef](https://www.jabref.org/)

### ¿Cómo funciona?

El proceso consta de tres pasos:

1. Introducción del texto.
2. Preparación del formato.
3. Presentación de la salida.

Mientras que los programas convencionales unen el primer paso con el tercero y ocultan o eliminan el segundo, TeX deja los tres pasos separados de forma que se puedan controlar y automatizar más fácilmente; de esta manera no hay atadura respecto de qué editor de textos usar, no importa en qué plataforma sea preparado y no hay restricción para la salida que se desee.

Algunos programas intentan adaptarse a este método de trabajo, como los programas FrameMaker de la empresa Adobe, o Pageflex de la empresa Bitstream, pero el concepto de funcionamiento de los programas WYSIWYG (acrónimo de What You See Is What You Get, en inglés, «lo que ves es lo que obtienes») hace que su adaptación a este modo de producción no sea nada fácil. A mi juicio el programa (ya descontinuado) que más se aproximo a esta idea de uso haya sido Ventura Publisher.

> No confundir esto, TeX trabaja sobre la estructura semántica y ortotipográfica del texto, al margen de parametrizar los atributos de la tipografía.

Otra ventaja de este método de trabajo es que un error de TeX en el paso 2 no corrompe el archivo de texto original (producido en el paso 1), ya que este no se toca al componerlo, al contrario de lo que sí puede pasar en los sistemas que manipulan un único archivo. Esto incrementa la seguridad en su uso y evita perder tiempo y trabajo; también se obtiene con este método de trabajo un menor peso de los archivos, en algunos casos muy sustancial.

## TeX y LaTeX

Existe una confusión, bastante común de encontrar entre los usuarios nuevos, y es el nombre del lenguaje que se usa, TeX es el motor, es la base de todo, LaTeX es un metalenguaje que utiliza a TeX como base, por lo general se utiliza LaTeX por ser más ameno y fácil de comprender, pero se sabe que es TeX quien hace el trabajo «duro».

## ¿Por qué trabajar con LaTeX?

Creo que son muchos motivos para editar con LaTeX, pero los más significativos que podría enumerar son:

1. Tiene licencia GPL (General Public License).
2. Multiplataforma, corre bajo Windows, MacOS y todas las variantes de Unix incluido GNU/Linux.
3. Control de guionizado por palabra (silábico o etimológico).
4. Escritura en múltiples idiomas en simultáneo (de izquierda a derecha y viceversa).
5. Soporte nativo para Unicode
6. Manejo de ligaduras (soporte para escritura en lenguas que se basan en el principio de las raíces, por ej. arabe).
7. Contadores separados para cada parte del artículo o libro con hasta niveles de seguimiento (por ejemplo 1.1.1.1.1.1).
8. Sistema de indexación para objetos,[^2] usados para generar índices de todo tipo.
9. Distinta salida final (RTF, PS, PDF, HTML) desde el mismo archivo.
10. Comillas inteligentes.
11. Llamadas a pie o margen de página con tolerancia para edición crítica (ajustados al estándar de la Universidad de Oxford para textos socráticos).
12. Soporte para edición bilingüe en paralelo.
13. Sin límite de páginas (en un ejercicio lo he probado hasta la página 15.300).
14. Foliado continuo entre libros (libro multivolumen).
15. Tratamiento automático de referencias cruzadas.
16. Uso de condicionales (por ejemplo If) en tiempo de compilación.

El listado se hace interminable, debido a que LaTeX es un lenguaje basado en la programación literal.

## Conclusión

Los primeros usuarios de TeX han sido principalmente matemáticos o científicos provenientes de las ciencias llamadas «duras», pero es algo que solo tiene que ver con la historia. Ellos fueron los que crearon el sistema. Luego de quedar instrumentado como sistema de facto en el mundo de las matemáticas, los primeros ambientes científicos que se acercan a TeX provienen del área de las ciencias médicas quedando para el final las ciencias sociales, aunque no por eso dejan de tener un gran peso en el desarrollo de extensiones complementarias, que facilitan el uso del lenguaje.


[^1]: Es importante aclarar que para referencias bibliográficas solo existen los 3 modelos mencionados, cada uno de ellos tiene múltiples estándares generalmente desarrollados por universidades o instituciones. La American Psychological Association (APA) y la Universidad de Harvard, por citar 2 estándares conocidos, utilizan el modelo autor/año y tienen diferentes intereses sobre qué datos son considerados obligatorios volcar y cuáles son opcionales en la representación de la bibliografía.

[^2]: Todo puede ser interpretado como un objeto, incluso un glifo tipográfico.


