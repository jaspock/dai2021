
Enunciados de las prácticas
===========================

Calendario
----------

Este es el calendario de cada uno de los entregables de la asignatura. No se admitirán entregas fuera de plazo.

.. list-table::
    :widths: 15 40 15 15 15
    :header-rows: 1
    :class: tablita

    * - Entregable
      - Título
      - Fecha límite de entrega
      - Tiempo medio estimado de realización
      - Porcentaje en la nota de prácticas
    * - Práctica #1
      - `Una página web con HTML5`_
      - 8 octubre 2020
      - 8 horas
      - 20%
    * - Práctica #2
      - Una aplicación web local
      - 29 octubre 2020 (provisional)
      - 12 horas
      - 25%
    * - Práctica #3
      - Una aplicación con acceso a servicios web de terceros y con componentes web
      - 19 noviembre 2020 (provisional)
      - 8 horas
      - 15%
    * - Práctica #4
      - Una aplicación con componentes web
      - 3 diciembre 2020 (provisional)
      - 4 horas
      - 10%
    * - Práctica #5
      - Una aplicación en la nube
      - 23 diciembre 2020 (provisional)
      - 18 horas
      - 30%


Instrucciones de entrega de las prácticas
-----------------------------------------

Realiza tu entrega en un único fichero comprimido a través del `servidor web del Departamento`_ antes de las 23.59 del día de la fecha límite. Recuerda que no se admitirán entregas fuera de plazo.

.. _`servidor web del Departamento`: https://pracdlsi.dlsi.ua.es/index.cgi?id=val


Una página web con HTML5
------------------------

En esta práctica vas a crear un documento HTML5 en el que *todo* el formato recaiga en hojas de estilo CSS (por tanto, no es posible usar atributos como ``style`` para el formato). Tu documento se llamará ``index.html`` y tendrá dos vistas diferentes, *normal* (la vista por defecto) y *compacta*; el usuario podrá cambiar de vista en cualquier momento usando los enlaces a pie de página. El objetivo es que consigas un documento que se muestre exactamente como puedes ver en estas imágenes de la `vista normal`_ y de la `vista compacta`_. Tu documento usará tres hojas de estilo: una con todo el contenido común a ambas vistas y dos más correspondientes a cada una de las vistas. Para poder alternar entre ambas hojas de estilo, añade este código a la cabecera (``head``) de tu página:

.. _`vista normal`: _static/img/p1-vista-normal.png
.. _`vista compacta`: _static/img/p1-vista-compacta.png
.. _`este código`: http://www.omnimint.com/A6/JavaScript/Change-external-CSS-stylesheet-file-with-JavaScript.html

.. code-block:: html

    <script type="text/javascript">
      function changeCSS(cssFile) {
        var oldlink = document.getElementById("estilo");
        var newlink = document.createElement("link")
        newlink.setAttribute("rel", "stylesheet");
        newlink.setAttribute("type", "text/css");
        newlink.setAttribute("id", "estilo");
        newlink.setAttribute("href", cssFile);
        document.getElementsByTagName("head")[0].replaceChild(newlink, oldlink);
      }
    </script>

Recuerda también añadir posteriormente este código en el pie de la página cuando lo crees:

.. code-block:: html

    <a href="#" onclick="changeCSS('./css/normal.css');">Vista normal</a> |
    <a href="#" onclick="changeCSS('./css/compact.css');">Vista compacta</a>

Añade, finalmente, un elemento como este a la cabecera de tu documento para que la vista normal sea la que se muestre por defecto:

.. code-block:: html

    <link id="estilo" rel="stylesheet" type="text/css" href="./css/normal.css">

Es muy importante que cuando implementes tu solución te asegures de que respetas **estrictamente** estas instrucciones, incluidos los nombres de identificadores, nombres de fichero, etc.; respeta las mayúsculas y minúsculas, las tildes, la posición de cada elemento en el documento, etc.

Marcado
~~~~~~~

Comienza preparando el documento HTML, sin tener en cuenta, por ahora, los aspectos estilísticos. El documento HTML seguirá los principios del lenguaje estudiados en clase. En particular, tendrá:

