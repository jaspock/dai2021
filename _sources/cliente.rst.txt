.. role:: problema-contador

Programar el lado del cliente
=============================

JavaScript es un lenguaje orientado a objetos, funcional, dinámico e interpretado, usado principalmente como el lenguaje de programación de las páginas web en el lado del navegador. Actualmente, sin embargo, se usa también en la parte del servidor en entornos como Node.js o MongoDB. El nombre del estándar que regula JavaScript es ECMAScript. Los navegadores recientes entienden las últimas versiones de ECMAScript; cada año se publica una nueva versión (por ejemplo, ECMAScript 2020, también conocido como ES11).

.. Important::

  Las habilidades que deberías adquirir con este tema incluyen las siguientes:

  - Comprender los elementos básicos de JavaScript como lenguaje de programación orientado a objetos.
  - Saber programar en JavaScript la parte del cliente de una aplicación web usando la API de los navegadores para la gestión del DOM, eventos, estilos, etc.
  - Usar las herramientas para desarrolladores integradas en los navegadores, como Chrome DevTools, para depurar un programa escrito en JavaScript.


.. _label-intro-js:

Introducción al lenguaje de programación JavaScript
---------------------------------------------------

.. admonition:: Hazlo tú ahora
  :class: hazlotu

  Estudia todos los vídeos de la serie "Introducción a JavaScript" en los que se presentan los elementos principales del lenguaje: `parte 1-1`_, `parte 1-2`_, `parte 1-3`_, `parte 1-4`_, `parte 1-5`_ y `parte 1-6`_.

  .. _`parte 1-1`: https://drive.google.com/file/d/1p3ThE3xA1ubg3jJXFd968ucwckVpayKy/view?usp=sharing
  .. _`parte 1-2`: https://drive.google.com/file/d/1MgFD19HaWSPo6P_CnPUFF6kmCLJJowEx/view?usp=sharing
  .. _`parte 1-3`: https://drive.google.com/file/d/1GInxvZFxgt8GcS2cWzbMRWEDpNi0kHmG/view?usp=sharing
  .. _`parte 1-4`: https://drive.google.com/file/d/1SrmuNde9DeOoOOClZ2WDGbf-aZH4vi33/view?usp=sharing
  .. _`parte 1-5`: https://drive.google.com/file/d/15Z-leYRlWbMmPWQZczqakCt0q3jMLAcJ/view?usp=sharing
  .. _`parte 1-6`: https://drive.google.com/file/d/1uP37JivyhSZeEgqwzcD57CznQwzLqS-Z/view?usp=sharing

Elementos más avanzados del lenguaje o las características adicionales a las que un programador puede acceder cuando escribe programas en JavaScript para ser ejecutados por un navegador se estudiarán más adelante. Los conceptos que tienes que comprender del lenguaje se encuentran recogidos en `estas diapositivas`_, que también contiene información sobre elementos más avanzados que estudiaremos más adelante.

.. _`estas diapositivas`: _static/slides/150-js-slides.html

.. admonition:: Hazlo tú ahora
  :class: hazlotu

  Practica con los diferentes conceptos de JavaScript hasta tener claro su uso. Puedes practicar usando la consola de JavaScript de las Chrome Devtools, instalando Node.js, abriendo una `consola en línea`_ o creando un proyecto en `repl.it`_ de tipo Node.js. 

  .. _`consola en línea`: https://jsconsole.com/
  .. _`repl.it`: https://repl.it/


.. _label-app-web-sencilla:

Una aplicación web sencilla
---------------------------

El código que se incluye más abajo muestra *en acción*, a modo de introducción, los elementos básicos del lenguaje JavaScript (variables, condicionales, bucles, funciones, etc.), así como la utilización de las APIs del navegador relacionadas con la gestión del DOM, de los eventos o de los estilos, para, con todo ello, presentar una `aplicación web muy sencilla`_ que permite añadir dinámicamente contenido a una página web e interactuar con el contenido añadido. 

.. _`aplicación web muy sencilla`: _static/data/ejemplo-apis-js.html

