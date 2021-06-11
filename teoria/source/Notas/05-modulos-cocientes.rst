.. role:: underline
    :class: underline

Módulos Cocientes
=========================


Si :math:`S` y :math:`T` son subconjuntos arbitrarios del grupo :math:`G`, entonces se acostumbra definir su producto :math:`ST` por la regla de que :math:`ST = \{st | s \in S,  t \in T\}`. Si :math:`H` es un subgrupo normal de :math:`G`, de modo que :math:`gH = Hg` para todo :math:`g\in G`, entonces :math:`(xH) (yH) = (xy) H` para todo :math:`x, y \in G`. Esto produce una operación de multiplicación bien definida en el establecer :math:`G / H = \{gH | g \in G\}`, y se puede comprobar que bajo esta operación :math:`G/H` es un grupo. El grupo :math:`G/H` se denomina cociente de :math:`G` por :math:`H`.

Si el grupo :math:`G` es abeliano (conmutativo), entonces cada subgrupo H es normal, por lo que el grupo del cociente siempre existe. En particular, si :math:`V` es un espacio vectorial sobre un cuerpo :math:`\mathbb{F}`, entonces :math:`V` es un grupo abeliano bajo la operación de suma vectorial, y dado que cualquier subespacio vectorial :math:`U` de :math:`V` es también un subgrupo aditivo de :math:`V`, se sigue que el grupo cociente :math:`V/U` se puede formar. Está claro que :math:`V/U` es abeliano.

Tenga en cuenta que dado que la operación en :math:`V` en este caso se escribe como :math:`+`, la clase lateral de :math:`U` que contiene el elemento :math:`v \in V` se escribe como :math:`v + U` en lugar de :math:`vU`, y la operación de grupo en :math:`V/U` también se escribe como :math:`+`. Nosotras tenemos :math:`V/U = { v + U | v \in V }`,

.. math::

    (x + U) + (y + U) = (x + y) + U \text{ para todo } x, y \in U

Ahora le damos a :math:`V/U` una estructura adicional, definiendo una operación de multiplicación escalar en él. La fórmula relevante es la siguiente:

.. math::

    \lambda (v + U) = (\lambda v) + U \text{ para todo } v \in V \text{ y } \lambda \in \mathbb{F}.

Es necesario comprobar que este está bien definido, ya que es posible tener :math:`v_{1} + U = v_{2} + U` sin tener :math:`v_{1} = v_{2}`. Pero si :math:`v_{1} + U = v_{2} + U` entonces :math:`v_{1} - v_{2} \in U`, y dado que el subespacio :math:`U` tiene que cerrarse bajo la multiplicación escalar, se sigue que :math:`\lambda v_{1} - \lambda v_{2} = \lambda (v_{1} - v_{2}) \in U`, y por lo tanto :math:`\lambda v_{1} + U = \lambda v_{2} + U`.

Esto muestra que :math:`\lambda v + U` no depende de la elección del elemento representativo :math:`v` en la clase lateral :math:`v + U`, sino solo de la clase lateral :math:`v + U` misma. En otras palabras, la fórmula anterior da una operación de multiplicación escalar bien definida en :math:`V/U`.

Recuerde que un espacio vectorial sobre :math:`\mathbb{F}` es un conjunto, cuyos elementos llamamos "vectores", equipado con operaciones de suma y multiplicación escalar, de modo que se satisfacen los siguientes ocho axiomas:

    :math:`(i)` :math:`(u + v) + w = u + (v + w)` para todo vectores :math:`u`, :math:`v` y :math:`w`;

    :math:`(ii)` :math:`u + v = v + u` para todo vectores :math:`u` y :math:`v`;

    :math:`(iii)` Existe un cero vector :math:`0`, tal que satisface :math:`0 + v = v` para todo vectores :math:`v`;

    :math:`(iv)` cada vector :math:`v` tiene un negativo, donde es un vector :math:`-v` satisface :math:`v + (−v) = 0`;

    :math:`(v)` :math:`\lambda (\mu v) = (\lambda \mu)v` para todos los escalares :math:`\lambda` y :math:`\mu` y para todo vector :math:`v`;

    :math:`(vi)` :math:`1v = v` para todo vector :math:`v`, donde :math:`1` es el elemento identidad de :math:`\mathbb{F}`;

    :math:`(vii)` :math:`\lambda (u + v) = \lambda u + \lambda v` para todo vector :math:`u` y :math:`v` y todos todo :math:`\lambda`;

    :math:`(viii)` :math:`(\lambda + \mu )v = \lambda v + \mu v` para todos los escalares :math:`\lambda` y :math:`\mu` todo vector :math:`v`.

