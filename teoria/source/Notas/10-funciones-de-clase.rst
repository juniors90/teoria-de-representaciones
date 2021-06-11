.. role:: underline
    :class: underline

Funciones de clase
===================

En la lección 10 describimos la representación regular de :math:`G` como la representación lineal derivada de la representación de permutación de :math:`G` sobre :math:`G` correspondiente a la acción de multiplicación por la izquierda de :math:`G` sobre sí mismo. Es decir, a cada elemento :math:`g \in G` asociamos la permutación :math:`\sigma_{g}: G \to G` definida por :math:`\sigma_{g}x = gx` (para todo :math:`x \in G`), y correspondiente a esta permutación tenemos una matriz de permutación :math:`Rg`. Entonces :math:`g \mapsto Rg` es una representación matricial. Se puede obtener una versión no matricial de la representación regular identificando los elementos de :math:`G` con los elementos base de un espacio vectorial :math:`V`; en otras palabras, sea :math:`V` un espacio vectorial :math:`|G|`-dimensional, luego elija cualquier base de :math:`V` y una correspondencia uno a uno entre estos vectores base y los elementos de :math:`G`, y asociar con cada elemento :math:`g \in G` la transformación lineal :math:`\rho_{g}: V \to V` que permuta la base de acuerdo con la permutación :math:`\sigma_{g}` definida anteriormente. Entonces :math:`\rho: g \mapsto \rho_{g}` es una representación de :math:`G` por transformaciones lineales del espacio :math:`V`.

Además, también notamos en la lección 10 que el conjunto :math:`V_{G}` de todas las funciones con valores complejos en :math:`G` es un espacio vectorial :math:`|G|`-dimensional sobre :math:`\mathbb{C}`. De modo que podemos tomar el espacio vectorial :math:`V` al que se hace referencia en el último párrafo como :math:`V_{G}`. Si para todo :math:`x \in G` definimos la función :math:`f_{x} \in V_{G}` por la fórmula

.. math::

    \begin{equation}
        f_{x}h =
        \begin{cases}
            1 & \text{ si } h=x^{-1}\\
            0 & \text{ si } h\not=x^{-1}
        \end{cases}
    \end{equation}

entonces se ve fácilmente que las :math:`f_{x}` forman una base de :math:`V_{G}` en correspondencia uno a uno con el elementos de :math:`G`. Las observaciones en el último párrafo afirman que hay una acción de :math:`G` sobre :math:`V_{G}` tal que :math:`gf_{x} = f_{gx}` para todo :math:`x \in G` y :math:`g \in G`. Una forma alternativa de describir esta acción es la siguiente: para todo :math:`g \in G` y :math:`f \in V_{G}` la función :math:`gf \in V_{G}` viene dada por

.. math::

    (gf)h = f(hg) \text{ para todo } h \in G.

El estudiante debe comprobar que esta fórmula efectivamente produce :math:`gf_{x} = f_{gx}`, y que los axiomas para una acción lineal de grupo en un espacio vectorial (ver Lección 3) se satisfacen de hecho.

Hemos definido un :math:`G`-módulo como un espacio vectorial con una acción :math:`G`; es decir, debe haber una función :math:`(g, v) \mapsto gv` de :math:`G\times V` a :math:`V` que satisfaga :math:`(i)`, :math:`(ii)` y :math:`(iii)` de la lección 3. Estrictamente hablando, este debe ser un :math:`G`-módulo izquierdo llamado, ya que la acción :math:`G` está a la izquierda. De manera similar, un :math:`G`-módulo derecho es un espacio vectorial :math:`V` equipado con una función :math:`(v, g) \mapsto vg` de :math:`V\times G` a :math:`G` que satisface

    :math:`(i)` :math:`v1 = v` para todo :math:`v \in V`, donde :math:`1` es el elemento identidad de :math:`G`,

    :math:`(ii)` :math:`(vg)h = v(gh)` para todo :math:`v \in V` y :math:`g`, :math:`h \in G`,

    :math:`(iii)` :math:`(u + v)g = ug + vg` para todo :math:`u`, :math:`v \in V` y :math:`g \in G`,

    :math:`(iv)` :math:`(\lambda v)g = \lambda (vg)` para todo :math:`v \in V` y :math:`g \in G` y todo escalar :math:`\lambda`.

