El Espacio Coordinado de una Representación
===========================================

En este curso, :math:`\mathbb{C}^{n}` generalmente significa el espacio vectorial de los vectores columna de :math:`n` componentes sobre :math:`\mathbb{C}`. Otros autores a menudo lo definen como el espacio de los vectores fila. Una tercera alternativa sería identificar :math:`\mathbb{C}^{n}` con el espacio de todas las funciones de valor complejo en el conjunto :math:`\{1, 2,\dots , n\}`. De hecho, una función :math:`f: \{1, 2,\dots , n\} \to \mathbb{C}` no es más que una :math:`n`-tupla de valores: :math:`f` puede identificarse con el vector de :math:`n` componentes cuyo :math:`i`-ésimo componente es :math:`f_{i}`. La moraleja de esta historia es simplemente que el conjunto de todas las funciones complejas valoradas en un conjunto de :math:`n` elementos :math:`S` es un espacio vectorial de dimensión :math:`n`. La suma y la multiplicación escalar se definen mediante las fórmulas :math:`(f + g) s = (fs) + (gs)` y :math:`(\lambda f) s = \lambda (fs)`.

Sea :math:`V_{G}` el :math:`|G|`-espacio dimensional de todas las funciones complejas con valores en :math:`G`. El espacio de coordenadas de una representación matricial :math:`S: G \to GL (d, \mathbb{C})` es el subespacio de :math:`V_{G}` que está generado por las funciones de coordenadas de :math:`S` Es decir, para todo :math:`i`, :math:`j \in \{1, 2,\dots , d\}` define :math:`S_{ij}: G \to \mathbb{C}`, de modo que :math:`S_{ij}g` es la entrada :math:`(i, j)` de :math:`Sg`; el espacio de coordenadas es entonces el espacio generado por todas las funciones :math:`S_{ij}`.

Proposición
----------------------

Las representaciones equivalentes tienen el mismo espacio de coordenadas.

**Demostración**

Sean :math:`R` y :math:`S` representaciones matriciales equivalentes de :math:`G` de grado :math:`d`, de modo que exista una matriz :math:`d \times d` invertible :math:`T` tal que :math:`T^{−1} (Rg) T = Sg` para todo :math:`g \in G`. Sean :math:`R_{ij}` y :math:`S_{ij}` las funciones de coordenadas de :math:`R` y :math:`S`, y denotan las entradas :math:`(i, j)` de :math:`T` y :math:`T^{-1}` por :math:`T_{ij}` y :math:`U_{ij}` respectivamente. Entonces para todo :math:`g \in G` tenemos eso

.. math::

    S_{ij}g = \sum_{k = 1}^{d} \sum_{l = 1}^{d} U_{ik} (R_{kl}g) T_{lj}

de donde se sigue que

.. math::
    
    S_{ij} = \sum_{k,l} (U_{ik}T_{lj}) R_{kl}

para todo i, :math:`j \in \{1, 2,\dots , d\}.` Dado que esto expresa cada función de coordenadas de :math:`S` como una combinación lineal de las funciones de coordenadas de :math:`R`, se deduce que todas las funciones de coordenadas de :math:`S` están contenidas en el espacio de coordenadas de :math:`R` y, por lo tanto, el espacio de coordenadas de :math:`S` está contenido en el espacio de coordenadas de :math:`R`. Pero la equivalencia de representaciones es una relación simétrica, por lo que el mismo argumento muestra que el espacio de coordenadas de :math:`R` está contenido en el de :math:`S`.

Tenga en cuenta también el siguiente resultado, que es bastante trivial.

Proposición
----------------------

El espacio de coordenadas de la suma diagonal de dos representaciones :math:`R` y :math:`S` es la suma del espacio vectorial de los espacios de coordenadas de :math:`R` y :math:`S`.

**Demostración**

Sea :math:`m` y :math:`n` el grado de :math:`R` y :math:`S` respectivamente, y sea :math:`T` la suma diagonal, dada por

.. math::

    T g =\left(\begin{matrix}Rg & 0 \\ 0 & Sg \end{matrix}\right)


para todo :math:`g \in G`. Denote las funciones de coordenadas de :math:`R` por :math:`R_{ij}`, y denote las de :math:`S` y :math:`T` de manera similar.

Para :math:`i`, :math:`j \in \{1, 2,\dots, m\}` vemos que :math:`T_{ij} = R_{ij}`, mientras que para :math:`i`, :math:`j \in \{m + 1, m + 2,\dots , m + n\}` tenemos :math:`T_{ij} = S_{i − m, j − m}`. Además, todas las demás funciones de coordenadas de :math:`T` son cero. Entonces, un elemento arbitrario :math:`\sum_{i, j} \lambda_{ij}T_{ij}` del espacio de coordenadas de :math:`T` se puede expresar como

