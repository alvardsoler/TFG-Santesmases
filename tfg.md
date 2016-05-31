Autorización {#h.dq7ahit8sjpf .c13}
============

        Nosotros, Raúl Cobos Hernando, María Picado Álvarez y Álvar D.
Soler Rus, alumnos matriculados en la asignatura Trabajo de Fin de Grado
(TFG) en la Facultad de Informática de la Universidad complutense de
Madrid durante el curso 2015/2016, dirigidos por Guillermo Jiménez Díaz,
autorizamos la difusión y utilización con fines académicos, no
comerciales, y mencionando expresamente a sus autores del contenido de
esta memoria, el código, la documentación adicional y el prototipo
desarrollado.

Raúl Cobos Hernando, María Picado Álvarez y Álvar D. Soler Rus

 {#h.i17pqbm23uz3 .c13 .c26}

* * * * *

 {#h.8vit5zt1sh8v .c13 .c26}

Agradecimientos {#h.l576qby6rf7i .c13 .c52}
===============

* * * * *

 {#h.1dq7twhfep2p .c13 .c26}

Resumen {#h.a9b04t74nw7y .c13 .c52}
=======

        La Realidad Aumentada es una tecnología que combina imágenes
reales con la superposición de imágenes virtuales. En esta memoria se
detalla el trabajo hecho con esta tecnología en la creación de varios
minijuegos para dotar al Museo García Santesmases de un atractivo
añadido al de los objetos físicos ya expuestos. Veremos cómo ha sido el
proceso de desarrollo de la aplicación, la toma de decisiones y los
problemas que hemos encontrado. El nombre de la aplicación es NOMBREAPP,
y está disponible en Play Store para que cualquiera que visite el museo
la pueda descargar y usar.

Palabras clave: Realidad Aumentada, Museos, Unity3D, Vuforia, Android,
Videojuegos

Abstract {#h.74j509ivflvc .c13}
========

Key words:

NOTAS NUESTRAS

Falta: Agradecimientos, Resumen, Abstract, Introducción a nuestro
proyecto y no a la realidad aumentada (1.1), Capítulo 3 entero, añadir
diagrama de las escenas y su explicación en el tema 4 al final, líneas
futuras (9.2) y conclusiones de los cuestionarios.

* * * * *

* * * * *

Contenido

[Capítulo 1: Introducción a “NOMBRE
JUEGO”](#h.gjdgxs)[        ](#h.gjdgxs)

[1.1.](#h.30j0zll)[        ](#h.30j0zll)[Introducción](#h.30j0zll)[        ](#h.30j0zll)

[1.2.](#h.1fob9te)[        ](#h.1fob9te)[Museo de informática
“García-Santesmases”](#h.1fob9te)[        ](#h.1fob9te)

[1.3.](#h.3znysh7)[        ](#h.3znysh7)[Objetivos y
motivación](#h.3znysh7)[        ](#h.3znysh7)

[1.4.](#h.2et92p0)[        ](#h.2et92p0)[Antecedentes](#h.2et92p0)[        ](#h.2et92p0)

[Capítulo 2: Estado del arte](#h.tyjcwt)[        ](#h.tyjcwt)

[2.1.](#h.3dy6vkm)[        ](#h.3dy6vkm)[La realidad
aumentada](#h.3dy6vkm)[        ](#h.3dy6vkm)

[2.2.](#h.1t3h5sf)[        ](#h.1t3h5sf)[Alcance](#h.1t3h5sf)[        ](#h.1t3h5sf)

[2.2.1.](#h.4d34og8)[        ](#h.4d34og8)[Información
interactiva](#h.4d34og8)[        ](#h.4d34og8)

[2.2.2.](#h.2s8eyo1)[        ](#h.2s8eyo1)[Entretenimiento](#h.2s8eyo1)[        ](#h.2s8eyo1)

[2.2.3.](#h.17dp8vu)[        ](#h.17dp8vu)[Ciencia y
desarrollo](#h.17dp8vu)[        ](#h.17dp8vu)

[2.2.4.](#h.3rdcrjn)[        ](#h.3rdcrjn)[Otros](#h.3rdcrjn)[        ](#h.3rdcrjn)

[2.3.](#h.26in1rg)[        ](#h.26in1rg)[Herramientas de
desarrollo](#h.26in1rg)[        ](#h.26in1rg)

[2.3.1.](#h.lnxbz9)[        ](#h.lnxbz9)[Vuforia](#h.lnxbz9)[        ](#h.lnxbz9)

[Cómo genera realidad aumentada](#h.35nkun2)[        ](#h.35nkun2)

[Plataformas de desarrollo](#h.1ksv4uv)[        ](#h.1ksv4uv)

[2.3.2.](#h.44sinio)[        ](#h.44sinio)[Unity](#h.44sinio)[        ](#h.44sinio)

[2.3.3.](#h.2jxsxqh)[        ](#h.2jxsxqh)[C\#](#h.2jxsxqh)[        ](#h.2jxsxqh)

[2.3.4.](#h.z337ya)[        ](#h.z337ya)[Unity +
Vuforia](#h.z337ya)[        ](#h.z337ya)

[Capítulo 3: Diseño del videojuego](#h.3j2qqm3)[        ](#h.3j2qqm3)

[3.1.](#h.1y810tw)[        ](#h.1y810tw)[Introducción](#h.1y810tw)[        ](#h.1y810tw)

[3.2.](#h.4i7ojhp)[        ](#h.4i7ojhp)[Plan de
trabajo](#h.4i7ojhp)[        ](#h.4i7ojhp)

[3.3.](#h.2xcytpi)[        ](#h.2xcytpi)[Conclusiones](#h.2xcytpi)[        ](#h.2xcytpi)

[Capítulo 4: Space Invaders](#h.1ci93xb)[        ](#h.1ci93xb)

[4.1.](#h.3whwml4)[        ](#h.3whwml4)[Historia](#h.3whwml4)[        ](#h.3whwml4)

[4.2.](#h.2bn6wsx)[        ](#h.2bn6wsx)[Nuestra
versión](#h.2bn6wsx)[        ](#h.2bn6wsx)

[4.3.](#h.qsh70q)[        ](#h.qsh70q)[Implementación](#h.qsh70q)[        ](#h.qsh70q)

[4.3.1.](#h.3as4poj)[        ](#h.3as4poj)[Diseño](#h.3as4poj)[        ](#h.3as4poj)

[4.3.2.](#h.1pxezwc)[        ](#h.1pxezwc)[Desarrollo](#h.1pxezwc)[        ](#h.1pxezwc)

4.4.        Conclusiones        

[Capítulo 5: Arkanoid](#h.2p2csry)[        ](#h.2p2csry)

[5.1.](#h.147n2zr)[        ](#h.147n2zr)[Historia](#h.147n2zr)[        ](#h.147n2zr)

[5.2.](#h.3o7alnk)[        ](#h.3o7alnk)[Nuestra
versión](#h.3o7alnk)[        ](#h.3o7alnk)

[5.3.](#h.23ckvvd)[        ](#h.23ckvvd)[Implementación](#h.23ckvvd)[        ](#h.23ckvvd)

[5.3.1.](#h.ihv636)[        ](#h.ihv636)[Diseño](#h.ihv636)[        ](#h.ihv636)

[5.3.2.](#h.32hioqz)[        ](#h.32hioqz)[Desarrollo](#h.32hioqz)[        ](#h.32hioqz)

[5.4.](#h.41mghml)[        ](#h.41mghml)[Conclusiones](#h.41mghml)[        ](#h.41mghml)

[Capítulo 6: Water Pipes](#h.2grqrue)[        ](#h.2grqrue)

[6.1.](#h.vx1227)[        ](#h.vx1227)[Historia](#h.vx1227)[        ](#h.vx1227)

[6.2.](#h.3fwokq0)[        ](#h.3fwokq0)[Nuestra
versión](#h.3fwokq0)[        ](#h.3fwokq0)

[6.3.](#h.1v1yuxt)[        ](#h.1v1yuxt)[Implementación](#h.1v1yuxt)[        ](#h.1v1yuxt)

[6.3.1.](#h.4f1mdlm)[        ](#h.4f1mdlm)[Diseño](#h.4f1mdlm)[        ](#h.4f1mdlm)

6.3.2.        Desarrollo        

6.4.        Conclusiones        

[Capítulo 7: Evaluación con usuarios](#h.3tbugp1)[        ](#h.3tbugp1)

[7.1.](#h.3tbugp1)[        ](#h.3tbugp1)[Plan de
evaluación](#h.3tbugp1)[        ](#h.3tbugp1)

[7.1.2.](#h.28h4qwu)[        ](#h.28h4qwu)[Objetivos de la
evaluación](#h.28h4qwu)[        ](#h.28h4qwu)

[7.1.3](#h.nmf14n)[        ](#h.nmf14n)[Tareas a
realizar](#h.nmf14n)[        ](#h.nmf14n)

[7.2.](#h.37m2jsg)[        ](#h.37m2jsg)[Descripción de la metodología
del análisis de los datos](#h.37m2jsg)[        ](#h.37m2jsg)

[7.3.](#h.1mrcu09)[        ](#h.1mrcu09)[Informe de
resultados](#h.1mrcu09)[        ](#h.1mrcu09)

Capítulo 8: Conclusiones y trabajo futuro        

8.1.        Conclusiones        

[8.2.](#h.111kx3o)[        ](#h.111kx3o)[Líneas
futuras](#h.111kx3o)[        ](#h.111kx3o)

[Capítulo 9: Aportaciones
individuales](#h.3l18frh)[        ](#h.3l18frh)

9.1.        Organización general del proyecto        

9.2.        Raúl Cobos        

9.3.        Álvar Soler        

[9.4.](#h.1egqt2p)[        ](#h.1egqt2p)[María
Picado](#h.1egqt2p)[        ](#h.1egqt2p)

[](#h.1egqt2p)

* * * * *

[](#h.1egqt2p)

[](#h.1egqt2p)

Capítulo 1

Introducción a “NOMBRE JUEGO”

1.  Introducción {#h.30j0zll style="display:inline"}
    ------------

        El proyecto que hemos desarrollado tiene como finalidad atraer
al público al museo García Santesmases con una característica nueva y
atractiva. Para ésto, hemos utilizado la Realidad Aumentada; en adelante
RA, y con ella, diseñado tres pequeños minijuegos que requieren poco
tiempo para ser jugados y dan una visión nueva de lo que la RA puede
aportar a un museo. Todo esto dentro de una aplicación para móviles
Android.

        La Realidad Aumentada es el término que se usa para definir una
visión a través de un dispositivo tecnológico, directa o indirecta, de
un entorno físico del mundo real, cuyos elementos se combinan con
elementos virtuales para la creación de una realidad mixta en tiempo
real.                  

        Este tipo de tecnología se está utilizando cada vez más en
distintos museos, para dinamizar su visita.

2.  Museo de informática “García-Santesmases”                             {#h.1fob9te style="display:inline"}
    ---------------------------------------------------------------------

El museo de informática “García-Santesmases”, se encuentra en los
pasillos de las plantas 3º y 4º de la facultad de informática de la
universidad Complutense de Madrid. Este museo hace un recorrido por las
diferentes máquinas creadas por la Universidad Complutense de Madrid,
así como de computadoras comerciales y equipos donados a la universidad.

![](images/image03.png)

Figura 1.1: Fotografía del

3.  Objetivos y motivación {#h.3znysh7 style="display:inline"}
    ----------------------

        Nuestro objetivo ha sido el desarrollo de una aplicación que
mejorará la experiencia del usuario en un museo, en este caso, el museo
de la Facultad de Informática “García-Santesmases”. Pero no solo esto,
sino que nuestro objetivo era hacerlo a través de los videojuegos y
utilizando la RA.

        Esto lo logramos mediante una “gymkana”, guiando al visitante a
que recorra el museo en busca de misiones que tendrá que ir completando
minijuegos para poder pasar a la siguiente misión. Así, al finalizar la
visita, el jugador habrá recorrido el museo de una forma amena y
divertida.

        Nuestra motivación principal en la realización de este proyecto,
fue profundizar en el desarrollo de videojuegos con una herramienta tan
innovadora como lo es la RA. Por lo que enseguida comenzamos a
investigar sobre aplicaciones creadas anteriormente y descubrimos que
los museos se están haciendo cada vez más eco de los beneficios de
aplicaciones como ésta para atraer al público. Esto nos motivó más, ya
que nos ponía delante una opción real de desarrollo.

4.  Antecedentes {#h.2et92p0 style="display:inline"}
    ------------

        El proyecto que hemos realizado para este TFG, es un proyecto
nuevo y que ha sido diseñado e implementado desde el principio por
nosotros. En años anteriores se realizaron trabajos de fin de grado
dedicados a la RA en museos, como el realizado el año pasado (2014/2015)
para el Museo de América. Nuestro proyecto guarda muchas similitudes con
el citado anteriormente, como el uso de RA en museos para mejorar la
experiencia del visitante. Por tanto, este trabajo puede que sea nuestro
antecedente, aunque el concepto de proyecto sea distinto, ya que ellos
utilizaban la RA como medio de información, mientras que nosotros
añadimos los videojuegos en RA como medio de entretenimiento en la
visita.

* * * * *

Capítulo 2:

Estado del arte

1.  La realidad aumentada {#h.3dy6vkm style="display:inline"}
    ---------------------

        Según Ronald Azuma, desarrollador y líder de proyecto en New
Media, Intel Corporation, y uno de los pioneros en el campo de la
realidad aumentada, dice que la RA consta de las siguientes
características:

-   Combina elementos reales y virtuales.
-   Es interactiva en tiempo real.
-   Está registrada en 3D.

A su vez, consta de unos requisitos mínimos para poder ser emulada, los
cuales son:

1.  Una pantalla, donde mostrar la combinación de los elementos reales
    captados por algún dispositivo y los elementos virtuales generados
    por un software.
2.  Un conjunto de dispositivos que capturen los elementos del entorno y
    nuestra situación como son una cámara, acelerómetro, giroscopio...
    de tal forma que permita al software tener referencias de cómo y
    dónde debe mostrar sus elementos virtuales.
3.  Un hardware relativamente potente, para poder realizar los cálculos
    necesarios para mostrar el entorno que captura la cámara y ser capaz
    de hacer frente al software que genera los elementos virtuales y
    combinarlos en la pantalla con los reales.
4.  Un software capaz de reconocer el entorno y calcular donde y como
    debe representar los elementos virtuales combinados con los reales
    para conseguir una visión de RA.

Con el continuo avance de los dispositivos móviles y la potencia, a un
coste aceptable para la mayoría, de la que constan ahora mismo estos,
permiten que cualquier usuario pueda hacer uso de la RA, ya que sus
Smartphones cumplen todos los requisitos para ello.

2.  Alcance {#h.1t3h5sf style="display:inline"}
    -------

        La RA es una tecnología que aunque ya lleva muchos años, no se
conocía a nivel usuario, pero el incremento tan alto del uso de los
Smartphones en los últimos años en la sociedad, ha permitido crear más
aplicaciones que todo el mundo pueda utilizar, ya que hoy en día casi
cualquier persona de una edad comprendida entre los 16 y 55 años tiene
un dispositivo móvil que le permite ejecutar una aplicación de RA en
cualquier lugar y momento.

        Ahora mismo, tiene diferentes aplicaciones en diversos campos
como son:

1.  #### Información interactiva {#h.4d34og8 style="display:inline"}

        En este caso se utiliza para dar a conocer de forma interactiva
información acerca de un elemento cercano al usuario, de tal forma que
se puede mostrar un tipo de información u otra en función de la
interacción entre el usuario y dicho elemento.

        Ahora mismo este área está muy presente en museos como forma
 dinámica de conseguir una inmersión del usuario con lo que está viendo
y hacer de su visita una experiencia más atractiva e incluso hasta más
productiva.

        Dentro de este campo también se hace uso de la RA en
herramientas utilizadas para el intercambio de información en proyectos
profesionales o con fines comerciales como el de mostrar catálogos de
productos de una forma interactiva.
(http://ciencialaultima.blogspot.com.es/2015/01/realidad-aumentada-y-realidad-virtual.html)

2.  #### Entretenimiento {#h.2s8eyo1 style="display:inline"}

        En la actualidad, aunque no está todavía muy popularizado su
uso, existen una gran cantidad de videojuegos que hacen uso de esta
tecnología que, junto con diferentes mecánicas que se adaptan a ella,
generan una novedosa experiencia para entretener el usuario.

3.  #### Ciencia y desarrollo {#h.17dp8vu style="display:inline"}

        Aunque todavía no está normalizado el uso de la RA en este
campo, si están naciendo numerosos proyectos con el fin de desarrollar
esta tecnología para utilizarse en áreas como la medicina y la
construcción entre otras.
(http://mocadele.net/arloon-app-educativas-de-ciencias-con-realidad-aumentada/)

4.  #### Otros {#h.3rdcrjn style="display:inline"}

        Además de los ya mencionados, existen todavía muchísimas áreas
en las que tienen cabida en sus tecnologías la RA además de muchos otros
usos que o bien están por descubrir o no se consta todavía de la
tecnología suficiente como para integrarlo.

Algo que todavía está en una fase temprana de desarrollo pero que tiene
un futuro prometedor es el uso de la RA para generación de terreno de
forma que se pueda reconocer el mismo y en función de su forma generar
un medio en relación un entorno que todavía no estaba registrado. Esta
tecnología dota de un sinfín de posibilidades añadidas a las ya
existentes para el uso de la RA en muchos otros campos.

2.3.        Herramientas de desarrollo {#h.26in1rg .c13}
--------------------------------------

        En este apartado explicaremos las herramientas que hemos
utilizado para la realización de este proyecto.

#### 2.3.1.        Vuforia {#h.lnxbz9 .c13 .c15}

Vuforia es el framework que hemos utilizado para hacer toda la parte de
RA. Es gratuito y tiene una gran comunidad, así como buenos ejemplos y
tutoriales. Facilita mucho el trabajo, y se puede utilizar con
diferentes SDK (Android, iOs, Unity 3D, ahora con gafas de realidad
virtual también...).

#### 2.3.2.        Cómo genera realidad aumentada {#h.35nkun2 .c13 .c15}

        Básicamente, Vuforia superpone a la imagen tomada por la cámara
de, en este caso, nuestro Smartphone, cualquier modelo en tres
dimensiones que queramos sobre la posición de un Image Target (u otro
marcador) que le hayamos indicado. De esta manera, tenemos un "fondo"
con la imagen tomada por la cámara, con modelos en tres dimensiones "por
encima". Además, nos mantiene siempre los objetos de tres dimensiones en
el mismo punto del espacio, por lo que si movemos nuestra cámara,
cambiará la perspectiva desde donde vemos el objeto, pudiendo girar
alrededor de éste. El comportamiento puede ser diferente, dependiendo de
cómo lo hayamos configurado (podemos hacer que el objeto persista aun
que perdamos de vista el detector).

#### 2.3.3.        Plataformas de desarrollo {#h.1ksv4uv .c13 .c38}

        Vuforia proporciona paquetes para trabajar directamente con el
SDK de Android o el de iOS, así como para Unity3D. Utilizando Unity3D
podemos exportarlo después a una aplicación de Android o iOS también,
aunque no quedaría de una manera tan "pulida" como desarrollándola
directamente con el SDK del sistema operativo deseado. Nosotros hemos
decidido utilizar el paquete para Unity3D porque los tres teníamos unos
conocimientos básicos en desarrollo con Unity, además de que nos permite
exportar después el proyecto al sistema operativo que quisiéramos.

#### Unity {#h.44sinio .c13}

Unity funciona con algo a lo que han llamado escenas, que son diferentes
situaciones o niveles del juego. En toda escena hay una jerarquía de
objetos que la componen, y de cada objeto pueden colgar otros objetos,
además de que se pueden añadir (por medio de código programable) otros
objetos a esa jerarquía de manera dinámica. Todos los objetos de Unity
tienen una serie de componentes, el más básico sería el de su situación
en las tres dimensiones (o dos), su escala y su rotación con respecto a
los tres planos. Estos componentes permiten configurar los objetos de
manera sencilla, encapsulando funcionalidades. Esta forma de "componer"
los objetos no es casual: es la más utilizada en programación de
videojuegos. (ejemplo
http://forum.unity3d.com/attachments/screen-shot-2014-05-27-at-2-34-04-pm-png.102002/)

        Además, Unity cuenta con una extensísima comunidad de
desarrolladores, así como tutoriales, guías, dudas resueltas... solo con
los tutoriales que proporciona la propia gente de Unity podemos hacer un
sencillo juego casi de cada uno de los tipos más comunes de juegos.

        Unity nos proporciona por defecto el cálculo de colisiones entre
objetos, gravedad, eventos de teclado o ratón... en pocos minutos
podemos hacer cosas sencillas pero que con otras herramientas, o
programándolo directamente a mano con un lenguaje de programación
cualquiera como podría ser Java o C++, nos llevarían bastante más
tiempo.

####  {#h.sl0g53rzcit .c13 .c30}

#### C\# {#h.2jxsxqh .c13}

        Los scripts los podemos escribir en C\#, Boo o un lenguaje
"parecido" a JavaScript. Nosotros hemos decidido utilizar C\#, ya que
era la opción que más nos convencía por varias razones:

-   Hemos leído que es más eficiente.
    [[http://answers.unity3d.com/questions/7567/is-there-a-performance-difference-between-unitys-j.html](https://www.google.com/url?q=http://answers.unity3d.com/questions/7567/is-there-a-performance-difference-between-unitys-j.html&sa=D&ust=1464634042320000&usg=AFQjCNElUd6YFcsJJ9k7ZvzxqyA4HdoAKg)]
-   Los tres teníamos conocimientos previos de Java, y C\# es muy
    similar a Java en cuanto a sintaxis.
-   Es el más usado por la comunidad.
    [[http://forum.unity3d.com/threads/boo-c-and-javascript-in-unity-experiences-and-opinions.18507/](https://www.google.com/url?q=http://forum.unity3d.com/threads/boo-c-and-javascript-in-unity-experiences-and-opinions.18507/&sa=D&ust=1464634042321000&usg=AFQjCNGiTcG4FXN6wxE7m2bMy44Ah01J-Q)]

        Todos los Scripts utilizados en Unity heredan de la
clase MonoBehaviour, la cual permite a estos scripts integrarse con la
ejecución interna de Unity. Toda clase que herede de MonoBehaviour tiene
los métodos Start (), Awake (), Update (), FixedUpdate (), y OnGUI (),
entre otros.

        Éstos se ejecutan en diferentes momentos del juego.

1.  Awake (): el primer método al que se llama, antes incluso de que el
    objeto asociado esté habilitado en la escena. Se utiliza para
    inicializaciones o referencias entre scripts.
2.  Start (): se ejecuta después de Awake (), justo antes del
    primer Update () y después de que se active el objeto.
3.  Update (): se ejecuta en cada frame. Esto hace que dependa del
    procesador y del equipo donde se ejecuta. Se usa para
    actualizaciones comunes como mover objetos no físicos, recoger
    entrada del usuario...
4.  FixedUpdate (): el intervalo entre una ejecución y otra es
    consistente y siempre el mismo. Se utiliza para actualizaciones como
    ajustar objetos físicos.
5.  OnGUI (): se utiliza para gestionar y renderizar eventos de
    la Interfaz Gráfica de Usuario (Graphic User Interface, GUI). Sólo
    es llamada si el objeto está habilitado.

         {.c13}
--------

#### Unity + Vuforia {#h.z337ya .c13}

        Vuforia nos proporciona un paquete de extensión de Unity 3D el
cual debemos importar para trabajar. Éste paquete contiene
diferentes prefabs (objetos ya construidos) que nos harán la tarea muy
sencilla.

        Lo que debe tener toda aplicación de RA hecha con Vuforia y
Unity 3D es una ARCamera (cámara de RA). A ésta hay que indicarle
el product key que nos da Vuforia desde su portal para desarrolladores,
además de ésto, se le indicará el paquete de targets propios (lo
explicaremos más adelante en profundidad). Es la unidad mínima de
desarrollo de RA con Vuforia.

        Una vez hecho esto, tendremos diferentes opciones para lanzar
los objetos de RA, que deben colgar en la jerarquía de Unity de
cualquiera de los siguientes prefabs:

1.  Frame Markers:

Son marcadores muy sencillos que son proporcionados por la gente de
Vuforia en su paquete. Se pueden utilizar para calibrar la cámara, pero
no tienen una gran calidad a la hora de ser detectados. Son lo más
sencillo para comenzar una aplicación de prueba.

2.  Image Targets:

Imágenes propias del desarrollador. Funcionan como los Frame Markers,
pero éstas deben ser importadas desde un paquete generado por el portal
de desarrolladores de Vuforia, el cual nos indicará la calidad de esa
imagen para ser detectada.

                                   

![](images/image05.png)

Figura5: Ejemplo de calidad de un ImageTarget en la plataforma para
desarrolladores de Vuforia

3.  Multi-Targets:

Son varios ImageTargets que representan las diferentes caras de un
prisma en tres dimensiones.

4.  Cylinder Targets: 

ImageTarget que envuelve un cilindro, para representar, por ejemplo, una
botella u otro objeto similar.

5.  Text Recognition:

Nos permite detectar textos, ya sean del diccionario proporcionado por
Vuforia de palabras en inglés (más de 100.000 palabras diferentes) o de
uno creado por nosotros mismos.

6.  Object Recognition:

Sirve para configurar un objeto en tres dimensiones que no sea ninguno
de los anteriores.

7.  Smart Terrain:

Permite reconstruir el entorno del usuario de la aplicación en tres
dimensiones.                           

![](images/image07.png)

Figura 3: Ejemplo de aplicación con Smart Terrain

Con cualquiera de estos objetos, la funcionalidad por defecto (que
podemos modificar creando nuestras propias clases que hereden de las que
nos da Vuforia) es que al detectarse (ya sea un ImageTarget, un Text
Recognition, etcétera) se comenzarán a mostrar todos los objetos que
cuelguen de él en la jerarquía de Unity.

        

* * * * *

Capítulo 3:

Realidad aumentada en museos

        En el capítulo anterior hemos hecho una introducción a la RA en
general. En este capítulo vamos a ver cómo aplicarla a museos para
hacerlos más atractivos e interesantes al público.

3.1 Introducción {#h.c7u31zer9vix .c13}
----------------

        La RA ha supuesto un avance muy importante en los museos ya que
aporta nuevas experiencias para los visitantes. Se usan diferentes
formas de usar la RA en el museo, desde aportar información adicional de
un objeto expuesto (enlace a un vídeo, descarga de contenido extra, más
información en texto, audios…) hasta búsquedas del tesoro, gymkanas como
la desarrollada en este trabajo… todo ello son experiencias añadidas y
nuevas para la mayoría de museos.

A parte de los beneficios para el público, para el museo son formas de
añadir contenido muy baratas en relación con lo que puede costar hacer
obras para añadir salas, expositores… Además, se puede añadir contenido
adicional a las aplicaciones, consiguiendo que el público vuelva. Sí se
puede contemplar la posibilidad de tener smartphones y/o tabletas para
el público visitante, una red WiFi abierta para facilitar la descarga de
la aplicación.

3.2 El museo García Santesmases {#h.w6fqwheeko74 .c13}
-------------------------------

3.3 Otros museos {#h.alfq827rfehx .c13}
----------------

        Vamos a ver algunos de los museos que aplican la RA:

-   Centro de artes Ca l’Arenas del Museo de Mataró: para la exposicion
    Mar de Fons el museo dispone de una aplicación que, al enfocar a
    cualquiera de los cuadros, se muestra informacion extra.
     [http://blogs.elpais.com/arte-en-la-edad-silicio/2012/05/construye-tu-propia-exhibicion.html](https://www.google.com/url?q=http://blogs.elpais.com/arte-en-la-edad-silicio/2012/05/construye-tu-propia-exhibicion.html&sa=D&ust=1464634042346000&usg=AFQjCNHvgsQY0u1IlFpSEFDb2hRFwhUq7A)

![museomataro.jpg](images/image02.jpg)

Imagen 3.1: Aplicación del museo

-   Street Museum del Museo de Londres: una de las más famosas. Añade
    contenidos en el exterior del museo. Básicamente, nos permite ver
    fotografías antiguas de los sitios donde estamos, dándonos una
    visión de cómo era mientras vemos cómo es ahora ayudándose del
    posicionamiento GPS del dispositivo.
    [http://www.museumoflondon.org.uk/Resources/app/you-are-here-app/home.html](https://www.google.com/url?q=http://www.museumoflondon.org.uk/Resources/app/you-are-here-app/home.html&sa=D&ust=1464634042348000&usg=AFQjCNGdJb_A_77n_DSENri1i1G4Bq7zGw)

![](images/image01.jpg)

Imagen 3.2: StreetMuseum (fuente
http://www.noordtopics.nl/cultuur/2012\_05\_29-5.shtm)

* * * * *

Capítulo 4:

Diseño del videojuego

4.1.        Introducción {.c13}
------------------------

        El trabajo que se ha realizado para este proyecto es un
videojuego. Éste está ambientado en el espacio y hace uso de la RA como
entorno.

La idea principal del proyecto es la de implementar minijuegos con
diferentes mecánicas y adaptarlos a su uso con RA y la tecnología móvil.
Con este fin, creemos que se puede hacer de cualquier espacio, un lugar
mucho más interesante haciendo uso de esta tecnología, ya que no solo
imaginas la realidad del lugar sino que puedes interactuar con
él.        

Con el fin de hacer uso de la tecnología actual que se nos brinda para
el desarrollo de la RA, hemos implementado tres juegos que creíamos
viables, y que nos permiten poder experimentar con ella. Estos tres
juegos son el Arkanoid, un Space invaders adaptado al uso de la RA y
WaterPipes. Los tres, están unidos haciendo uso de un hilo argumental
que no solo da coherencia a los juegos, sino que obliga al usuario a
moverse por la facultad para poder completar los niveles.

4.2.        Plan de trabajo {#h.4i7ojhp .c13}
---------------------------

        Inicialmente nos reunimos para definir nuestros objetivos para
este proyecto y así posteriormente diseñar un primer boceto de lo que
será nuestra aplicación. Como la idea fundamental del proyecto está
bastante clara, realizar una aplicación con varios mini juegos por el
museo “García-Santesmases” de la facultad, con RA; decidimos investigar
qué tipo de juegos podemos implementar, para ello realizaremos un
estudio de los juegos ya existentes en museos con y sin RA, e iremos al
museo de la facultad. Durante la visita al museo, y ya con una idea de
lo que podemos o no desarrollar, obtendremos una lista de los posibles
juegos que podemos realizar en distintas partes del museo.

        Una vez elegidos los juegos, haremos un pequeño estudio del
alcance del proyecto y decidiremos cuales son los juegos más viables,
teniendo en cuenta el tiempo de desarrollo y pero sobretodo la
experiencia del usuario. Aunque la aplicación se basa en varios
minijuegos repartidos por diferentes zonas del museo, no hay que olvidar
que el objetivo principal es mejorar la experiencia del usuario y para
conseguirlo es fundamental crear un hilo argumentativo que facilite al
usuario encontrar los juegos y lo más importante añada emoción y
diversión a la visita. Por lo que, cuando ya tengamos los juegos y
sepamos la distribución por el museo, debemos crear un hilo argumental
que una de una manera amena todos los juegos entre sí. Cuando tengamos
una versión estable, realizaremos pruebas con usuarios de distintos
perfiles, para poder obtener un estudio de viabilidad de la aplicación
más fiable y detallada.

4.3 Otros aspectos {#h.yyppnqmy8a9a .c13 .c32}
------------------

ESCENAS INTERMEDIAS {#h.hulp4wa8ygn2 .c13 .c55}
-------------------

Entre cada escena; o minijuego del desarrollo, se ha establecido una
intermedia donde un "humanoide" nos pone en situación antes de cada
misión y nos sitúa acerca de cómo se ha llegado a dicha situación y a
dónde debemos ir para resolverla.

![diagrama\_escenas.png](images/image00.png)

Figura X.Y: Diagrama de flujo entre las escenas del juego (hecho con
draw.io)

Gracias al paquete de Unity animación por voz, SAMBA, el proceso de
sincronizar el audio con la animación del discurso del modelo ha sido
algo muy sencillo. Dicha animación consta de tres componentes:

1.  El modelo, que en este caso era un prefab que venía configurado por
    defecto para soportar el componente de audio y de enfoque aleatoria.
2.  Componente de animación de los músculos faciales, al cual se le
    asigna un conjunto de audios de tal forma que la cara del modelo se
    articula de forma sincronizada con el audio proporcionado. El
    componente viene configurado para que el audio que le proporcionamos
    al modelo pueda ser interpretado por este con más o menos énfasis o
    con diferentes estados de ánimo.
3.  Random eyes es un componente que, asignado al modelo, articula sus
    ojos de tal forma que definiendo unos puntos objetivo, alterna y
    gesticula mirando a los diferentes objetivos a lo largo de la
    animación del objeto.

Además del modelo utilizado, también hubo que crear los audios que
narran el hilo argumental de nuestro juego. Para esta tarea, se
generarón los audio con la herramienta de la url
[http://vozme.com/index.php?lang=es](https://www.google.com/url?q=http://vozme.com/index.php?lang%3Des&sa=D&ust=1464634042357000&usg=AFQjCNEA_3BX58Z94ki6b1o_kIEjPNZW2g) que
convierte a \*.mp3, con una voz un "robótica", un texto dado.

En último lugar, la escena contiene también un texto donde se muestra de
forma escrita todo lo que se va narrando. Esto es así porque pueden
haber problemas de audio, o el usuario puede tener la necesidad de
volver a ver el mensaje y sintetizar lo que el "robot" ha dicho para
poder encontrar el próximo lugar donde aparecerá el siguiente minijuego.

[imagen de una escena intermedia]

SISTEMA DE PERSISTENCIA DE PUNTUACIONES {#h.es5w8jt0xlk6 .c13 .c48}
---------------------------------------

Al finalizar el juego, el usuario puede almacenar su puntuación, y ver
el ranking de estas. Este sistema se hizo para enlazar el juego con lo
que es un servicio web, ya que nos parecía una práctica interesante el
hacer uso de la parte cliente que nos ofrece Unity para comunicarnos con
servicios web. ;Se han implementado ambas partes en este caso, tanto el
lado cliente que consume los servicios en Unity, como el lado del
servidor, en el que se ha implementado un sistema de gestión de usuarios
con una sencilla api REST en PHP, haciendo uso del framework Symfony 2.

Desarrollo

Diseño

-   Base de datos: Se genera una base de datos SQL con una sola tabla,
    la de usuarios y los campos que deseábamos guardar: id, nombre y
    puntuación.
-   [imagen de phpMyAdmin tabla de usuarios]
-   Operaciones: Para la parte REST; los servicios, solo pueden realizar
    las operaciones de leer y crear nuevos usuarios. En el panel de
    administración, se pueden realizar las CRUD, crear un nuevo usuario,
    leer los usuarios y ver el usuario en detalle, actualizar y
    eliminar.
-   Panel de administración: Se accede con el usuario administrador a
    través de la siguiente URL
    [http://augmentedreality.hol.es/web/users/](https://www.google.com/url?q=http://augmentedreality.hol.es/web/users/&sa=D&ust=1464634042361000&usg=AFQjCNFwQ4SJk4Ygawz6Jrw4gptT3InHkA) y
    en ella se pueden realizar las descritas en el apartado anterior.
-   REST: la URL base es
    [http://augmentedreality.hol.es/api/](https://www.google.com/url?q=http://augmentedreality.hol.es/api/&sa=D&ust=1464634042362000&usg=AFQjCNEf7jvsZruymzVfFypQzxAwzfAuuw) y
    las operaciones son; de tipo GET /users.[json | xml] para obtener un
    listado de los usuarios y sus puntuaciones en uno de los formatos
    especificados. Y para guardar la puntuación de un usuario, de tipo
    POST /api/users dónde se les manda, en el body de la petición, la
    puntuación del usuario y el nombre de este.
-   Seguridad: De lado del servidor, Symfony nos provee de un sistema de
    seguridad basado en tres factores; la dirección a la que se accede,
    la autenticación para acceder a ella y una vez autenticado, el rol
    que tiene dicho usuario para poder acceder. En nuestro caso hay dos
    usuario. "admin", con el rol de administrador, que le permite entrar
    tanto en el panel de administración, como hacer uso de la api. Y
    "api\_user", un usuario cuyo rol solo le permite usar los servicios
    web. El tipo de autenticación es a través de Basic auth. Consiste en
    añadir un campo en el header con la clave "Authorization" y como
    valor, la palabra "Basic" concatenada y separados por un espacio con
    la combinación de "username:password" codificada en Base64.

4.3.        Conclusiones {.c13}
------------------------

        En general hemos quedado bastante satisfechos con el resultado
final. Sí nos hemos dado cuenta que podríamos haber implementado más
minijuegos, pero los primeros meses fueron bastante lentos en cuanto a
desarrollo. Fuimos probando las diferentes técnicas individualmente y
aprendiendo Unity3D según la necesidad de cada uno. Además, la RA y la
librería de Vuforia nos dieron algunos problemas que explicamos con más
detalle en los siguientes capítulos que no esperábamos, por lo que el
tiempo que en un principio consideramos que nos iba a llevar fue mayor.

Hemos visto que es bastante interesante tanto la RA en museos como los
videojuegos con RA. Además, al hacer versiones de juegos clásicos, hemos
podido intentar darle un vuelto a las mecánicas y una visión nueva. Si
ya de por si la RA en museos es un gran atractivo para acercar al
público jóven a los museos, con la inclusión de minijuegos (que no tenga
partidas largas) creemos que es algo con un gran potencial a explotar.

Sí que hemos visto que la interacción con el Smartphone es algo a
revisar, ya que interactuar con el móvil mientras se apunta en una
dirección en particular puede ser incómodo si hay que hacer pulsaciones
en diferentes puntos de la pantalla.

* * * * *

Capítulo 5:

Space Invaders

1.  Historia {#h.3whwml4 style="display:inline"}
    --------

        Quizá uno de los juegos arcade clásicos más conocidos. La
primera versión salió al mercado en 1978, hace casi cuarenta años. Uno
de los precursores del género shoot 'em up. El jugador controla una nave
espacial que se mueve horizontalmente y debe hacer frente a hordas de
alienígenas enemigos que atacan al jugador disparándole proyectiles.
Además, a veces el jugador cuenta con pequeñas construcciones que hacen
la labor de búnker donde ponerse a cubierto de los disparos, aunque
éstos se van destruyendo.

                                   

![](images/image06.png)

Figura 4: Space Invader original

Éste juego está ampliamente extendido en la cultura popular ya que es
uno de los grandes clásicos, por eso hemos considerado acertado
incluirlo en nuestro proyecto.

        

2.  Nuestra versión {#h.2bn6wsx style="display:inline"}
    ---------------

        Nosotros hemos decidido darle un cambio a la jugabilidad del
juego, y cambiar el sistema. En nuestra versión utilizamos la RA para
que la experiencia sea completamente diferente. Nuestro juego arrancará
al detectar el cartel de FACULTAD DE INFORMÁTICA (Text Recognition),
mostrándonos unos invasores alienígenas sobre el cartel, y
unas defensas bajo éste.

[imagen de como empieza el juego en el cartel de la facultad]

Para destruir a los invasores, lo que tenemos que hacer es mover
nuestro Smartphone para mover nuestra cámara y pulsar en la pantalla
para realizar el disparo. Hemos pasado de manejar la nave defensora en
tercera persona, a hacerlo en primera persona, con un punto de mira en
el centro de la pantalla que nos marca en qué dirección irán los láseres
de nuestra torreta de defensa, convirtiendo el juego en un First Person
Shooter, y tendremos que hacerlo antes de que los enemigos consigan
destruir el escudo de nuestra nave espacial (cuando pasa del verde al
rojo). Iremos obteniendo puntos según destruyamos naves enemigas, y
perderemos puntos al recibir impactos en el escudo, por lo que cuanto
más rápidos seamos, más puntos obtendremos.

Con estos cambios, hemos conseguido (a nuestro juicio), transformar un
clásico de los arcade en un nuevo juego que utiliza la RA dando una
experiencia diferente.

3.  Implementación {#h.qsh70q style="display:inline"}
    --------------

        Durante el desarrollo de este juego hemos encontrado unos
cuantos escollos que superar, algunos que nos han llevado quebraderos de
cabeza. Comenzamos desarrollando el videojuego utilizando un código QR
como marcador de la RA, pensando que después pasar a utilizar un texto
no tendría complicaciones. Una vez teníamos el juego desarrollado con un
código QR (ImageTarget), probamos a detectar texto propio, ya que
Vuforia nos da un diccionario con miles de palabras en inglés, pero
nosotros no queríamos detectar esas palabras, si no únicamente FACULTAD
DE INFORMÁTICA.

        Para esto, seguimos los tutoriales de Vuforia, y, tras resolver
algunas dudas, implementamos una escena sencilla en la que se mostraba
una esfera sobre el texto. Después, intentamos transferir lo
desarrollado con el ImageTarget, al texto.

        Entonces surgieron los problemas. El primero que vimos, era que
las proporciones de nuestros Invasores y las Defensas se quedaron muy
pequeñas, haciendo imposible jugar cómodamente. La mejor manera que
conseguimos para que se ajustaran los elementos del juego a un tamaño
aceptable fue mediante un Script de C\# que aumentaba la escala local de
los Invasores y las Defensas (local scale).

        El siguiente problema que encontramos fue al insertar nuestro
Enjambre de Invasores. Por un lado, una vez aparecían los enemigos, si
movíamos la cámara, éstos se quedaban en la misma posición respecto a la
cámara, es decir, si cuando salían por primera vez estaban en la parte
superior izquierda (por ejemplo) de la pantalla, y nos movíamos, seguían
ahí, en vez de ajustar su posición con respecto al texto detectado.
Tuvimos que cambiar la forma en la que los insertábamos en la escena,
antes de manera dinámica y creando una instancia con un Script, y ahora
como hijos del GameObject que representa al texto detectado. Éste tipo
de problema (de la posición respecto a los objetos de RA) nos volvería a
salir más adelante, pero con los proyectiles que lanzábamos para acabar
con los enemigos.

        En las primeras versiones del juego, lanzábamos un prisma
(nuestro Proyectil) contra los enemigos. Según lanzábamos, el proyectil
se iba dirigiendo en la dirección que tenía la cámara respecto
al ImageTarget al realizar el disparo. Al pasar a utilizar el texto,
esto cambió. Vimos que nuestro disparo se mantenía siempre en el vector
de dirección de la cámara, y cambiaba con éste. Es decir, nuestro
proyectil siempre estaba en el centro de la pantalla, con lo cual se
perdía toda la gracia al juego y su jugabilidad pasaba a ser bastante
complicada. Éste problema nos dejó bastante confusos, ya que con cambiar
el objeto de la RA (ImageTarget o TextRecognition) cambiaba el
comportamiento del proyectil.

        Para resolver esto, cambiamos nuestro proyectil por un láser.
Ahora al tocar la pantalla no se lanza un proyectil, si no que se
dispara un láser que destruirá los enemigos que estén en el vector de
dirección de la cámara. Así hemos conseguido solventar este extraño
comportamiento.

#### Diseño {#h.3as4poj .c13}

        El juego se compone de una única escena que contiene todo el
juego. Básicamente se compone de:

-   La cámara de Vuforia, que a su vez tiene los siguientes hijos:

-   El canvas con la Interfaz de usuario (puntos y mensajes de inicio y
    fin del juego).
-   El punto de mira que utilizamos para apuntar al disparar, que
    también está hecho con un canvas.
-   El Cannon (Cañón de disparo) que representa nuestra arma.
    Básicamente dibuja una línea hacia el infinito para que de la
    sensación de un puntero láser para apuntar, además, desde su
    posición se lanza el raycast que calcula las colisiones con los
    posibles enemigos.

-   Un GameObject vacío llamado SpaceInvadersGame que contiene la
    clase singleton que gestiona el juego y la información mostrada por
    la interfaz.
-   El TextRecognition que sirve para cargar la detección de textos. A
    éste le hemos añadido un diccionario propio de palabras para poder
    leer texto en castellano. El diccionario contiene únicamente dos
    palabras, facultad e informática. Hemos configurado el
    TextRecognition de manera que sólo busque las palabras que están en
    su white list (lista blanca), que son las dos antes mencionadas, así
    las operaciones son más ligeras ya que no tiene que comprobar las
    miles de palabras.
-   Word representa a una palabra detectada por Vuforia. Se puede
    configurar para que represente cualquier palabra detectada o alguna
    en particular. Nosotros lo utilizamos para representar en particular
    la palabra INFORMÁTICA. Éste es el GameObject que sustituye
    al ImageTarget que utilizábamos en el pasado. Al detectar la palabra
    "INFORMÁTICA" en la cámara de RA, activa sus hijos y "avisa" al
    gestor del juego de que debe empezar a ejecutarse.
-   Un Enjambre, que contiene la lógica para crear varios Invasores y
    posicionarlos a cada uno en su sitio, así como para moverlos todos
    juntos.
-   Las copias de los invasores, las cuales disparan a veces a las
    defensas.

[imagen de los invasores]

-   Las defensas, un objeto en tres dimensiones que representa a las
    defensas del jugador. Van cambiando de color, desde el verde al rojo
    según van recibiendo impactos de los invasores (o del propio jugador
    que apunta mal, para ser algo más realista).        

#### Desarrollo {#h.1pxezwc .c13}

        Pasamos a explicar qué clases componen el juego y para qué las
utilizamos.

1.  Defense.cs:

Gestiona las defensas del usuario. Marca el color de inicio y el de
final que debe tener la defensa para calcular los colores intermedios.
Además gestiona las colisiones.

2.  Projectile.cs:

Muy simple. Va asociada a los proyectiles y los destruye al pasar unos
segundos en escena. Es para que los proyectiles que no impacten con
nada, no se queden siempre en la escena.

3.  Enjambre.cs:

Se encarga de gestionar la inicialización del Enjambre y de sus
invasores (colocándolos en la posición que les corresponda en función de
cuántos sean y cuántas filas queremos que haya) y el movimiento del
Enjambre (del que "cuelgan" los invasores), así como la escala de los
invasores. Además contiene la información para saber si se han eliminado
a todos los invasores o no.

4.  GameManager.cs:

Es la clase que gestiona el juego en sí. Es un singleton y se le llama
desde la mayoría de los otros scripts. Gestiona la interfaz de usuario,
mostrando mensajes y los puntos cuando empieza el juego, además de
cuando se puede disparar, etcétera.

5.  Invader.cs:

Lógica del invasor. Gestiona los disparos de los invasores, la muerte de
éstos y el sonido que hacen al ser destruidos.

6.  TextInformaticaTrackableEventHandler.cs:

Implementación propia de la clase ITrackableEventHandler de Vuforia. Va
asociada al Text de RA. Al "encontrarse" y si no está instanciado ya (es
decir, que no se ha "encontrado" varias veces), le dice al GameManager
que comience el juego, indicándole dónde están el Enjambre y las
Defensas en relación al Text.

7.  TextTimer.cs:

De manera muy sencilla destruye el texto (de la interfaz gráfica) al que
está asociado al pasar un tiempo dado una vez se ha habilitado. Lo
utilizamos para mostrar los mensajes de texto de información.

4.  Conclusiones {#h.49x2ik5 style="display:inline"}
    ------------

El juego en general ha quedado sencillo pero con todos los aspectos que
debe tener un juego completo. Sonidos, animaciones, efectos visuales y
jugabilidad aceptable. Creemos que sirve como una buena aproximación a
otros juegos de este tipo, y que se podría ir escalando para desarrollar
un juego más ambicioso.

La complejidad no es grande, aunque sí es recomendable que se tenga
cierta habilidad para apuntar con el móvil.

* * * * *

Capítulo 6

Arkanoid

 {#h.147n2zr .c13 .c20}

6.1.        Historia {.c13}
--------------------

        El Arkanoid es un juego de los 80, donde el jugador controla una
plataforma que impide que una bola se salga de la superficie que limita
el juego. El objetivo principal de la bola es el de destruir todos los
ladrillos o bloques de la pantalla sin salirse de esta. La misión del
jugador es la de, no solo impedir que la bola se salga de la escena, si
no la de situar la plataforma que maneja de tal forma que consiga que la
bola rebote y destruya todos los bloques.

                                   

![](images/image09.jpg)

Figura 1: Portada original Arkanoid

A lo largo del juego puede haber un gran número de variaciones que
complican el juego o que facilitan las cosas. La plataforma del jugador
puede modificar su tamaño, u obtener mejoras como disparos para romper
los bloques. La bola, puede verse modificada mediante variaciones de
tamaño o en la física del juego como romper varios bloques sin rebotar o
incluso multiplicarse. Y los bloques pueden variar en su posición e
incluso desplazarse con el fin de finalizar el juego cuando llegan
abajo.

2.  Nuestra versión {#h.3o7alnk style="display:inline"}
    ---------------

        Es nuestra versión las cosas son sencillas. El usuario proviene
de defender la facultad (nave espacial tfg-III) de unos invasores, y
tras finalizar, recibirá una misión, que es la de despejar el campo de
batalla para poder despegar la nave. Para ello debe abrir paso
reciclando escombros, haciendo uso del panel de reciclaje que se sitúa
en la tercera planta, y que se accede a él, apuntando al código QR
de Super Mario situado junto a una de las consolas.

                                   

![](images/image08.jpg)

Figura 2: qr Super Mario

Una vez se reconozca el ImageTarget (el QR de Super Mario), aparecerá un
viejo televisor, y en su pantalla se observa el juego y dos contadores.
El objetivo es sencillo, hay que despejar los escombros. Hay un minuto
para realizar dicha tarea o hasta que la bola atraviese la deathzone.
Cuantos más residuos recicle, mayor será la puntuación que arrastrará al
siguiente juego.

Una vez en situación, mientras enfoca al target para no perder de vista
la escena, el jugador deberá arrastrar su dedo por la pantalla de su
smartphone para poder desplazar la plataforma y controlar donde rebota
la bola. Mientras hace eso, la bola irá rebotando y el tiempo
decrementando. A medida que destruya objetivos, la puntuación crecerá y
el tiempo se irá agotando.

[captura del juego enfocado en el museo de la facultad]

El juego está ambientado en un entorno espacial, haciendo referencia al
hilo del juego pero solo de forma superficial. Lo que conforma el tema
del espacio es lo que aparece en la pantalla del televisor que contiene
la escena. Pero, en realidad, la escena tiene una connotación retro,
donde un antiguo televisor al lado de una de las consolas que en un
pasado ejecutaba el juego, quiere recrear la forma primitiva de jugar al
Arkanoid; en un televisor de tubo y con un juego sencillo que era para
lo que daba de sí la tecnología y los medios de la época.

Con esta recreación, lo que se intenta es, no tanto simular un juego
entretenido para cumplir con el objetivo de la historia, si no el
recrear una escena pasada basada en este juego. De esta forma, se hace
uso de la RA en este caso, no como medio de entretenimiento a través las
mecánicas que proporciona, si no generando una escena para mejorar la
experiencia del visitante del lugar, el museo de la facultad.

        

3.  Implementación {#h.23ckvvd style="display:inline"}
    --------------

#### Diseño {#h.ihv636 .c13}

        La escena se conforma por los siguientes elementos:

-   ARCamera e ImageTarget como elementos principales en una escena de
    RA. La propia librería de Vuforia nos provee de ellos, solo hay que
    definir el Image target al que reacciona la escena y añadirlos; del
    resto ya se encarga su lógica interna.
-   Un modelo 3D de un televisor que hace de contenedor de la escena y
    que no tiene ninguna mecánica asociada.
-   La bola, en la que se han implementado dos componentes; uno físico
    para hacer que esta rebote, y un script cuya finalidad es la de
    destruir los bloques, o mejor dicho, la de lanzar la animación de
    destrucción del bloque y finalizar el juego al acabar con todos los
    bloques, o, al salirse de la zona de juego. Para evitar problemas y
    por lógica del juego, aunque la escena sea 3D los componentes sobre
    este juego son en 2D.

-   Ball Material: Es un material de Unity que, junto al
    componente RigidBody2D, elimina la gravedad en el objeto, configura
    a este para poder rebotar, consigue que la fuerza aplicada sobre la
    bola sea infinita, de forma que no pare jamás de desplazarse; y,
    define las coordenadas en las que puede desplazarse el objeto (x e
    y) y en las que puede rotar (ninguna).

![](images/image11.jpg)

Imagen X: BallMaterial

-   BoxCollider2D: Para controlar todo el tema de colisiones. En este
    caso, el Collider que envuelve a la bola es un cuadrado rotado 45
    grados para evitar problemas en los rebotes.

                                   ![](images/image10.jpg)

Figura X: BoxCollider Bola Arkanoid

-   Los bloques, que se reparten por la escena esperando a que la bola
    colisione con ellos y recibir así, la orden de que se lance su
    animación de destrucción y se aumente el marcador.

-   Audio source: el componente que da sonido a la acción de
    destrucción.
-   Animación: la animación de destrucción que se lanza al colisionar
    con la bola. Esta se genera por interpolación, ya que es el sistema
    del que nos dota Unity, y lo que hace es reducir la escala del
    objeto a cero.

                                   

![](images/image13.jpg)

Figura X: Distintos tipos de bloques del Arkanoid

-   La plataforma: Esta contiene un componente que reacciona a los
    eventos de la pantalla táctil y que le permite desplazarse, además
    también tiene un RigidBody2D cuyas constraints impiden que pueda
    verse desplazado en el eje vertical o rotado.
-   Canvas: Contiene la información del estado del juego. Este objeto y
    sus hijos, a diferencia del resto, en escena, se muestra en función
    a la pantalla del dispositivo en el que se ejecuta el juego y no en
    función de lo que enfoca la cámara. Sus hijos son, el marcador, el
    contador de tiempo y la pantalla de precarga que muestra la
    información de la ejecución del juego al usuario.

#### Desarrollo {#h.32hioqz .c13}

                 Para el Arkanoid, se han tenido que implementar las
siguientes lógicas de juego:

1.  ScreenDragListener.cs:

        Se encarga de capturar las pulsaciones en pantalla. En su
método Update () se comprueba con cada llamada si la pantalla ha sido
pulsada; si es así, se guarda el punto inicial donde se detectó la
pulsación y se guarda, de forma que al volverse a llamar al método, esta
vez, no solo se comprueba si ha habido contacto con la pantalla, sino
que, además, se comprueba si ha habido variación en la posición del
punto.

        El script, tiene una interfaz interna. En el método Start (), se
comprueba todos los componentes que implementan dicha interfaz en la
escena y se almacenan en un array. Cada vez que se detecta y calcula un
movimiento de drag sobre la pantalla del dispositivo, se recorren los
componentes del array. Estos reciben, a través del método, las
variaciones en los ejes de la pulsación; y así pueden realizar las
acciones correspondientes.

2.  BallIA.cs:

        No tiene mucha explicación, aplica una fuerza en dos coordenadas
que se le asignan como atributos en el momento en el que está activa y
se toque por primera vez la pantalla.

3.  DefaultTrackableEventHandle:

         Es un script que viene por defecto asociado
al ImageTarget de Vuforia. En este caso, hemos hecho una leve
modificación sobre este script, donde hemos añadido un array de
componentes que, cuando se detecta el QR en escena (OnTrackingFound ())
se recorre y estos se van activando.

4.  DieOnCollide.cs:

Con dos parámetros que definen las etiquetas de los gameObjects que se
comportarán como enemigo (el gameObject que delimita la deathzone) y los
objetivos (los bloques que se destruyen al colisionar con ellos).
Implementa el método OnCollisionEnter2D (), que es aquel al que llama el
collider 2D cuando entra en colisión el gameObject con otro objeto con
collider. Cuando se detecta una colisión, se comprueba la etiqueta del
objeto con el que se ha producido y si es de tipo enemigo, se destruye
el propio objeto y se pasa a la siguiente escena. Si es de tipo
objetivo, se llama a la animación de destrucción de este, se aumenta el
marcador y se comprueba si quedan más, para que, en el caso de que no,
pasar también a la siguiente escena.

Los mencionados son los más importantes, ya que son los que dotan de
lógica al juego, aunque existen más de los que se hacen uso como el
globalGameManager, que es el encargado de navegar entre escenas,
ScoreMarkerObserver y TimeMarkerObserver, que pintan en el canvas el
estado del juego o un script que se añade a la escena para controlar el
back de nuestro dispositivo. Además, hay también otros scripts sencillos
que controlan el resto de los objetos de la escena.

4.  Conclusiones {#h.41mghml style="display:inline"}
    ------------

        La RA tiene muchos usos como se menciona en el estado del arte.
En este caso, el objetivo principal no es el de aprovecharnos de las
dinámicas que nos provee para convertirlas en objeto de entretenimiento,
si no el de dotar de dinamismo una parte del museo, ya que aportamos
información de uno de los objetos expuestos en forma de videojuego (una
versión propia que funcionaba en dicha máquina).

Una de las partes complejas en el desarrollo del juego, es la de
configurar una forma de jugar en la que se le haga posible al usuario
interaccionar con su dispositivo mientras apunta al target. Para esto se
han hecho diferentes pruebas, y se ha llegado a la configuración actual
teniendo en cuenta los siguientes factores:

-   El usuario tiene una posición incómoda al utilizar su Smartphone. Él
    tiene que apuntar a la imagen mientras interacciona con el teléfono
    para evitar que la bola caiga. La mejor solución en este caso es la
    de implementar una mecánica basada en detectar el arrastre del dedo
    de la pantalla y que sea este movimiento el que desplace la
    plataforma en el juego. De esta forma, el usuario puede apuntar sin
    problema al QR mientras a su vez puede jugar. Esta forma de hacer
    las cosas consigue los dos objetivos, una mantener la cámara fijada
    en el target, y dos la de hacer cómodo junto con esto el poder
    manejar la plataforma.
-   La complejidad del juego. En este caso se implementa un juego
    sencillo, muy intuitivo y corto, porque el jugador, por la posición
    que tiene, no puede pasar mucho tiempo jugando. El juego tiene como
    máximo un minuto de duración. Y es creemos que es la apropiada ya
    que en este período se puede jugar sin cansarse y acabar el juego si
    se tiene la habilidad suficiente sin que el cansancio de la posición
    evite dicho propósito.
-   La escena. Es cierto que el modelo 3D del televisor no ayuda mucho a
    la jugabilidad. Pero en este caso en el que recrear una escena es
    casi más importante que la experiencia del jugador en el juego. Se
    ha preferido penalizar un poco la jugabilidad (tampoco en exceso)
    para añadir este elemento de forma que añadiendo este objeto a la
    escena, se haga una referencia a la forma de jugar de la época.

[imagen de un usuario apuntando al target y jugando]

Con este juego respecto al desarrollo de RA con Unity y Vuforia, los
conceptos sintetizados son:

-   Aunque se trate de una escena 3D el uso de componentes 2D en los
    objetos de la escena simplifican mucho el trabajo, ya que al no
    tener que contar con un eje más; controlar el movimiento de la bola,
    los rebotes y las colisiones es más sencillo. Al fin y al cabo es
    como mantener el eje restante en un objeto 3D bloqueado pero esto lo
    hace por ti, por lo que te ahorras muchos quebraderos de cabeza a la
    hora de controlar casuísticas que se pueden escapar por ser detalles
    tan pequeños.
-   El manejo de los componentes Collider y RigidBody que en esta escena
    hay que modificar el material por defecto para cambiar la lógica de
    la gravedad, el rozamiento, etc.; que en este caso, no es el que
    está por defecto, ya que en este juego no hay nada de eso. Además
    hay que hacer uso de las constraints del RigidBody para poder
    bloquear las rotaciones y desplazamientos de algunos de los objetos
    de la escena que no interesan que puedan moverse.
-   La depuración del juego en modo escena en vez de hacer uso de la
    cámara. En Vuforia es normal el uso de una webcam para probar tu
    escena, pero en este caso, para probar el juego, era incómodo el
    tener que estar usando dicho elemento, por lo que, desactivando
    dicha opción de depurar la webcam en el ImageTarget y colocando
    la ARCamera apuntando a nuestro modelo 3D podíamos depurar
    simplemente haciendo click en el play del IDE de Unity sin
    preocuparnos de apuntar al QR. Lo malo de este planteamiento es que
    traía un problema consigo, los eventos de pantalla; por
    defecto, Unity no detecta como eventos de pantalla en un dispositivo
    Android el uso del ratón. Para solventar esto se hizo uso de una
    aplicación llamada UnityRemote, que lo que hace es mostrar en la
    pantalla de nuestro dispositivo la escena que se está ejecutando en
    el IDE; y de esta forma podemos capturar los eventos que se realizan
    sobre esta pantalla.

[imagen del depurador de Unity y la tablet capturando la escena]

-   OnTrackingFound () es un método que contiene el ImageTarget en uno
    de sus scripts por defecto, y que en un principio, parece que se
    encarga de habilitar todos los hijos que cuelgan de él en el momento
    en que se reconoce el QR asignado. Pero no, uno de los problemas en
    el desarrollo fue, que aún sin tener enfocado el QR; aunque no se
    vieran los objetos de la escena, todos los componentes de estos, si
    se ejecutaban. Esto es, porque lo único que hace el método
    OnTrackingFound (), solo es renderizar los objetos en escena cuando
    se detecte el ImageTarget, por lo que se modificó este método para,
    además, los scripts, que deshabilitados por defecto al comienzo de
    la escena, se habilitarán al llamarse este método.

* * * * *

Capítulo 7:

Water Pipes

1.  Historia {#h.vx1227 style="display:inline"}
    --------

        Este juego fue creado a finales de los años 80 bajo el nombre de
“Pipe Mania” por “The Assembly Line”, teniendo muchas versiones a lo
largo de los años. Las primeras fueron realizadas por el estudio
“LucasFilm Game” que lanzó el juego “Pipe Dream”.

![](images/image12.jpg)

Imagen X: Juego original de 1989

Aunque posteriormente fueron lanzadas otras versiones del juego para PC,
PS2, NintendoDS y PSP.

En la versión original, el juego consistía en ir colocando las tuberías
que salían de forma aleatoria en un tablero (matriz de NxN) de tal
manera que el agua pudiera fluir por ellas. El objetivo, era construir
el mayor recorrido posible antes de que el agua lo inundara todo. Cada
tubería llena de agua sumaba puntos y cada tubería que no hubiera sido
inundada a la finalización del juego restaba puntos para obtener así la
puntuación final. En cada nivel se iban complicando las cosas, esto lo
conseguían poniendo posiciones de la matriz de juego en las cuales no se
pudieran colocar tuberías. O comenzando antes a fluir el agua por las
tuberías, dando al jugador menos tiempo de reacción.

2.  Nuestra versión {#h.3fwokq0 style="display:inline"}
    ---------------

        En nuestra versión del juego, existen algunas diferencias con
respecto a la versión original. La principal es la mecánica del juego ya
que en esta ocasión el usuario acaba de exterminar al enemigo que estaba
poniendo en peligro a la Facultad, y ahora su misión cambia para poder
despegar la nave y ponerse a salvo definitivamente. En esta última
misión el jugador se encontrará frente a frente con los conductos de
refrigeración de la nave, el problema es que debido a la batalla éstos
se han dispersado y si quiere despegar la nave tendrá que reordenarlos
para que el agua pueda fluir correctamente.

Al comienzo, el jugador verá una matriz rellena aleatoriamente con estos
conductos, además de una salida y una meta. Por lo tanto, el objetivo
del jugador es ir cambiando de posición las tuberías que encuentra en la
matriz, entre sí, para que el agua pueda fluir del punto de origen al de
destino. En esta ocasión, el jugador tiene 6 segundos por cada tubería
para ir colocando las demás y otros 6 segundos adicionales desde que el
juego comienza hasta que la casilla de salida comienza a llenarse. Para
poder despegar la nave, el agua ha debido fluir por todas las tuberías
necesarias para llegar a la meta. En cambio si el agua ya ha comenzado a
fluir y el jugador no ha conseguido recolocar los conductos, en cuanto
el agua no encuentre un camino factible la nave ya no se podrá despegar
y el juego terminará.

3.  Implementación {#h.1v1yuxt style="display:inline"}
    --------------

#### Diseño {#h.4f1mdlm .c13}

Existen dos elementos fundamentales, en cualquier aplicación de RA, y
que nos lo proporciona la librería de Vuforia, la AR Camera y el Image
Target.

-   AR Camera: Es la cámara del juego, y a nivel de usuario del Unity
    funciona como “main camera” de otros juegos sin RA.
-   Image Target: Este objeto también nos lo proporciona Vuforia, y
    cuando lo configuremos con el código QR (u otra imagen o texto) será
    el responsable de relacionar la escena con lo que nuestro
    dispositivo móvil este leyendo.

Para este juego existe un solo tipo de objeto, el quad que representan a
los conductos. Todos estos objetos son hijos del Image Target.

-   Quad: todo el juego se compone de 25 (matriz de 5x5) objetos Quad
    que representan los conductos de refrigeración. A cada objeto se les
    han incluido los mismo componentes:

-   Box Collider: para detectar la colisión y así poder intercambiar dos
    objetos entre sí, en este caso, solo existe la colisión entre el
    usuario y los objetos (Touch).
-   RigidBody: Elimina la gravedad de los objetos y congela ciertos
    movimientos de desplazamiento y rotación de estos, en este caso
    hemos querido bloquear todas las rotaciones y la dimensión Z del
    desplazamiento. Esto es debido a que aunque es un juego en 3D, la
    experiencia con el jugador es totalmente en 2D y esos movimientos no
    nos serán necesarios.

-   Animación: Aunque el único objeto “visible” en el juego sean los
    conductos (Quad), cada uno de ellos contiene un GameObject como
    hijo. La funcionalidad de éste es la animación del agua cuando pasa
    por la tubería, por lo que cada uno de estos “hijos” contienen
    también los mismos componentes cada uno:

-   Sprite Renderer: Esto es necesario, ya que la animación se compone
    de un sprites.
-   Animator: que contiene el Animator Controller de ese tipo de
    tubería. Cada controlador suele tener dos animaciones por tubería,
    que dependiendo de la salida de la anterior se reproduce una
    animación u otra.

-   Canvas: Muestra la información del juego, en este caso se encarga de
    mostrar el tiempo restante que le queda al jugador y cuando el juego
    finaliza muestra la pantalla de marcadores, para que el jugador
    pueda introducir su nombre y así entrar en la lista de clasificados.
-   GameManager: Es un GameObject vacío en la escena que contiene los
    scripts para la funcionalidad del juego:

-   GameManagerWaterPipes: es el encargado de generar toda la escena al
    inicio del juego.
-   WaterController: desde este script, se controla todo el flujo del
    agua.
-   TimeController: clase que decrementa el tiempo de juego y el tiempo
    que tarda el agua en pasar por cada conducto.

#### Desarrollo {#h.2u6wntf .c13}

        Este juego se ha implementado en base al patrón command, que
encapsula la decisión de por dónde va a ir fluyendo el agua. Esta
funcionalidad es la principal de todo el juego, ya que aunque el jugador
de lo que se encarga es de intercambiar las tuberías, el objetivo del
juego es conseguir que el agua fluya desde la casilla de salida hasta la
meta.

[imagen del diagrama de clases del patrón command]

En primer lugar, vamos a describir las clases que se encargan de las
otras funcionalidades del juego, las cuales son, el intercambio de
tuberías que realiza el jugador, la inicialización y creación del
entorno del juego y el tiempo del juego.

1.  TouchObject:

Este script es el encargado de controlar el cambio de los conductos.
Para ello, lo primero que hace es capturar en el método Update todos los
toques en la pantalla y llamar a getObjectHit para obtener el objeto
presionado. Este objeto lo obtenemos a través del método
“GetNearestHitGameObject”, que genera un rayo con origen en la ARCamera
y con la dirección generada por el rayo. Y de esos se queda con el que
haya menor distancia.

Una vez tenemos el objeto presionado, tenemos que saber si ya existe
otro objeto pulsado para poder intercambiarlos, o si es el primer
elemento que queremos cambiar. Si es el primero, lo único que haremos es
cambiarle a ese objeto el tag a “ButtonPush” y si es el segundo,
obtenemos el que ya hemos pulsado anteriormente e intercambiamos su
posición.

2.  GameManager:        

Es el encargado de crear dinámicamente todos los objetos de la escena al
comienzo del juego, y de llevar el control del tiempo que tiene el
jugador para completar la misión. Lo primero que hace es añadir los
objetos prefabs de cada tipo de conducto (Horizontal, Vertical, Codo
Derecho Arriba, Codo Derecho Abajo, Codo Izquierdo Arriba y Codo
Izquierdo Abajo)

[Imagen de los tipos de conductos]

en una lista de SquareReceiver para luego ir eligiendo de manera
aleatoria los 23 conductos totales.

[imagen del tablero]

 A continuación crea la salida y la meta, ya que estos siempre van a
tener una posición fija en el tablero. Y cuando ya está todo listo, lo
único que falta es ir creando el resto del tablero. Esto lo hace
recorriendo todo el tablero desde la casilla 1 hasta la 23 y por cada
una escoge aleatoriamente un tipo de conducto, de la lista anterior.Crea
una instancia de ese tipo de objeto que será un hijo del Image Target.
Dándole además las propiedades como la posición, el nombre, y la escala.
Esta instancia la guardamos en un array del tipo SquareReceiver para
luego poder acceder a él. El método Update controla el tiempo del juego.

Por último, vamos a describir las clases necesarias para controlar el
flujo del agua.

3.  WaterController:

Este script es, junto con el gameManagerWaterPipes, el más importante,
ya que se encarga de controlar el flujo del agua, que es la
funcionalidad básica de nuestro juego. En etse caso, el flujo de agua
funciona de la siguiente manera:

Por cada tipo de conducto el agua puede fluir en dos sentidos cada vez,
por lo tanto a partir de la entrada del agua de la casilla anterior se
calculará la casilla siguiente por la que el agua debería de fluir. Y
una vez que ya sepamos cual es la siguiente casilla por la que tenemos
que llevar el agua, podremos comprobar si esa casilla es válida, es
decir su entrada de agua coincide con la salida de agua anterior.

4.  Conclusiones                                    {#h.19c6y18 style="display:inline"}
    -----------------------------------------------

* * * * *

Capítulo 8:

Evaluación con usuarios

8.1.        Plan de evaluación {.c13}
------------------------------

#### Objetivos de la evaluación {#h.3l4e42ltrrrz .c13}

        Nuestros objetivos a la hora de realizar test a distintos
usuarios es detectar la mayor cantidad de fallos que nosotros mismos no
podemos ver al no ser objetivos a la hora de jugar.

        Cuando se desarrolla un juego, el programador realiza distintas
pruebas durante toda la implementación. Y una vez que ha terminado el
juego, intenta jugar de varias formas posibles con la única intención de
encontrar el mayor número de errores posibles para luego solventarlos.
Pero esto, no suele ser suficiente debido a que si realiza las pruebas
la misma persona que lo ha implementado, pasará por alto muchas cosas.
Comó sabe como funciona, inconscientemente jugará bien y nunca podrá
darse cuenta de si por ejemplo el juego es intuitivo, es decir, si
aunque no sepas como funciona, esta lo suficientemente bien explicado y
diseñado para que el usuario no tenga problemas de ese tipo. Entre otras
cosas.

        

 

#### Tareas a realizar {#h.nmf14n .c13}

(meter tabla del cuestionario SUS)

8.2.        Descripción de la metodología del análisis de los datos {#h.37m2jsg .c13}
-------------------------------------------------------------------

8.3.        Informe de resultados {#h.1mrcu09 .c13}
---------------------------------

* * * * *

Capítulo 9:

Conclusiones y trabajo futuro

        En este capítulo haremos un análisis del trabajo realizado, así
como de las decisiones que hemos tomado y los resultados de esas
decisiones.

Además, haremos un análisis de posibles trabajos futuros a partir de
éste proyecto.

        9.1.        Conclusiones {.c13}
--------------------------------

Como ya hemos comentado en el capítulo 2, la realidad aumentada tiene
unas posibilidades enormes en multitud de campos. Desde los puramente
lúdicos, como los videojuegos, hasta aplicaciones en ciencia o
educativas (como pretende ser éste trabajo). En el campo que nos ocupa,
que es la educación, encontramos infinidad de posibilidades. Desde
atraer a gente a un museo para divulgar la información de éste, hasta
formar a profesionales de la medicina con modelos en tres dimensiones de
órganos o a ingenieros para ver cómo funcionan motores, engranajes o
sistemas de transmisión en tiempo real.

        Éste trabajo nos ha hecho darnos cuenta del hecho de que
probablemente, si no lo es ya, la siguiente gran revolución en los
museos sea la RA. Aporta una cantidad de posibilidades para atraer al
público que todavía, creemos, no nos podemos hacer a la idea.

        Aplicaciones como ésta en los museos, con una gymkana, creemos
es muy atractiva. Ya que se consigue que el usuario vaya a distintos
puntos del museo y realice acciones determinadas, por lo que podemos
acercar contenidos del museo que quizá no fueran en apariencia tan
atractivos para los usuarios.

        Teniendo esto presente, el objetivo de este proyecto era crear
un atractivo para los usuarios del museo a través de la RA y videojuegos
más que transmitir información al usuario sobre el contenido del museo.
Consideramos que esto lo hemos conseguido. Hemos creado tres minijuegos
de una dificultad muy aceptable, cada uno utilizando una manera de
interactuar por parte del usuario. Además, se puede realizar el circuito
en poco tiempo, y como se obtiene al final una puntuación que podemos
comparar con las de otros usuarios, esto dinamiza la experiencia.

        9.2.        Líneas futuras {#h.111kx3o .c13}
----------------------------------

        La verdad es que las posibles líneas futuras son muchísimas.
Durante el desarrollo del proyecto hemos tenido muchas ideas que no
hemos podido llevar a cabo por falta de tiempo.

        Por un lado, con añadir más minijuegos o más niveles a los ya
existentes, se podría hacer otra aplicación nueva. También hemos tenido
otras ideas de minijuegos. Por ejemplo, un juego al estilo “aplasta
topos” de las ferias se podría poner en un cuadro informativo que hay
con imágenes de disquetes. Otro juego, más complejo, que se nos había
ocurrido era, de alguna forma, hacer que el jugador tuviera que conectar
diferentes salidas y entradas de cables en uno de los primeros
ordenadores que hay en el museo.

![disquetesMuseo.png](images/image04.png)

Imágen 9.1: Fotografía del cuadro informativo con los disquetes

        Otra posibilidad es mostrar información acerca de los equipos
expuestos y después hacer un test con preguntas al jugador.

\

* * * * *

Capítulo 10:  {#h.3l18frh .c13}
=============

Aportaciones individuales

10.1.        Organización general del proyecto {.c13}
----------------------------------------------

        En general nos hemos organizado de manera independiente. Cada
uno de los miembros ha realizado uno de los minijuegos, aunque luego
hemos desarrollado algunas funcionalidades juntos y otras, a parte del
minijuego de cada uno, también de manera individual. Aun siendo cada uno
de los minijuegos responsabilidad de uno de los miembros del equipo, nos
hemos apoyado cuando teníamos problemas en el desarrollo individual de
cada uno.

10.2.        Raúl Cobos {#h.4k668n3 .c13}
-----------------------

-   Realización de tutoriales en Unity3D para comprender en profundidad
    cómo funcionan sus escenas y sus mecánicas.
-   Autoaprendizaje e investigación de nuevas tecnologías para mi como
    era Vuforia.
-   Realización de prototipos de Unity3D y Vuforia.
-   Testeo con Álvar de diferentes maneras de interactuar con la RA en
    los primeros momentos.
-   Comunicación y reuniones con nuestro tutor Guillermo a través de
    reuniones presenciales y correos electrónicos.
-   Evaluación con usuarios e interpretación de éstas.
-   Escritura de todos los apartados de la memoria (menos los de los
    minijuegos de mis compañeros) y revisión de los contenidos del a
    misma.
-   Toma de decisiones con el resto de mis compañeros.

10.3.        Álvar D. Soler {#h.2zbgiuw .c13}
---------------------------

        El minijuego que yo he desarrollado ha sido el Space Invader.
Además de todo este minijuego, he llevado a cabo las siguientes tareas:

-   Realización de tutoriales en Unity3D para comprender en profundidad
    cómo funcionan sus escenas y sus mecánicas.
-   Autoaprendizaje e investigación de nuevas tecnologías para mi como
    era Vuforia.
-   Realización de prototipos de Unity3D y Vuforia.
-   Puesta en práctica de reconocimiento de texto propio en castellano.
-   Testeo con Raúl de diferentes maneras de interactuar con la RA en
    los primeros momentos.
-   Realización de fotografías en el museo para poder orientarnos cuando
    trabajáramos en nuestras casas.
-   Comunicación y reuniones con nuestro tutor Guillermo a través de
    reuniones presenciales y correos electrónicos.
-   Testeo para calibrar bien el tamaño de los Invaders y las Defensas
    con el cartel del exterior de la Facultad.
-   Evaluación con usuarios e interpretación de éstas.
-   Búsqueda de imágenes que fueran fáciles de reconocer por la cámara
    de Vuforia.
-   Escritura de todos los apartados de la memoria (menos los de los
    minijuegos de mis compañeros) y revisión de los contenidos del a
    misma.
-   Toma de decisiones con el resto de mis compañeros.
-   Traducción al inglés de los apartados de la memoria que están
    traducidos.

* * * * *

10.4.        María Picado {#h.1egqt2p .c13}
-------------------------

                En mi caso, mi trabajo ha estado dividido en varias
etapas, en cada una de las cuales me he dedicado a diferentes tareas.

-   La primera de ellas, fue junto a mis compañeros la realización de
    tutoriales en Unity3D para comprender y afianzar los conocimientos
    sobre el funcionamiento de esta herramienta.

-   Como ya dijimos anteriormente, aunque si conocíamos Unity, Vuforia
    era completamente desconocida para nosotros, con lo que mi siguiente
    tarea fue la de investigación y autoaprendizaje para conocer el
    funcionamiento de Vuforia. Y más adelante comencé con la creación de
    pequeños prototipos en Unity3d y Vuforia.

-   Durante todo el proceso de creación del proyecto, hemos mantenido
    los tres reuniones periódicas con nuestro director del TFG para ir
    mostrándole los avances y ponernos nuevos objetivos de cara a la
    siguiente reunión.

-   Una vez adquirimos los suficientes conocimientos para poder
    desenvolvernos tanto con Unity como con Vuforia, decidimos reunirnos
    los tres para diseñar el videojuego y decidir qué minijuegos
    implementaremos.

-   En esa reunión, una de las decisiones que tomamos fue la de que
    juegos íbamos a implementar cada uno, y a partir de ese momento me
    centré en la realización del minijuego Water Pipes.

-   Lo primero que hice fue documentarme del juego original para ver
    cómo sería la mejor manera de adaptarlo a la RA.
-   Una de las cosas más importantes para que el juego se pudiera
    adaptar a la RA, era obtener la forma de que el usuario pudiera
    manipular las tuberías. Al ser una aplicación móvil, lo primero que
    intenté fue el “DRAG AND DROP”, para que el jugador pulsara una
    tubería y la arrastrarse hasta donde quisiera cambiarla y al
    soltarla se cambiará automáticamente una tubería por la otra. Pero
    esta opción me dio bastantes problemas y entonces decidí que la
    forma en que se fueran colocando las tuberías fuera el intercambio
    entre ellas, pulsando sobre una e intercambiando por la siguiente en
    ser pulsada.
-   Una vez implementada la funcionalidad para colocar las tuberías,
    comencé a implementar la parte más importante del juego; el flujo
    del agua. Como existen 6 opciones de tuberías distintas y cada una
    de ellas tiene otras dos direcciones posibles por las que puede
    circular el agua. Tenía que buscar una forma de encapsular esa
    información para que lo único que nos preocupase fuera la salida de
    la tubería actual y la entrada de la siguiente. Por eso decidí usar
    el patrón de diseño Command.

-   Al acabar la implementación del juego, el siguiente paso fue
    realizar el mayor número de test posibles a los usuarios. Los test
    los realizamos del juego completo, pero pedimos a los usuarios que
    puntuaron los juegos de manera independiente. Por eso, un vez que
    obtuvimos los primeros resultados, me dispuse a realizar varias
    mejoras que me aconsejaron los usuarios. Después de realizar esos
    cambios en el juego, volvimos a pasar los test a otros usuarios para
    después comparar los test de las dos iteraciones.

-   Durante todo el proyecto he colaborado en el desarrollo de esta
    memoria.