Hemos visto que :math:`V_{G}` se convierte en un :math:`G`-módulo izquierdo a través de la acción (izquierda) dada por :math:`(gf) h = f (hg)` para todo :math:`g, h \in G` y todas las funciones :math:`f\in V_{G}`. De hecho, también podemos convertir :math:`V_{G}` en un :math:`G`-módulo derecho definiendo :math:`fg: G \to \mathbb{C}` (siempre que :math:`f\in V_{G}` y :math:`g\in G`) por

.. math::

    (fg)h = f(gh) \text{ para todo } h \in G.

Es un asunto sencillo, que dejamos al lector, para comprobar que se cumplen :math:`(i)` a :math:`(iv)` anteriores.


Una pregunta que surge ahora es la siguiente: ¿qué funciones :math:`f: G \to \mathbb{C}` tienen la propiedad de que :math:`gf = fg` para todo :math:`g\in G`? Es decir, ¿en qué elementos :math:`f\in V_{G}` concuerdan las acciones izquierda y derecha de :math:`G`?

Definición
---------------

Una función :math:`f: G \to \mathbb{C}` se denomina función de clase si es constante en las clases de conjugación. Por tanto, :math:`f` es una función de clase si y solo si :math:`fx = fy` siempre que :math:`x` e :math:`y` se conjugan en :math:`G`.

Proposición
---------------

Una función :math:`f\in V_{G}` satisface :math:`gf = fg` para todo :math:`g\in G` si y solo si es una función de clase.

**Demostración**

Supongamos que :math:`gf = fg` para todo :math:`g\in G` y sean :math:`x` e :math:`y` elementos conjugados de :math:`G`. Entonces existe :math:`g\in G` tal que :math:`g^{−1} xg = y`, y por lo tanto

.. math::

    fy = f(g^{−1} xg) = (gf)(g^{−1} x) = (fg)(g^{−1} x) = f(g(g^{−1} x)) = fx,

donde hemos utilizado las definiciones de :math:`gf` y :math:`fg` y el supuesto de que :math:`gf = fg`. Por tanto, es una función de clase.

A la inversa, suponga que :math:`f` es una función de clase y sea :math:`g\in G` arbitrario. Teniendo en cuenta que para todos los :math:`h\in G` tenemos

.. math::

    g^{−1}(gh)g = hg,

de modo que :math:`gh` y :math:`hg` se conjugan, se sigue que :math:`f (gh) = f (hg)` (ya que :math:`f` es una función de clase). Por lo tanto

.. math::

    (gf)h = f(hg) = f(gh) = (fg)h \text{ para todo } h \in G,

mostrando que :math:`gf = fg` para todo :math:`g\in G`, según se requiera.

Por ejemplo, el grupo :math:`S_{3}` tiene tres clases de conjugación. El elemento de identidad constituye una clase de conjugación por sí mismo, este es el caso en cualquier grupo, ya que :math:`\sigma^{−1} (id) \sigma = id` para todo :math:`\sigma`. Como :math:`(2, 3)^{−1} (1, 2) (2, 3) = (1, 3)` y :math:`(1,3)^{−1} (1, 2) (1, 3) = (2, 3)` vemos que :math:`(1, 2)`, :math:`(1, 3)` y :math:`(2, 3)` son todos conjugados, y de manera similar :math:`(1, 2, 3) = (1, 2)^{−1} (1, 3, 2) (1, 2)` muestra que :math:`(1, 2, 3)` y :math:`(1, 3, 2)` son todos conjugado.

Se necesita un poco más de trabajo para demostrar que :math:`(1, 2)` y :math:`(1, 2, 3)` no se conjugan, pero dado que este es un tema secundario en la actualidad, lo omitimos. El punto es que una función de clase :math:`f` en :math:`S_{3}` está determinada por una terna :math:`x`, :math:`y`, :math:`z` de números complejos, donde

