.. role:: underline
    :class: underline

Caracterización de Características de Representaciones Complejas Irreducibles de un Grupo Finito
=================================================================================================

Repasemos la situación que hemos estado discutiendo en las últimas conferencias. Dado un grupo finito :math:`G`, comenzamos eligiendo representaciones complejas irreducibles :math:`R^{(1)}`, :math:`R^{(2)}`, :math:`\dots` , :math:`R^{(s)}` tal que :math:`R^{(i)}` y :math:`R^{(j)}` no son equivalentes si :math:`i \not = j`. Demostramos que :math:`\sum_{k} d_{k}^{2} \leq | G |`, donde :math:`d_{k}` es el grado de :math:`R^{(k)}`. Esto limita el número de representaciones complejas irreducibles desiguales por pares que :math:`G` puede tener. Si ahora suponemos que hemos elegido la secuencia de representaciones anterior para incluir tantas representaciones como sea posible, entonces seguirá siendo una secuencia finita, y cada representación compleja irreductible de G tendrá que ser equivalente exactamente a una de las :math:`R^{(i)}`. Expresamos esto diciendo que :math:`R^{(1)}`, :math:`R^{(2)}`, :math:`\dots` , :math:`R^{(s)}` constituyen un conjunto completo de representaciones complejas irreductibles de :math:`G`.

Dado un conjunto completo de representaciones irreductibles de :math:`G` como arriba, sea :math:`\chi^{(k)}` el carácter de :math:`R^{(k)}`. Es decir, si las funciones de coordenadas de :math:`R^{(k)}` se denotan por :math:`R_{ij}^{(k)}`, entonces :math:`\chi^{(k)} = \sum_{j=1}^{d_{k}} R_{jj}^{(k)}`. Vimos en una pregunta de asignación que las representaciones equivalentes tienen el mismo carácter, la razón es que si :math:`R`, :math:`S: G \to GL (d,\mathbb{C})` son equivalentes, entonces existe un :math:`T \in GL (d, \mathbb{C})` tal que :math:`Sg = T^{−1} (Rg) T` para todo :math:`g \in G`, y esto da 

.. math::

    traza(Sg) = traza(T^{−1}(Rg)T) = traza(Rg) \text{ para todo } g \in G.

Entonces, el carácter de cualquier representación compleja irreducible de G debe ser igual a uno de los caracteres :math:`\chi^{(1)}`, :math:`\chi^{(2)}`, :math:`\dots`, :math:`\chi^{(s)}`.

También hemos probado la ortogonalidad de las funciones de coordenadas:

.. math::

    \frac{1}{|G|} \sum_{g\in G} (R_{pm}^{(k)} g)(R_{nq}^{(l)}(g^{−1})) = (1/d_{k})\delta_{kl}\delta_{nm}\delta_{pq}

para todos los valores significativos de :math:`k`, :math:`l`, :math:`p`, :math:`m`, :math:`n` y :math:`q`. Poniendo :math:`p = m` y :math:`q = n` y sumando :math:`m` de :math:`1` a :math:`d_{k}` y :math:`n` de :math:`1` a :math:`d_{l}` da

.. math::

    \frac{1}{|G|} \sum_{g\in G} \left( \sum_{m =1}^{d_{k}} R_{mm}^{(k)} g\right)\left( \sum_{n =1}^{d_{l}} R_{nn}^{(l)} (g^{−1})\right) = (1/d_{k})\delta_{kl} \sum_{m =1}{d_{k}} \sum_{n =1}^{d_{l}} \delta_{nm}\delta_{mn}.

La cantidad en el lado derecho es cero a menos que :math:`l = k`, en cuyo caso :math:`\sum_{m = 1}^{d_{k}} \sum_{n = 1}^{d_{l}} \delta_{nm}\delta_{mn}` se evalúa como :math:`d_{k}` (ya que los términos :math:`d_{k}` con :math:`n = m` contribuyen cada uno con :math:`1` y los otros términos son :math:`0`). Por lo tanto

.. math::

    \frac{1}{|G|} \sum_{g\in G} \chi^{(k)}(g)\chi^{(l)}(g^{−1}) = \delta_{kl}.

Supongamos ahora que :math:`\chi` y :math:`\phi` son caracteres de representaciones complejas irreducibles :math:`R` y :math:`S`. Como se explicó anteriormente, sabemos que :math:`R` es equivalente a :math:`R^{(k)}` y :math:`S` a :math:`R^{(l)}` para algunos :math:`k` y :math:`l`. Esto da :math:`\chi = \chi^{(k)}` y :math:`\phi = \chi^{(l)}`. Dado que :math:`R^{(k)}` y :math:`R^{(l)}` son equivalentes si y solo si :math:`k=l`, se deduce que :math:`R` y :math:`S` son equivalentes si y solo si :math:`k = l`. Si no son equivalentes entonces

