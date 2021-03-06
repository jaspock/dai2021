
.. Desarrollo de Aplicaciones en Internet, materiales, documentation master file

Materiales de Desarrollo de Aplicaciones en Internet
====================================================

Universitat d'Alacant, curso 2020–2021
--------------------------------------

*«The web is more a social creation than a technical one», Tim Berners-Lee*


.. |ss| raw:: html

   <strike>

.. |se| raw:: html

   </strike>

.. role:: strike
    :class: strike

Novedades
---------

.. list-table::
    :widths: 10 90
    :header-rows: 0
    :class: tablita

    * - 15 Ene 
      - Los siguientes son algunos comentarios adicionales respecto a los exámenes de teoría y prácticas de la convocatoria C2 a celebrar el día 19 de enero de 2021. Lee, en primer lugar, lo que se dice en el apartado de evaluación de la `guía docente`_ en el subapartado "Adaptación de la evaluación a la COVID-19 para el curso 2020-21". Ambos exámenes se realizarán online a través de una reunión en ``meet.google.com`` cuya dirección se ha anunciado a través de UACloud; se dispone también de una sala virtual del sistema interno de videoconferencia de la UA en la que poder continuar el examen en caso de que los servidores de Google comiencen a fallar. Los estudiantes se incorporarán a la reunión con su cuenta de dominio ``gcloud.ua.es`` 10 minutos antes del inicio del examen con el micrófono y la cámara apagados, y permanecerán así (con la excepción que se comenta a continuación) hasta el fin del examen, atentos a cualquier aviso que el profesor pueda realizar. Las posibles dudas y preguntas se formularán por escrito al profesor a través de la plataforma ``chat.google.com`` en la que se identificarán con su cuenta ``gcloud.ua.es`` y en la que podrán encontrar al profesor en todo momento. El URL para descargar el enunciado de los exámenes se anunciará al comienzo de cada uno de ellos. Las soluciones de ambos exámenes (un documento de texto con las respuestas para el examen de teoría y un zip con el código para el examen de prácticas) se entregarán antes del fin del plazo correspondiente a través del servidor de `entrega de prácticas`_. El profesor podrá requerir a cualquier estudiante que acuda a una reunión paralela privada en ``meet.google.com`` durante un corto periodo de tiempo para verificar su identidad o comentar cualquier otro aspecto relacionado con la prueba. El estudiante debe tener un documento de identificación a mano, así como la posibilidad de compartir su pantalla, activar la cámara (se admite poner un fondo virtual y usar un móvil o tablet si el ordenador no tiene cámara) o abrir el micrófono si el profesor se lo requiere. Se recomienda tener el ordenador conectado por cable a internet. El examen de teoría comenzará a las 9.00 y tendrá una duración aproximada de 75 minutos. El examen de teoría constará de unos 10 problemas similares a algunos de los de la página ":ref:`label-problemas`"; es muy probable que el examen *no incluya* (o lo haga muy tangencialmente) problemas de los que piden la salida de la ejecución de un determinado programa o un dibujo sobre cómo representa el navegador una determinada página; sí habrá preguntas de las de rellenar huecos en un código o una frase, o incluso de escribir pequeños fragmentos de código (en HTML, CSS o JavaScript) de unas pocas líneas de longitud. Se pedirá que cada respuesta vaya acompañada de una pequeña justificación. Esta justificación ha de ser la mínima necesaria para que el profesor, que también conoce la materia, pueda concluir que eres capaz de defender tu respuesta y que esta no es consecuencia del azar o de otras causas. El profesor indicará al comienzo del examen teórico de dónde descargar un fichero de texto que contendrá una plantilla para escribir las respuestas. Por otro lado, el examen práctico comenzará aproximadamente a las 10.30 y tendrá una duración de en torno a 110 minutos. Constará de una ampliación de la última práctica similar a las que se pueden consultar en el apartado ":ref:`label-ampliaciones`". Se recomienda que, antes del examen, te familiarices con las plataformas de videoconferencia y chat que se van a usar, así como con el editor de texto con el que vayas a trabajar durante el examen teórico y con el entorno de desarrollo de Node.js para el examen práctico.
    * - 11 Ene
      - Ya puedes consultar en la `web del departamento`_ las notas de la práctica 4. Los apartados marcados con un asterisco cuentan la cuarta parte que los otros. El apartado opcional de autenticación supone un máximo de 2 puntos de la nota final de la práctica. Escribe al profesor para cualquier aclaración sobre tu nota. *Nota:* no dejes de leer el anuncio del día 8 de enero que aparece más abajo ya que contiene información muy importante sobre los exámenes de enero de la asignatura.
    * - 08 Ene
      - La Universidad ha permitido a los coordinadores de asignaturas `decidir unilateralmente`_ si los exámenes de enero de sus asignaturas se realizan de forma presencial u online. En el caso de esta asignatura, **tanto el examen de teoría como el de prácticas se realizarán online** en la misma fecha y hora que ya conocíamos. Esta fecha y hora se indican desde hace tiempo en la `guía docente`_; aunque allí siga apareciendo el listado original de laboratorios donde se iba a realizar en principio el examen, este no será, como se ha comentado, presencial sino online. La sala virtual a la que conectarse el día del examen se puede consultar en un anuncio que se acaba de publicar en UACloud. En los días previos al examen puede que aparezca aquí o en los anuncios de UACloud alguna información adicional.
    * - 15 Dic
      - El examen de enero :strike:`se realizará presencialmente` [ya no; mira el anuncio del 8 de enero] en las instalaciones de la Universidad de Alicante, salvo nueva disposición en contra que pueda aparecer antes de su celebración. El examen teórico y el práctico se realizarán en el mismo lugar, en la fecha y laboratorios que se indica en la `guía docente`_. El examen de teoría tendrá lugar de 9.00 a 10.40 aproximadamente. El examen de prácticas tendrá lugar de 11.00 a 13.00 aproximadamente. El único material que puedes llevar al examen de teoría es un documento identificativo, un boligrafo y una hoja de tamaño ISO/DIN A5 (nunca mayor, por tanto, a 148 x 210 mm) en la que puedes escribir o imprimir toda la información que consideres útil. El único material que puedes llevar al examen de prácticas es un documento identificativo y un portátil en el que tengas instaladas las herramientas de desarrollo y tu código de la última práctica. Si no puedes llevar tu propio portátil, podrás usar los ordenadores del laboratorio, pero es recomendable que hables antes con el profesor para que te aconseje acerca de cómo configurar rápidamente el entorno de trabajo el día del examen.
    * - 14 Dic
      - Se han habilitado dos fechas de entrega diferentes para la última práctica. La primera es la fecha de entrega original (23 de diciembre) y en ella se corregirá la parte obligatoria de la práctica, es decir, todo menos la autenticación de usuarios. Para la segunda entrega (fecha límite: 8 de enero) se corregirá únicamente la parte opcional, es decir, la de autenticación de usuarios, que permite obtener hasta dos puntos más. Aunque tu práctica de la primera entrega ya incluya la autenticación de usuarios, súbela también para la segunda entrega. Recuerda que la segunda entrega es opcional en tanto que en el examen de prácticas no se asumirá en ningún momento que has implementado la autenticación de usuarios. El servidor de prácticas del departamento permitirá la entrega (optativa) de la segunda parte unos minutos después de que se cierre la entrega de la primera parte.
    * - 10 Dic 
      - Ya puedes consultar en la `web del departamento`_ las notas de la práctica 3.
    * - 17 nov
      - Ya puedes consultar en la `web del departamento`_ las notas de la práctica 2. Los apartados marcados con un asterisco cuentan la cuarta parte que los otros.
    * - 24 oct
      - Ya puedes consultar en la `web del departamento`_ las notas de la práctica 1.
    * - 24 oct
      - Las prácticas 3 y 4 planificadas originalmente para este curso se han refundido en la práctica 3 (en el curso anterior, de hecho, se trataba de una sola práctica). La práctica 5 planificada inicialmente pasa a ser ahora la cuarta y última. Los contenidos de las prácticas, en cualquier caso, no sufren modificación respecto a la planificación inicial. El plazo de entrega de la nueva práctica 3 es el 26 de noviembre, lo que nos permite ganar una semana de tiempo para la última práctica que, tradicionalmente, es la que más esfuerzo ha requerido para los estudiantes de la asignatura.
    * - 05 oct
      - Es importante señalar que los vídeos que se están publicando no pretenden ser una fuente de información que tengas que ver una y otra vez para asimilar la materia. El profesor te aconseja que los veas quizás un par de veces y que tomes apuntes que te permitan afrontar el visionado como una tarea activa y consultar luego la información de forma mucho más rápida y eficiente. Busca en fuentes fiables de internet o pregunta todas aquellas cosas que no te hayan quedado claras e incorpora también tus conclusiones a tus apuntes. A la hora de preparar el examen, puede ser interesante realizar un visionado adicional (probablemente a velocidad 1,5x) para refrescar ideas y asegurarte de que no se dice nada en los vídeos que no sepas ya por tus apuntes.
    * - 21 sep
      - En la sección ":ref:`label-actividades`" puedes encontrar las actividades a realizar antes de la clase del 29 de septiembre. Hay un pequeño cuestionario que tienes que rellenar antes de las 23.59 del día anterior. Recuerda que estos cuestionarios contribuyen a la nota final. Como has de consultar tras cada clase la sección ":ref:`label-actividades`" para comprobar si esa semana hay que realizar actividades antes de la clase siguiente, este tipo de anuncios recordándolo no se mostrará más.
    * - 15 sep
      - En la sección ":ref:`label-actividades`" puedes encontrar las actividades a realizar antes de la clase del 22 de septiembre. Hay un pequeño cuestionario que tienes que rellenar antes de las 23.59 del día anterior. Recuerda que estos cuestionarios contribuyen a la nota final. Consulta tras cada clase la sección ":ref:`label-actividades`" para comprobar si esa semana hay que realizar actividades antes de la clase siguiente.
    * - 13 sep
      - Con la normativa actual, puedes seguir y superar la asignatura sin problemas por vía cien por cien telemática, con la única excepción de los exámenes finales de enero y julio que a día de hoy están previstos únicamente en modalidad presencial. No obstante, si lo deseas también puedes asisitir presencialmente a las clases que la universidad te indique a través de la aplicación de Docencia Dual de UACloud (pero únicamente a las sesiones que allí aparezcan reflejadas).
    * - 13 sep
      - Ya está publicado el enunciado de la primera práctica. Las clases de teoría y prácticas comienzan el día 15 de septiembre.