.. admonition:: Hazlo tú ahora
  :class: hazlotu

  Lee los comentarios para entender el propósito de cada línea, pero ten en cuenta que en actividades posteriores ampliaremos estos elementos. Estudia después todos los vídeos de la serie "Una aplicación web sencilla con JavaScript" en los que se comenta este código con detalle: `parte 2-1`_, `parte 2-2`_, `parte 2-3`_, `parte 2-4`_ y `parte 2-5`_. Repasa después, otra vez, el código y asegúrate de que ahora comprendes mejor cada una de sus instrucciones.

  .. _`parte 2-1`: https://drive.google.com/file/d/1YUI7AIgzHO9vcGnmxJ9h84YyEZy9MnXi/view?usp=sharing
  .. _`parte 2-2`: https://drive.google.com/file/d/1g_enM9nz9iVIsGJYmV_HOUORdIs6PUeA/view?usp=sharing
  .. _`parte 2-3`: https://drive.google.com/file/d/1Iw6z9tf4Jc-XztH7sDa16LANPVF56xDw/view?usp=sharing
  .. _`parte 2-4`: https://drive.google.com/file/d/1Py4eM_Zu8EHW6hIqw1JXktSVnGuSw47j/view?usp=sharing
  .. _`parte 2-5`: https://drive.google.com/file/d/16ZE7bQHXPTcRO7xCbqml_9m-nsenmgBB/view?usp=sharing


.. literalinclude:: _static/data/ejemplo-apis-js.html
  :language: html
  :linenos:

Ámbitos y clausuras
~~~~~~~~~~~~~~~~~~~

Las clausuras y su relación con las variables declaradas con ``var`` o ``let`` es uno de los aspectos que más cuesta entender a los programadores que acaban de empezar con JavaScript. Existen cuatro tipos de ámbitos para las variables en JavaScript:

- ámbito de función: corresponde a las variables locales declaradas con ``var``; estas variables se almacenan en la pila y pueden usarse incluso antes de haber sido definidas; esto es así por un mecanismo conocido como *izado* (*hoisting*) que aupa las declaraciones de variables locales (pero no sus inicializaciones) al comienzo de la función; declarar dos o más veces una variable con ``var`` dentro de la misma función equivale a declararla una sola vez al comienzo de esta; si intentamos leer el valor de una variable antes de su declaración en el código y antes de haberle asignado ningún valor obtenemos el valor *undefined*;
- ámbito de bloque: corresponde a las variables locales declaradas con ``let``; estas variables se almacenan en la pila también, pero no hay ningún proceso de izado y la variable se circunscribe al ámbito en el que ha sido declarada; dos variables declaradas en ámbitos diferentes de una misma función tienen espacios separados en la pila; no se pueden declarar dos variables de este tipo con el mismo nombre dentro del mismo contexto; si se declara una variable con ``let`` dentro de un bucle, se reserva sitio en la pila para una variable distinta en cada iteración;  el uso de ``let`` está permitido en el lenguaje desde la versión 6 de ECMAScript, publicada en 2015, por lo que es normal que encuentres muchos ejemplos de código que no lo usan;
- ámbito global: corresponde a las variables globales declaradas fuera de cualquier función; estas variables se almacenan en el *heap* y sus declaraciones también son *izadas* al principio del ámbito global;
- ámbito léxico: corresponde al hecho de que una función definida dentro de otra función puede acceder a las variables locales de esta última; si una función interna *sobrevive* a la función contenedora, las variables referenciadas no se borran de la memoria (a la asociación entre la función y las variables externas se le conoce como *clausura*);

Las declaraciones de funciones locales y globales también sufren el mecanismo de izado en sus ámbitos respectivos.

Estudia el siguiente código y ejécutalo después de dedicar un rato a pensar qué valores imprime por la consola.


.. code-block:: javascript
  :linenos:

  function f() {
    var i = 0;
    var x = {};
    {
      var i = 0;
      x.f1 = function() {
        console.log(i);
      };
    }
    i++;
    {
      var i = 1;
      x.f2 = () => { console.log(i); };
    }
    i++;
    return x;
  }

  var x = f();
  x.f1();
  x.f2();

.. |
.. la barra introduce una línea en blanco en restructured text

