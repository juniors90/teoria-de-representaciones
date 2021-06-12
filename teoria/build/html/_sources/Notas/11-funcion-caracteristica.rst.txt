.. role:: underline
    :class: underline

Función Característica
============================

Las funciones :math:`f_{x}` para :math:`x \in G` forman una base de :math:`V_{G}`. Pero también vimos en la lección 10 que si :math:`R^{(1)}`, :math:`R^{(2)}`, :math:`\dots`, :math:`R^{(s)}` son un conjunto completo de representaciones matriciales irreductibles desiguales por pares de :math:`S`, entonces la colección :math:`S` de todas las funciones de coordenadas de todas las :math:`R^{(k)}` también forma una base de :math:`V_{G}` (de donde deducimos que la suma de los cuadrados de los grados de :math:`R^{(k)}` es igual a :math:`| G |`). Demostraremos que los caracteres (ver definición a continuación) :math:`\chi^{(1)}`, :math:`\chi^{(1)}`, :math:`\dots`, :math:`\chi^{(s)}` de las representaciones :math:`R^{(1)}`, :math:`R^{(2)}`, :math:`\dots`, :math:`R^{(s)}` forman una base del espacio de funciones de clase en :math:`G`.

Definición
-------------------

El *carácter de una representación matricial* :math:`R` de :math:`G` es la función :math:`\chi: G \to \mathbb{C}` definida por :math:`\chi (g) = traza (R_g)`. Por lo tanto, si el grado de :math:`R` es :math:`d` y :math:`R_{ij}` (donde :math:`1 \leq i`, :math:`j \leq d`) son las funciones de coordenadas de :math:`R`, entonces :math:`\chi = \sum_{i = 1}^{d} R_{ii}`.

Hemos visto en una pregunta de asignación que el carácter de una representación es siempre una función de clase. El punto es que matrices similares tienen la misma traza, por lo que siempre que :math:`g`, :math:`x \in G` la matriz

.. math::

    R_{g^{−1}xg} = (R_g)^{−1}(R_{x})(R_g)

tiene la misma traza que :math:`R_x`, y esto muestra que el carácter :math:`\chi` toma el mismo valor en :math:`g^{−1}xg` que en :math:`x`. La independencia lineal de la colección :math:`S` de todas las funciones de coordenadas de :math:`R^{(k)}` implica la independencia lineal de los caracteres :math:`\chi^{(k)}`, porque si :math:`\sum_{k} \lambda_{k}\chi^{(k)} = 0` entonces

.. math::

    0 = \sum_{k} \lambda_{k}\left(\sum_{i = 1}^{d_{k}}R_{ii}^{(k)}\right) = \sum_{i, k}\lambda_{k}R_{ii}^{(k)},

y esto implica que todos los coeficientes :math:`\lambda_{k}` son cero. Entonces, para probar que los caracteres de las representaciones irreductibles forman una base para el espacio de todas las funciones de clase, queda probar que abarcan.

Proposición
-------------------

Si :math:`\chi^{(1)}`, :math:`\chi^{(1)}`, :math:`\dots`, :math:`\chi^{(s)}` son los caracteres de un conjunto completo de representaciones irreductibles de :math:`G`, entonces cada función de clase en :math:`G` puede expresarse como una combinación lineal :math:`\sum_{k} \lambda_{k}\chi^{(k)}`.

**Demostración**

Sea :math:`f` una función de clase en :math:`G`, y para cada una de las representaciones irreductibles :math:`R^{(h)}` (notación como arriba) considere la matriz

.. math::

    M_{h} = \sum_{g\in G} \overline{(fg)}(R^{(h)}g),\hspace{3cm}(1)


(donde la línea superior indica conjugación compleja). Demostramos que :math:`M_{h}` conmuta con :math:`R^{(h)} x` para todo :math:`x \in G`. De hecho, dado que :math:`f` es una función de clase, tenemos que :math:`\overline{f (x^{−1}gx)} = \overline{fg}` para todo :math:`g \in G`, y así

