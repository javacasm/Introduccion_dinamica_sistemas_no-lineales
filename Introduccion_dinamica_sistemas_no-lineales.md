# Introducción a la dinámica de los sistemas no-lineales



<a data-flickr-embed="true" href="https://www.flickr.com/photos/kevinmgill/44583965185/" title="Voyage of the Moons"><img src="https://live.staticflickr.com/1919/44583965185_ec68fe0838_w.jpg" width="400" height="400" alt="Voyage of the Moons"></a> by [Kevin Gil](https://www.flickr.com/photos/kevinmgill/44583965185/)


En esta foto vemos los dos tipos de movimiento. Por un lado tenemos el movimiento regular de lo y Europa alrededor de Júpiter. Por otro lado la Gran Mancha Roja, un enorme remolino, que presenta movimiento turbulento, típicamente caótico. 

![Dedicatoria "para mis Papis"](./images/dedicatoria.jpg)


## Del porqué perdonarle los errores a los metereólogos, y por qué siempre los cometerán. 

Me resistía a poner la palabra caos en el título para no dar imagen de desordenado. Tampoco me parecía bien usar el término sin haberlo definido previamente. 
Vamos a hacer un viaje sobre la fauna de los sistemas no lineales viendo algunos de los ejemplos más representativos. Algunos de ellos se han quedado en el tintero, en algún sitio tendriamos que terminar. 
El tema realmente es apasionante y pienso seguir profundizando en él. 
José Antonio Vacas Martínez @javacasm

1992, 4o de Física Teórica 

![Licencia CC by SA](./images/Licencia_CC.png)


INDICE: 
1. [INTRODUCCION](./Introduccion_dinamica_sistemas_no-lineales.md#introducci%C3%B3n)
1. [¿QUE ES EL CAOS?](./Introduccion_dinamica_sistemas_no-lineales.md#qu%C3%A9-es-el-caos)
1. [ECUACION LOGISTICA](./Introduccion_dinamica_sistemas_no-lineales.md#ecuaci%C3%B3n-log%C3%ADstica)
1. [ATRACTORES](./Introduccion_dinamica_sistemas_no-lineales.md#atractores)
1. [¿CAOS?](./Introduccion_dinamica_sistemas_no-lineales.md#caos)
1. [RESUMIENDO...](./Introduccion_dinamica_sistemas_no-lineales.md#resumiendo)
1. [UNIVERSALIDAD](./Introduccion_dinamica_sistemas_no-lineales.md#universalidad)
1. [CAOS Y ERGODICIDAD. Teorema KAM](./Introduccion_dinamica_sistemas_no-lineales.md#caos-y-ergodicidad-teorema-kam)
1. [CAOS CUANTICO](./Introduccion_dinamica_sistemas_no-lineales.md#caos-cu%C3%A1ntico)
[APÉNDICE A: FRACTALES](./Introduccion_dinamica_sistemas_no-lineales.md#ap%C3%A9ndice-a-fractales)
[APÉNDICE B: ATRACTOR DE LORENZ](./Introduccion_dinamica_sistemas_no-lineales.md#ap%C3%A9ndice-b-atractor-de-lorenz)
BIBLIOGRAFIA

## Introducción

Se hace extraño al oído oír hablar a los físicos de caos. Hasta hace sólo unos años, y durante un montón de siglos (todo depende de a quién consideremos como el primer físico, al hombre que vio que una rueda podía girar o al que pensó que las estrellas eran grandes fogatas de otras tribus que estaban un poco lejos) los físicos han intentado buscar el orden dentro de todo. Lo único que han hecho (y no es que sea poco) ha sido intentar ordenar y sistematizar todo lo que podían ver, oír o tocar usando sus sentidos (a veces ayudados por instrumentos que ellos mismos hacían para percibir mejor). 

Para ello han buscado leyes que fueran lo más generales posibles. Han sacado lo realmente importante de los fenómenos y se han atrevido a formular predicciones con sus modelos simplificados, y lo sorprendente (al menos para mi) es que estas predicciones funcionan. La naturaleza, que es lo que estudia un físico, se comporta de forma regular, de modo predecible. Al menos eso pensaban ellos. 

Newton montó un universo mecánico. Laplace llegó a pensar en "una inteligencia suprema que sería capaz de en una sola fórmula abarcar todos los movimientos de los cuerpos más grandes y de los más pequeños; para ella no habría nada incierto, y así el pasado y el futuro estaría ante sus ojos" (Ensayo filosófico sobre las posibilidades). Es el determinismo. 

Cuando comenzamos a considerar sistemas con muchos grados de libertad todo cambia. Tenemos que recurrir al cálculo de probabilidades. Los sistemas de pocos grados parecen deterministas y los de muchos probabilistas. Es como si la complejidad se debiera sólo a la asociación de muchas cosas simples. 
 

Poincaré fue el primero en darse cuenta de que un mismo sistema podía 
presentar dos tipos de movimiento bien diferenciados para cambios arbitrariamente pequeños de un parámetro en su hamiltoniano. Incluso podía presentar movimiento regular y caótico para distinta condiciones iniciales. El mismo demostró que un sistema tan simple como el de los tres cuerpos ofrecía comportamiento impredecible (físicamente decimos que no es integrable). 

La relatividad de Einstein acabó con el tiempo absoluto de Newton. La mecánica cuántica arruinó el sueño de Laplace de medir el universo en un momento dado. Ahora tampoco la mecánica clásica funcionaba. 

Con la llegada en este siglo de los ordenadores, parecía que todo iba a ser calculable. Quizás no conociéramos las condiciones iniciales exactas, pero sí las conocíamos aproximadamente. Nuestros resultados no serían exactos, pero sí bastante aproximados. 

En 1960 un físico llamado Lorenz estaba trabajando sobre predicción metereológica. Hizo un modelo de tiempo atmosférico con doce ecuaciones diferenciales no lineales introduciéndolo en su ordenador. Un día le dio los valores que había obtenido el día anterior, esperando así poder continuar con su tarea!. Al principio obtenía valores similares a los ya obtenidos, pero después el comportamiento del sistema comenzó a separarse del esperado llegando a evolucionar de modo totalmente distinto a como lo había hecho el día de antes. Lorenz intuyó que el problema estaba en que los sistemas no-lineales tienen fuerte dependencia con las condiciones iniciales. 

Su ordenador usaba para los cálculos 2 decimales más de los que daba como resultado, para que así los números representados fueran todos correctos. Las calculadoras hacen lo mismo. 



Estamos acostumbrados a trabajar con sistemas lineales. La propagación de los errores en ellos es lineal. Pero la mayoría de los sistemas reales son no lineales. En éstos, datos iniciales arbitrariamente cercanos conducen a trayectorias totalmente distintas. En estos sistemas encontramos entrelazados movimientos regulares y movimientos impredecibles (caóticos). 

En las ecuaciones diferenciales no-lineales las perturbaciones pequeñas no se mantienen pequeñas, sino que crecen i y de modo exponencial !. Decimos que las ecuaciones no-lineales tienen una gran dependencia con las condiciones iniciales. 

Todo el mundo se sorprendería si supiera que un sistema tan simple e inocente como un péndulo es capaz de presentar un comportamiento caótico si se le somete a una fuerza armónica. El término sin(O) es el responsable de todo con su comportamiento no lineal. 

. Son muchos los sistemas en los que se presenta una fuerte dependencia a las condiciones iniciales. Un ejemplo claro es el tiempo atmosférico. De ahí viene su impredecibilidad. Cualquier pequeña perturbación que escape a nuestra medida es capaz de adueñarse del comportamiento global del sistema. Los metereólogos lo llaman el efecto mariposa. Supongamos que conocemos las ecuaciones que rigen el tiempo (por supuesto serían no-lineales) y que somos capaces de conocer en un momento dado el estado exacto de nuestro sistema. El batir de una mariposa en Australia daría lugar a una perturbación que iría creciendo. En unos meses la perturbación habría llegado a cualquier parte del mundo y se adueñaría del comportamiento atmosférico. Nuestro pronóstico fallaría. 


Estamos acostumbrados a trabajar con sistemas lineales. La propagación de los errores en ellos es lineal. Pero la mayoría de los sistemas reales son no lineales. En éstos, datos iniciales arbitrariamente cercanos conducen a trayectorias totalmente distintas. En estos sistemas encontramos entrelazados movimientos regulares y movimientos impredecibles (caóticos). 

En las ecuaciones diferenciales no-lineales las perturbaciones pequeñas no se mantienen pequeñas, sino que crecen i y de modo exponencial !. Decimos  que las ecuaciones no-lineales tienen una gran dependencia con las condiciones iniciales. 

Todo el mundo se sorprendería si supiera que un sistema tan simple e inocente como un péndulo es capaz de presentar un comportamiento caótico si se le somete a una fuerza armónica. El término sin(O) es el responsable de todo con su comportamiento no lineal. 

. Son muchos los sistemas en los que se presenta una fuerte dependencia a las condiciones iniciales. Un ejemplo claro es el tiempo atmosférico. De ahí viene su impredecibilidad. Cualquier pequeña perturbación que escape a nuestra medida es capaz de adueñarse del comportamiento global del sistema. Los metereólogos lo llaman el efecto mariposa. Supongamos que conocemos las ecuaciones que rigen el tiempo (por supuesto serían no-lineales) y que somos capaces de conocer en un momento dado el estado exacto de nuestro sistema. El batir de una mariposa en Australia daría lugar a una perturbación que iría creciendo. En unos meses la perturbación habría llegado a cualquier parte del mundo y se adueñaría del comportamiento atmosférico. Nuestro pronóstico fallaría. 


Los fluidos son otro claro ejemplo, su comportamiento caótico se debe al término no-lineal (7-7)y de la ecuación de Navier-Stokes: 
+(võ] = - Løp+vi 
donde p es la presión, v es la viscosidad y p la densidad. 

Pero no sólo se ha encontrado comportamiento caótico en sistemas tan físicos como los citados. En campos tan lejanos de la física como la economía (precios de algunos productos) o incluso en el ritmo cardíaco se han encontrado pautas de movimiento caótico. 

Los físicos ahora luchan con el caos, con sus movimientos erráticos, aparentemente aleatorios, buscando un orden dentro de ellos, intentando dominarlos. 

Pero la física funciona. Nuestra vida está llena de un tecnología que nuestra física ha desarrollado. Ahora los físicos buscan como poder utilizar el caos, entendiéndolo, para llegar a usarlo en nuestro mundo de todos los días. 


## ¿Qué es el caos? 

Tenemos dos tipos de movimiento: el regular caracterizado por una cierta "suavidad" en la trayectoria. Existen un número adecuado de constantes del movimiento lo que hace que las ecuaciones del movimiento sean integrables. Su 
espectro en frecuencias es discreto. 

El otro tipo de movimiento es el caótico. En él nunca aparece una pauta regular, que se repita. Su espectro debe ser continuo. Bajo este tipo de movimiento tenemos una fuerte dependencia a las condiciones iniciales. Esta dependencia es la que nos echa por tierra las predicciones a largo plazo. En sólo unos instante el error ha crecido y es mayor que nuestra medida. 

Nos sentimos tentados a simplificar el esquema diciendo que el movimiento regular es estable y el caótico inestable. Pero no todo es tan simple. La primera parte de la afirmación sí es correcta. Pero sí que el movimiento caótico puede ser estable globalmente. Un ejemplo claro de ello es la Gran Mancha Roja de Júpiter que lleva siendo observada desde el siglo XVII. Sin embargo está formada por remolinos y turbulencias, típicamente caóticos. 

La inestabilidad del caos es local. La encontramos en cada punto. De ahí la divergencia exponencial de las trayectorias. En cada punto el sistema puede moverse en direcciones opuestas. Diferencias infinitesimales le harán evolucionar de modos totalmente distintos. 

Si las ecuaciones del sistema son integrables, nuestro sistema tendrá una solución explícita. Dado un estado inicial, lo metemos en la "fórmulita" y obtenemos 

cual será el estado final para un tiempo t. En los sistemas no integrables, no tenemos solución explícita. Dado un estado inicial tenemos que pasar por todos los intermedios para llegar hasta el estado final en t. Aquí no tenemos el atajo de las fórmulas. Al ser las ecuaciones no lineales en cada paso de nuestra integración el error se irá incrementando hasta llegar a tapar nuestro resultado. 

Los sistemas caóticos también son deterministas, pues están regidos por ecuaciones del movimiento como lo estaban los sistemas con movimientos regulares. Dado un estado inicial tenemos determinado el final. El tener una precisión determinada en la medida y en el cálculo van a hacer que no sepamos exactamente cual es el estado inicial ni por supuesto cuales son los intermedios durante nuestro cálculo. Nuestra finitud es la responsable de la impredecibilidad de los sistemas caóticos. 

Vemos así que un sistema determinista puede producir mucho más que movimiento periódico. El caos es generado por reglas fijas que en sí mismas no tiene ningún elemento de azar. El caos es determinista. 
 
Un buen ejemplo de ello es la ecuación logística. 


## Ecuación logística. 
Existen sistemas aparentemente simples y que son capaces de producir comportamiento caótico. Un ejemplo es la ecuación logística. Se trata de un sistema discreto iterativo, la salida se vuelve a introducir y lo que estudiamos es el comportamiento de la sucesión así obtenida. Cuando trabajamos en una sección de Poincaré (calculamos la intersección de la trayectoria con una superficie determinada), obtenemos una evolución discreta del sistema. La forma explícita de la ecuación logística es: 

Xo+1=bX,(1-x) 

donde X puede variar entre 0 y 1. b actúa como parámetro de control (nos determinará el comportamiento del sistema) y puede tomar valores entre 0 y 4. 

Aunque se trata de una sencilla sucesión discreta nos puede servir para ilustrar muchas de las características de sistemas caóticos. Esta ecuación puede servirnos como un modelo ecológico simple. La variable X puede representar la cantidad de individuos de una especie Podemos estudiar su evolución para un valor inicial Xo y un b dados. Si X se hace muy grande (cercana a 1) el alimento escaseará y la población empezará a disminuir como nos indica el término (1-x). 

Con una simple calculadora podemos realizar unas cuantas iteraciones de la fórmula. Nos podemos sorprender de los resultados. Vamos a tratarlo de un modo más matemático y empezaremos con un poco de teoría de sucesiones iterativas unidimensionales. 

-9 

Consideremos la sucesión como una función: 

x'=f(x) 

y supondremos que es lo bastante suave como para poder derivarla. 
Un punto fijo será aquel en el que se cumple que f(E)=E. La posibilidad que le sigue en complejidad es una órbita o ciclo, que está formada por puntos periódicos. Un punto periódico & de orden m va a ser un punto fijo de f"(x), siendo m el menor número entero para el que esto se cumple. f($), f(E), ... ,1" (3) son también puntos periódicos de orden m. 

Para conocer el comportamiento cerca de un punto fijo , estudiaremos el valor de î=f'(E) (el símbolo se refiere a la derivada de f respecto de su variable). 

Si tenemos en cuenta el carácter iterativo de nuestra sucesión veremos que podemos clasificar los puntos fijos según el valor de a en: 

- 19/<1 de atracción o estables. 
- 121=0 superestables. 
- a>1 de repulsión o inestables 
- 12|=1 neutrales 

Podemos hacer exactamente la misma clasificación para las órbitas periódicas. Si Xos...,Xm-1 son los miembros de un ciclo de período m. Para estudiar su evolución definiremos ahora =f'(X.)f'(X,)...f'(X. -_-) 
Con todo esto podemos clasificar los puntos en: 

a) Puntos fijos 

b) Puntos periódicos 

- 10 - 

c) Puntos eventualmente periódicos, son preimagen de un punto periódico, es decir existe un m para el que se cumple que f(x) es periódico. 
d) Puntos asintóticamente periódicos, la sucesión contiene una parcial que converge a un punto periódico. 
e) Punto aperiódico que no es de ninguna de las clases anteriores. La sucesión será estocástica o aperiódica. 

También podemos estudiar propiedades de f en función de b. Así podemos fijar nuestra atención en un punto fijo £(b) y en su evolución en función de b. Puede pasar de ser estable a ser inestable dependiendo del valor de ^(b). 

Vamos a entrar ahora de lleno en le estudio de la ecuación logística. Aquí 2=(1-2x). Vamos a tener dos puntos fijos: 
X=0 con a=b y 
X=1 - con 1-2-6 

Para b=1 el punto X=0 pierde la estabilidad y pasa a ser inestable. X=1 
lo hará para b=3 pues 1=-1. Aparecerá así un ciclo de período 2 para el que se cumple: 

Xx=bX(1-x) X,=bX/(1-x) operando algebraicamente podemos llegar a que X, y X, cumplen b2x1-(6+1)bX,+b+1=0 De aquí podemos calcular el valor de a 
1=b?(1-2x,)(1-2x) = -b2+26+4 

Vemos que 2=1 para b=3 y que =-1 para b=1+V6=3.4495 

- 11 - 

lo que significa que para este valor de b el ciclo de período dos pierde estabilidad y se produce una nueva duplicación, con lo que se creará un ciclo de período 4. 

Podemos encontrar valores de b para los que hay nuevas duplicaciones b=3, 3.4495, 3.5441, 3.56421, 3.5688... 

Estos valores parecen seguir una progresión del tipo 

beb-cF con los valores b=3.5670 c=2.6327 F=4,6692 

Pasados estos valores encontramos una región de comportamiento caótico, en el que X se mueve por toda la zona de forma irregular. 

Llamamos F a la razón de la progresión porque fue Feigenbaum, un físico teórico de partículas quien encontró esta regularidad en los puntos en los que aparece duplicación. 

Más importante aún que este hallazgo fue encontrar en una gran clase de sistemas dinámicos el mismo esquema de duplicaciones de período con la misma constante F. Este comportamiento se mantiene para todas las f(x) bien comportadas con f(0)=f(1) y con un solo máximo en el intervalo (0,1). 

Este fue el descubrimiento de la universalidad de las duplicaciones de período en las transiciones al caos. Posteriormente hablaremos más extensamente de este tema. 

El intervalo ( 
64) contiene infinitas pequeñas ventanas en la región de 
movimiento caótico en las que para ciertos valores de b aparecen ciclos estables de período m. Por ejemplo desde b=3.8284 hasta b= 3.8415 encontramos un ciclo 

- 12 

Diagrama de bifurcación. 

de período 3 que permanece estable. Para el último valor de b encontramos duplicación de período, pasando a un ciclo de período 6, luego 12,... llegando otra vez a comportamiento caótico. 

Estas zonas de comportamiento regular en medio de la región caótica son realmente sorprendentes. Es algo parecido a que en un momento dado mientras estamos moviendo el café para disolver el azúcar, encontráramos que la leche está por un lado, el café por otro y el azúcar en el fondo, para luego si seguimos moviendo volver a encontrar la mezcla normal. 

- 13 - 

## Atractores

Otra forma de ver el comportamiento de un sistema dinámico es estudiando el espacio de las fases completo. 

Empecemos con un péndulo ideal sin amortiguamiento. La trayectoria es una especie de elipse, que viene determinada por la energía del sistema (que es una constante, pues el sistema es conservativo) 

d2e 
de 9 +0,sin8-0 

Para pequeñas amplitudes la frecuencia del péndulo está determinada por 
. Para mayores amplitudes (donde las no-linealidades son más acusadas) el 
período depende de la energía del sistema. 

Veamos ahora un péndulo con amortiguamiento 

dt2 dt la trayectoria es una espiral que siempre converge hacia el mismo punto sin depender de la condición inicial que tomemos. Es como si este punto atrajera al sistema. En este sistema podemos ver una propiedad típica de los sistemas disipativos: la contracción del espacio de las fases. Es como si la evolución temporal fuera haciendo que el espacio fásico encogiera. 

Otro ejemplo de sistema disipativo es el oscilador de Van der Pol 

- 14 

Oscilador de Van der Pol. 

en el que a veces término de amortiguamiento es negativo y a veces positivo. Sin depender de la condición inicial el sistema queda confinado a una sucesión de estados que se repiten. La órbita es cerrada. Tenemos un ciclo límite. El sistema "olvida" las condiciones iniciales, en el sentido de que su destino final del sistema no depende de ellas. Tenemos que el ciclo límite atrae hacia así a la trayectoria del sistema. 

Decimos que una región (de menor dimensión que nuestro espacio fásico) es un atractor si el movimiento del sistema tiende a acercarse a esa zona quedando confinado en ella después de un cierto tiempo. El atractor más sencillo es el punto hacia el que tiende un péndulo con amortiguamiento. 

Un atractor es una configuración estable, porque se mantiene en el tiempo. 
2 Podemos considerarlo como un acercamiento asintótico. 

- 15 - 

Oscilador de Van der Pol. 

en el que a veces término de amortiguamiento es negativo y a veces positivo. Sin depender de la condición inicial el sistema queda confinado a una sucesión de estados que se repiten. La órbita es cerrada. Tenemos un ciclo límite. El sistema "olvida" las condiciones iniciales, en el sentido de que su destino final del sistema no depende de ellas. Tenemos que el ciclo límite atrae hacia así a la trayectoria del sistema. 

Decimos que una región (de menor dimensión que nuestro espacio fásico) es un atractor si el movimiento del sistema tiende a acercarse a esa zona quedando confinado en ella después de un cierto tiempo. El atractor más sencillo es el punto hacia el que tiende un péndulo con amortiguamiento. 

Un atractor es una configuración estable, porque se mantiene en el tiempo. 
2 Podemos considerarlo como un acercamiento asintótico. 


- 15 - 

Un sistema puede tener varios atractores. La región que evoluciona hacia un atractor se llama cuenca de atracción y puede ser muy complicada, pero debe cumplirse que la trayectoria pase cerca de cada uno de los puntos del atractor a lo largo del tiempo. Esto significa que el atractor no puede estar formado por partes disconexas. 

Ejemplo de sistema con dos atractores 

Dos osciladores acoplados nos darían un atractor mas complicado como es un toroide. Para frecuencias inconmensurables tenemos movimiento cuasiperiódico, el sistema se puede mover impredeciblemente por la superficie, aunque nunca se repita y la trayectoria no sea cerrada. 

Un mismo sistema puede presentar distintas clases de atractores dependiendo de los valores de sus parámetros de control (energía para el péndulo, número de Reynolds en un fluido, ...). Veamos un ejemplo con un péndulo forzado armónicamente 

every - užsino-Acos(wt 

- 16 

Péndulo normal. 
periódico 
algo más 

Movimiento complicado. 
... 

Movimiento caótico. 

Lorenz, para comprobar sus ideas sobre los sistemas no-lineales, hizo un modelo para la convección. Se trata de un sistema de 3 ecuaciones no lineales con 3 incógnitas: 

- 17 - 



ay=x(R-z)-y 
dx=xy-bz 

Por supuesto la estructura del atractor debe cambiar continuamente con los parámetros del sistema. Lorenz encontró que este sistema para ciertos valores de estos, evolucionaba hacia una zona determinada, independientemente de la condición inicial. 

HOWS 

Atractor de Lorenz. 

Se trata de una figura con dos zonas redondas, parecidas a espirales, como una mariposa. 

Tenía un tamaño finito, pero nunca se cortaba a sí mismo (es una figura 
tridimensional). 

- 18 - 

La diferencia con el toroide anterior es que aquí dos trayectorias de puntos cercanos originariamente, se separan de modo exponencial. Esto implica extremada dependencia de las condiciones iniciales. 

Lorenz, no sabía lo que había encontrado. Por la misma fecha, Ruelle y Takens, teóricamente habían dado con una figura parecida. A este tipo de atractor le llamaremos atractor extraño. 

Ruelle lo define así (primero definiremos un concepto previo, el de conjunto atractivo): 

Un conjunto A es un conjunto atractivo si satisface (siendo U el entorno fundamental de A y representando f la evolución): 

1) Atracción: para cada abierto V - A tenemos f'U CV para t 
suficientemente grande. 

2) Invariancia: f*A = A 
Vt 
Definimos su base de atracción como el conjunto de los x tales que fx se 
aproxima a A para t + ". Un atractor será el conjunto de los puntos de 
acumulación de {f'(x)}. Debe ser invariante pero no necesita tener una base de atracción abierta. 

3) Irreducibilidad: no puede estar formado por regiones disjuntas. Matemáticamente: podemos elegir x' de tal forma que V XE A 3t : f'x' está arbitrariamente cerca de x. 

- 19 - 

Estas condiciones las cumplen todos los atractores. La condición especial que cumplen los atractores extraños es: 

4) Dependencia sensitiva a las condiciones iniciales. Técnicamente: 
su medida asintótica tiene exponente positivo (su exponente de Lyapunov es positivo. Más adelante veremos qué es ésto). 

También le exigiremos una cierta estabilidad ante las perturbaciones 
interiores y exteriores. 

5) Estabilidad bajo pequeñas perturbaciones aleatorias. 
Los atractores nos darán una descripción global del comportamiento asintótico del sistema. 

Se encuentra que incluso para sistemas con muchos grados de libertad, el sistema acaba confinado en atractores de dimensión baja, lo que implica que sólo unos pocos grados de libertad están activos. La mayoría de las condiciones iniciales conducen a un movimiento que queda confinado en el atractor. 

El volumen en el espacio de las fases para sistemas disipativos siempre disminuye y en sistemas de muchas dimensiones esto da lugar a una reducción en la dimensionalidad, cuando el sistema se aproxima al atractor, con una dimensión mucho menor que la del sistema dinámico mismo. 

En el caso simple de un péndulo amortiguado se produce una reducción de la dimensión de 2 a 1 al alcanzar el ciclo límite. 

- 20 - 

La diferencia entre los atractores extraños y los demás está en (ya lo hemos repetido varias veces, pero es muy importante) que éstos tienen sensibilidad a las condiciones iniciales. Dos trayectorias que empezaran arbitrariamente cerca acabarán totalmente separadas. Esto ocurre a la vez que el volumen se contrae, lo  que significa que no hay una contracción uniforme en todas las direcciones. Esto nos va a dar lugar a una reducción en la dimensionalidad del movimiento del sistema. 

El secreto de que separándose las trayectorias todo se mantenga en un espacio finito está en plegar, estirar y pegar el espacio de las fases. 
Plegamiento del espacio de las fases. 

Este proceso de estirar y pegar continua ad infinitum. Y esto es lo que le da complejidad al movimiento caótico. Es como amasar el pan. El caos amasa el espacio de las fases como si fuera un panadero. Dos puntos que al principio estaban cercanos acabarán muy lejos. Lo mismo puede pasar al revés. La figura resultante es un fractal. 

Un fractal es un objeto matemático autosemejante, es decir a cualquier escala es parecido a sí mismo. A ninguna escala encontramos simplicidad básica. Podemos verlo en el apéndice. 

- 21 - 

El conseguir una imagen de un atractor no es nada fácil. Normalmente suelen tener tres o más dimensiones. Una forma de visualizarlos, aunque sea poco a poco es cortarlos por rebanadas, llamadas secciones de Poincaré. Esta proyección retira una dimensión del atractor y convierte un línea de una trayectoria 
en un punto. 

Sección de Poincaré de un toroide 
Sección de Poincaré 

- 22 - 

## ¿Caos? 

Existen varias propiedades del caos que nos permiten reconocerlo en cualquier fenómeno. Estas propiedades también pueden servirnos para ver como el comportamiento caótico aparece en sistemas completamente deterministas. 

Una de ellas puede ser el estudio del espectro de frecuencias, que nos permitirá distinguir entre movimiento periódico, y caótico. 

Š(w)=sdt ewrx (1) 
P(w)= X(w) 

donde X(w) representa la transformada de Fourier de la función X(t) y P(w) representa el espectro de la función. Para movimiento periódico vamos a encontrar un conjunto discreto de líneas, mientras que en el caótico encontraremos un espectro continuo y mayor en las frecuencias bajas. En la transición de sistema periódico a caótico obtenemos un espectro oscilatorio primero y después la superposición de comportamiento oscilatorio y al fin un amplio espectro continuo típicamente caótico. 

La principal característica del movimiento caótico, la divergencia exponencial de las trayectorias nos puede servir como pista inequívoca. Esto implica una extremadamente alta sensibilidad a las condiciones iniciales. 

Tiene que ser continuo para dar lugar a movimiento aperiódico. 

- 23 - 

Un modo de caracterizar esta divergencia es el exponente de Lyapunov 
X(X). Vamos a trabajar con sistemas discretos. Al trabajar con secciones de Poincaré, los puntos no se mueven continuamente, sino que lo hacen de modo discreto. 

Xn+1 =f(x) 
tomamos como puntos Xo y Xo+€ 
Después de N iteraciones 
EENASS=fN(X +e)-FA 
y haciendo el límite e- 
0 
y 
N 
+ 
No 

Por ejemplo, para un punto fijo el exponente es negativo, para un ciclo límite es nulo y positivo para los atractores extraños. 
El exponente de Lyapunov nos da una medida de la separación entre dos puntos adyacentes después de una iteración. También da una idea del número de pliegues y estiramientos. 

Podemos representar el exponente de Lyapunov en función del parámetro b para la ecuación logística: 

Vemos como en los puntos en los que se produce bifurcación el exponente se hace positivo. Contrariamente, en las ventanas de movimiento regular dentro de la zona caótica, el exponente se hace negativo. 

- 24 - 

Exponente de Lyapunov de la ecuación logística. 

Para sistemas n-dimensionales tendremos un exponente de Lyapunov para cada eje. Un volumen inicial Vo se convertirá en media en: 

V=V.er, that ... thn)n 

Para sistemas disipativos la suma de los exponentes debe ser negativa. Si el sistema es caótico, al menos uno de los exponentes debe ser positivo. 
Otro parámetro que nos puede decir si el sistema es o no caótico es la entropía de Kolmogorov. Su definición procede la teoría de la información de Shannon. 

Sabemos de termo que la entropía es una medida del desorden del sistema y se incrementa cuando éste aumenta. 

Supongamos que tenemos un sistema en el que el resultado de una medida debe estar en un el intervalo unidad. Si lo dividimos en N subintervalos, podemos asociar al i-ésimo subintervalo una probabilidad pz. La entropía del sistema se definirá: 

-25 

S=-Klog(p;logp ;) 

Podemos definir para nuestro sistema una entropía K que nos da una medida de lo caótico que es su movimiento. Va a ser proporcional a la velocidad a la que el sistema pierde información. Por un lado tenemos una pérdida de información de las condiciones iniciales y por otro hay una aparición de información, pues de un conjunto de puntos sin estructura puede surgir la del atractor correspondiente. 

Un atractor caótico crea información, crea entropía. Une orden y desorden. La creación de información equivale a la aparición de pautas. Podemos ver esto en el Apendice que hay al final del trabajo. 

La entropía del. Kolmogorov está definida de forma que es nula en movimientos regulares, donde no se crea información. Es positiva para sistemas caóticos donde sí que se crea información y se vuelve infinita para sistemas aleatorios, ya que para representar el comportamiento de un sistema aleatorio necesitamos infinita información. 

Supongamos que fuéramos capaces, en algún modo de hacer que un sistema tuviera un atractor de una determinada forma. Tendríamos así un sistema con memoria, capaz de guardar una forma. Esta posibilidad parece interesante. 

No existe una única ruta que nos lleve desde el comportamiento regular hasta el caótico. Pero sí que existe una rica variedad de estados de inestabilidad intermedios hasta que se alcanza el caos. Algunas características típicas son: 

- 26 

- Cuando un parámetro de control típico del sistema se incrementa aparecen gradualmente más frecuencias, es como si se fueran excitando gradualmente.  Ocurre en láseres, osciladores y por supuesto en la turbulencia. 

- Ruelle y Takens encontraron teóricamente que un estado oscilatorio de dos frecuencias que se desarrolla en la superficie de un toroide, precedía al establecimiento del caos. Pero esta teoría se basa sólo en propiedades matemáticas del sistema y no puede ser aplicada directamente a situaciones reales. 
- Otro fenómeno típico es la intermitencia . Algunas cantidades permanecen estáticas y de repente cambian de modo caótico, volviendo a estar 
estáticas y otra vez caóticas, repitiéndose el proceso una y otra vez. 

- Otra posible ruta es una sucesión de bifurcaciones, de duplicaciones del período a medida que el parámetro de control del sistema va tomando unos valores determinados. Este mismo tipo de transición se ha encontrado en muchos sistemas. También se ha observado la aparición de otros armónicos. 

A continuación hablaremos de la universalidad de este fenómeno. 

-27 

## Resumiendo 

Nuestra imprecisión en la medida, nos da como resultado una 
impredecibilidad en nuestro resultado. 

En los sistemas regulares si dos puntos empezaban cercanos permanecen cercanos, los errores están bajo control. En sistemas caóticos ésto no ocurre. Por ésto no existen soluciones exactas, nuestra información inicial acaba distribuyéndose por todo el atractor al cabo de un cierto tiempo. 

Un atractor caótico amplifica las pequeñas fluctuaciones y acerca las trayectorias que antes estaban alejadas. Cualquier fluctuación se extiende, por eso es imposible anular el ruido. En el proceso de estirado y plegado del espacio de las fases se crea nueva información, aleatoria. 

Se ha demostrado en los últimos años que muchos sistemas presentan comportamiento estocástico debido a un simple atractor caótico (reacciones químicas, fluido calentado en una caja pequeña, ritmo cardíaco, ...) 

El saber que un sistema es caótico, no arregla nada, no nos da predicciones. 

Produce problemas a nivel del método científico. Verificar una teoría ahora se ve más difícil. Supongamos que se trata de un proceso caótico, las predicciones se vuelven imposibles. Deberemos usar propiedades estadísticas y geométricas. Nuestro modo de hacer física ha cambiado. Antes los sistemas que no eran integrables los estudiábamos como perturbaciones a partir de los regulares. 

- 28 - 

Ahora sabemos el caos es algo patológico de los sistemas. En el apartado del T KAM estudiaremos ésto con más detalle. 

Vemos como la interacción entre los componentes en una escala puede llevar a un comportamiento global mucho más complejo en otra escala mayor y que no puede reducirse al conocimiento de los componentes individuales. 

Todas estas cuestiones pueden hacernos entender mejor la irreversibilidad 


El mundo de los sistemas caóticos, y en general el de los no-lineales es realmente apasionante. Aparecen fenómenos nuevos, interesantes, capaces de sorprendernos, en este mundo donde ya nada despierta nuestro interés. 

- 29 - 

## Universalidad 

En 1975 Mitchell Feigenbaum, un físico teórico de partículas, descubrió la universalidad en las sucesiones iterativas de una dimensión. El descubrimiento era que grandes clases de sistemas mostraban transiciones hacia el caos universales y medibles cuantitativamente. 

Un experimento, ya clásico, en el que se encuentran pruebas de esta universalidad es el de Libchaber y Maurer. Tenemos un liquido dentro de una caja pequeña que es calentada por la parte de abajo. Podemos controlar el movimiento del sistema con el número de Raylegh R que es proporcional a la diferencia de temperaturas entre el fondo y la parte de arriba de la caja. Por supuesto el sistema es disipativo, los estados transitorios desperecerán con el tiempo. 

Para R pequeño hay flujo de calor pero no de líquido. Pasado un valor crítico aparece movimiento de convección en la caja que da lugar a dos cilindros. Para R mayor una onda de frecuencia fo comienza a recorrer los cilindros. En el espectro de frecuencias del sistema tendremos un solo pico. Si incrementamos AT aparecerá otra onda con menor amplitud y de frecuencia 

Si hacemos aún mayor AT aparecerán más ondas con frecuencias amplitudes mucho menores. Si volvemos a aumentar AT, el movimiento de los cilindros se vuelve turbulento. Ahora encontramos un espectro continuo con picos que destacan. Resumiendo, al aumentar el valor del parámetro de control hemos encontrado duplicaciones de período antes de que aparezca el movimiento caótico. 

- 30 
En los experimentos existe una resolución limitada. Para resultados más precisos, podemos usar modelo matemático. Tomemos la ecuación de un oscilador no lineal: 

on - 3+4x2= Acos(wa) 

Tenemos un tiempo característico del sistema To=271. La disipación la controla el parámetro k, el valor de A nos dará la amplitud del movimiento. 

Para muchas condiciones iniciales el sistema acaba atrapado en un ciclo límite de período To. El término disipativo hace que el sistema "olvide" las condiciones iniciales. La fuerza armónica hará que el oscilador no se pare. 

Si disminuimos el valor de k observaremos duplicaciones de período. Las trayectorias se hacen más complicadas, pero siguen siendo periódicas. Encontramos que aparecen órbitas de período 2"To, igual que ocurría antes de establecerse la turbulencia en el líquido. 

Realizamos una sección de Poincaré del sistema. En general se trata de ver la intersección de la trayectoria entera en el espacio de las fases con una superficie dada. En nuestro caso por ser unidimensional, será la intersección de una línea con la trayectoria del sistema, lo que nos dará un conjunto de puntos. 

Al principio cuando sólo teníamos un ciclo de período T, la intersección sería un solo punto. Ahora tendremos muchos puntos. Si miramos localmente las intersecciones veremos que coinciden las experimentales del líquido y las de nuestro oscilador, aunque las trayectorias no se parezcan globalmente. Si representamos nuestra sección de Poincaré en función del parámetro de control del sistema, obtendremos un árbol de bifurcación. 
Vemos que cualitativamente los hechos coinciden. El descubrimiento de Feigenbaum fue que también coincidían cuantitativamente. Dos fueron sus observaciones: 

- Las diferencias entre dos valores consecutivos del parámetro de control para los que hay bifurcación tiende a un valor universal 
P=limbi+by+ -Him 4 -4.6692... 
i-o biti-b; 
Ai+1 

-También el cociente entre consecutivas separaciones de las dos ramas cuando hay bifurcación es universal 
lim : -=2.5029 *** & +1 

Tenemos que le caos aparece tras una sucesión de duplicaciones de período.

Todo esto nos proporciona predicciones experimentales sobre valores de los parámetros de control para los que encontraremos bifurcaciones y sobre la separación de estos. Pero experimentalmente es muy difícil controlar el sistema hasta llegar a encontrar más allá de 5 6 6 bifurcaciones, lo que hace que no podamos dar las constantes con más de 2 decimales. En experimentos numéricos más complicados se ha podido llegar hasta un número de decimales que confirman totalmente los valores predichos. Por ejemplo se tiene que F-4.6692016091029909... 

- 32 

También existen experimentos en más de una dimensión. Por ejemplo Franceschini y Tebaldi estudiaron una truncación de las ecuaciones de Navier Stokes con 5 variables, lo que nos da un espacio de las fases de 10 dimensiones. Se encuentran duplicaciones de período en todas las secciones de Poincaré y las constantes F y a obtenidas están en perfecto acuerdo con los valores de Feigenbaum. 

Podemos explicar el que los sistemas de más dimensiones se comporten como unidimensionales si recordamos que el espacio de las fases se estira en algunas direcciones, se encoge en muchas y se pliega en todas. Así el sistema puede quedar reducido a unidimensional. 

Un estupendo resultado de la universalidad es que no importa lo cerca que nuestras ecuaciones estén de las reales. Mientras que el modelo esté en la misma clase de universalidad (tenga una misma forma de desarrollo en la f(x) que nos da la evolución) que el sistema real ambos tendrán una misma sucesión de duplicaciones de período. Esto significa que podemos obtener la física correcta de modelos muy simples. Pero por supuesto, no sabemos cuando dos sistemas están en la misma clase de universalidad. 

Mirando el espacio de las fases vemos que las trayectorias se mueven en una zona restringida del espacio de las fases. Para trabajar con ciclos límite es más cómodo expresar cada punto como función del anterior, Xn+1=f(x.). No sabemos la expresión explícita de f(x) pero sí que tiene que caer en los extremos, es decir que va a tener un máximo en un punto interior del intervalo xc. Podemos desarrollarla alrededor de este máximo en la forma: 

- 33 - 

f(x)=2, +az(x-x)2 +... 

Sabemos del estudio de este tipo de sucesiones, que un comportamiento estable no tiene porqué implicar la existencia de un valor límite, sino que se puede establecer un ciclo periódico. 

Como vimos tendremos bifurcación cuando la derivada de f(x) en el punto se haga en valor absoluto mayor que 1, lo que hará al punto inestable. 

Nuestro argumento no depende para nada de la forma explícita de f(x): aquí tenemos la universalidad de las duplicaciones de período. 

Pero esta universalidad no es sólo cualitativa. Para estudiar la estabilidad de un punto fijo hacemos un reescalado de su entorno. El entorno de éstos puntos queda prácticamente igual después de una iteración y un reescalado. Tras haber ampliado muchas veces los entornos, casi toda la información sobre la forma global de f(x) ha desaparecido. Nos queda una función universal g(x). Esta función se autoreproduce después de una iteración y un reescalado 

860)=-as 81-) 

lo que nos permite determinar a. 

Resumiendo. Tenemos un sistema multidimensional. La sección de Poincaré nos permite pasar del estudio de un sistema de ecuaciones diferenciales al estudio de iteraciones discretas. La disipación reduce la dimensión hasta dejar al sistema como unidimensional. Las sucesiones de bifurcaciones tienen lugar a escalas cada vez menores. Después de n bifurcaciones la separación entre las trayectorias será de a" y prácticamente no queda nada de la estructura global del sistema. Tenemos aquí la universalidad. 

- 34 

## Caos y ergodicidad. Teorema KAM

Nada hay que preocupe más a un físico dedicado a hacer mecánica estadística, que saber si su sistema tiene comportamiento ergódico o no. 
La mecánica estadística trata, aprovechando la enorme cantidad de partículas que forman un sistema real, de promediando, obtener información macroscópica sobre el sistema global. Esto equivale a decir que aprovechamos la gran cantidad de microestados compatibles con un macroestado para encontrar información útil sobre este último. 

Queremos, entonces, hacer promedios sobre los microestados en los que se encuentra el sistema. Para ello debemos saber cuales son éstos. Al conjunto de los estados posibles lo llamaremos espacio accesible y es donde promediaremos la función dinámica. 

Otra forma de promediar sería sobre el valor que va tomando la función a lo largo del tiempo. Físicamente podemos justificar esto pues nuestras medidas nunca son instantáneas y necesitamos un tiempo finito para hacerlas. Suponemos que durante este tiempo el movimiento microscópico del sistema es tal que nos permite afirmar que la trayectoria ha pasado por casi todos los microestados accesibles con igual probabilidad. Es la hipótesis ergódica. Así el promedio temporal y el promedio sobre el espacio accesible coincidirán. 

Dado un sistema y para aplicarle el formalismo de la mecánica estadística con toda tranquilidad necesitamos saber si su comportamiento es o no ergódico. 

- 35 - 

Sólo se ha demostrado este tipo de comportamiento para una clase de sistemas, una colección de esferas duras en una caja. Sin embargo la mayoría de todos los otros sistemas tienen un comportamiento mezcla de coherente y caótico. 

Veremos que sistemas de muy pocos grados de libertad (dos para ser mas exactos) pueden pasar de un comportamiento totalmente determinista a otro caótico, dependiendo la transición de un parámetro de control en el hamiltoniano del sistema. 

Podemos entender la transición de un tipo de comportamiento a otro con la ayuda del Teorema KAM formulado por Kolmogorov, Arnold y Moser. 

Tenemos un sistema integrable (es decir con el suficiente número de constantes del movimiento) de 2N grados de libertad, su espacio accesible en el espacio de las fases estará restringido a un superficie de dimensión N. Si ahora perturbamos el sistema aunque sea con una perturbación débil, podemos pensar que estas superficies serán destruidas, que la perturbación introduce algo patológico en el sistema o bien que sólo las deformará levemente. El Teorema KAM nos dice que las dos afirmaciones tienen su parte de verdad. Originariamente fue formulado en términos avanzados de topología, análisis y teoría de números, aquí lo formularemos de un modo más intuitivo: 

"Sea H=H.+2H, el hamiltoniano de un sistema. Con tal que a sea suficientemente pequeña, el espacio de las fases queda dividido en dos regiones de volumen no nulo (en el sentido de medida de Lebesgue), una de 
Fue formulado por Kolmogorov en 1954, pero se perdió su demostración. En 1963 Amold y Moser independientemente lo volvieron a demostrar. 

- 36 

las cuales es pequeña comparada con la otra y se encoge hasta medir cero cuando a tiende a anularse. La región mayor tiene la estructura de las superficies de H. pero recubiertas con trayectorias densas." 

O sea, para perturbaciones pequeñas la mayoría de las condiciones iniciales producen movimiento regular y las trayectorias están restringidas a la superficie. La superficie del hamiltoniano Ho es solo levemente distorsionada. Sin embargo hay una pequeña región (un conjunto de condiciones iniciales) en la que el sistema presenta comportamiento errático. Y esta región es de medida no nula. Tenemos comportamiento caótico introducido patológicamente en el sistema dentro del toroide. Incluso se conjetura que el movimiento sea ergódico. 

La mayoría de los movimientos periódicos con frecuencias inconmensurables continúan existiendo dentro del toroide sólo débilmente perturbados. Los de frecuencias conmensurables (o inconmensurables con una razón t/s cercana a un número racional con r y s pequeños) son grandemente perturbados y no permanecen en el toroide, dando lugar a movimiento estocástico o caótico. 

La perturbación va a introducir pequeñas zonas de resonancia en las cuales el sistema tendrá comportamiento caótico. A medida que la perturbación aumente las superficies se van destruyendo cerca de estas zonas. Cuando dos zonas vecinas se solapan, la superficie es completamente destruida y la trayectoria del sistema 

Tenemos una situación idéntica en la distribución de los asteroides en el sistema solar. Fue estudiado por Wisdom. Sus órbitas son perturbadas por Júpiter. Si estudiamos su distribución frente a la razón de la frecuencia angular del asteroide y la de Júpiter, encontramos que para razones racionales o cercanas no hay asteroides y sí para las irracionales. 
- 37 - 
puede vagar por las dos libremente. Si seguimos aumentado la perturbación llegarán a solaparse todas las zonas de resonancia y la región entera se volverá caótica. 

En un comportamiento determinista tenemos al sistema confinado en unas órbitas determinadas. En la transición a uno caótico estas órbitas empiezan a deformarse hasta llegar a llenar el espacio accesible. Si las órbitas llegaran a llenarlo completamente, podríamos tener comportamiento ergódico en el sistema. 

Para un astrónomo este resultado es estupendo. La perturbación de Plutón no va a hacer que la Tierra abandone su órbita. Su trabajo se reduce. Pero un físico interesado por la mecánica estadística hubiera preferido que el comportamiento del sistema se volviera caótico y que llenara el espacio de las fases accesibles, por lo que todos sus promedios temporales se verían justificados. 

Podemos recurrir al as que todos los físicos estadísticos tienen en la manga: dado el gran numero de grados de libertad de nuestros sistemas, las resonancias aparecen a montones y nuestro sistemas será ergódico. 

Vamos ver todo esto "con cuentas". 

Tenemos un sistema de dos grados de libertad. En variables acción y ángulo. 

H=H,0,1)) + VJ/2,41,42) 
OH, 