- una cabecera (elemento ``header``) que incluya el título (elemento ``h1``), el párrafo descriptivo y el índice (el índice será un elemento de tipo ``nav`` que incluirá una lista no numerada, ``ul``), los tres como descendientes inmediatos (hijos) del elemento ``header``;
- la cabecera irá seguida de un fragmento principal (encerrado en el elemento ``main``) que incluirá ambos cuestionarios;
- la página acabará con un pie de página (elemento ``footer``) con tus datos y los enlaces para cambiar la vista; encierra tu nombre de usuario de ``alu.ua.es`` (por ejemplo, ``zawm``) en un ``span`` (hijo de ``footer``) con identificador ``nombre``; utiliza el carácter ``'|'`` en el documento HTML para separar los diferentes contenidos del pie de página.

Cada cuestionario estará incluido en su propia sección (mediante sendos elementos ``section``, que han de incluir atributos ``id``, con valores ``paris``, sin tilde y todo en minúsculas, y ``londres``, todo en minúsculas, que serán referenciados desde el índice) y tendrá un título de segundo nivel (un elemento ``h2``, que será hijo de ``section``) que incluirá una imagen (que no ha de coincidir necesariamente en tu solución con la de este enunciado, pero no ha de tener tamaño superior a 512x512 píxeles) seguida del texto del título tal como sigue:

.. code-block::

    <section ...>
      <h2 ...>
        <img ...>
        Cuestionario sobre...
      </h2>

La forma de codificar cada pregunta será la siguiente:

.. code-block:: html

    <div class="bloque">
      <div class="pregunta">
      La ciudad de París se sitúa a ambos lados del río Sena.
      </div>
      <div class="respuesta" data-valor="true">
      </div>
    </div>

El contador de pregunta se ha de inicializar para cada nuevo cuestionario. El atributo ``data-valor`` es un atributo personalizado de HTML que usaremos para almacenar la respuesta (true/false) a la pregunta. En general, no es posible añadir a un elemento atributos que no estén especificados en el estándar excepto si estos comienzan por el prefijo ``data-``. 

Tanto los números de pregunta como el texto usado en la página para indicar la respuesta correcta no pueden aparecer explícitamente en el documento HTML, sino que han de ser generados dinámicamente desde CSS.

Estilo
~~~~~~

Una vez tengas el documento HTML finalizado, puedes pasar a diseñar las hojas de estilo. Para el contador de preguntas, añade un número secuencial a cada pregunta obtenido automáticamente mediante un uso adecuado de los `contadores de CSS`_. Para las respuestas usa los `pseudoelementos CSS`_ ``::before`` y ``::after``.

.. _`contadores de CSS`: https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Counters
.. _`pseudoelementos CSS`: http://www.smashingmagazine.com/2011/07/13/learning-to-use-the-before-and-after-pseudo-elements-in-css/

Se describen a continuación las características comunes de ambas vistas:

- la página completa (elemento ``body``) tiene fondo blanco, letra de color ``#333333`` y no tiene margen (esto es, el margen se ha de establecer explícitamente a cero);
- la cabecera (elemento ``header``) tiene un ancho máximo de 1080px y márgenes automáticos a derecha e izquierda; su ancho, además, es el 98% del de la página para que siempre haya un pequeño margen entre el contenido de la página y la ventana del navegador; el texto de la cabecera está centrado;
- los encabezados de nivel 1 usan letra negrita de 36px;
- los encabezados de nivel 2 usan letra negrita de 25px;
- el índice no usa ningún adorno especial de lista; los enlaces del índice no aparecen subrayados; lo único que los identifica como enlaces es su color (``cornflowerblue``) y el hecho de que el cursor del ratón cambia al pasar sobre ellos;
- el fragmento principal (elemento ``main``) tiene un ancho máximo de 1080px y márgenes automáticos a derecha e izquierda; su ancho, además, es el 98% del de la página para que siempre haya un pequeño margen entre el contenido de la página y la ventana del navegador;
- la sección correspondiente a cada cuestionario tiene un margen superior de 80px;
- cada pregunta (selector ``.pregunta``) tiene un margen superior e inferior de 1ex;
- el texto en otro idioma (*arrondissement*) se marca con la clase *idioma* (usa un elemento ``span`` para rodear la palabra) y se muestra en itálica;
- la imagen junto al título de cada cuestionario está alineada verticalmente con la parte superior de la línea (``text-top``) y se escala *mediante CSS* a un tamaño de 50x50 píxels; la separa del encabezado un margen de 10px por la derecha; la imagen tiene un borde de 1px sólido de color ``lightgray``;
- el pie de página (elemento ``footer``) tiene una altura de 50px y un margen superior de 100px; el color de fondo es ``steelblue`` y su anchura abarca el 100% de la ventana del navegador; el texto de una sola línea incluido usa una letra de tamaño 80% de color ``white``, excepto para los enlaces, que usan color ``lightgray``; el texto, además, está centrado verticalmente, lo que puedes conseguir siguiendo la primera recomendación de `esta respuesta`_; ten en cuenta, además, que si el tamaño de la ventana de tu navegador es superior al tamaño de la página (lo que puede suceder si abres la página sin haber añadido los diferentes cuestionarios), el pie de página no quedará pegado al borde inferior de la ventana; el comportamiento anterior es correcto y no has de cambiarlo.

