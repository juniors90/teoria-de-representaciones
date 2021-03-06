Ejemplos de acción de un grupo sobre un conjunto
=================================================

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