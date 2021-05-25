Representaciones, Acciones lineales y módulos
=================================================

Sea :math:`V` es un espacio vectorial sobre el campo :math:`\mathbb{F}` y :math:`G` es un grupo.

Definición
--------------

Una acción de :math:`G` sobre :math:`V` es una función :math:`(g, v) \mapsto gv` de :math:`G\times V` a :math:`V` tal que

    :math:`(i)` :math:`(gh)v = g(hv)` para todo :math:`g, h \in G` y :math:`v \in V`,

    :math:`(ii)` :math:`1v = v` para todo :math:`v \in V`, donde :math:`1` es el elemento identidad de :math:`G`,

    :math:`(iii)` :math:`g(u + v) = gu + gv` para todo :math:`g \in G` y :math:`u, v \in V`,

    :math:`(iv)` :math:`g(\lambda v) = \lambda (gv)` para todo :math:`g \in G`, :math:`v \in V` y todo :math:`\lambda \in \mathbb{F}`.


.. note::

    Tenga en cuenta que, según nuestras definiciones, una acción de :math:`G` sobre el espacio vectorial :math:`V` no es lo mismo que una acción de :math:`G` sobre el conjunto :math:`V`: los elementos :math:`(iii)` y :math:`(iv)` no son necesarios para este último. Esta terminología puede dar lugar a confusión, y quizás sería mejor referirse siempre a una acción de :math:`G` sobre :math:`V` que satisface :math:`(iii)` y :math:`(iv)` como una acción lineal. Sin embargo, en este curso las únicas acciones grupales que encontraremos en conjuntos que son los espacios vectoriales serán acciones lineales.) Ya hemos señalado que una acción de un grupo :math:`G` sobre un conjunto :math:`S` es esencialmente lo mismo que una representación de permutación de :math:`G` sobre :math:`S`.
    
    De la misma manera, una acción lineal de un grupo :math:`G` en un espacio vectorial :math:`V` es esencialmente lo mismo que una representación de :math:`G` mediante transformaciones lineales en :math:`V`.

Proposición
-----------------

Dada una acción de un grupo :math:`G` sobre un espacio vectorial :math:`V`, para cada :math:`g\in G` definimos una función :math:`\rho g: V \to V` dada por :math:`(\rho g) v = gv` para todo :math:`v\in V`. Entonces :math:`\rho g` es una transformación lineal invertible, y la función :math:`\rho` definido por :math:`g \mapsto \rho g` es un homomorfismo de :math:`G` al grupo de todas las transformaciones lineales invertibles en :math:`V`. A la inversa, dado un homomorfismo :math:`\rho` de :math:`G` al grupo de transformaciones lineales invertibles en :math:`V`, la fórmula :math:`gv = (\rho g) v` define una acción de :math:`G` sobre :math:`V`.

**Demostración:**

Supongamos primero que se da la acción. Como tenemos una acción de :math:`G` sobre el conjunto :math:`V`, sabemos por el argumento anterior que :math:`g \mapsto \rho g` es un homomorfismo de :math:`G` al grupo de todas las funciones invertibles :math:`V \to V`, por lo que todo lo que tenemos que mostrar es que cada función ρg también es lineal. Pero esto es precisamente lo que dicen los puntos :math:`(iii)` y :math:`(iv)` anteriores:

.. math::

    \begin{align}
        (\rho g)(v + w) &= g(v + w) = gv + gw = (\rho g)v + (\rho g)w            \\
        (\rho g)(\lambda v) &= g(\lambda v) = \lambda (gv) = \lambda ((\rho g)v)
    \end{align}

para todo :math:`v, w \in V` y :math:`\lambda \in \mathbb{F}`.

A la inversa, suponga que se da el homomorfismo :math:`\rho`. Si ignoramos el hecho de que las funciones :math:`\rho g` son lineales y, en cambio, nos centramos en el hecho de que son funciones biyectivas :math:`V \to V`, entonces :math:`g \mapsto \rho g` puede considerarse como una representación de permutación de :math:`G` en el conjunto :math:`V`, y de ahí se sigue que :math:`gv = (\rho g) v` define una acción de :math:`G` sobre el conjunto :math:`V`. Así que tenemos que demostrar que la acción es lineal; es decir, que se cumplen :math:`(iii)` y :math:`(iv)`. Por supuesto, esto es exactamente lo que nos dice la linealidad de :math:`\rho g`:

.. math::

    \begin{align}
        g(v + w) &= (\rho g)(v + w) = (\rho g)v + (\rho g)w = gv + gw \\
        g(\lambda v) &= (\rho g)(\lambda v) = \lambda ((\rho g)v) = \lambda (gv)
    \end{align}

para todo :math:`v, w \in V` y :math:`\lambda \in \mathbb{F}`.

Entonces, una representación de un grupo en un vector es lo mismo que una acción de un grupo en un espacio vectorial. Bien, entonces, ¿por qué no introducir un tercer término para describir esta misma situación?

Definición
-----------------

Un espacio vectorial :math:`V` en el que un grupo :math:`G` tiene una acción se llama :math:`G`-módulo.

.. note::

    Naturalmente, deberíamos investigar funciones desde :math:`G`-módulos a :math:`G`-módulos que preservan la estructura del :math:`G`-módulo, así como también investigar las circunstancias en las que un subconjunto de un :math:`G`-módulo es también un :math:`G`-módulo. Por lo tanto, hacemos las siguientes definiciones:

Definición
-----------------

    :math:`(i)` Un submódulo de un :math:`G`-módulo :math:`V` es un subespacio vectorial :math:`U` de :math:`V` tal que :math:`gu \in U` para todo :math:`g \in G` y :math:`u \in U`.
    
    :math:`(ii)` Si :math:`U` y :math:`V` son :math:`G`-módulo, entonces un :math:`G`-homomorfismo de :math:`U` a :math:`V` es una transformación lineal :math:`f: U \to V` tal que :math:`f (gu) = g (fu)` para todo :math:`g \in G` y :math:`u \in U.`

Tendremos mucho más que decir sobre los :math:`G`-módulo. En particular, existe una versión en :math:`G`-módulo del *Primer Teorema del Isomorfismo*, que será de gran importancia para la teoría que desarrollaremos.

También es importante el concepto de suma directa de dos :math:`G`-módulo, análogo a las sumas directas en la teoría de grupos y la teoría del espacio vectorial. Sin embargo, antes de continuar con estos asuntos, hay otro aspecto básico de las representaciones que debe tenerse en cuenta.



