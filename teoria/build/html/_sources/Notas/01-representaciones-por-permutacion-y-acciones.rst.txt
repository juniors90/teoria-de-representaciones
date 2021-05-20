Teoría de Representaciones de Grupos
=====================================

Introducción
------------

Para comprender las notas del curso se deben tener nociones de

- Teoría de Grupos
- Álgebra lineal

En matemáticas, la palabra "representación" significa básicamente "función de preservación de la estructura". Por lo tanto, en la "Teoría de Grupos" una representación es un homomorfismo.

Pero, más concretamente, debería ser un homomorfismo de un objeto (grupo o anillo) que se está intentando estudiar a otro que es de alguna forma más concreto y por tanto, de un salto, más fácil de entender. Los dos tipos de grupos concretos más simples son, en primer lugar, el grupo de todas las permutaciones de un conjunto arbitrario y, en segundo lugar, el grupo de todas las transformaciones lineales invertibles en un espacio vectorial arbitrario. Entonces, para los grupos, las representaciones más comúnmente estudiadas son las representaciones de permutación y las representaciones lineales.

Representaciones por Permutación y Acciones
-----------------------------------------------

Definición
~~~~~~~~~~~~~

Una representación de permutación de un grupo :math:`G` en un conjunto :math:`S` es un homomorfismo de :math:`G` al conjunto (grupo) de todas las permutaciones de :math:`S`.

    Preguntar si es conjunto o grupo de permutaciones.

Definición
~~~~~~~~~~~~~
    
Una representación lineal de un grupo :math:`G` en un espacio vectorial :math:`V` es un homomorfismo de :math:`G` al grupo de todas las transformaciones lineales invertibles de :math:`V`.


A menos que esté calificado con algún otro adjetivo, "representación" generalmente significa "representación lineal", por lo que este curso se ocupará de las representaciones lineales de grupos. Por lo general, restringiremos nuestra atención a grupos finitos y espacios vectoriales sobre el campo complejo, ya que esto simplifica las cosas y proporciona una teoría más completa. Si bien sería posible lanzarnos de inmediato al desarrollo de esta teoría, primero dedicaremos un poco de tiempo a familiarizarnos con algunos pequeños grupos finitos, para luego poder ver cómo se aplica la teoría en ejemplos particulares.

- El fundador del tema fue Ferdinand Georg Frobenius (1849-1917), quien descubrió las asombrosas propiedades básicas de los caracteres grupales irreductibles y las publicó en una serie de artículos en la década de 1890.
- Su alumno, Issai Schur, fue otro que hizo muchas contribuciones tempranas importantes al tema.
- En su forma moderna, el tema debe mucho a las contribuciones de Emmy Noether (en la década de 1920), cuyo trabajo forma la base de lo que ahora se llama "álgebra moderna".
- Sobre esta base, Richard Brauer desarrolló la teoría de la representación modular, en la que se estudian las representaciones sobre campos de características distintas de cero y se relacionan con representaciones complejas.

Grupos
----------

Los grupos se inventaron como una herramienta para estudiar objetos simétricos. Estos pueden ser objetos de cualquier tipo. Si definimos una simetría de un objeto como una transformación de ese objeto que conserva su estructura esencial, entonces el conjunto de todas las simetrías del objeto forma un grupo. En matemáticas siempre es posible considerar cualquier objeto como un conjunto con alguna estructura adicional; por tanto, una simetría es una función biyectiva que preserva la estructura desde el conjunto hacia sí mismo. La composición de funciones proporciona una operación en este conjunto, y no es difícil demostrar que los axiomas de grupo deben satisfacerse.

Por ejemplo, un campo es un conjunto dotado con operaciones de suma y multiplicación, que satisface varios axiomas. Un cuadrado puede considerarse como un conjunto de puntos y líneas en el plano euclidiano que satisfacen varias propiedades relacionadas con los ángulos y las distancias. Una simetría de un campo es una función biyectiva del campo a sí mismo que conserva las operaciones de suma y multiplicación. (Es decir, una simetría de un campo es un automorfismo del campo). Una simetría de un cuadrado es una función del conjunto relevante de puntos y líneas a sí mismo que conserva todos los ángulos y distancias. En ambos casos, el conjunto de todas las simetrías es un grupo.

Está claro que la combinación de dos funciones que conservan alguna propiedad también conservará esa propiedad. Por ejemplo, si :math:`R` es un conjunto equipado con una operación :math:`\ast` (como suma o multiplicación) y si :math:`f, g: R \to R` son funciones que conservan :math:`\ast`, entonces para todo :math:`x, y \in R`

.. math::

    (fg)(x \ast y) = f(g(x \ast y)) = f((gx) \ast (gy)) = (f(gx)) \ast (f(gy)) = ((fg)x) \ast ((fg)y),