Si V=0 J;=cte y 

a 

Recordemos que la estabilidad del sistema solar un problema sin resolver aún. 

- 38 - 

Podemos representar esto gráficamente como un toroide de dos dimensiones con radios J; y donde o representa la variable angular. 

Desarrollando por Fourier 

H=H.(11/2) +fm (1) cos(mo, +nop) + ... 


Buscamos una transformación infinitesimal que nos elimine la dependencia angular. Encontramos que nos puede servir ésta: 

F=1,4, +1,42+Bm ni)sin(mų, +no) 

hacemos el cambio de variables Joli 

Ahora tenemos en primer orden H=H(, I)+{{mw,+nw,)Bm „(,+fm „[„Šx)}cos(m6, +n0,)+ ... 

CO 

Podemos anular la perturbación haciendo 

Bar -- Smo pa 
mn 
mw, +no 

con tal que mw, +nw, no sea muy pequeño, porque para que la 
transformación F sea infinitesimal, B debe ser pequeña, o sea, se debe cumplir 

mw, nw, Así encontramos una banda de frecuencias. Si la perturbación es grande entonces la banda de frecuencias será ancha. 

- 39 - 

Pao si tremos la distorsión de cos(mw, +nw,) también tendemos la decos(m'w, +n'w) 

siempre que ****, Tendremos entonces una multitud de perturbaciones que se 
m m' 
nnd 

suman. Se trata de un fenómeno de resonancia. 

El movimiento del sistema será el resultado del solapamiento de todas estas zonas de resonancia, siendo muy complicado, quizás ergódico. 
Si V es pequeño f lo será y la banda de frecuencias también. 

Si V es grande (o la energía se incrementa lo suficiente), la medida de las zonas de solapamiento de las resonancias se incrementa hasta que casi el espacio entero esta lleno de trayectorias erráticas. 

El Teorema KAM indica, no prueba, la posibilidad de transición de un movimiento periódico a otro predominantemente caótico y casi ergódico. 
Existen experimentos con ordenador. 

Dos astrónomos Henon y Heiles en 1983 haciendo un modelo de la distribución de estrellas dentro de la galaxias. Trataban de ver si existía alguna constante del movimiento además de la energía (si existiera, todas las trayectorias estarían confinadas en superficies bidimensionales. Al hacer una sección de Poincaré encontraríamos curvas. Si no tuviéramos esta constante la trayectoria sería tridimensional y sólo encontraríamos puntos dispersos aleatoriamente). EI hamiltoniano que usaron era 

- 40 - 

H=_+P3+qi+a)+a?an 