.. math::

    \begin{align}
        (R^{(h)}x)^{−1}M_{h}(R^{(h)}x) &= (R(h)x)−1\left(\sum_{g\in G} \overline{f(x^{−1}gx)}(R^{(h)}g)\right) (R^{(h)}x) \\
                                       &= \sum_{g\in G} \overline{f(x^{−1}gx)}((R^{(h)}x)^{−1}(R^{(h)}g)(R^{(h)}x))       \\
                                       &= \sum_{g\in G} \overline{f(x^{−1}gx)})R^{(h)}(x^{−1}gx)                          \\
                                       &= \sum_{g\in G} \overline{(fg)}(R^{(h)}g)
    \end{align}

ya que, con :math:`x` fijo, :math:`x^{−1}gx` atraviesa todos los elementos de :math:`G` como lo hace :math:`g`. Entonces :math:`(R^{(h)} x)^{−1}M_{h} (R^{(h)} x) = M_{h}`.

Ahora, como :math:`R^{(h)}` es irreducible, el lema de Schur nos dice que :math:`M_{h} = \lambda_{h}I` para algún :math:`\lambda_{h}` escalar. :math:`(1)` nos dice que

.. math::

    \sum_{g\in G} \overline{(fg)}(R_{ij}^{(h)}g) = \delta_{h}\delta_{ij}.\hspace{3cm}(2)

para todo :math:`f_{1}`, :math:`f_{2} \in V_{G}` se define :math:`f_{1} \ast f_{2} \in \mathbb{C}` por

.. math::

    f_{1} \ast f_{2} = \frac{1}{|G|} \sum_{g\in G} (f_{1}g)\overline{(f_{2}g)}.

Vimos en la lección 9 (ver la Ecuación :math:`(3)` de esa lección) que :math:`R_{pm}^{(k)} \ast R_{qn}^{(l)}` es cero a menos que :math:`k = l`, :math:`p = q` y :math:`m = n`, en cuyo caso es :math:`1 / d_{k}`. Dado que las funciones :math:`R_{pm}^{(k)}` abarcan :math:`V_{G}`, podemos escribir :math:`f = \sum_{k, p, m} \mu_{k p m} R_{pm}^{(k)}` para algunos coeficientes :math:`\mu_{k p m}`, y esto da

.. math::

    \begin{align}
        R_{ij}^{(h)} \ast f &= \sum_{k,p,m} \overline{\mu_{k, p, m}} (R_{ij}^{(h)} \ast R_{pm}^{(k)} )\\
                        &= \sum_{k,p,m} \overline{\mu_{k, p, m}}(1/d_{k})\delta_{hk}\delta_{ip}\delta_{jm}\\
                        &= (1/d_{h})\overline{\mu_{h, i, j}}.
    \end{align}

Pero la Ecuación :math:`(2)` dice que :math:`R_{ij}^{(h)} \ast f = \lambda_{h}\delta_{ij} / | G |`. Así hemos demostrado que

.. math::

    \mu_{h i j} = \frac{d_{h}\overline{\lambda_{h}}\delta_{ij}}{|G|} ,

y se sigue que

.. math::

    \begin{align}
        f &= \sum_{h,i,j} \mu_{h i j}R_{ij}^{(h)}\\
          &= \frac{1}{|G|} \sum_{h,i,j} d_{h}\overline{\lambda_{h}}\delta_{ij}R_{ij}^{(h)}\\
          &= \frac{1}{|G|} \sum_{h} d_{h}\overline{\lambda_{h}}\left(\sum_{i} R_{ii}^{(h)}\right)\\
          &= \frac{1}{|G|} \sum_{h}d_{h}\overline{\lambda_{h}}\chi^{(h)}.
    \end{align}    

Ésta es una combinación lineal de las :math:`\chi^{(h)}`, como queríamos probar.