Es trivial comprobar que las operaciones de suma y multiplicación escalar que hemos definido en :math:`V/U` satisfacen estos axiomas. (Por supuesto, los primeros cinco axiomas solo dicen que un espacio vectorial es un grupo abeliano bajo la suma, y ​​ya habíamos notado anteriormente que :math:`V/U` satisface esto). Se deja al lector verificar todos los detalles. Llamamos a :math:`V/U` un espacio de cociente (vector).

Procedemos a embellecer aún más la situación anterior asumiendo que :math:`V` y :math:`U` están equipados con acciones :math:`G`. Más precisamente, suponga que :math:`V` es un :math:`G`-módulo y :math:`U` un submódulo de :math:`V`. Entonces el espacio del cociente :math:`V/U` también es un :math:`G`-módulo, con la :math:`G`-acción cumpliendo que

.. math::

    g(v + U) = (gv) + U \text{ para todo } g \in G \text{ y } v \in V.

Al igual que con la suma y la multiplicación escalar, es fundamental comprobar que esta :math:`G`-acción esté bien definida. El argumento necesario es totalmente análogo al argumento en el caso de la multiplicación escalar: si :math:`v_{1} + U = v_{2} + U` entonces :math:`v_{1} - v_{2} \in U`, y dado que :math:`U` está cerrado bajo la :math:`G`-acción, se sigue que :math:`gv_{1} - gv_{2} = g (v_{1} - gv_{2}) \in U`, de donde :math:`gv_{1} + U = gv_{2} + U`. De nuevo se deja al lector comprobar los axiomas.


Teorema Isomorfismo
~~~~~~~~~~~~~~~~~~~

Sean :math:`V` y :math:`W`  dos:math:`G`-modulo y sean :math:`f: V \to W` un :math:`G`-homomorfismo. Entonces

.. math::

    ker f = \{ v \in V | fv = 0 \}

es un :math:`G`-submodulo de :math:`V`,

.. math::

    im f = \{ fv | v \in V \}

es un :math:`G`-submodulo de :math:`W`, y es un :math:`G`-isomorfismo :math:`V/ ker f \in im f` tal que :math:`v + U \mapsto gv` para todo :math:`v \in V`.

Un teorema similar es válido para espacios vectoriales sin ninguna :math:`G`-acción: si :math:`U` y :math:`V` son espacios vectoriales y :math:`f: V \to W` un mapa lineal, entonces el núcleo y la imagen de :math:`f` son subespacios de :math:`V` y :math:`W`, y el cociente espacio :math:`V/ker f` es isomorfo a :math:`im f`. Este resultado a veces se denomina "El teorema principal de las asignaciones lineales". Debido a que dos espacios vectoriales son isomorfos si y solo si tienen la misma dimensión, es común expresar el resultado en términos de dimensiones, y dado que se muestra fácilmente que :math:`dim (V / U) = dim V - dim U` la declaración se convierte en :math:`dim V = dim (ker f) + dim (im f)`.

Volviendo a la demostración del teorema en la forma indicada anteriormente, primero mostremos que :math:`ker f` es un :math:`G`-submódulo de :math:`V`. Como :math:`f` es lineal, tenemos que :math:`f (0_{V}) = 0_{W}`, y entonces :math:`0_{V} \in ker f`. Si :math:`v_{1}`, :math:`v_{2} \in ker f` entonces :math:`f (v_{1} + v_{2}) = fv_{1} + fv_{2} = 0 + 0 = 0`, de donde :math:`v_{1} + v_{2} \in ker f`, y se sigue que :math:`ker f` se cierra bajo adición. Si :math:`v \in ker f` y :math:`\lambda \in \mathbb{F}` entonces :math:`f (\lambda v) = \lambda (fv) = \lambda 0 = 0`, y se deduce que :math:`ker f` está cerrado bajo la multiplicación escalar. Entonces :math:`ker f` es el subespacio vectorial de :math:`V`. Además, :math:`ker f` está cerrado bajo la :math:`G`-acción, ya que si :math:`v\in ker f` y :math:`g \in G` entonces :math:`f (gv) = g (fv) = g0 = 0`, donde el último paso se deduce del hecho de que :math:`x \mapsto gx` es un mapa lineal :math:`V \to V` y, por lo tanto, debe tomar de :math:`0` a :math:`0`.