Para bajas energías encontraron que todas las trayectorias estaban sobre una superficie. Si incrementamos la energía vemos que empiezan a aparecer cadenas de islas alrededor de las órbitas estables, evidencia de la inestabilidad microscópica KAM. Si aumentamos la energía aún más, encontramos movimiento totalmente estadístico. 

Sección de Poincaré para el sistema de Henon-Heiles para baja energia 

- 41 - 

Para mayores energías las zonas de inestabilidad se hacen mayores. 

Para aún mayores energías, el comportamiento del sistema parece aleatorio. Sin embargo quizás para una mayor precisión en la integración encontrariamos otro resultado. 

- 42 - 

Vemos como hay cantidades que son constantes del movimiento para bajas energías, pero que van dejando de serlo al incrementarse la energía. 
Existen otros muchos experimentos como el de Thiele, Wilson y Bunker, el de Izrailev y Chirikov, etc. En todos ellos encontramos los mismos resultados. 

Vamos a estudiar con un poco de mayor detalle resonancias aisladas. Si 
tenemos un hamiltoniano de la forma 

H=H.(1/2) +fm (1) cos(mo, +no) 

Llamaremos a este tipo de perturbación una resonancia m-n y a la zona del toroide deformado dada por la desigualdad anterior zona de resonancia m-n. 
Este tipo de perturbación tiene una constante del movimiento 1=nd, -md, 
que nos permitirá calcular las curvas intersección de la trayectoria con el plano que queramos. 