.. _`web del departamento`: https://www.dlsi.ua.es/alumnes/index.cgi?id=val
.. _`decidir unilateralmente`: https://web.ua.es/es/vr-estudis/indicaciones/indicaciones-e-informacion-de-interes-sobre-la-modalidad-de-examen-en-la-convocatoria-c2.html
.. _`entrega de prácticas`: https://pracdlsi.dlsi.ua.es/index.cgi?id=val

.. _label-actividades:

Actividades previas a las clases
--------------------------------

- Antes de la clase del 15/12/2020: realiza la actividad ":ref:`label-comp-nube`", que incluye la lectura de una definición concisa de lo que es la computación en la nube y el visionado de unos vídeos; a continuación, contesta el `test sobre computación en la nube`_ (plazo límite: 14/12/2020, 23:59 horas). Después, realiza la actividad ":ref:`label-appengine`", en la que aprenderás a desplegar en la nube la aplicación del carrito, lo que necesitarás saber hacer por ti mismo como paso final de la práctica 4.
- Antes de la clase del 01/12/2020: sigue la actividad ":ref:`label-gcloud`", donde se muestra cómo configurar tu entorno de trabajo para poder trabajar con la nube de Google, y, a continuación, la actividad ":ref:`label-gcp`" en la que tendrás que ver unos vídeos (duración: 40 minutos), leer unos tutoriales y realizar un pequeño ejercicio. A continuación, contesta el `test sobre Google Cloud Platform`_ (plazo límite: 30/11/2020, 23:59 horas)
- Antes de la clase del 24/11/2020: practica con lo que se comenta en las actividades siguientes: ":ref:`label-local`", ":ref:`label-prueba-carrito`", ":ref:`label-api-cambio`", ":ref:`label-heroku`" y ":ref:`label-cors`". A continuación, contesta el `test sobre despliegue de aplicaciones web`_ (plazo límite: 23/11/2020, 23:59 horas)
- Antes de la clase del 17/11/2020: lee detenidamente y practica con lo discutido en las actividades siguientes: ":ref:`label-curl`", ":ref:`label-cliente-rest`" y ":ref:`label-servidor-rest`"; la última incluye un vídeo con una traza de la aplicación del carrito (duración: 28 minutos; unos 20 a 1,5x). Para poder practicar con el código de esas actividades, tendrás que configurar tu entorno de trabajo como se indica en la actividad ":ref:`label-local`". A continuación, contesta el `test sobre implementación de servicios web`_ (plazo límite: 16/11/2020, 23:59 horas).
- Antes de la clase del 10/11/2020: lee detenidamente y practica con lo discutido en las actividades siguientes: ":ref:`label-intro-comp`", ":ref:`label-ejemplo-comp`" y ":ref:`label-avanzado-comp`". A continuación, contesta el `test sobre componentes web`_ (plazo límite: 09/11/2020, 23:59 horas).
- Antes de la clase del 03/11/2020: realiza las actividades ":ref:`label-servicios-http`", ":ref:`label-servicios-promesas`", ":ref:`label-servicios-xhr`" y ":ref:`label-servicios-fetch`". Todas las actividades menos la segunda consisten principalmente en el estudio de una serie de vídeos (duración total de los vídeos: 50 minutos; unos 35 a 1,5x). Para la la segunda actividad, sin embargo, tienes que leer su contenido (tiempo estimado de lectura: 30 minutos). A continuación contesta el `test sobre acceso a servicios web`_ (plazo límite: 02/11/2020, 23:59 horas).
- Antes de la clase del 27/10/2020: realiza la actividad ":ref:`label-js-objetos`" (en esta actividad tienes que leer un texto con un tiempo estimado de lectura de unos 80 minutos); después, lee y practica con lo que se discute en la actividad ":ref:`label-js-clausuras`" (tiempo estimado de lectura: 15 minutos). A continuación contesta el `test sobre prototipos y clausuras en JavaScript`_ (plazo límite: 26/10/2020, 23:59 horas). 
- Antes de la clase del 20/10/2020: estudia los vídeos de la actividad ":ref:`label-api-web-js`" (duración total de los vídeos: unos 55 minutos; unos 40 a 1,5x). A continuación, contesta el `test sobre la API de los navegadores para JavaScript`_ (plazo límite: 19/10/2020, 23:59 horas).
- Antes de la clase del 13/10/2020: estudia el código y los vídeos de la actividad ":ref:`label-app-web-sencilla`" (duración total de los vídeos: unos 50 minutos; unos 35 a 1,5x). A continuación, contesta el `test sobre la aplicación web sencilla con JavaScript`_ (plazo límite: 12/10/2020, 23:59 horas).
- Antes de la clase del 06/10/2020: estudia los vídeos de la actividad ":ref:`label-intro-js`" (duración total de los vídeos: unos 55 minutos; unos 40 a 1,5x). A continuación, contesta el `test sobre la introducción a JavaScript`_ (plazo límite: 05/10/2020, 23:59 horas). Utiliza tu cuenta de ``gcloud.ua.es`` para acceder a todos estos materiales.
- Antes de la clase del 29/09/2020: lee detenidamente y practica con lo discutido en las actividades siguientes: ":ref:`label-inline-css`", ":ref:`label-caja-css`" y ":ref:`label-posicionamiento-css`". A continuación, contesta el `test sobre el modelo de caja de CSS`_ (plazo límite: 28/09/2020, 23:59 horas). Recuerda utilizar tu cuenta de ``gcloud.ua.es`` para acceder a todos estos materiales.
- Antes de la clase del 22/09/2020: estudia los vídeos y practica con la actividad ":ref:`label-intro-css`" (duración total de los vídeos: unos 35 minutos; unos 25 a velocidad 1,5x). A continuación, contesta el `test sobre la introducción a CSS`_ (plazo límite: 21/09/2020, 23:59 horas). Utiliza tu cuenta de ``gcloud.ua.es`` para acceder a todos estos materiales.