para que :math:`fg` también conserve :math:`\ast`. De manera similar, si :math:`S` es un conjunto de puntos en el plano euclidiano y :math:`\phi, \psi: S \to S `son funciones que conservan ángulos, entonces para todo :math:`P_{1}, P_{2}, P_{3} \in S`,

.. math::

    \begin{align}
        \angle P_{1}, P_{2}, P_{3} &= \angle P_{1}'P_{2}'P_{3}' \text{ donde } P_{i}' = \psi P_{i} \\
                                   &= \angle P_{1}''P_{2}''P_{3}'' \text{ donde } P_{i}'' = \phi P_{i}' = ( \phi \psi ) P_{i},
    \end{align}

de modo que :math:`\phi \psi` también conserva los ángulos. Así se puede ver que el compuesto de dos simetrías es una simetría. De manera similar, la inversa de una simetría también es una simetría. Además, la composición de funciones es una operación asociativa. De modo que se satisfacen los axiomas de grupo. Podemos esperar que comprender el grupo de simetría de un objeto pueda conducir a una comprensión más profunda del objeto en sí.

La teoría de la representación en realidad invierte esta filosofía. Si uno considera los grupos como cosas que son de interés por derecho propio, entonces quizás uno pueda esperar comprender mejor un grupo dado descubriendo un objeto del cual el grupo es el grupo de simetría, y usando las propiedades de ese objeto para descubrir información sobre el grupo. grupo. Sin embargo, el tema subyacente sigue siendo que los elementos de un grupo deben asociarse con las transformaciones de un conjunto. Por tanto, la siguiente definición es natural.

acción de un grupo sobre un conjunto
------------------------------------

Una acción de un grupo :math:`G` sobre un conjunto :math:`S` es una función :math:`(g, s) \mapsto gs` de :math:`G \times S` a :math:`S` tal que
    
    :math:`(i)` :math:`(gh)s = g(hs)` para todo :math:`g, h \in G`, :math:`s \in S`,

    :math:`(i)` :math:`1s = s` para todo :math:`s \in S`, donde :math:`1` es el elemento identidad de :math:`G`.

.. note::

    - Habitualmente usaremos la notación ":math:`1`" para el elemento de identidad de un grupo abstracto, aunque si la operación de grupo se escribe como ":math:`+`" entonces usaremos ":math:`0`" para la identidad. Para un grupo de transformaciones de un conjunto, el elemento identidad será la función identidad del conjunto a sí mismo, y esto lo denotaremos por ":math:`id`". La matriz de identidad se indicará con ":math:`I`"

    - Una acción de :math:`G` sobre :math:`S` puede verse como una regla para multiplicar elementos de :math:`S` por elementos de :math:`G`, de modo que el resultado es otro elemento de :math:`S`.

Ejemplos
------------------------------------

Pasamos ahora a una discusión de algunos ejemplos de grupos.

El grupo cíclico :math:`C_{n}` consta de :math:`n` elementos :math:`1`, :math:`x`, :math:`x^{2}`, :math:`\dots`, :math:`x^{n-1}`, donde :math:`x^{n}=1`. Este grupo se puede representar como el grupo de todas las rotaciones del plano que llevan consigo un polígono regular de :math:`n` lados, representando :math:`x` como una rotación a través de :math:`2\pi / n`. Alternativamente, se puede pensar en el grupo aditivo de :math:`\mathbb{Z}_{n}`, el anillo de números enteros módulo :math:`n`, identificando el generador :math:`x` de :math:`C_{n}` con :math:`1\in\mathbb{Z}_{n}`, y el elemento identidad de :math:`C_{n}` con :math:`0\in\mathbb{Z}_{n}`. Otra realización de este grupo se obtiene identificando :math:`x^{k}` con el número complejo :math:`e^{k (2\pi i / n)}`, siendo la operación de grupo la multiplicación habitual de números complejos.

Podemos obtener una representación de permutación de :math:`C_{n}` en el conjunto :math:`{1, 2,\dots , n}` mapeando :math:`x` a la permutación :math:`\sigma` definida por :math:`\sigma i = i + 1` para :math:`1 \leq i \leq n - 1` y :math:`\sigma n = 1`, y podemos obtener una representación matricial de :math:`C_{n}` mapeando :math:`x` a la matriz :math:`\left(\begin{matrix} \cos{\theta} & -\sin{\theta} \\ \sin{\theta}  & \cos{\theta}  \end{matrix}\right)` de orden :math:`2 \times 2`, donde :math:`\theta = 2\pi / n`.