.. math::

    \frac{1}{|G|} \sum_{g\in G} \chi(g)\phi(g^{−1}) = \frac{1}{|G|} \sum_{g\in G} \chi^{(k)}(g)\chi^{(l)}(g^{−1}) = 0,

y si son equivalentes entonces

.. math::

    \frac{1}{|G|} \sum_{g\in G} \chi(g)\phi(g^{−1}) = \frac{1}{|G|} \sum_{g\in G} \chi^{(k)}(g)\chi^{(k)}(g^{−1}) = 1.

Por tanto, hemos probado el siguiente teorema.

Teorema
---------

Si :math:`\chi` y :math:`\phi` son caracteres de representaciones complejas irreducibles del grupo finito :math:`G`, entonces :math:`R` y :math:`S` son equivalentes si y solo si :math:`\chi=\phi` Además,

.. math::

    \sum_{g\in G} \chi(g) \phi(g^{−1}) = \begin{cases} 1 & \text{ si } \chi=\phi\\ 0 & \text{si } \chi\not =\phi \end{cases}.

Hemos visto que toda representación compleja de un grupo finito :math:`G` equivale a una representación unitaria; por tanto, cada carácter de :math:`G` es el carácter de una representación unitaria. Pero si :math:`R` es unitario entonces

.. math::

    R_{ij}(g^{−1}) = R_{ji}g (\text{ para todo }g \in G)

donde :math:`R_{ij}` son las funciones de coordenadas de :math:`R`. Ahora, si :math:`\chi` es el carácter, se sigue que 

.. math::

    \chi(g^{−1}) = \sum_{i} R_{ii}(g^{−1}) = \sum_{i}R_{ii}g = \chi(g),

y entonces deducimos que :math:`\chi (g^{−1}) = \chi (g)` para cada carácter complejo del grupo finito :math:`G`. (Otra forma de ver esto es observar que :math:`\chi (g) = traza (Rg)` es la suma de la valores propios de la matriz :math:`Rg`, mientras que :math:`\chi (g^{−1})` es la suma de los valores propios de :math:`R (g^{−1}) = (Rg)^{−1}`, que son los inversos de los valores propios de :math:`Rg`. Pero :math:`g^{n} = 1` para algunos :math:`n`, de modo que :math:`(Rg)^{n} = I`, de lo cual se sigue que los valores propios de :math:`Rg` son raíces :math:`n`-ésimas de :math:`1`. Y la inversa de una raíz :math:`n`-ésima de :math:`1` coincide con su conjugado complejo.)

Abandonemos la notación :math:`\ast` introducida en la lección 12 en favor de algo más estándar: para las funciones :math:`f_{1}`, :math:`f_{2}: G \to \mathbb{C}` define

.. math::

    (f_{1}, f_{2}) = \frac{1}{|G|} \sum_{g\in G} \overline{(f_{1}g)}(f_{2}g).

Este es un producto interno en el espacio :math:`V_{G}` de todas estas funciones. Si :math:`\chi` y :math:`\phi` son caracteres de representaciones irreductibles, entonces :math:`(\chi, \phi)` es :math:`0` si :math:`\chi\not = \phi` y es :math:`1` si :math:`\chi = \phi`. Ésta es la famosa ortogonalidad de los caracteres irreductibles. Podemos elegir las representaciones :math:`R^{(1)}`, :math:`R^{(2)}`, :math:`\dots` , :math:`R^{(s)}` para que todos sean unitarios, y luego la ortogonalidad de las funciones de coordenadas se convierte en

.. math::

    (R_{pm}^{(k)} , R_{qn}^{(l)}) = (1/d_{k})\delta_{kl}\delta_{pq}\delta_{mn}.

En la lección 10 mostramos que estas funciones de coordenadas forman una base para :math:`V_{G}`, de donde :math:`\sum_{k = 1}^{s}d_{k}^{2} = | G |`. En la lección 12 mostramos que los caracteres :math:`\chi^{(1)}`, :math:`\chi^{(2)}`, :math:`\dots` , :math:`\chi^{(s)}` abarcan el espacio de funciones de clase en :math:`G`, y dado que la ortogonalidad de caracteres irreductibles da

.. math::

    (\chi^{(i)} , \chi^{(j)}) = \delta_{ij}.

se sigue que :math:`\chi^{(1)}`, :math:`\chi^{(2)}`, :math:`\dots` , :math:`\chi^{(s)}` forman una base ortonormal para el espacio de funciones de clase. Por tanto, :math:`s`, el número total de caracteres complejos irreducibles de :math:`G`, es igual al número de clases de conjugación de :math:`G`.