.. _`test sobre computación en la nube`: https://forms.gle/WUqR6Z3AaHKrqZ9J7
.. _`test sobre Google Cloud Platform`: https://forms.gle/6cCTbvJWTekiHGLc9
.. _`test sobre despliegue de aplicaciones web`: https://forms.gle/GUbu37fNwaYyfgPV7
.. _`test sobre implementación de servicios web`: https://forms.gle/H3pTR3LwudaJwE4b8 
.. _`test sobre componentes web`: https://forms.gle/DowYFoTLpv4BTCpcA
.. _`test sobre acceso a servicios web`: https://forms.gle/M9Hy9FxV8KRXiWNeA
.. _`test sobre prototipos y clausuras en JavaScript`: https://forms.gle/3Z4WfGQzZNx31Sui8
.. _`test sobre la API de los navegadores para JavaScript`: https://forms.gle/mmMFWaZP2dqy2juw9
.. _`test sobre la aplicación web sencilla con JavaScript`: https://forms.gle/mQw11xgGZCjzcSkp6
.. _`test sobre la introducción a JavaScript`: https://forms.gle/K5krpteo4L9qzSud8
.. _`Selectores y propiedades de CSS (parte 1)`: https://drive.google.com/file/d/1i3s-LKeMsCam5-kmD65G-BMGWsJjmaA8/view?usp=sharing
.. _`Selectores y propiedades de CSS (parte 2)`: https://drive.google.com/file/d/1XpPhulZBzbsS-ODtjuwZUzDNznKVphj6/view?usp=sharing
.. _`Selectores y propiedades de CSS (parte 3)`: https://drive.google.com/file/d/1PhItC2tHklcq82pHclsrt1sG5eD8PmNl/view?usp=sharing
.. _`test sobre la introducción a CSS`: https://forms.gle/YUznititAny8dagi8
.. _`test sobre el modelo de caja de CSS`: https://forms.gle/PNmsNUSdrYMUsj5d9