En este punto, el estudiante tendría razón al quejarse de que no se ha dado una definición adecuada de :math:`C_{n}`. ¿Qué es este grupo cíclico, realmente? ¿Son sus elementos los símbolos :math:`x^{k}`, y si hubiéramos escrito :math:`y^{k}` en su lugar, sería el mismo grupo o uno diferente? ¿O los elementos de :math:`C_{n}` son realmente números enteros módulo :math:`n`, o raíces :math:`n`-ésimas complejas de :math:`1`, o quizás ciertas permutaciones o ciertas matrices? De hecho, hablar del grupo cíclico de orden :math:`n`, como hacen los teóricos de grupos, es bastante impreciso. Los cinco ejemplos que dimos anteriormente pueden denominarse grupos cíclicos de orden :math:`n`. Sin embargo, el hecho crucial es que dos grupos cíclicos cualesquiera de orden :math:`n` son isomorfos entre sí: si :math:`G` y :math:`H` son ambos grupos cíclicos de orden :math:`n`, entonces existe una correspondencia uno a uno entre los elementos de :math:`G` y los elementos de :math:`H` que respeta las dos operaciones del grupo. Cuando un teórico de grupos dice "hay solo un grupo cíclico de orden :math:`n`", lo que se quiere decir es que solo hay una clase de isomorfismo de grupos cíclicos de orden :math:`n`. Si uno realmente quisiera tener un solo objeto llamado grupo cíclico de orden :math:`n`, ¡tendría que ser de hecho una clase de grupos de isomorfismo, en lugar de un grupo!

Antes de continuar con ejemplos de grupos, necesitamos una notación para las permutaciones. Una permutación de un conjunto es una función biyectiva del conjunto a sí mismo. Si :math:`\sigma` es una permutación de :math:`\{1, 2,\dots, n\}` luego :math:`\sigma 1`, :math:`\sigma 2`, :math:`\dots`, :math:`\sigma n` son :math:`1`, :math:`2`, :math:`\dots`, :math:`n` en algún orden, y escribimos :math:`\left[\begin{matrix} 1 & 2 & \dots & n \\ \sigma 1  & \sigma 2 & \dots & \sigma n  \end{matrix}\right]`. Así, por ejemplo, :math:`\left[\begin{matrix} 1 & 2 & 3 & 4 & 5 \\ 4 & 1 & 5 & 2 & 3 \end{matrix}\right]`  denota la función :math:`\sigma: \{1, 2, 3, 4, 5\} \to \{1, 2, 3, 4, 5\}` tal que :math:`\sigma 1 = 4`, :math:`\sigma 2 = 1`, :math:`\sigma 3 = 5`, :math:`\sigma 4 = 2` y :math:`\sigma 5 = 3`. Habiendo introducido esta notación, quiero abandonarla inmediatamente a favor de la "notación cíclica" más compacta, que hace que la permutación anterior sea :math:`(1, 4, 2) (3, 5)`. En la notación cíclica para :math:`\sigma` los elementos del conjunto :math:`\{1, 2,\dots, n\}` se reúnen en secuencias en las que cada término sucesivo se obtiene aplicando :math:`\sigma` al anterior, y :math:`\sigma` aplicado al último término de una secuencia da el primero. Las secuencias con un solo término :math:`k` corresponden a aquellas :math:`k` para las que :math:`\sigma k = k`, y estas a menudo se omiten. Por lo tanto, en la notación de ciclo, la permutación :math:`\tau = \left[\begin{matrix} 1 & 2 & 3 & 4 & 5 \\ 3 & 2 & 4 & 1 & 5 \end{matrix}\right]` generalmente se escribe como :math:`(1, 3, 4)`, pero a veces se escribe como :math:`(1, 3, 4) (2) (5)` , especialmente si no está claro por el contexto que :math:`\tau` es una permutación de :math:`\{1, 2, 3, 4, 5\}` en lugar de :math:`\{1, 2, 3, 4\}`.

La combinación de dos permutaciones :math:`\sigma` y :math:`\tau` del mismo conjunto es la función στ definida por :math:`(\sigma \tau) k = \sigma (\tau k)` para cada :math:`k`. Como la combinación de dos biyecciones es una biyección, se deduce que :math:`\sigma \tau` es una permutación. El conjunto de todas las permutaciones de un conjunto dado :math:`S` forma un grupo, llamado grupo simétrico en :math:`S`, y a veces denotado por :math:`Sym(S)`. Si el número de elementos en :math:`S` es :math:`n`, entonces :math:`Sym(S)` se llama grupo simétrico de grado :math:`n`, comúnmente escrito como :math:`S_{n}`. Por supuesto, existe realmente un grupo simétrico de grado :math:`n` para cada conjunto de :math:`n` elementos, pero todos son isomórficos entre sí y, en cualquier caso, es natural y habitual utilizar el conjunto :math:`\{1, 2,\dots, n\}` como el conjunto estándar de :math:`n` elementos (a menos que el contexto favorezca alguna otra opción). Observe que el grupo :math:`S_{3}` tiene seis elementos, es decir, :math:`id`, :math:`(1, 2)`, :math:`(1, 3)`, :math:`(2, 3)`, :math:`(1, 2, 3)` y :math:`(1, 3, 2)`. La tabla de multiplicar para este grupo es la siguiente.

