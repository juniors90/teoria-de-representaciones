Matrices Interventoras
================================

Estabilizador
-----------------

Supongamos que un grupo :math:`G` tiene una acción sobre un conjunto :math:`S`. Para la variedad, asumiremos que esta es una acción correcta, pero declaraciones totalmente análogas también son válidas para acciones izquierdas. Para cada :math:`s\in G` el subconjunto de :math:`G`

.. math::

    StabG(s) = \{ g \in G | sg = s \}

se llama estabilizador de :math:`s` en :math:`G`. Es bastante sencillo observar que :math:`1 \in StabG (s)`, que :math:`g^{−1} \in StabG (s)` siempre que :math:`x \in StabG (s)`, y que :math:`xy \in StabG (s)` siempre que :math:`x, y \in StabG (s)`. Por tanto, el estabilizador de :math:`S` es un subgrupo de :math:`G`. El subconjunto de :math:`S`

.. math::

    \mathcal{O} = \{ sg | g \in G \}

se llama la órbita de s bajo la acción de :math:`G`. Si :math:`\mathcal{O} = S`, entonces se dice que la acción de :math:`G` sobre :math:`S` es transitiva.

Como notación temporal, para :math:`s, t \in S` escribamos :math:`s \sim t` si existe :math:`g\in G` tal que :math:`sg = t`.

- Como :math:`s1 = s` tenemos que :math:`s \sim s`, para todo :math:`s \in S`; entonces la relación :math:`\sim` es reflexiva.

- Si :math:`sg = t` entonces :math:`tg^{−1} = s`; por tanto, si :math:`s \sim t` entonces :math:`t \sim s`, y entonces :math:`\sim` es simétrico.

- Y :math:`\sim` también es transitiva, ya que si :math:`s, t, u \in S` con :math:`s \sim t` y :math:`t \sim u` entonces existen :math:`g, h \in G` con :math:`sg = t` y :math:`th = u`, y esto da :math:`s \sim u` ya que :math:`s (gh ) = (sg) h = th = u`.

Por tanto, :math:`\sim` es una relación de equivalencia y, en consecuencia, el conjunto :math:`S` es la unión disjunta de clases de equivalencia :math:`\sim`. La clase de equivalencia que contiene :math:`s` es el conjunto :math:`\{t \in S | s \sim t\} = \{sg | g \in G\}`, que es precisamente la órbita de :math:`s`. Las órbitas de :math:`G` sobre :math:`S` son las clases de equivalencia para la relación :math:`\sim` como se definió anteriormente.

Se puede ver que si el estabilizador de un elemento :math:`s` es grande, entonces la órbita de :math:`s` es pequeña y viceversa. Los dos casos extremos son los siguientes: si el estabilizador de :math:`s` es todo el grupo :math:`G`, entonces la órbita es el conjunto singleton :math:`\{s\}`; si el estabilizador es el subgrupo trivial que consiste solo en el elemento de identidad, entonces los elementos de la órbita de :math:`s` están en correspondencia uno a uno con los elementos de :math:`G` (ya que si :math:`g, h \in G` y :math:`sg = sh` entonces :math:`s (gh^{−1}) = s`, lo que significa que :math:`gh{−1} \in StabG (s) = \{1\}`, y por lo tanto :math:`g = h`). En el caso general, si escribimos :math:`L = StabG (s)` entonces :math:`sg = sh` si y solo si :math:`gh^{−1} \in L`, que es equivalente a :math:`g \in Lh`, y esto a su vez es equivalente a la igualdad de las clases laterales derechas :math:`Lg` y :math:`Lh`. (Si hubiéramos comenzado con una acción izquierda, habríamos obtenido clases laterales izquierdas en este punto: :math:`gs = hs` si y solo si :math:`gL = hL`.) Entonces concluimos que hay un mapeo biyectivo bien definido :math:`sg \mapsto Lg` desde la órbita :math:`\mathcal{O} = \{sg | g \in G\}` al conjunto :math:`\{ Lg | g \in G \}` (cuyos elementos son las clases laterales derechas en :math:`G` del estabilizador de :math:`s`). Por tanto, si :math:`g_{1}`, :math:`g_{2}`, :math:`\dots` , :math:`g_{m}` es una transversal recta para :math:`L`, de modo que

.. math::

    G = Lg_{1} \dot{\cup} Lg_{2} \dot{\cup} \cdots \dot{\cup} Lg_{m}

(donde ":math:`\dot{\cup}`" indica unión disjunta) entonces

.. math::

    \mathcal{O} = \{sg_{1}, sg_{2}, \dots, sg_{m}\},

y los :math:`sg_{i}` son distintos por pares.

Hay dos formas diferentes de definir las acciones correctas de un grupo :math:`G` sobre el propio :math:`G`. En primer lugar, la operación de multiplicación del grupo :math:`G \times G \to G` se puede interpretar como una función :math:`S \times G \to S`, donde el conjunto :math:`S` es igual a :math:`G`. Los axiomas del grupo implican inmediatamente que esta función satisface las propiedades definitorias de una acción correcta. A esto lo llamaremos la acción de multiplicación correcta de :math:`G` sobre sí mismo. Es una acción transitiva — solo hay una órbita — ya que si :math:`s, t \in G` son arbitrarios, entonces el elemento :math:`g = s^{−1}t` satisface :math:`sg = t`. Además, el estabilizador de cualquier elemento es trivial, ya que :math:`sg = g` implica :math:`g = 1`. La otra acción estándar de :math:`G` sobre sí mismo es la acción de conjugación. Para evitar confusiones con la acción de multiplicación correcta, usamos una notación exponencial para la acción de conjugación y definimos :math:`xg = g^{−1}xg` para todo :math:`x, g \in G`. Tenga en cuenta que mientras que la acción de multiplicación correcta es una acción de :math:`G` sobre :math:`G` considerada solo como un conjunto, la acción de conjugación es una acción de :math:`G` sobre :math:`G` considerado como un grupo.