.. _`esta respuesta`: http://stackoverflow.com/questions/9249359/is-it-possible-to-vertically-align-text-within-a-div/14850381#14850381

Las características particulares de la vista compacta son:

- usa el tipo de letra Ubuntu_ para todo el documento; para ver cómo usar en tus estilos un tipo de letra de Google Fonts, haz clic en :guilabel:`Select this font` en la página correspondiente al tipo de letra y después haz clic en la caja que aparece en la parte inferior de la ventana;
- cada pregunta/respuesta (selector ``.bloque``) tiene  un margen superior de 10px e inferior de 20px.

.. _Ubuntu: https://fonts.google.com/specimen/Ubuntu?selection.family=Ubuntu
.. _`página correspondiente al tipo de letra`: https://fonts.google.com/specimen/Ubuntu?selection.family=Ubuntu

Las características particulares de la vista normal son:

- usa el tipo de letra Droid Serif  para todo el documento; la web que describía_ este tipo de letra ya no está en Google Fonts, pero puedes seguir usándola añadiendo lo siguiente a tu página:

.. _describía: https://fonts.google.com/specimen/Droid+Serif

.. code-block:: html

    <link href='https://fonts.googleapis.com/css?family=Droid+Serif' rel='stylesheet' type='text/css'>

y lo siguiente a tu hoja de estilo:

.. code-block:: css

  font-family: 'Droid Serif', serif;

- cada pregunta/respuesta (selector ``.bloque``) tiene un fondo de color ``whitesmoke``; su borde es sólido de 1px de ancho y color ``lightgray``; el margen superior es de 10px y el inferior de 20px; el relleno (*padding*) es de 10px; la sombra de la caja se obtiene dando el siguiente valor a la propiedad CSS ``box-shadow`` (averigua para qué sirve cada parámetro):

.. code-block:: css

    box-shadow: 6px 6px 3px slategray;

Aunque es una práctica habitual, no resetees a cero los márgenes y el relleno de todos los estilos del documento mediante una regla que use el selector universal ``*``.

Recomendaciones finales
~~~~~~~~~~~~~~~~~~~~~~~

Asegúrate de que tus ficheros se validan correctamente con los validadores HTML5 y CSS del W3C (usando la pestaña :guilabel:`Validate by File Upload` en ambos casos). Además, usa Chrome DevTools para comprobar que el estilo aplicado en cada punto del documento es correcto. Finalmente, asegúrate de que cumple con todas las especificaciones de este enunciado (por ejemplo, los nombres o valores de atributos, elementos o ficheros).

Recuerda poner tu usuario de la cuenta de ``alu.ua.es`` (pero sin la arroba y el dominio) en el pie del documento. Realiza tu entrega en un único fichero comprimido llamado ``p1-dai.zip`` a través del `servidor web del Departamento`_. El archivo comprimido contendrá directamente (sin ninguna carpeta contenedora) el fichero ``index.html``, una carpeta ``css`` con los ficheros con las hojas de estilo que hayas usado y una carpeta ``img`` con las imágenes.

Por último, coloca en algún punto del pie de la página un fragmento de HTML como ``<span id="tiempo">[5 horas]</span>`` donde has de sustituir el 5 por el número de horas aproximadas que te haya llevado hacer esta prática.

.. _`servidor web del Departamento`: https://pracdlsi.dlsi.ua.es/index.cgi?id=val




.. _label-ampliaciones:

Ejemplos de posibles ejercicios para el examen práctico
-------------------------------------------------------