+-------------------+-----------------+-----------------+------------------+------------------+---------------------+----------------------+
| :math:`S_{3}`     | :math:`id`      | :math:`(1,2)`   | :math:`(1, 3)`   | :math:`(2, 3)`   | :math:`(1, 2, 3)`   | :math:`(1, 3, 2)`    |
+===================+=================+=================+==================+==================+=====================+======================+
| :math:`id`        | :math:`id`      | :math:`(1,2)`   | :math:`(1,3)`    | :math:`(2, 3)`   | :math:`(1, 2, 3)`   | :math:`(1, 3, 2)`    |
+-------------------+-----------------+-----------------+------------------+------------------+---------------------+----------------------+
| :math:`(1,2)`     | :math:`(1,2)`   | :math:`id`      | :math:`(1,3,2)`  | :math:`(1,2,3)`  | :math:`(2, 3)`      | :math:`(1, 3)`       |
+-------------------+-----------------+-----------------+------------------+------------------+---------------------+----------------------+
| :math:`(1,3)`     | :math:`(1,3)`   | :math:`(1,2,3)` | :math:`id`       | :math:`(1,3,2)`  | :math:`(1, 2)`      | :math:`(2, 3)`       |
+-------------------+-----------------+-----------------+------------------+------------------+---------------------+----------------------+
| :math:`(2, 3)`    | :math:`(2, 3)`  | :math:`(1,3,2)` | :math:`(1,2,3)`  | :math:`id`       |  :math:`(1, 3)`     | :math:`(1, 2)`       |
+-------------------+-----------------+-----------------+------------------+------------------+---------------------+----------------------+
| :math:`(1,2,3)`   | :math:`(1,2,3)` | :math:`(1, 2)`  | :math:`(2, 3)`   | :math:`(1,2)`    |  :math:`(1,3,2)`    | :math:`id`           |
+-------------------+-----------------+-----------------+------------------+------------------+---------------------+----------------------+
| :math:`(1,3,2)`   | :math:`(1,3,2)` | :math:`(2, 3)`  |  :math:`(1, 2)`  | :math:`(1,3)`    |  :math:`id`         | :math:`(1, 2, 3)`    |
+-------------------+-----------------+-----------------+------------------+------------------+---------------------+----------------------+




Revisemos una entrada en esta tabla. Si :math:`\sigma = (1, 2, 3)` y :math:`\tau = (1, 3)` entonces

.. math::

    \begin{align}
        (\sigma \tau) 1 &= \sigma (\tau 1) = \sigma 3 = 1,\\
        (\sigma \tau) 2 &= \sigma (\tau 2) = \sigma 2 = 3,\\
        (\sigma \tau) 3 &= \sigma (\tau 3) = \sigma 1 = 2.
    \end{align}

de modo que :math:`\sigma \tau = (2, 3)`, de acuerdo con la tabla.

Manteniendo la notación :math:`\sigma = (1, 2, 3)` y :math:`\tau = (1, 3)`, observe que :math:`\tau \sigma \tau = (1, 3, 2) = \sigma^{-1}`. Esta relación permite reescribir cualquier producto de potencias de :math:`\sigma` y potencias de :math:`\tau` de modo que las potencias de :math:`\sigma` precedan a las potencias de :math:`\tau`. Dado que :math:`\tau = \tau^{− 1}` la relación :math:`\tau \sigma \tau = \sigma^{-1}` puede escribirse alternativamente como :math:`\tau \sigma = \sigma^{-1} \tau` o como :math:`\tau \sigma^{-1} = \sigma \tau`; en consecuencia, siempre se puede mover :math:`\tau` más allá de :math:`\sigma^{\epsilon}` a expensas de reemplazar :math:`\sigma^{\epsilon}` por :math:`\sigma^{-\epsilon}`. Por ejemplo,

.. math::

    (\sigma^{2}\tau)(\sigma \tau) = \sigma^{2}(\sigma^{−1}\tau)\tau= \sigma.

Tales consideraciones, cuando se combinan con el hecho de que :math:`\sigma^{3} = id`, dejan en claro que el producto de dos elementos cualesquiera del conjunto :math:`\{id, \sigma, \sigma^{2}, \tau, \sigma \tau, \sigma^{2}\tau \}` siempre será otro elemento del mismo conjunto.

Además, si :math:`\sigma^{i} \tau^{j} = \sigma^{k} \tau^{l}` entonces :math:`\sigma^{i-k} = \tau^{l-j}`; sin embargo, la única permutación que es tanto una potencia de :math:`\sigma` como una potencia de :math:`\tau` es id, por lo que se deduce que :math:`\sigma^{i} = \sigma^{k}` y :math:`\tau^{j} = \tau^{l}`. Las seis expresiones :math:`\sigma^{i} \tau^{j}` para :math:`i \in \{0, 1, 2\}` y :math:`j \in \{0, 1\}` corresponden a seis elementos distintos del grupo, y como :math:`S_{3}` tiene solo seis elementos en total, los tenemos todos. El resultado de esto es que la estructura de :math:`S_{3}` está completamente determinada por las relaciones :math:`\sigma^{3} = \tau^{2} = id` y :math:`\tau \sigma \tau = \sigma^{-1}`.