Al introducir una perturbación 2-2 obtenemos en el plano Jz=0 las curvas de H, (que son circunferencias concéntricas) y la zona de la perturbación 2-2 encerada por una separatriz que se corta a sí misma en 2 puntos inestables. En cada lado de la separatriz encontramos órbitas estables. La resonancia aparece Para E20. Si incrementamos la energía las zonas de resonancia se alejan del origen, aumentando de tamaño. 

- 43 

Sección de Poincaré para resonancia 2-2. 

una 

Sección de Poincaré para una resonancia aislada 3-2. La cadena de tres islas aparece para E=0,08. 

- 44 - 

Estudiamos ahora una resonancia 3-2. Encontramos en el plano J,=0 igual que antes las curvas de H. y una separatriz que ahora se corta en tres puntos inestables, separando tres órbitas estables. La resonancia aparece para EžE, E #0 

Para una resonancia 2–3 encontramos un esquema similar pero en el plano 
JO. 

Una resonancia m-n (men) introduce m islas en J, y n en Jz. 

Una resonancia aislada distorsiona el toroide introduciendo por pares nuevas órbitas estables e inestables. Aparecen para E20 y están acotadas por una separatriz que pasa a través de los puntos inestables. Se puede demostrar que las zonas de resonancia se hacen cada vez menores cuando m yn crecen. 