La demostración de que :math:`im f` es un submódulo de :math:`W` es igualmente sencilla. Si :math:`w_{1}`, :math:`w_{2} \in im f` entonces :math:`w_{1} = fv_{1}` y :math:`w_{2} = fv_{2}` para algún :math:`v_{i} \in V`, y dado que :math:`w_{1} + w_{2} = fv_{1} + fv_{2} = f (v_{1} + v_{2})` se deduce que :math:`im f` está cerrado bajo adición. El cierre bajo la multiplicación escalar y la :math:`G`-acción son igualmente fáciles: si :math:`w = fv \in im f` entonces para todo :math:`\lambda \in \mathbb{F}` tenemos :math:`\lambda w = f (\lambda v) \in im f`, y para todo :math:`g \in G` tenemos :math:`gw = g ( fv) = f (gv) \in im f`. Y también :math:`im f \not = \emptyset` ya que :math:`V \not = \emptyset`. Entonces :math:`im f` es un submódulo de :math:`W`.

Como :math:`ker f` es un submódulo de :math:`V`, existe el módulo cociente :math:`V/ker f`. Necesitamos mostrar que hay un mapa bien definido :math:`\psi : V / ker f \to im f` tal que :math:`\psi (v + ker f) = fv` para todo :math:`v \in V`.

Ciertamente es cierto que :math:`fv \in im f` para todo :math:`v`, por lo que solo necesitamos mostrar que si :math:`v_{1}`, :math:`v_{2}\in V` con :math:`v_{1} + ker f = v_{2} + ker f` entonces :math:`fv_{1} = fv_{2}`. Pero esto está claro: si :math:`v_{1} + ker f = v_{2} + ker f` entonces :math:`v_{1} −v_{2} \in ker f`; entonces :math:`f (v_{1} - v_{2}) = 0`, y por lo tanto :math:`fv_{1} = fv_{2}`.

Habiendo establecido que :math:`\psi` está bien definido, queda por demostrar que es biyectiva y respeta la suma, la multiplicación escalar y la acción de :math:`G`. Este último punto se deriva inmediatamente del hecho de que :math:`f` respeta la suma, la multiplicación escalar y la acción de :math:`G`. Explícitamente, si :math:`u`, :math:`v \in V` y :math:`\lambda \in \mathbb{F}` entonces

.. math::

    \begin{align}
        \psi ((u + ker f) + (v + ker f)) &= \psi ((u + v) + ker f)                \\
                                            &= f(u + v)                                 \\
                                            &= fu + fv                                  \\
                                            &= \psi (u + ker f) + \psi (v + ker f)
    \end{align}

y

.. math::

    \begin{align}
        \psi (\lambda (v + ker f)) &= \psi (\lambda v + ker f) \\
                                      &= f(\lambda v)                \\
                                      &= \lambda (fv)                \\
                                      &= \lambda \psi (v + ker f),
    \end{align}

y similarmente :math:`g \in G`,

.. math::

    \begin{align}
        \psi (g(v + ker f)) &= \psi (gv + ker f)    \\
                               &= f(gv)                   \\
                               &= g(fv)                   \\
                               &= g\psi (v + ker f).
    \end{align}

La sobreyectividad de :math:`\psi` es obvia: por definición, cada elemento de :math:`im f` tiene la forma :math:`fv = \psi (v + ker f)` para algunos :math:`v \in V`. Y la inyectividad no es mucho más difícil: si :math:`\psi (v_{1} + ker f) = \psi (v_{2} + ker f)` entonces :math:`fv_{1} = fv_{2}`, de donde :math:`f (v_{1} - v_{2}) = 0`, lo que da como resultado que :math:`v_{1} - v_{2} \in ker f`, y por lo tanto :math:`v_{1} + ker f = v_{2} + ker f`.