La variable ``i`` se declara con ``var`` y, por tanto, su ámbito es el de la función ``f``. No importa que usemos ``var`` varias veces a continuación dentro de la función, incluso aunque estas declaraciones adicionales estén dentro de un nuevo ámbito. En la pila de ejecución solo se reserva sitio para una variable cuando se ejecuta la función y esta única posición es la que no se destruye al salir de la función debido a las clausuras que se crean por las dos funciones anónimas asignadas a ``x.f1`` y ``x.f2``. La variable ``i`` vale 2 al salir de la función y este valor es el que se usa al llamar a las dos funciones.

.. Note::

  Observa de paso que para introducir nuevos ámbitos no es necesario usar una instrucción condicional o un bucle, sino que en JavaScript, como en la mayoría de lenguajes, basta con encerrar un bloque de código entre llaves para conseguirlo.

Sin embargo, si usamos ``let`` en lugar de ``var`` en las declaraciones de ``i``, el ámbito de cada variable será el del bloque y tendremos tres variables distintas en la pila de ejecución justo antes de salir de la función. La primera de ellas será destruida en ese momento, pero las otras dos se *salvarán* de dicha destrucción para mantener las clausuras:

.. code-block:: javascript
  :linenos:

  function f () {
    let i=0;
    let x= {};
    {
      let i=0;
      x.f1= function() {
        console.log(i);
      };
    }
    i++;
    {
      let i=1;
      x.f2= () => {console.log(i);};
    }
    i++;
    return x;
  }

  let x= f();
  x.f1();
  x.f2();


Las APIs del navegador para programar el lado del cliente
---------------------------------------------------------

Los navegadores incluyen una serie de librerías estandarizadas para programar la parte de la aplicación web que se ejecuta en el navegador (lo que se conoce como el *front-end* de la aplicación, en oposición al *back-end*, que denotaría la parte del servidor). En esta actividad profundizaremos en las APIs para el manejo del árbol DOM, la gestión de eventos y el control de estilos. Otras APIs, como la que permite realizar peticiones asíncronas desde el cliente a un servidor, se explorarán más adelante.

Los conceptos que tienes que estudiar de estas APIs se encuentran recogidos en `estas otras diapositivas`_.

.. _`estas otras diapositivas`: _static/slides/150-apidom-slides.html

.. admonition:: Hazlo tú ahora
  :class: hazlotu

  Lee el `capítulo sobre el Document Object Model`_ del libro "Client-Side Web Development", donde se explican las principales funciones de las APIs ya mencionadas. Puedes practicar con la consola de JavaScript de las Chrome Devtools o con entornos como `JSFiddle`_.

  .. _`capítulo sobre el Document Object Model`: https://info340.github.io/dom.html
  .. _`JSFiddle`: https://jsfiddle.net/

Herramientas para desarrolladores
---------------------------------

Las herramientas para desarrolladores que incorporan los navegadores permiten depurar el código en JavaScript de la parte del cliente de una aplicación web.

.. admonition:: Hazlo tú ahora
  :class: hazlotu

  Familiarízate con las opciones de depuración de JavaScript de las pestañas :guilabel:`Console` y :guilabel:`Sources` del entorno de las Chrome DevTools siguiendo estas páginas de su documentación: `Console Overview`_ , `Get Started`_, `Pause your Code with Breakpoints`_ y `JS Debugging Reference`_. Practica las distintas posibilidades en DevTools con una aplicación web como la de la primera actividad de este tema.

  .. _`Console Overview`: https://developers.google.com/web/tools/chrome-devtools/console
  .. _`Get Started`: https://developers.google.com/web/tools/chrome-devtools/javascript
  .. _`Pause your Code with Breakpoints`: https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints
  .. _`JS Debugging Reference`: https://developers.google.com/web/tools/chrome-devtools/javascript/reference


Profundizar en JavaScript
-------------------------

JavaScript tiene obviamente muchos más elementos que los que hemos explorado en este tema. Si quieres ampliar por tu cuenta tu conocimiento del lenguaje, puedes seguir con referencias como `The Modern JavaScript Tutorial`_ o `Eloquent JavaScript`_.

.. _`The Modern JavaScript Tutorial`: https://javascript.info/
.. _`Eloquent JavaScript`: https://eloquentjavascript.net/