Supongamos ahora que tenemos una resonancia doble, por ejemplo una 2-2 y una 2-3. Puesto que la 2-3 aparece para energías mayores que la 2–2 podemos usar el truco de Bon para eliminarla. Obtenemos una gráfica parecida a la obtenida para la resonancia 2-2. La constante del movimiento I ahora lo es con una menor precisión (si antes lo eran en 5 6 6 decimales, ahora no lo es con más de 3). 

Aumentamos la energía para que pueda aparecer la resonancia 2-3. Esperamos que la inestabilidad aparezca en la región en la que las dos zonas se solapan. Las dos resonancias aparecen en los lugares esperados, pero también encontramos cadenas de cinco y siete islas. 

- 45 

Sección de Poincaré para una resonacia doble 2-2 y 2-3. La resonancia 2-3 aún no ha aparecido. 

La resonancia 2-3 ya ha aparecido. Antes de que comiencen a solaparse aparece una cadena cinco islas. Aunque no se vea en el dibujo existen zonas de inestabilidad. 

- 46 - 

Podemos explicarlas del modo siguiente: el hamiltoniano H, con la resonancia 2-2 es integrable (pues tiene dos constantes del movimiento). 

Pasamos à unas nuevas coordenadas en las que el nuevo hamiltoniano H, no tenga dependencia angular. Tomamos el hamiltoniano total como el H, no perturbado y una resonancia 2–3. Si ahora transformamos a la inversa las coordenadas volviendo a las originales vemos que la resonancia 2–3 son las cadenas de 5 y 7 islas. Las llamaremos resonancias secundarias. 