Observe que :math:`S_{3}` es isomorfo al grupo de todas las simetrías de un triángulo equilátero. Etiquetar los vértices del triángulo como :math:`1`, :math:`2` y :math:`3` nos permite identificar las simetrías con permutaciones de los vértices y vemos que hay tres simetrías de rotación (a través de ángulos de :math:`0`, :math:`2\pi/3` y :math:`4\pi/3`) correspondientes permutaciones :math:`id`, :math:`(1, 2, 3)` y :math:`(1, 3, 2)`, y tres simetrías de reflexión correspondientes a los otros tres elementos de :math:`S_{3}`. (Por ejemplo, la reflexión en la bisectriz perpendicular del lado que une el vértice :math:`1` y el vértice :math:`2` intercambia estos dos vértices y fija el otro, y por lo tanto corresponde a la permutación :math:`(1, 2)`.)

El grupo de todas las simetrías de un polígono regular de :math:`n` lados se conoce como grupo diedro de orden :math:`2n`. Muchos autores denotan este grupo por :math:`D_{2n}`, y muchos otros lo denotan por :math:`D_{n}`. Hay :math:`n` simetrías de rotación, a través de ángulos de :math:`2k\pi/n`, donde :math:`k \in \{1, 2,\dots , n− 1\}`, y hay :math:`n` simetrías de reflexión, en las :math:`n` líneas que son las bisectrices de los ángulos internos y las bisectrices perpendiculares de los lados. (Tenga en cuenta que si :math:`n` es par entonces para cada lado del polígono hay un lado opuesto, y las bisectrices perpendiculares de estos dos lados son iguales. Asimismo, la bisectriz del ángulo en un vértice coincide con la bisectriz del ángulo en el vértice opuesto. Si :math:`n` es impar, entonces la bisectriz de un ángulo coincide con la bisectriz perpendicular del lado opuesto.) Si dejamos que :math:`\sigma` sea la rotación en sentido horario a través de :math:`2 \pi / n` y sea :math:`\tau` cualquiera de las reflexiones, entonces es bastante fácil para comprobar que se cumplen las siguientes relaciones: :math:`\sigma^{n} = \sigma^{2} = id`, y :math:`\tau \sigma \tau = \sigma^{-1}`. Como en el caso :math:`n = 3`, tratado anteriormente, vemos que los :math:`2n` elementos del grupo son :math:`id`, :math:`\sigma`, :math:`\sigma^{2}`, :math:`\dots` , :math:`\sigma^{n-1}`, :math:`\tau`, :math:` \sigma \tau`, :math:`\sigma^{2} \tau`, :math:`\dots` , :math:`\sigma^{n-1} \tau`.

Además, la tabla de multiplicar está completamente determinada por las relaciones que hemos escrito. También es sencillo representar el grupo diedro como un grupo de permutaciones.

Numeración de los vértices del polígono regular :math:`1`, :math:`2`, :math:`\dots`, :math:`n` (sentido horario), la rotación :math:`\sigma` corresponde al :math:`n`-ciclo :math:`(1, 2, \dots , n)`, mientras que la reflexión en la bisectriz perpendicular del lado que une los vértices :math:`1` y :math:`n` corresponde a la permutación :math:`(1, n )(2, n - 1)(3, n - 2)\dots`, donde el último factor es :math:`(k, k + 1)` si :math:`n = 2k` es par, o :math:`(k - 1, k + 1)` si :math:`n = 2k - 1` es impar.

Podemos obtener un grupo interesante con :math:`21` elementos, que son permutaciones del conjunto :math:`\{1, 2, 3, 4, 5, 6, 7\}`, de la siguiente manera. Sea :math:`a = (1, 2, 3, 4, 5, 6, 7)` y sea :math:`b = (2, 3, 5) (4, 7, 6)`.

Claramente :math:`a^{7} = id` y :math:`b^{3} = id`. (Por ejemplo, :math:`b^{3}2 = b (b (b2)) = b (b3) = b5 = 2`.) También es fácil comprobar que

.. math::

    \begin{align}
        bab^{−1} &= (2, 3, 5)(4, 7, 6)(1, 2, 3, 4, 5, 6, 7)(7, 6, 4)(5, 3, 2)    \\
                 &= (1, 3, 5, 7, 2, 4, 6)                                        \\
                 &= a^{2}.
    \end{align}


Entonces :math:`ba = a2b`, y esta relación nos permite reescribir cualquier producto de las potencias de :math:`a` y las potencias de :math:`b` de modo que todas las potencias de :math:`a` precedan a todas las potencias de :math:`b`. Por ejemplo,