.. math::

    \sum_{ i\leq m, j\leq m} \lambda_{ij}R_{ij} + \sum_{i> m, j> m} \lambda_{ij}S_{i − m, j − m},

que está en la suma de los espacios de coordenadas de :math:`R` y :math:`S`.

Por el teorema de Maschke sabemos que toda representación compleja de un grupo finito es equivalente a una suma diagonal de representaciones irreductibles. Entonces, si, como arriba, fijamos un conjunto completo de representaciones irreductibles * :math:`R^{(1)}`, :math:`R^{(2)}`, :math:`\dots` , :math:`R^{(s)}` entonces el espacio de coordenadas de una representación arbitraria está contenido en la suma de los espacios de coordenadas de :math:`R^{(k)}`. Ahora demostraremos un resultado que, aunque fácil, es crucial para nuestra causa.

Proposición
----------------------

El espacio de coordenadas de la representación regular es igual a :math:`V_{G}`, el espacio de todas las funciones con valores complejos en :math:`G`.

**Demostración**

Por supuesto, el espacio de coordenadas de la representación regular está contenido en :math:`V_{G}`; por lo que solo tenemos que probar la inclusión inversa.

Sea :math:`g_{1}`, :math:`g_{2}`, :math:`\dots` , :math:`g_{n}` los elementos de :math:`G`, de modo que en particular el grado de representación regular es :math:`n`, y sea :math:`g \in G` arbitrario.

Podemos elegir :math:`i`, :math:`j \in \{1, 2,\dots, n\}` tal que :math:`g_{i} = gg_{j}`: por ejemplo, elija :math:`j` para que :math:`g_{j}` sea el elemento de identidad e :math:`i` para que :math:`g_{i} = g`. Ahora la función de coordenadas :math:`R_{ij}` de la representación regular :math:`R` satisface, para todo :math:`h \in G`,

.. math::

    \begin{align}
        R_{ij}h &=
            \begin{cases}
                1 & \text{ si }g_{i} = hg_{j} \\
                0 & \text{en caso contrario}
            \end{cases}\\
            &=
            \begin{cases}
                1 & \text{ si }h = g \\
                0 & \text{en caso contrario}
            \end{cases}
    \end{align}

Por tanto, la función :math:`R_{ij}` es análoga a un vector fila que tiene un componente igual a :math:`1` y todos los demás componentes :math:`0`. Además, el posicionamiento del :math:`1` corresponde a la elección del elemento :math:`h`, que era arbitrario. El conjunto de todas las funciones de esta forma abarca :math:`V_{G}`. Explícitamente, si :math:`f: G \to \mathbb{C}` es arbitrario, entonces

.. math::

    f = \sum_{i = 1}^{n} (f_{i})R_{ij}

donde :math:`j` es fijo de modo que :math:`g_{j}` es el elemento de identidad.

El espacio de coordenadas de la representación irreducible :math:`R^{(k)}` está generado por las funciones de coordenadas :math:`d_{k}^{2} R_{pm}^{(k)}`(donde :math:`p`, :math:`m \in \{1, 2,\dots , d_{k}\}`), y la suma de los espacios de coordenadas de :math:`R^{(1)}`, :math:`R^{(2)}`, :math:`\dots`, :math:`R^{(s)}` está generado por la totalidad de todas las funciones de coordenadas :math:`R_{pm}^{(k)}` para :math:`(k, p, m)` en el conjunto

.. math::

    S = \{(k, p, m) | 1 \leq k \leq s\text{ y }p, m \in \{1, 2,\dots  , d_{k}\}\}.

Pero esta suma de espacios de coordenadas debe ser igual al espacio completo :math:`V_{G}` de funciones con valores complejos en :math:`G`, ya que debe contener el espacio de coordenadas de la representación regular, por lo que el número de elementos en el conjunto de expansión :math:`S` debe ser al menos :math:`|G| = dim V_{G}`. Entonces llegamos a la conclusión de que :math:`\sum_{k=1}^{s} d_{k}^{2} \geq | G |`, y por lo tanto :math:`\sum_{k = 1}^{s} d_{k}^{2} = |G|` ya que la desigualdad inversa se obtuvo previamente. Dado que esto también muestra que el número de elementos en :math:`S` es igual a la dimensión de :math:`V_{G}`, que abarca, se deduce que los elementos de :math:`S` son linealmente independientes.