Una integración más precisa nos muesta zonas de inestabilidad antes de que aparezca la resonancia 3-2. 

Cuando las resonancias 2-2 y 2-3 se acercan, las resonancias de órdenes mayores empiezan a distorsionar macroscópicamente la superficie del toroide. La inestabilidad se debe a la multitud de órbitas estables e inestables que aparecen en la estrecha región entre las dos resonancias. 

- 47 - 

Resumiendo tenemos que las resonancias aisladas no afectan grandemente al movimiento del sistema. Pero en cuanto que las zonas de resonancia empiezan a solaparse, la inestabilidad aparece y las trayectorias dejan el toroide. 

El teorema de Poincaré sobre la no existencia (no integrabilidad) de constantes del movimiento (ecuaciones del movimiento) había servido de base para la mecánica estadística. Nos daba un argumento para que los estados fueran igualmente probables. 

El teorema KAM prueba que aunque no existan constantes del movimiento, si V es pequeño la mayoría de las condiciones iniciales conducen al movimiento sin apenas influencias por las resonancias, con lo que no todos los estados son igualmente probables. 

La existencia de estas constantes no viola el Teorema de Poincaré porque la menor parte de las trayectorias que se mueve bajo la influencia de muchas resonancias está incluida densamente dentro de la zona de comportamiento regular. 

