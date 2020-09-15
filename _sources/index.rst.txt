
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

Novedades
---------

.. list-table::
    :widths: 10 90
    :header-rows: 0
    :class: tablita

    * - 15 sep
      - En la sección ":ref:`label-actividades`" puedes encontrar las actividades a realizar antes de la clase del 22 de septiembre. Hay un pequeño cuestionario que tienes que rellenar antes de las 23.59 del día anterior. Recuerda que estos cuestionarios contribuyen a la nota final. Consulta tras cada clase la sección ":ref:`label-actividades`" para comprobar si esa semana hay que realizar actividades antes de la clase siguiente.
    * - 13 sep
      - Con la normativa actual, puedes seguir y superar la asignatura sin problemas por vía cien por cien telemática, con la única excepción de los exámenes finales de enero y julio que a día de hoy están previstos únicamente en modalidad presencial. No obstante, si lo deseas también puedes asisitir presencialmente a las clases que la universidad te indique a través de la aplicación de Docencia Dual de UACloud (pero únicamente a las sesiones que allí aparezcan reflejadas).
    * - 13 sep
      - Ya está publicado el enunciado de la primera práctica. Las clases de teoría y prácticas comienzan el día 15 de septiembre.

.. _`capítulo sobre HTML`: https://info340.github.io/html-fundamentals.html


.. _label-actividades:

Actividades previas a las clases
--------------------------------

- Antes de la clase del 22/09/2020: estudia los siguientes vídeos: "`Selectores y propiedades de CSS (parte 1)`_", "`Selectores y propiedades de CSS (parte 2)`_" y "`Selectores y propiedades de CSS (parte 3)`_"; a continuación, contesta el `test sobre la introducción a CSS`_ (plazo límite: 21/09/2020, 23:59 horas). Utiliza tu cuenta de ``gcloud.ua.es`` para acceder a todos estos materiales.

.. _`Selectores y propiedades de CSS (parte 1)`: https://drive.google.com/file/d/1i3s-LKeMsCam5-kmD65G-BMGWsJjmaA8/view?usp=sharing
.. _`Selectores y propiedades de CSS (parte 2)`: https://drive.google.com/file/d/1XpPhulZBzbsS-ODtjuwZUzDNznKVphj6/view?usp=sharing
.. _`Selectores y propiedades de CSS (parte 3)`: https://drive.google.com/file/d/1PhItC2tHklcq82pHclsrt1sG5eD8PmNl/view?usp=sharing
.. _`test sobre la introducción a CSS`: https://forms.gle/YUznititAny8dagi8


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
- Puedes lazanr tu aplicación con el botón :guilabel:`Run`.
- Clica en el botón :guilabel:`Share` y manda el enlace al profesor.
- Si no es necesario que el profesor edite tu código, también puedes mandarle simplemente el URL de tu código; para ello, tienes que haber creado el espacio como público.

.. _`repl.it`: https://repl.it/


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
    problemas
    practicas

.. estilo
.. cliente
.. servicios
.. componentes
.. nube
   
.. >>> add new documents here
