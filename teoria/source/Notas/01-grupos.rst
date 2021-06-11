Grupos
==========

Los grupos se inventaron como una herramienta para estudiar objetos simétricos. Estos pueden ser objetos de cualquier tipo. Si definimos una simetría de un objeto como una transformación de ese objeto que conserva su estructura esencial, entonces el conjunto de todas las simetrías del objeto forma un grupo. En matemáticas siempre es posible considerar cualquier objeto como un conjunto con alguna estructura adicional; por tanto, una simetría es una función biyectiva que preserva la estructura desde el conjunto hacia sí mismo. La composición de funciones proporciona una operación en este conjunto, y no es difícil demostrar que los axiomas de grupo deben satisfacerse.

Por ejemplo, un cuerpo es un conjunto dotado con operaciones de suma y multiplicación, que satisface varios axiomas. Un cuadrado puede considerarse como un conjunto de puntos y líneas en el plano euclidiano que satisfacen varias propiedades relacionadas con los ángulos y las distancias. Una simetría de un cuerpo es una función biyectiva del cuerpo a sí mismo que conserva las operaciones de suma y multiplicación. (Es decir, una simetría de un cuerpo es un automorfismo del cuerpo). Una simetría de un cuadrado es una función del conjunto relevante de puntos y líneas a sí mismo que conserva todos los ángulos y distancias. En ambos casos, el conjunto de todas las simetrías es un grupo.

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


Proposición
-------------------------------------------------

Sea :math:`G` un grupo y :math:`g\in G`. Entonces el conjunto :math:`C_{G} (g) = \{x \in G | xg = gx \}` es un subgrupo de :math:`G`.

**Demostración:**

- Por definición de elemento identidad tenemos que :math:`1g = g1` y por lo tanto, :math:`1 \in C_{G} (g)`.

- Si :math:`x \in C_{G} (g)` entonces :math:`xg = gx`, y multiplicar esta ecuación a la izquierda y a la derecha por :math:`x^{−1}` da :math:`gx^{−1} = x^{−1}g`, de donde :math:`x^{-1} \in C_{G} (g)`.

- Si :math:`x, y \in C_{G} (g)` entonces :math:`xg = gx` y :math:`yg = gy`, y vemos que

.. math::

    (xy)g = x(yg) = x(gy) = (xg)y = (gx)y = g(xy),

entonces :math:`xy \in C_{G} (g)`. Luego, tenemos que :math:`C_{G} (g) = \{x \in G | xg = gx \}` es un subgrupo de :math:`G`, como queriamos probar.

Definición de Centralizador
-------------------------------------------------

El subgrupo :math:`C_{G} (g)` definido en la proposición anterior se denomina centralizador en :math:`G` del elemento :math:`g`.

.. en vez de nota colocar "Recordemos"

.. note::

    - si :math:`H` es un subgrupo de un grupo :math:`G`, entonces para cada :math:`x\in G` el subconjunto :math:`xH = \{ xh | h \in H \}` se llama una clase lateral izquierda de :math:`H` en :math:`G`.

El mapeo :math:`h \mapsto xh` de :math:`H` a :math:`xH` es una biyección, por lo que el número de elementos de la clase lateral :math:`xH` es el mismo que el número de elementos de :math:`G`. Si :math:`x, y \in G` entonces las clases laterales izquierdas :math:`xH` e :math:`yH` coinciden o son disjuntas. Coinciden si :math:`x \in yH` o (de manera equivalente) si :math:`y \in xH`, o (una tercera condición equivalente) si :math:`x^{−1}y \in H`. Además, cada elemento de :math:`G` se encuentra en alguna clase lateral izquierda de :math:`H`: de hecho, :math:`g \in gH.` De ello se deduce que podemos elegir una transversal izquierda, o sistema de representantes de las clases laterales izquierdas, para el subgrupo :math:`H`. Esta es una familia :math:`(x_{i})_{i\in I}` de elementos de :math:`G` tal que :math:`G` es la unión disjunta de las clases laterales :math:`x_{i}H` para :math:`i \in I`. Suponiendo que el grupo :math:`G` es finito, entonces, por supuesto, el número de clases laterales izquierdas de :math:`H` también es finito. 

El número de clases laterales izquierdas de :math:`H` en :math:`G` se denomina índice de :math:`H` en :math:`G`, denotado por :math:`[G:H]`. Si :math:`n = [G:H]` entonces una transversal izquierda para :math:`H` constará de :math:`n` elementos :math:`x_{1}`, :math:`x_{2}`, :math:`\dots`, :math:`x_{n}`, y dado que :math:`G = x_{1}H \cup x_{2}H \cup \cdots \cup x_{n}H` expresa :math:`G` como la unión disjunta de :math:`n = [G: H]` conjuntos todos los cuales tienen :math:`|H|` elementos, llegamos a la conclusión de que :math:`|G| = [G: H] |H|`.

Supongamos ahora que :math:`H = C_{G} (g)`, donde :math:`g \in G`. Si :math:`x,y \in G` están en la misma clase lateral izquierda de :math:`H`, entonces :math:`y = xh` para algunos :math:`h\in H`, y

.. math::

    ygy^{−1} = (xh)g(xh)^{−1} = x(hg)h^{−1} x^{−1} = x(gh)h^{−1}x^{−1} = xgx^{−1},

ya que :math:`h` está en el centralizador de :math:`g`. Por tanto, hemos demostrado que :math:`ygy^{−1} = xgx^{−1}` para todo :math:`x`, :math:`y` en la misma clase lateral izquierda del centralizador. Por el contrario, si :math:`ygy^{−1} = xgx^{−1}` entonces :math:`(x^{−1}y) g = g (x^{− 1}y)`, de modo que :math:`x^{−1}y \in C_{G} (g)`, y por lo tanto :math:`x` e :math:`y` están en la misma clase lateral del centralizador. Así, los elementos de :math:`G` de la forma :math:`xgx^{−1}` están en correspondencia uno a uno con las clases laterales izquierdas de :math:`C_{G} (g)`: si :math:`x_{1}`, :math:`x_{2}`, :math:`\dots` , :math:`x_{n}` es una transversal izquierda, entonces cada elemento de la forma :math:`xgx^{−1}` es igual a uno u otro de los :math:`n` elementos :math:`x_{i}gx_{i}^{-1}`, y estos elementos son todos distintos (ya que corresponden a clases laterales distintas). Estos elementos de la forma :math:`xgx^{−1}` se denominan conjugados de :math:`g` en :math:`G`; hemos demostrado que el número de conjugados de :math:`G` es igual al índice del centralizador de :math:`g`.