El teorema KAM apunta al inicio de una inestabilidad que daría lugar a trayectoria irregulares volviéndose el movimiento estadístico. 

La inestabilidad KAM ocurre solo cuando la amplitud del movimiento se vuelve grande. Sin embargo, a temperaturas cercanas al cero sigue siendo válidas las leyes estadísticas. Por tanto debe de existir una inestabilidad KAM incluso para pequeñas amplitudes. Encontramos esta inestabilidad para potenciales altamente repulsivos. 
- 48 - 
Hasta hace poco se pensaba que la ergodicidad era cosa de los sistemas de muchas partículas. Hemos visto que es posible encontrar zonas de comportamiento caótico para sistemas con sólo dos grados de libertad. 

Cuando aumentemos el número de grados de libertad se incrementará el número de resonancias y mayor será la probabilidad de que dos resonancias se solapen. Para un sistema típico de 106 partículas puede parecer que la ergodicidad es la regla y no la excepción. El teorema KAM no tiene en cuenta que al sumar todos lo pequeños efectos de todas las partículas obtengamos el resultado tan apetecido de la ergodicidad. 

De todas formas no se ha probado nada. No sabemos qué zonas de inestabilidad son ergódicas. Quizás con mayores precisiones de integración los puntos aparentemente aleatorios llevaran un cierto orden. 

Para pequeñas amplitudes sólo intervienen unas pocas resonancias, la mecánica estadística puede predecir solo unas pocas de las más simples magnitudes. Al aumentar la amplitud intervienen más resonancias permitiéndonos predecir más cantidades (pero no todas) correctamente. 
- 49 - 

## Caos cuántico 

La física cuántica no relativista está basada en la ecuación de Schrödinger, que es una ecuación diferencial cuyas soluciones nos darán distribuciones de probabilidad de cantidades observables. Algo que diferencia grandemente la física cuántica de la clásica son las relaciones de incertidumbre de Heisemberg entre dos variables conjugadas de una partícula (por ejemplo la posición y el momento o la energía y el tiempo) 
Axapel 

Esto nos impide conocer simultáneamente sus valores. 

Por ser una ecuación lineal obtendremos soluciones periódicas o cuasiperiódicas. Las relaciones de Heisemberg nos impiden tener trayectorias definidas. Por tanto los sistemas cuánticos no serán caóticos en el sentido que hemos usado hasta ahora. 

El principio de correspondencia de Bohr nos dice que para cortos periodos de tiempo (para que la energía esté fijada, para periodos mayores necesitamos cálculos cuánticos) podemos describir los estados atómicos muy excitados de un modo clásico. En estas condiciones las funciones de onda revelan características clásicas. 

Por ejemplo una partícula dentro de una caja bidimensional con forma de pista de atletismo tiene una probabilidad de estar cerca de las órbitas periódicas inestables de la correspondiente partícula clásica. 

- 50 - 

Podemos también estudiar átomos Rydberg, en los que un electrón están tan excitado que podemos suponerlo en un espectro continuo. Si añadimos al sistema un campo de microondas producimos la ionización del electrón que dependerá grandemente de la amplitud del campo y débilmente de la frecuencia. Esta fenómeno se ha simulado con éxito por medio de un modelo clásico. En el modelo encontramos comportamiento caótico para una amplitud mayor que un cierto valor crítico. Para estos valores de amplitud se producía la ionización en el sistema real. Para explicarlo podemos suponer que las trayectorias vagan por el espacio de las fases dando lugar a un mecanismo de difusión haciendo que el electrón se escape. 

- 51 - 

## Apéndice A: Fractales

Supongamos que miramos un objeto con un microscopio de resolución y aumento ilimitados. Si el objeto fuera un fractal, al incrementar el aumento obtendríamos cada vez más detalles. Pero la estructura observada sería totalmente similar a la que teníamos con menor aumento. Decimos que el objeto es autosimilar. Los objetos fractales son autosimilares, tienen simetría ante un cambio de escala. 

Conjunto de Cantor. D=0.631. 

El concepto de autosimilitud no es nuevo en física. Se había estudiado en detalle en las propiedades críticas de las transiciones de fase. Aquí la autosimilitud se consideraba como una peculiaridad de la competición entre orden y desorden a la temperatura de la transición. Podemos ver que es mucho más común y aparece en muchos fenómenos de equilibrio y no equilibrio, aparentemente no relacionados con las transiciones de fase. 

La mayoría de los métodos matemáticos empleados en la física se basan en funciones analíticas y podemos definir sus derivadas. La geometría usual trata de objetos suaves, sin defectos. Sin embargo en la naturaleza encontramos objetos que no poseen estas propiedades de suavidad y en los que la irregularidad parece 

- 52 - 

ser la norma y no la excepción. La geometría fractal trata estas irregularidades como elementos esenciales. 

Es claro que la autosimilitud no es compatible con la analiticidad. Una curva derivable (suave) no puede ser autosimilar, puesto que es aproximable localmente por una recta. La autosimilitud implica lo contrario, que a cada vez menores escalas encontramos la misma complejidad. 

www 
. 
.edu ergren 
Helecho fractal. D=1.5. 

Un árbol, una montaña o la costa tienen estructura autosimilar”. Pensemos en la costa. Desde el espacio podemos ver sólo los grandes cabos y golfos. 

Si viajamos en avión, veremos más golfos y cabos dentro de los que veíamos antes. Si volamos a ras de suelo, veremos otros aún menores dentro de los de antes. La longitud de la costa depende de la escala a la que la midamos. 

Vamos a definir todo esto con un poco de más rigor. 

Incluso nosotros mismos tenemos estructuras autosimilares en nuestro cuerpo como el aparato circulatorio o los pulmones. (Ver "Caos y fractales en la fisiologia humana" Goldberger, Rigney y West en Investigación y Ciencia). 
- 53 - 
Matemáticamente un fractal es un objeto en el que la dimensión Haussdorf es mayor que la topológica. La dimensión topológica es la normal, a la que estamos acostumbrados. Vamos a definir ahora la dimensión Haussdorf. 

Supongamos que tenemos nuestro objeto en un espacio de p dimensiones. 

Vamos a recubrir nuestro conjunto con cubos de lado ε. Sea N(E) el menor número de estos cubos necesario para cubrirlo. Este número se incrementará como  N(E)- " 

siendo D la dimensión Haussdorf de nuestro objeto. Despejando 

D = -lim logN(e) -0 log(e) 


donde hemos despreciado las constantes de proporcionalidad en el límite. 

Con esta definición evidentemente podemos obtener dimensiones no 
enteras. 

Veamos como recuperamos el concepto topológico de dimensión. Para un 
punto N(E)-1, lo que da D-0. Para una línea N(e)= 
y obtenemos D-1, para una superficie obtendríamos D=2 etc. 

Vamos a calcular la dimensión para el dibujo de la figura. Para construirlo retiramos el triángulo central de cada uno de los triángulos de la figura. En cada paso el no de triángulos se multiplica por tres y la longitud del lado se divide por dos, por lo que N(E)=3" y €=2 lo que nos da en total: D-lim log3" log3 -1.58496... 

n- log2" log2 
- 54 - 

Triángulo de Sierpinski. D=1.585 

Otra propiedad de los fractales es que pueden tener un superficie infinita guardando en su interior un volumen finito. 

Tenemos un ejemplo de esto en la conocida curva de Koch. Se obtiene retirando la parte central de cada uno de los lados de un triángulo y sustituyéndolos por dos segmentos de un tercio de la longitud del inicial.

- ^ are Curva de Koch 

Su dimensión: 

D =lim log3" =1.2628 
--- log2" 

Evidentemente su longitud es infinita, en cada paso multiplicamos el no de 
lados por cuatro y dividimos su longitud por tres. La longitud sería L =lim 
=00, 
- 
3 

Y el área es finita pues cabe en un círculo de radio el lado inicial. 
Esta última propiedad es la que permite que los atractores caóticos (gracias a su naturaleza fractal, el de Lorenz tiene dimensión 2.06 ) puedan contener en un volumen finito a las trayectorias que divergen exponencialmente unas de otras. 
- 55 - 