Este apartado muestra algunos ejemplos de posibles ejercicios para el examen práctico. Un examen típico incluiría solo uno de ellos, pero sería posible también que hubiera dos o más ejercicios de menor complejidad. El tiempo de realización del examen suele estar en torno a los 110 minutos. No podrás hacer estos ejercicios hasta que hayas acabado la práctica 4, ya que se basan en ella. Ejercicios adicionales con los que podrías practicar son:

- permitir hacer un cuestionario *público* de forma que pueda consultarse a través de una URL propia;
- permitir que un cuestionario pueda borrarse sin necesidad de borrar anteriormente todas sus preguntas;
- permitir que los cuestionarios o las preguntas puedan moverse *arriba o abajo* en la ventana de la aplicación para ponerlos en un orden concreto;
- permitir que las preguntas puedan editarse;
- permitir que la aplicación use otros servicios web de terceros; posiblemente se te ocurran ideas cuando repases esta `lista de APIs públicas`_;
- cualquier otra modificación de complejidad similar que se te pueda ocurrir; inspírate para ello en las aplicaciones web que usas, especialmente en aquellas que se basan en gestionar *listas de listas*.

.. _`lista de APIs públicas`: https://github.com/toddmotto/public-apis

Colapsar los enunciados de las preguntas
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Modifica tu práctica 4 para que junto al título de cada cuestionario aparezca un elemento (un botón, por ejemplo) que permita colapsar o expandir la lista de preguntas asociadas a dicho cuestionario. Mientras la lista de preguntas esté colapsada, las preguntas no se mostrarán en pantalla, ni siquiera cuando se añada una nueva pregunta al cuestionario correspondiente. Cuando la lista de preguntas esté expandida, el comportamiento de la aplicación será similar al actual.

El estado colapsado/expandido de un cuestionario se almacenará en la base de datos y se mantendrá aunque la aplicación se recargue. Al crear un nuevo cuestionario, este estará por defecto expandido.

Para obtener la máxima nota será necesario, además, que cuando el cuestionario esté colapsado se indique el número de preguntas ocultas existentes.

Lo siguiente son algunos consejos relativos a la implementación que no es obligatorio que sigas. Únicamente se dan a modo de recomendación y pueden estar más o menos incompletos según como sea tu implementación.

- Cada entrada de la tabla de cuestionarios de la base de datos tendrá un nuevo atributo (llamado, por ejemplo,  ``colapsado``) que almacenará su estado de colapso.
- Comienza implementando dos servicios web: uno que devuelva en formato JSON el estado de colapso de un determinado cuestionario (referenciado mediante su id) y otro para cambiarlo.
- Para crear los servicios web anteriores, te puedes inspirar en los servicios que ya has implementado para listar cuestionarios o preguntas.
- Para modificar una entrada de la base de datos con Knex.js puedes usar un código como el siguiente que equivale a la instrucción SQL indicada en el comentario:

.. code-block:: javascript
  :linenos:

  knex('books')
  .where('published_date', '=', 2000)
  .update({
    status: 'archived'
  });

  // SQL: update `books` set `status` = 'archived' where `published_date` < 2000

- Una posible manera de gestionar fácilmente el estado de expandido/colapsado de las preguntas de un cuestionario en el navegador es añadiendo un atributo ``data-colapsado`` (con valores ``true`` o ``false``) al elemento ``section`` que rodea el cuestionario. Con algunas reglas de estilo sencillas basadas en la propiedad ``display`` de CSS podrás hacer que las preguntas de cada cuestionario se muestren o no en la aplicación según el valor de ``data-colapsado``.
- Modifica tu código en JavaScript para que el atributo ``data-colapsado`` se añada con el valor adecuado tanto al crear un nuevo cuestionario como al recuperar la lista de cuestionarios del servidor. Para este segundo caso, tendrás que llamar al servicio que devuelve la información de colapso con cada tema de cuestionario. Recuerda cómo funcionan las clausuras en JavaScript si para lo anterior usaras un bucle que iterara sobre todos los temas y llamara con *fetch* al servicio web con cada uno de ellos; es posible en ese caso que te interese definir una variable con ``let`` (y no con ``var``) para obtener el nodo ``section`` al que añadir el atributo:


.. code-block:: javascript
  :linenos:

  for (...) {  /* itera sobre los temas */
    ...
    let node = /* nodo section del cuestionario correspondiente */
    ...
    fetch("...info-colapsado...")
    ...
    .then(
    ...
      node.setAttribute("data-colapsado",...); /* clausura */
    ...
    )
  }