Guía docente y normas del curso
-------------------------------

Estos son los materiales de clase de la asignatura Desarrollo de Aplicaciones en Internet, coordinada por el profesor `Juan Antonio Pérez Ortiz`_ (`@japer3z`_) de la Universitat d'Alacant. Para obtener información sobre la evaluación de la asignatura puedes consultar la `guía docente`_. Algunos aspectos adicionales que no están recogidos en la guía son los siguientes:

.. _`Juan Antonio Pérez Ortiz`: https://www.dlsi.ua.es/~japerez/
.. _`@japer3z`: https://twitter.com/japer3z
.. _`guía docente`: http://cv1.cpd.ua.es/ConsPlanesEstudio/cvFichaAsiEEES.asp?wCodEst=C203&wcodasi=34063&wLengua=C&scaca=2020-21

- La asistencia a prácticas es obligatoria, aunque se puede tener un máximo de 4 faltas no justificadas. La asistencia contará indistintamente tanto si la realizas presencialmente (en las semanas que te asigne la universidad a través de la aplicación de Docencia Dual) o telemáticamente (en cualquiera de las semanas de curso, incluso en las que en principio la aplicación te permita asistir presencialmente). Si tienes alguna ocupación que te impide asistir a todas o gran parte de las prácticas incluso online, envía un justificante escaneado al profesor a través del sistema de tutoría de UACloud. Para justificar una falta puntual, envía al profesor el justificante por una tutoría de UACloud. Cada falta no justificada por encima de las permitidas, restará una parte de la nota final de prácticas.
- La visita (virtual en este curso) al profesor durante sus horas de tutoría no puede ser obligatoria por cuestiones normativas, pero es muy recomendable, ya que es la oportunidad de recibir supervisión sobre tus conocimientos de la materia o la calidad del código que has desarrollado. Reserva turno a través de UACloud con anterioridad y conéctate con o sin cámara activada a la sala virtual allí indicada. Si el horario no es compatible con tu agenda, escribe al profesor e intentará encontrar un hueco fuera de dicho horario para atenderte.
- Las prácticas se realizan individualmente. Lee lo que se comenta más abajo sobre plagios.
- Cada una de las cinco prácticas contribuye según lo indicado en la sección de prácticas a la nota final.
- Para acceder a Google Cloud Platform en las últimas semanas del curso necesitarás tu `cuenta de correo electrónico de GCloud`_ con dominio ``@gcloud.ua.es`` de la que dispones como alumno de la Universitat d'Alacant. Asegúrate antes de la cuarta semana de clase de que la tienes activada entrando en la sección *Servicios externos* de UACloud.