## Apéndice B: Atractor de Lorenz

Como aplicación y a la vez como ejercicio, me propuse reproducir una ilustración que encontré en el artículo "Caos" de Crutchfield. En ella se veía como la evolución en un atractor caótico depende fuertemente de las condiciones iniciales. Partiendo de muchos puntos arbitrariamente cercanos, podemos encontrar en ellos trayectorias completamente distintas. 

Para ello tomamos como parámetros del sistema de Lorenz: 

0=10, b= , R-28. 

Ahora hacemos evolucionar 100 puntos que inicialmente se encontraban en un volumen de 0.008. 

En los distintos dibujos podemos ver como se van separando las trayectorias. Me gusta especialmente el dibujo de 1000 iteraciones. Vemos como lo que antes era un punto, ahora es una línea y además plegada sobre sí misma. 

El proyecto era llegar hasta las 10000 iteraciones, pero un infortunado cortocircuito (causado por mi mismo) acabó con dos días de cálculo continuado de mi sufrido ordenador. El programa, que se incluye después, lo realicé en BASIC y se dejó correr en un Comodore Amiga. 

En la integración se usa el método de Runge-Kutta en cuarto orden, que si bien ralentiza al programa, sí que nos da una mayor precisión en los resultados. 

- 56 

```BASIC
*************************************************  
************  Atractor de Lorenz. ***************
************************************************** 
BEM definimos el sistema de ecuaciones diferenciales 
DEF FNx(x,y)=sig\(y-x) 
EF FNy(x, y, z)=x*(R-2)-y DEF FNz(x, y, z)=x*y-b*z 
REM condición inicial x=1 
y=10 z=3 
N 
REM parámetros sig=10 b=8/3 R=28 
REM paso de integración t=.01 
REM imágenes que queremos salvar DIM pau(15) 
FOR a=1 TO 15 > READ pau(a) 
NEXT > DATA 1,400,500,600,800, 1000, 1200, 1500, 1600, 2000,2500, 3000, 4000,5000, 
conpau=1 
REM ángulos de la perspectiva col=COS(3.1416/4) sil=SIN(3.1416/4) 
con=2 fx=8.9 fy=3 
REM pintamos atractor de Lorenz FOR por=1 TO 10000 
x0=x yO=y 20=z GOSUB paso 
GOSUB pintar.line > NEXT BEEP GOSUB pausa 
REM Ahora hacemos evolucionar DA puntos IT iteraciones 
iter: da=100 
-57 
it=10000 
DIM x1(da), y1(da), z1(da) DTM asignamos posiciones aleatorias FOR c=1 TO da 
x1(c)=10+RND/5 y1(c)=1+RND/5 
z1(c)=3+RND/5 NEXT 
XN 
FOR a=1 TO it 
FOR v=1 TO da 
x0=x1(v) yO=y1(v) 20=z1(v) GOSUB paso x1(v)=x yl(v)=y 
z1(v)=2 Ο NEXT 
IF a=pau(conpau) THEN conpau=conpau+1: GOSUB salvar.iter NEXT END 
imprimir: REM Pinta los dibujos en pantalla para poder imprimirlos > FOR b=1 TO 15 
c=pau(b) GOSUB leer 
NEXT → END 
salvar.iter: REM Guarda en un archivo las posiciones en pantalla de los puntos 
CLS 
a$="lorenz"+STR$ (a) OPEN "r", #1, a$,8 FIELD #1,4 AS X$,4 AS y$ FOR C=1 TO da 
x0=x1(c) yO=y1(c) 20=21(c) GOSUB pintar LSET X$=MKS$(280+x1) LSET y$=MKS$(170-yl) 
PUT #1,0 NEXT 
CLOSE #1 RETURN 
pintar.iter: REM pinta todos los puntos 
CLS 
- 58 - 
11 
11 
11 
PRINT a FOR c=1 TO da 
XO=x1(c) yO=y1(c) 20=z1(c) 
GOSUB pintar NEXT BEEP 
GOSUB pausa RETURN 
pausa: IF INKEY$="" THEN GOTO pausa RETURN 
> paso: 
REM Integra por medio de un Runge-Kutta en cuarto orden REM dado el inicial en x0 devuelve el final en x 
kix=t*FNx(x0, y0) kly=t*FNy(x0, y0, 20) kiz=t*FNz(x0, y0, 20) k2x=t+FNx(x0+k1x2,y0+k1y/2) k2y=t*FNy(x0+k1x/2, y0+k1y/2, z0+k12/2) k2z=t*FNz(x0+k1x/2, yO+k1y/2, 20+k12/2) k3x=t*FNX(X0+k2x/2,y0+k2y/2) k3y=t*FNy(xO+k2x/2, yO+k2y/2, 20+k2z/2) k3z=t*FN2(xO+k2x/2, yO+k2y/2,20+k2z/2) k4x=t*FNx(x0+k3x, yO+k3y) k4y=t*FNy(xO+k3x, yO+k3y, z0+k3z) k4zst*FNz(x0+k3x,y0+k3y, z0+k3z) 
NNN 
I NXN 
11 
x=x0+k1x/0+k2x/3+k3x/3+k4x/6 y=yO+kly/6+k2y/3+k3y/3+k4y/6 z=20+k1z/6+k2z/3+k3z/3+k4z/6 
RETURN 
REM rutinas gráficas 
pintaro: REM pinta en diédrico 
x1=80+x0*fx y1=50-yO*fy PSET (x1, y1) x1=80+x0*fx y1=180-20*fy PSET (x1, y1) x1=300+z0*fx y1=50-y0*fy PSET (x1, y1) 
pintar.line: 
- 59 - 
y pinta lineas en isométrica, recordando el último punto 
x1=(co1*x0+si1*y)*fx y1=(20-x0*si1+co1*y0)*fy IF flag=0 THEN xold=x1:yold-yl:flag=1 LINE (280+xold, 170-yold)-(280+x1,170-y1) xold=x1 yold=y1 
RETURN 
pintar: REM pinta lineas en isométrica 
x1=(co1*xO+si1*y0 )*fx y1=(20-x0*sil+c01*y0 )*fy PSET (280+x1,170-y1) 
RETURN 
ejes: REM pinta los ejes COLOR 2 
O 
FOR a=-40 TO 40 STEP .4 
XO=a yO=0 20=0 GOSUB pintar XO=0 yO=a GOSUB pintar yO=0 20=a*1.2 
GOSUB pintar NEXT RETURN 
leer: REM carga un archivo de imagen del disco 
CLS PRINT C OPEN "r",#1, "lorenz"+STR$(c),8 FIELD #1,4 AS x$,4 AS y$ 
FOR a=1 TO 100 
GET #1, a 
PSET (CVS (x$), CVS(y$)) NEXT CLOSE #1 
```

### Evolución en el atractor de Lorenz 

- 60 - 
Evolución en el atractor de Lorenz 
- 61 - 
Evolución en el atractor de Lorenz 
- 62 - 
ID Evolución en el atractor de Lorenz 
- 62 - 
Evolución en el atractor de Lorenz: 488 
- 63 - 
Evolución en el atractor de Lorenz: 588 
- 64 - 
Evolución en el atractor de Lorenz 688 
- 65 
ID Evolución en el atractor de Lorenz 888 
- 66 
Evolución en el atractor de Lorenz 1888 
- 67 - 
Evolución en el atractor de Lorenz 1288 
- 68 
Evolución en el atractor de Lorenz 1588 
- 69 - 
Evolución en el atractor de Lorenz 1688 
- 70 - 
Evolución en el atractor de Lorenz 2888 
- 71 - 
Evolución en el atractor de Lorenz 2588 
- 72 - 
Evolución en el atractor de Lorenz: 3888 
- 73 
Evolución en el atractor de Lorenz 4888 
- 74 
Evolución en el atractor de Lorenz 5888 
- 75 - 
- 76 - 

## Bibliografía

### Bibliografía utilizada

- Nonlinear resonance and chaos in conservative systems, L.E. Reichl & W.M. Zheng. 
- Amplitude instability and ergodic behavior for conservative nonlinear oscillator system, Grayson H. Walker & Joseph Ford. Physical Review V. 188 N.1. 
- Apendice The ergodic problem, Balescu. 
- Movimiento caótico, Antonio F. Rañada, Investigación y Ciencia, Marzo 1986. 
- Chaos, Order, Patterrns, Fractals. An overview S. Lundqvist. 
- Caos, Crutchfield, Doyne Farmer, Investigación y Ciencia Febrero  1987. 
- One-dimensional iterative maps, H.A. Laumerierr. 
- Fractals in Physics: introductory concepts, L. Pietronero. 
- Order and Chaos in Hamiltonian system, I.C. Precival. 
- Universality in Chaos, Cvitanovic. 



- 77 

### Para ampliar
- Chaotics dynamic: an introduccion, Baker and Gollub. 
- Caos cuántico, Martin C. Gutzwiller. 
- Chaotic dynamic and strange attractors, David Ruelle. 
- Como hacer caos en casa, Investigacion y ciencia Marzo 1992. 

- 78 -