.. math::

    \begin{align}
        f1 &= x                          \\
        f(1, 2) &= f(1, 3) = f(2, 3) = y \\
        f(1, 2, 3) &= f(1, 3, 2) = z.
    \end{align}

Por tanto, vemos que las funciones de clase en :math:`S_{3}` forman un espacio vectorial tridimensional. En general,

Proposición
---------------

El conjunto de todas las funciones de clase :math:`G \to \mathbb{C}` forma un subespacio vectorial de :math:`V_{G}` de dimensión igual al número de clases de conjugación de :math:`G`.

**Demostración**

La función cero es claramente constante en las clases de conjugación, por lo que el conjunto de todas las funciones de clase no está vacío. Si :math:`e` y :math:`f` son funciones de clase y si :math:`x` e :math:`y` son elementos conjugados arbitrarios de :math:`G`, entonces :math:`fx = fy` y :math:`ex = ey` (dado que :math:`e`, :math:`f` son funciones de clase, y así

.. math::

    (e + f)x = ex + fx = ey + fy = (e + f)y

por la definición de la suma de dos funciones. Por tanto, :math:`e + f` es una función de clase, por lo que hemos demostrado que el conjunto de funciones de clase se cierra con la suma. De manera similar, si :math:`f` es una función de clase y :math:`\lambda` cualquier escalar, entonces para todos los elementos conjugados :math:`x`, :math:`y\in G`,

.. math::

    (\lambda f)x = \lambda (fx) = \lambda (fy) = (\lambda f)y,


lo que muestra que :math:`\lambda_{f}` es una función de clase. (El estudiante debe tener cuidado de examinar cada paso de este cálculo y asegurarse de que sabe exactamente lo que se afirma y por qué es cierto.

Es muy fácil mirar ecuaciones como las anteriores y creerlas porque parecen vagamente razonables, pero eso no es lo suficientemente bueno en matemáticas puras). Por lo tanto, el conjunto de todas las funciones de clase también se cierra bajo la multiplicación escalar. Por tanto, es un subespacio de :math:`V_{G}`.

Sean :math:`\mathcal{C}_{1}`, :math:`\mathcal{C}_{2}`, :math:`\dots`, :math:`\mathcal{C}_{t}` todas las clases de conjugación de :math:`G`, y para cada :math:`i` de :math:`1` a :math:`t` sea :math:`F_{i}` la función :math:`G \to \mathbb{C}` dada por :math:`F_{i} = \sum_{y∈Ci} f_{y^{− 1}}`, donde las funciones :math:`f_{x} \in V_{G}` son los definidos al comienzo de esta lección. Luego

.. math::

    F_{i}g = \sum_{ y\in\mathcal{ C_{i} } } f_{y^{−1}} (g) = \begin{cases} 1 & \text{ si } g\in \mathcal{C}_{i}\\ 0 & \text{ si } g\not \in \mathcal{C}_{i}\end{cases}, 

ya que :math:`f_{y^{−1}} (g)` es :math:`1` si :math:`g = y` y es cero en caso contrario. Ahora, cada función de clase en :math:`G` se puede expresar como una combinación lineal de Fi; específicamente, si :math:`f: G \to \mathbb{C}` toma el valor :math:`\delta_{i}` en elementos de la clase :math:`\mathcal{C}_{i}` (para :math:`1` de :math:`1` a :math:`t`) entonces :math:`f = \sum_{i} \delta_{i}F_{i}`. Por tanto, :math:`F_{i}` abarca el espacio de las funciones de clase. Además, se puede ver que para todas las elecciones de los coeficientes :math:`\delta_{i}` la función :math:`\sum_{i}\delta_{i}F_{i}` toma el valor :math:`\delta_{i}` en elementos de clase :math:`\mathcal{C}_{i}`. Por lo tanto, si :math:`\sum_{i}\delta_{i}F_{i} = 0`, entonces todos los coeficientes :math:`\delta_{i}` deben ser :math:`0`, lo que significa que :math:`F_{i}` son linealmente independientes. Entonces :math:`F_{1}`, :math:`F_{2}`, :math:`\dots`, :math:`F_{t}` forman una base para el espacio de funciones de clase, que por lo tanto tiene dimensión :math:`t`, según se requiera.