.. _`cuenta de correo electrónico de GCloud`: https://si.ua.es/es/manuales/uacloud/uacloudse/servicios-externos.html

.. .. _`punto del mapa`: https://goo.gl/maps/hU5oJbA7yD82

Puedes encontrar algo de información adicional en las diapositivas usadas en la `presentación del curso`_.

.. _`presentación del curso`: _static/slides/000-presentacion-curso.html

El `código fuente`_ de estas páginas, escrito en reStructuredText, está disponible en Github.

.. _`código fuente`: https://github.com/jaspock/dai2021

Puedes obtener una copia local de estas páginas (por ejemplo, para poder consultarlas sin conexión) ejecutando::

  wget --mirror --no-parent --convert-links --page-requisites https://jaspock.github.io/dai2021/index.html


Cómo compartir código con el profesor en clase, tutorías virtuales o consultas por escrito
------------------------------------------------------------------------------------------

Si quieres que el profesor pueda ayudarte con algún código que estás desarrollando, mandar un pantallazo no es la mejor opción. Utiliza repl.it en su lugar para que el profesor pueda probar tu código e incluso realizar modificaciones en directo.

- Accede a la web de `repl.it`_ con tu usuario. 
- Clica en el botón para añadir un nuevo espacio, elige :guilabel:`HTML,CSS,JS` o :guilabel:`Node.js` dependiendo de si tu aplicación es solo para el navegador o también incluye la parte del servidor, y clica en :guilabel:`Create repl`.
- Arrastra desde el explorador de archivos tus ficheros sobre la zona :guilabel:`Files`.
- Si tu aplicación incluye la parte del servidor programada con Express bajo Node.js, será más sencillo si copias el código del servidor (que probablemente tendrás en el fichero ``app.js``) en ``index.js`` y editas el código para que la aplicación se lance en el puerto 3000, ya que repl.it espera esta configuración. Como ejemplo, aquí puedes probar la aplicación del `carrito`_ que estudiamos en clase.
- Puedes lanzar tu aplicación con el botón :guilabel:`Run`.
- Clica en el botón :guilabel:`Share` y manda el enlace al profesor.
- Si no es necesario que el profesor edite tu código, también puedes mandarle simplemente el URL de tu código; para ello, tienes que haber creado el espacio como público.