- Añade un botón o simplemente texto al inicio de cada cuestionario que permita cambiar el estado de colapsado/expandido. Asóciale un nuevo manejador de evento y escribe su código inspirándote, por ejemplo, en el de la función ya existente que borra un cuestionario. Llama adecuadamente con *fetch* al servicio de cambio de estado de colapso desde la función del nuevo manejador de evento.


Destacar algunas preguntas de un cuestionario
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Modifica tu práctica 4 para que cada pregunta incluya un nuevo icono (por ejemplo, la estrella ★ con código Unicode U+2605 o un simple asterisco) junto al icono de borrado que permita *destacar* dicha pregunta. Una pregunta destacada se muestra la primera en la lista de preguntas de un cuestionario dado. Solo se puede destacar una pregunta como máximo en cada cuestionario. Cada clic sobre el icono de destacar activa o desactiva el estado de la pregunta. El color del icono ha de cambiar cuando la pregunta esté destacada. El estado de destacada de una pregunta se almacenará en la base de datos y se mantendrá aunque la aplicación se recargue. Al crear un nueva pregunta, esta estará por defecto no destacada.

Cuando se cambia el estado de una pregunta destacada, esta no tiene que volver a su posición original en la lista de preguntas salvo, quizás, si se recarga la página. Además, no tienes que cambiar el siguiente comportamiento, que probablemente será el que tenga tu aplicación: al subir una pregunta al principio de la lista, esta pasará a ser la pregunta 1 y las siguientes se renumerarán en consonancia.

Lo siguiente son algunos consejos relativos a la implementación que no es obligatorio que sigas. Únicamente se dan a modo de recomendación y pueden estar más o menos incompletos según como sea tu implementación.

- Cada entrada de tipo pregunta de la base de datos tendrá una nueva propiedad (llamada, por ejemplo, ``destacada``) que almacenará su estado de destacada.
- Comienza añadiendo el nuevo icono al bloque en la misma función de tu código en Javascript en la que añades la cruz de borrado.
- En el DOM del documento representa el estado de una pregunta mediante un atributo ``data-destacada`` en el elemento del bloque correspondiente:

.. code-block:: html
  :linenos:
			
  <div class="bloque" data-destacada="true">
    ...
  </div>

- Asegúrate de que en la parte de tu código JavaScript encargada de crear una nueva pregunta se inicializa a falso el atributo ``data-destacada``.
- Añade un manejador de evento para cuando se haga clic sobre el nuevo icono. Este manejador cambia el valor del atributo ``data-destacada``.
- Para ahorrarte algunas conversiones, haz que cualquier nueva variable en tu código JavaScript que represente el estado de una pregunta sea de tipo cadena y no booleana.
- Modifica la hoja de estilo para que el nuevo icono se muestre junto a la cruz de borrado. Añade los estilos necesarios para que se muestre en rojo si la pregunta está destacada y en negro en otro caso.
- Modifica el manejador del evento del nuevo icono para que solo cambie el valor de ``data-destacada`` si no hay otra pregunta destacada en el cuestionario; si la hay, ha de mostrar una ventana de *alerta* y no hacer nada más.
- Crea un nuevo servicio web para cambiar el valor de la propiedad ``destacada`` de una pregunta en la base de datos. Es posible que te interese basarte en el codigo ya existente de algún otro servicio web.
- Para modificar una entrada de la base de datos con Knex.js puedes usar un código como el siguiente que equivale a la instrucción SQL indicada en el comentario:

.. code-block:: javascript
  :linenos:

  knex('books')
  .where('published_date', '=', 2000)
  .update({
    status: 'archived'
  });

  // SQL: update `books` set `status` = 'archived' where `published_date` < 2000

- Cambia también el servicio web que se invoca al crear una nueva pregunta para que la propiedad ``destacada`` se inicialice adecuadamente.
- En el código del cliente, cuando el servidor no dé error al cambiar el estado de una pregunta, mueve la pregunta al inicio de la lista de preguntas del cuestionario; es posible que te venga bien usar la función ``insertBeforeChild`` para ello.
- Haz que al recargar la página y leer todas las preguntas de un cuestionario, la pregunta destacada se coloque al principio. Modifica los servicios web oportunos para que devuelvan en los datos en JSON la nueva propiedad. Modifica el código de la función ``init`` de JavaScript para que al leer las preguntas de cada cuestionario coloque al comienzo la pregunta destacada, si la hay.
