# Práctica 11. Programación Gráfica en JavaScript. Eventos. Curvas de Lissajous.
### Factor de ponderación: 9

### Objetivos
Los objetivos de esta tarea son poner en práctica:
* Conceptos básicos de Programación orientada a eventos en JavaScript.
* Conceptos básicos de Programación Gráfica en JavaScript usando la API Canvas.
* Metodologías y conceptos de Programación Orientada a Objetos en JavaScript.
* Principios y Buenas prácticas de programación Orientada a Objetos.

### Rúbrica de evaluacion del ejercicio
Se señalan a continuación los aspectos más relevantes (la lista no es exhaustiva)
que se tendrán en cuenta a la hora de evaluar esta práctica:
* Se valorará la realización de las diferentes tareas que se proponen.
* El comportamiento del programa debe ajustarse a lo solicitado en este documento.
* Capacidad de la programadora de introducir cambios en el programa desarrollado.
* Conocer y poner en prácticas los principios y buenas prácticas de programación orientada a objetos.
* Deben usarse estructuras de datos adecuadas para representar los diferentes elementos que intervienen en el problema
* Acreditar que se sabe generar informes de cubrimiento de código utilizando tanto 
[Jest](https://jestjs.io/)
como
[CodeCov](https://docs.codecov.com/docs)
* Saber corregir bugs en sus programas utilizando el depurador de Visual Studio Code
* Ser capaz de desarrollar tests unitarios para sus programas utilizando 
[Jest](https://jestjs.io/)
* Acreditar su capacidad para configurar y utilizar 
[ESLint](https://eslint.org/)
  y que es capaz de trabajar con la misma en Visual Studio Code.
* El código ha de estar documentado con 
[JSDoc](https://jsdoc.app/). 
  y ha de acreditarse la capacidad de generar documentación para sus programas utilizando la herramienta.
  Haga que la documentación del programa generada con JSDoc esté disponible a través de una web alojada en su máquina IaaS de la asignatura.
* Ser capaz de resolver problemas de la plataforma Exercism, subiendo sus soluciones a la misma.
* Acreditar que es capaz de desarrollar y ejecutar programas simples de la plataforma Jutge.
* Se comprobará que el código que el alumnado escribe se adhiere a las reglas de la 
[Guía de Estilo de Google para Javascript](https://google.github.io/styleguide/jsguide.html).
* Acreditar que es capaz de editar ficheros de forma remota en su VM usando Visual Studio
  Code (VSC)

### Indicaciones de caracter general
Los programas han de organizarse en torno a clases que se han de implementar usando la sintaxis para
clases ES6 de JavaScript y poniendo en práctica los principios de abstracción y encapsulamiento característicos 
de la Programación Orientada a Objetos.
En los ejercicios han de ponerse en práctica los principios y buenas prácticas que han sido expuestos en las clases de la asignatura.

Vigile siempre el tipo de visibilidad que elige para los atributos (properties) de sus clases
y tenga en cuenta tanto las reglas de 
[estilo](https://google.github.io/styleguide/jsguide.html#features-classes)
como las 
[etiquetas JSDoc](https://stackoverflow.com/questions/41715994/how-to-document-ecma6-classes-with-jsdoc)
relacionadas con el constructo `class`.

Previo a la implementación de cada clase, diseñe y desarrolle un conjunto de tests para probar el correcto
funcionamiento de todos los métodos públicos.

Encapsule las clases en módulos que exporten la correspondiete clase hacia otros programas clientes que pudieran utilizarla.

Configure para la práctica una página web que sirva de índice para mostrar la documentación generada por
JSDoc para todos los ejercicios de la práctica.

Configure un fichero `package.json` en el directorio raíz de su repositorio de modo que ejecutando 
`npm install` queden instaladas todas las dependencias de su proyecto.

### Las curvas de Lissajous
Las 
[curvas de Lissajous](https://es.wikipedia.org/wiki/Curva_de_Lissajous)
son las curvas que recorre un punto sometido a un doble movimiento armónico simple en dos direcciones perpendiculares. 

La forma de la curva depende exclusivamente de la relación entre las frecuencias de los dos movimientos, 
`m/n` y de su desfase *phi*. 
Si `m/ n = 1`, la curva es un segmento, una elipse o una circunferencia en función del desfase. 
Si este cociente es racional, la curva será cerrada, aunque aquí solo se aprecia si `a` y `b` y n son enteros. 
Aunque para algunos valores de `a` y `b`pueda parecer abierta, como `m = n = 1` y `m = 2` y `n = 3` con desfase *phi* = 0, 
en realidad se recorre dos veces, en un sentido y otro. 
En cambio si el cociente es irracional, la curva es abierta y densa en el cuadrado `[0, 1] x [0, 1]`, en el sentido de que 
pasa arbitrariamente cerca de cualquier punto contenido en él.
Consulte 
[esta
referencia](https://www.investigacionyciencia.es/revistas/investigacion-y-ciencia/el-nuevo-coronavirus-796/las-figuras-de-lissajous-18475)
si quiere conocer la historia de estas curvas y
[estos
vídeos](https://www.investigacionyciencia.es/blogs/tecnologia/14/posts/las-figuras-de-lissajous-videos-18493)
si quiere ver las curvas y saber cómo generarlas físicamente.

### La clase *Lissajous*
En esta práctica se propone desarrollar una clase `Lissajous` 
que posibilite la visualización en una página web de curvas de Lissajous.
La clase ha de encapsularse en un módulo ES6 `lissajous.js`.

La visualización de la ejecución del programa se realizará a través de una página web alojada
en la máquina IaaS-ULL de la asignatura y cuya URL tendrá la forma:

`http://10.6.129.123:8080/einstein-albert-lissajous.html` [1]

en la que se incustará un canvas para dibujar las curvas.
Sustituya *Albert Einstein* por su nombre y apellidos en la URL de su página.

Utilice código HTML y CSS para imitar en la medida de lo posible la apariencia de
[esta página](https://academo.org/demos/lissajous-curves/) [2]
que se tomará como referencia.
La página que Ud. diseñe ha de contener exclusivamente el canvas de dibujo de las curvas (área cuadriculada en
la web de referencia9 y una columna con los campos de texto que permitan introducir valores de los parámetros
(columna derecha en la web [2] de referencia.
Se propone además que su página muestre
* Texto explicativo de las curvas de Lissajous
* Enlaces a páginas de referencia que se hayan utilizado para realizar este trabajo.
* Cualquier elemento que les parezca oportuno e interesante

Diseñe asimismo otra página HTML simple 

`http://10.6.129.123:8080/index.html` [3]

que sirva de "página índice" para los ejercicios de la sesión de evaluación de la práctica.
La página [1] será uno de los enlaces de [3] y a su vez [1] tendrá un enlace `Home` que apunte a [3].
Enlace también en la página índice [3] las páginas que contienen los informes de documentación y de
cubrimiento de código de su proyecto.

Tenga en cuenta las siguientes especificaciones a la hora de diseñar su programa:

* Haga que el canvas junto con el área de entrada de datos ocupe la mayor parte del viewport de su navegador.

* La curva comenzará a dibujarse automáticamente una vez cagada la página en el navegador, sin esperar por ninguna interacción por parte del usuario.

* Dote de funcionalidad al botón `Reset` de su página de modo que al actuar sobre él, se reinicie el dibujo
  del camino aleatorio.

El diseño de su página, que ha de imitar el de
[la de referencia](https://academo.org/demos/lissajous-curves/)
brinda una oportunidad para practicar los elementos HTML y CSS que se han estudiado hasta ahora.
No se pretende que se utilicen elementos no estudiados hasta esta fecha.

## Referencias
* [Lissajous Curves](https://academo.org/demos/lissajous-curves/) An interactive demonstration of Lissajous curves
* [ESLint](https://eslint.org/)
* [JSDoc](https://jsdoc.app/)
* [The Modern Javascript Tutorial](https://javascript.info)
* [PAI Code Examples](https://github.com/ULL-ESIT-PAI-2021-2022/PAI-class-code-examples/tree/master/src)
* [Google JavaScript Style Guide](https://google.github.io/styleguide/jsguide.html)