.. _`repl.it`: https://repl.it/
.. _carrito: https://repl.it/@jaspock/Carrito


Recomendaciones
---------------

Este prefacio es un buen lugar para decir unas palabras sobre integridad profesional y ética académica. Durante este cuatrimestre, la carga de trabajo producida por esta y otras asignaturas puede hacer que en ocasiones te sientas desbordado por la faena pendiente. Esta situación también se producirá frecuentemente en el ámbito profesional para el que te estás formando. Es muy importante que afrontes esos momentos de presión con integridad. El Massachusettts Institute of Technology (MIT) da una `serie de recomendaciones`_ a sus estudiantes al respecto que es importante que leas. Este tipo de universidades suelen tener bien especificado los `procedimientos y sanciones`_ posibles en caso de fraude académico; también la Universitat d'Alacant tiene un reglamento_ al respecto, que probablemente ya conoces. Todos estos aspectos también has de tenerlos en cuenta en esta asignatura: se pueden discutir soluciones en equipo pero nunca compartir código.

.. _`serie de recomendaciones`: http://integrity.mit.edu/
.. _`procedimientos y sanciones`: http://web.mit.edu/policies/10/10.2.html
.. _reglamento: https://dma.ua.es/es/documentos/pdf/actuacion-ante-copia-en-pruebas-de-evaluacion-de-la-eps.pdf

Este es el momento también en el que enfatizar la importancia de tomar apuntes para poder preparar la asignatura con garantías. Las diapositivas, por ejemplo, solo contienen una parte de lo estudiado en clase. Por si se nos ha olvidado mencionarlo, también es muy aconsejable que acudas de vez en cuando a una tutoría presencial; usa antes para ello el sistema electrónico de solicitud de cita de UACloud.


.. directiva obligatoria
.. toctree::
    :maxdepth: 2
    :caption: Contenidos:
    :numbered:

    marcado
    estilo
    cliente
    servicios
    componentes
    rest
    nube
    problemas
    practicas
   
.. >>> add new documents here