.. math::

    \begin{align}
    (ab^{2})(a^{2}b) &= ab(ba)ab = ab(a^{2}b)ab = aba^{2}(ba)b = aba^{3}(a^{2}b)b = a(ba)a^{3}b^{2}\\
                     &= a(a^{2}b)a^{3}b^{2} = a^{3}(ba)a^{2}b^{2} = a^{3}(a^{2}b)a^{2}b^{2}\\
                     &= a^{5}(ba)ab^{2} = a^{5}(a^{2}b)ab^{2} = (ba)b^{2} = a^{2}b^{3}.
    \end{align}

De ello se deduce que el producto de dos elementos cualesquiera del conjunto :math:`\{a^{i}b^{j} | 0 \leq i \leq 6, 0 \leq j \leq 2\}` también está en este conjunto. Las potencias de no identidad de a son todas de :math:`7`-ciclos, y dado que ninguna potencia de b es una potencia de :math:`7`-ciclos, se deduce que el único elemento que es simultáneamente una potencia de :math:`a` y una potencia de :math:`b` es la identidad. Ahora bien, si :math:`a^{i}b^{j} = a^{k}b^{l}` entonces :math:`a^{i-k} = a^{l-j}` que debe ser la identidad, de donde :math:`a^{i}= a^{k}` y :math:`b^{j} = b^{l}`. Así que hay :math:`21` elementos distintos en el conjunto anterior, y no es difícil ver que deben constituir un grupo.

Este grupo - o, más bien, un grupo isomorfo a este grupo - también se puede construir mediante el uso de matrices. Sea :math:`\omega = e^{2\pi i / 7}`, y sea