Porque no solo tenemos :math:`x^{1} = 1^{−1}x 1 = x` y

.. math::

    x^{gh} = (gh)^{−1}x(gh) = h^{−1}(g^{−1}xg)h = (g^{−1}xg)^{h} = (x^{g})^{h},

para todo :math:`x, g, h \in G`, pero también

.. math::

    (xy)^{g} = g^{−1}(xy)g = (g^{−1}xg)(g^{−1}yg) = x{g}y^{g}

para todo :math:`x, y, g \in G`. Las órbitas de :math:`G` bajo la acción de conjugación de :math:`G` son, por supuesto, las clases de conjugación, como se define en la lección 4.



Matrices Interventoras
------------------------------

Sean :math:`U` y :math:`V` espacios vectoriales sobre el campo complejo que son módulos para el grupo :math:`G`, y sea :math:`f: U \to V` un homomorfismo :math:`G`. Es decir, :math:`f` es un mapa lineal que satisface :math:`g(fu) = f(gu)` para todo :math:`u \in U` y :math:`g \in G`. Sean :math:`\rho: G \to GL (V)` y :math:`\sigma: G \to GL (U)` las representaciones de :math:`G` en :math:`V` y :math:`U` respectivamente. Es decir, si :math:`g \in G` entonces :math:`\rho g` es la transformación lineal de :math:`V` dada por :math:`v \mapsto gv` para todo :math:`v \in V`, y :math:`\sigma g` es la transformación lineal de :math:`U` dada por :math:`u \mapsto gu` para todo :math:`u \in U`. Para todo :math:`u \in U` tenemos

.. math::

    ((\rho g)f)u = (\rho g)(fu) = g(fu) = f(gu) = f((\sigma g)u) = (f(\sigma g))u,

y entonces :math:`(\rho g) f = f (\sigma g)`. Esto es válido para todo :math:`g \in G`. Se dice que una función :math:`f` que satisface :math:`(\rho g) f = f (\sigma g)` entrelaza las representaciones :math:`\rho` y :math:`\sigma`. Entonces aquí nuevamente tenemos dos palabras que se usan para describir el mismo concepto: una función entrelazada es lo mismo que un :math:`G`-homomorfismo.

Suponga que :math:`u_{1}`, :math:`u_{2}`, :math:`\dots`, :math:`u_{n}` es una base para :math:`U` y :math:`v_{1}`, :math:`v_{2}`, :math:`\dots`, :math:`v_{m}` es una base para :math:`V`, y sea :math:`A` la matriz de :math:`f` relativa a estas dos bases. Por tanto, :math:`A` es la matriz :math:`m\times n` con :math:`(i, j)`-entrada :math:`a_{ij}` que satisface :math:`fu_{j} = \sum_{i = 1}^{m} a_{ij}v_{i}`. Para cada :math:`g \in G` sea :math:`Rg \in GL (m, \mathbb{C})` la matriz relativa a la base :math:`v_{1}`, :math:`v_{2}`, :math:`\dots`, :math:`v_{m}` de la transformación :math:`v \mapsto gv` del espacio :math:`V`, y sea :math:`Sg \in GL (m, \mathbb{C})` la matriz relativa a la base :math:`u_{1}`, :math:`u_{2}`, :math:`\dots`, :math:`u_{m}` de la transformación :math:`u \mapsto gu` del espacio :math:`U`. Entonces, :math:`R` y :math:`S` son versiones matriciales de las representaciones :math:`\rho` y :math:`\sigma`. Y la versión matricial de la ecuación :math:`(\rho g)f = f(\sigma g)` es :math:`(Rg)A = A(Sg).`

Definición
~~~~~~~~~~~~~~~~

Si :math:`R` y :math:`S` son representaciones matriciales del grupo :math:`G` de grados :math:`m` y :math:`n` respectivamente, se dice que una matriz :math:`A` de :math:`m × n` interviene :math:`R` y :math:`S` si :math:`(Rg) A = A (Sg)` para todo :math:`g \in G`.

Entonces, una matriz entrelazada es la versión matricial de un :math:`G`-homomorfismo.

.. note::

    Un mapa lineal es invertible si y solo si su matriz (relativa a cualquier base) es invertible.

Por supuesto, una matriz :math:`A` solo puede ser invertible si es cuadrada, y esto corresponde al hecho de que un mapa :math:`U \to V` solo puede ser invertible si :math:`U` y :math:`V` tienen la misma dimensión. Un :math:`G`-homomorfismo :math:`U \to V` se llama :math:`G`-isomorfismo si es invertible. La versión matricial de esto es una matriz entrelazada que es invertible.

Ahora, si :math:`A` es invertible, entonces la ecuación :math:`(Rg) A = A (Sg)` se puede reescribir como :math:`Rg = A (Sg) A^{− 1}`, y, según una definición de la Lección 3, esto significa que las representaciones :math:`R` y :math:`S` son equivalentes. . Por el contrario, si :math:`R` y :math:`S` son equivalentes, de modo que existe una matriz :math:`A` entrelazada invertible, entonces el mapa lineal :math:`f: U \to V` cuya matriz relativa a nuestras dos bases fijas es :math:`A` es un :math:`G`-isomorfismo. Entonces podemos decir que dos :math:`G`-módulos son :math:`G`-isomorfos si y solo si las representaciones matriciales correspondientes (relativas a cualquier base) son equivalentes.