.. math::

    \begin{align}
        a &= \left(\begin{matrix} \omega & 0 & 0 \\ 0 & \omega^{2} & 0 \\ 0 & 0 & \omega^{4}\end{matrix}\right) &&&
        b &= \left(\begin{matrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 1 & 0 & 0 \end{matrix}\right)
    \end{align}

Es sencillo comprobar que se satisfacen las relaciones :math:`a^{7} = b^{3} = I` y :math:`bab^{−1} = a^{2}`.

Acciones de Grupos
----------------------

Hemos definido los conceptos de una acción de un grupo :math:`G` sobre un conjunto :math:`S` y de una representación de permutación de :math:`G` sobre :math:`S`. De hecho, estos dos conceptos son esencialmente equivalentes. Supongamos que :math:`\phi: G \to Sym (S)` es una representación de permutación de :math:`G`. Entonces :math:`\phi g` es una permutación de :math:`S` siempre que :math:`g \in G`, por lo que para cada :math:`x\in S` podemos definir :math:`gx\in S` mediante la fórmula :math:`gx = (\phi g)x`. Dado que :math:`\phi` es un homomorfismo, tenemos que :math:`\phi (gh) = (\phi g) (\phi h) `para todo :math:`g, h \in G`, y dado que el producto de las permutaciones :math:`\phi g` y :math:`\phi h` es por definición su compuesto (:math:`\phi h` seguido de :math:`\phi g`), sigue que

.. math::

    (gh)x = (\phi (gh))x = ((\phi g)( \phi  h))x = ( \phi g)(( \phi h)x) = ( \phi g)(hx) = g(hx)

para todo :math:`x \in S`. Esto muestra que se satisface la primera propiedad en la definición de una acción de grupo.

Además, dado que un homomorfismo de grupo necesariamente lleva el elemento de identidad al elemento de identidad, debemos tener que :math:`\phi 1 = id`, y por lo tanto

.. math::

    1x = (\phi 1)x = id(x) = x

para todo :math:`x \in S`. Por lo tanto, el segundo requisito también se satisface, y tenemos una acción de :math:`G` sobre :math:`S`. A la inversa, si se nos da una acción de :math:`G` sobre :math:`S`, entonces para cada :math:`g \in G` podemos definir una función :math:`\phi g: S \to S` por :math:`(\phi g) x = gx`. Entonces para todo :math:`g, h \in G` y :math:`x \in S` tenemos que

.. math::

    ((\phi g) (\phi h)) x = (\phi g) ((\phi h) x) = (\phi g) (hx) = g (hx) = (gh) x = (\phi (gh)) x,

y por lo tanto :math:`(\phi g) (\phi h) = \phi (gh)`. Además, :math:`\phi 1 = id`, ya que

.. math::

    (\phi 1)x = 1x = x = id(x)

para todo :math:`x \in S`. Se deduce que :math:`(\phi g) (\phi (g^{−1})) = id = (\phi (g^{−1})) (\phi g)`, por lo que las funciones :math:`\phi g` y :math:`\phi (g^{−1})` son inversas a entre sí, lo que significa que ambos son biyectivos. Entonces :math:`\phi` es una función de :math:`G` a :math:`Sym (S)`, y como ya hemos demostrado que conserva la multiplicación, se deduce que :math:`\phi` es una representación de permutación.

Es una práctica bastante común entre los algebristas, especialmente los teóricos de grupos, que las funciones se escriban como operadores de derecha en lugar de operadores de izquierda. En otras palabras, el valor de la función :math:`f` en el elemento :math:`x` se escribe como :math:`xf` en lugar de :math:`f(x)`. Aunque esto es puramente una cuestión de notación, tiene ramificaciones. En particular, el compuesto :math:`fg` de dos funciones :math:`f` y :math:`g` se define mediante la regla :math:`x(fg) = (xf)g` si :math:`f` y :math:`g` se escriben como operadores de la derecha, mientras que para los operadores de la izquierda la fórmula correspondiente para :math:`fg` es :math:`(fg) ( x) = f (g (x))`. Según la convención del operador correcto, :math:`fg` significa :math:`f` seguida de :math:`g`; bajo la convención del operador de la izquierda significa :math:`g` seguido de :math:`f`. Como hay contextos en los que aparecen simultáneamente los operadores de la derecha y los de la izquierda, tenemos que poder trabajar con ambas convenciones. En consecuencia, definimos una acción correcta de un grupo :math:`G` sobre un conjunto :math:`S` como una función :math:`(x, g) \mapsto xg` de :math:`S \times G` a :math:`S` tal que :math:`x1 = x` y :math:`x (gh) = (xg) h` para todos :math:`g, h \in G` y todo :math:`x \in S`. Si uno escribiera las permutaciones de uno como operadores derechos en lugar de operadores izquierdos, y de hecho para las permutaciones, la convención del operador derecho es más común que la convención del operador izquierdo, entonces una representación de permutación de :math:`G` sobre :math:`S` sería esencialmente lo mismo que una acción correcta de :math:`G` sobre :math:`S`.

Si el conjunto :math:`S` sobre el que actúa un grupo no es solo un conjunto, sino un conjunto con alguna estructura adicional, entonces es natural preguntarse si la acción conserva la estructura. Así, por ejemplo, una acción izquierda de un grupo :math:`G` en un espacio vectorial :math:`V` significa implícitamente una acción izquierda de :math:`G` en el conjunto :math:`V` tal que :math:`g (u + v) = gu + gv y g (\lambda v) = \lambda (gv)` para todo :math:`u, v \in V` y todos los escalares :math:`\lambda` y todo :math:`g \in G`.

Una acción izquierda de :math:`G` sobre :math:`V` es entonces esencialmente lo mismo que un homomorfismo de :math:`G` al grupo de todas las transformaciones lineales invertibles en :math:`V` (donde las transformaciones lineales se escriben como operadores izquierdos).

También podemos hablar de una acción de un grupo sobre otro grupo. Es común usar una convención de operadores correctos y escribir los operadores como exponentes. Siguiendo esta convención, una acción de un grupo :math:`A` sobre otro grupo :math:`G` es una función :math:`(g, \alpha) \mapsto g\alpha` de :math:`G \times A` a :math:`G` tal que se satisfacen las siguientes propiedades:

    :math:`(i)` :math:`(g^{\alpha})^{\beta} = g^{\alpha \beta}` para todo :math:`g \in G` y :math:`\alpha, \beta \in A`,
    :math:`(ii)` :math:`g^{1} = g` para todo :math:`g \in G` (donde :math:`1` es el elemento identidad de :math:`A`),
    :math:`(iii)` :math:`(gh)^{\alpha} = g^{\alpha} h^{\alpha}` para todo :math:`g, h \in G` y :math:`\alpha \in A`.

Recuerde que un subgrupo normal :math:`K` de un grupo :math:`G` es un subgrupo de :math:`G` tal que :math:`g^{-1}kg \in K` para todo :math:`g \in G` y :math:`k\in K`. Es un teorema básico importante de la teoría de grupos que si :math:`K` es normal en :math:`G` entonces hay es una acción de :math:`G` sobre :math:`K` definida por :math:`kg = g^{−1}kg` para todo :math:`g \in G` y :math:`k\in K`. Es una cuestión sencilla comprobar que se satisfacen las tres propiedades anteriores. Por ejemplo, si :math:`k_{1}, k_{2} \in K` y :math:`g \in G` entonces

.. math::

    (k_{1}k_{2})^{g} = g^{−1}k_{1}k_{2}g = (g^{−1}k_{1}g)(g^{−1}k_{2}g) = k_{1}gk_{2}g.

Si :math:`G` y :math:`H` son grupos, el producto directo externo de :math:`G` y :math:`H` es el conjunto

.. math::

    G \times H = \{ (g, h) | g \in G, h \in H \},

equipado con la multiplicación definida por :math:`(g_{1}, h_{1}) (g_{2}, h_{2}) = (g_{1}g_{2}, h_{1}h_{2})`. Se comprueba fácilmente que :math:`G \times H` es un grupo con esta operación.

Suponga que :math:`S` y :math:`T` son subgrupos de :math:`G` tales que :math:`S\cap T = \{ 1 \}`, y suponga también que :math:`st = ts` para todo :math:`s\in S` y :math:`t\in T`. Se define una función :math:`f` del producto directo externo :math:`S \times T` a :math:`G` por :math:`f (s, t) = st` para todo :math:`s\in S` y :math:`t\in T`. Claramente :math:`f` es un homomorfismo:

.. math::

    f((s_{1}, t_{1})(s_{2}, t_{2})) = f(s_{1}s_{2}, t_{1}t_{2}) = (s_{1}s_{2})(t_{1}t_{2}) = (s_{1}t_{1})(s_{2}t_{2}) = f(s_{1}, t_{1})f(s_{2}, t_{2}).

También es fácil demostrar que :math:`f` es inyectiva: si :math:`f (s, t) = 1` entonces :math:`st = 1`, y entonces :math:`s = t^{− 1} \in S \cap T = {1}`, de donde :math:`(s, t) = (1 , 1)`, que es el elemento de identidad de :math:`S \times T`. Por tanto, el núcleo de :math:`f` es trivial, por lo que :math:`f` es inyectivo, como se afirma. Si también es el caso de que :math:`G = ST`, de modo que cada elemento de :math:`G` es expresable en la forma :math:`st` con :math:`s\in S` y :math:`t\in T`, entonces se deduce que :math:`f` es un isomorfismo de :math:`S \times T` a :math:`G`.


Definición
-------------

Se dice que un grupo :math:`G` es el producto directo interno de :math:`S` y :math:`T` si :math:`S` y :math:`T` son subgrupos de :math:`G` tales que :math:`S\cap T = \{ 1 \}` y :math:`ST = G`, y :math:`st = ts` para todo :math:`s\in S` y :math:`t\in T`.

Si :math:`S` y :math:`T` son subgrupos de :math:`G` tales que :math:`S\cap T = \{ 1 \}` y :math:`G = ST`, entonces la condición adicional de que :math:`st = ts` para todos :math:`s\in S` y :math:`t\in T` es equivalente a la condición de que :math:`S` y :math:`T` son ambos subgrupos normales. Pues suponga que :math:`S` y :math:`T` son ambos normales, y sean :math:`s\in S` y :math:`t\in T`.

- La normalidad de :math:`T` implica que :math:`s^{− 1}ts \in T`, y por tanto :math:`t^{−1}s^{− 1}ts \in T`.

- Por otro lado, la normalidad de :math:`S` implica que :math:`t^{−1}s^{−1}t in S`, de donde :math:`t^{−1}s^{−1}ts \in S`. Entonces :math:`t^{−1}s^{−1}ts \in S \cap T = \{1\}`, de modo que :math:`t^{−1}s^{−1}ts = 1`, y :math:`ts = st`.

Por el contrario, si asumimos que los elementos de :math:`S` y :math:`T` conmutan entonces para :math:`s\in S` y :math:`t, t_{0}\in T` tenemos que :math:`(st)^{−1}t_{0} (st)^{−1} = t^{−1}s^{−1}t_{0}st = t^{− 1}t_{0}t \in T`. Pero como :math:`G = ST` cada elemento de :math:`G` es expresable en la forma :math:`st`, y se sigue que :math:`g^{−1}tg \in T` para todo :math:`g\in G` y :math:`t_{0} \in T`; es decir, :math:`T` es normal. Del mismo modo, :math:`S` también es normal.

Si un grupo :math:`S` tiene una acción sobre otro grupo :math:`T`, entonces podemos definir un producto semidirecto :math:`S \ltimes T` de :math:`S` y :math:`T` de la siguiente manera. Los elementos de :math:`S \ltimes T` son pares ordenados :math:`(s, t)` (donde :math:`s\in S` y :math:`t\in T`).

La multiplicación de pares ordenados está definida por la regla

.. math::

    (s_{1}, t_{1}) (s_{2}, t_{2}) = (s_{1}s_{2}, t_{1}^{s_{2}}t_{2}).

Se deja como ejercicio para que el alumno demuestre que se satisfacen los axiomas del grupo.

Un grupo :math:`G` es un producto semidirecto interno de sus subgrupos :math:`S` y :math:`T` si :math:`G = ST` y :math:`S \cap T = \{1\}`, y el subgrupo :math:`T` es normal. En estas circunstancias, :math:`S` tiene una acción sobre :math:`T` dada por :math:`t^{s} = s^{−1}ts` para todo :math:`s\in S` y :math:`t\in T`, y ahora es una rutina comprobar que :math:`(s, t) \mapsto st` proporciona un isomorfismo de :math:`S \ltimes T` a :math:`G`.
