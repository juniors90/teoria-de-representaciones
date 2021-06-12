.. role:: underline
    :class: underline

Matrices Interventoras
================================

Estabilizador
-----------------

Supongamos que un grupo :math:`G` tiene una acción sobre un conjunto :math:`S`. Para variar, asumiremos que esta es una acción a derecha, pero declaraciones totalmente análogas también son válidas para acciones izquierdas.

Definición de Estabilizador
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Para cada :math:`s\in G` el subconjunto de :math:`G`

.. math::

    Stab_{G}(s) = \{ g \in G | sg = s \}

se llama estabilizador de :math:`s` en :math:`G`.

Es fácil ver que

- :math:`1 \in Stab_{G} (s)`
- :math:`g^{−1} \in Stab_{G} (s)` siempre que :math:`g \in Stab_{G} (s)` y
- :math:`gh \in Stab_{G} (s)` siempre que :math:`g, h \in Stab_{G} (s)`.

Por tanto, el estabilizador de :math:`S` es un subgrupo de :math:`G`.

Definición de Órbita
~~~~~~~~~~~~~~~~~~~~~~~~~~

El subconjunto de :math:`S` dado por :math:`\mathcal{O} = \{ sg | g \in G \}` se llama la órbita de :math:`s` bajo la acción de :math:`G`.

- Si :math:`\mathcal{O} = S`, entonces se dice que la acción de :math:`G` sobre :math:`S` es transitiva.


Las órbitas de un Grupo sobre un Conjunto como clases de equivalencia
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Como notación temporal, para :math:`s, t \in S` escribamos :math:`s \sim t` si existe :math:`g\in G` tal que :math:`sg = t`.

- Como :math:`s1 = s` tenemos que :math:`s \sim s`, para todo :math:`s \in S`; entonces la relación :math:`\sim` es reflexiva.

- Si :math:`sg = t` entonces :math:`tg^{−1} = s`; por tanto, si :math:`s \sim t` entonces :math:`t \sim s`, y entonces :math:`\sim` es simétrico.

- Y :math:`\sim` también es transitiva, ya que si :math:`s, t, u \in S` con :math:`s \sim t` y :math:`t \sim u` entonces existen :math:`g, h \in G` con :math:`sg = t` y :math:`th = u`, y esto da :math:`s \sim u` ya que :math:`s (gh ) = (sg) h = th = u`.

Por tanto, :math:`\sim` es una relación de equivalencia y, en consecuencia, el conjunto :math:`S` es la unión disjunta de clases de equivalencia :math:`\sim`. La clase de equivalencia que contiene :math:`s` es el conjunto :math:`\{t \in S | s \sim t\} = \{sg | g \in G\}`, que es precisamente la órbita de :math:`s`. Las órbitas de :math:`G` sobre :math:`S` son las clases de equivalencia para la relación :math:`\sim` como se definió anteriormente.

Realción entre el estabilizador y la órbita de un elemento
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Se puede ver que si el estabilizador de un elemento :math:`s` es grande, entonces la órbita de :math:`s` es pequeña y viceversa. Los dos casos extremos son los siguientes:

1. Si el estabilizador de :math:`s` es todo el grupo :math:`G`, entonces la órbita es el conjunto singleton :math:`\{s\}`. Es decir que, si :math:`Stab_{G}(s) = \{ g \in G | sg = s \} = G` entonces la órbita de :math:`s` está dada por :math:`\mathcal{O} = \{ sg | g \in G \} = \{ s | g \in G \} = \{ s \}`.

2. Si el estabilizador es el subgrupo trivial que consiste solo en el elemento de identidad, entonces los elementos de la órbita de :math:`s` están en correspondencia uno a uno con los elementos de :math:`G` (ya que si :math:`g, h \in G` y :math:`sg = sh` entonces :math:`s (gh^{−1}) = s`, lo que significa que :math:`gh^{−1} \in Stab_{G} (s) = \{1\}`, y por lo tanto :math:`g = h`).

.. reemplazar "Importante" por "En el caso general"

.. important::

    En el caso general, si escribimos :math:`L = Stab_{G} (s)` entonces :math:`sg = sh` si y solo si :math:`gh^{−1} \in L`, que es equivalente a :math:`g \in Lh`, y esto a su vez es equivalente a la igualdad de las clases laterales derechas :math:`Lg` y :math:`Lh`.

.. note::

    Veamos que si hubiéramos comenzado con una acción izquierda, habríamos obtenido clases laterales izquierdas en este punto: :math:`gs = hs` si y solo si :math:`gL = hL`.

Entonces concluimos que hay un mapeo biyectivo bien definido :math:`sg \mapsto Lg` desde la órbita :math:`\mathcal{O} = \{sg | g \in G\}` al conjunto :math:`\{ Lg | g \in G \}` (cuyos elementos son las clases laterales derechas en :math:`G` del estabilizador de :math:`s`). Por tanto, si :math:`g_{1}`, :math:`g_{2}`, :math:`\dots` , :math:`g_{m}` es una transversal derecha para :math:`L`, de modo que

.. math::

    G = Lg_{1} \dot{\cup} Lg_{2} \dot{\cup} \cdots \dot{\cup} Lg_{m}

(donde ":math:`\dot{\cup}`" indica unión disjunta) entonces

.. math::

    \mathcal{O} = \{sg_{1}, sg_{2}, \dots, sg_{m}\},

y los :math:`sg_{i}` son distintos por pares.

Hay dos formas diferentes de definir las acciones a derecha de un grupo :math:`G` sobre el propio :math:`G`. En primer lugar, la operación de multiplicación del grupo :math:`G \times G \to G` se puede interpretar como una función :math:`S \times G \to S`, donde el conjunto :math:`S` es igual a :math:`G`. Los axiomas de grupo implican inmediatamente que esta función satisface las propiedades definitorias de una acción correcta. A esto lo llamaremos la acción de multiplicación a derecha de :math:`G` sobre sí mismo. Es una acción transitiva - solo hay una órbita - ya que si :math:`s, t \in G` son arbitrarios, entonces el elemento :math:`g = s^{−1}t` satisface :math:`sg = t`. Además, el estabilizador de cualquier elemento es trivial, ya que :math:`sg = g` implica :math:`g = 1`. La otra acción estándar de :math:`G` sobre sí mismo es la *acción de conjugación*. Para evitar confusiones con la acción de multiplicación a derecha, usamos una notación exponencial para la acción de conjugación y definimos :math:`xg = g^{−1}xg` para todo :math:`x, g \in G`. Tenga en cuenta que mientras que la acción de multiplicación a derecha es una acción de :math:`G` sobre :math:`G` considerada solo como un conjunto, la acción de conjugación es una acción de :math:`G` sobre :math:`G` considerado como un grupo.

Porque no solo tenemos :math:`x^{1} = 1^{−1}x 1 = x` y

.. math::

    x^{gh} = (gh)^{−1}x(gh) = h^{−1}(g^{−1}xg)h = (g^{−1}xg)^{h} = (x^{g})^{h},

para todo :math:`x, g, h \in G`, pero también

.. math::

    (xy)^{g} = g^{−1}(xy)g = (g^{−1}xg)(g^{−1}yg) = x{g}y^{g}

para todo :math:`x, y, g \in G`. Las órbitas de :math:`G` bajo la acción de conjugación de :math:`G` son, por supuesto, las clases de conjugación, como se define en la lección 4.



Matrices Interventoras
------------------------------

- Sean :math:`U` y :math:`V` espacios vectoriales sobre :math:`\mathbb{C}` que son módulos para el grupo :math:`G`

- Sea :math:`f: U \to V` un :math:`G`-homomorfismo. Es decir, :math:`f` es un mapa lineal que satisface :math:`g(fu) = f(gu)` para todo :math:`u \in U` y :math:`g \in G`.

- Sean :math:`\rho: G \to GL (V)` y :math:`\sigma: G \to GL (U)` las representaciones de :math:`G` en :math:`V` y en :math:`U` respectivamente. Es decir, si :math:`g \in G` entonces :math:`\rho_g` es la transformación lineal de :math:`V` dada por :math:`v \mapsto gv` para todo :math:`v \in V`, y :math:`\sigma g` es la transformación lineal de :math:`U` dada por :math:`u \mapsto gu` para todo :math:`u \in U`. Para todo :math:`u \in U` tenemos

.. math::

    \begin{align}
        ((\rho_g)f)u &= (\rho_g)(fu)     &&&&\text{ por composición }\\
                     &= g(fu)            &&&&\text{ por la acción de }\rho\\
                     &= f(gu)            &&&&\text{ por definición de } f\\
                     &= f((\sigma g)u)   &&&&\text{ por la acción de }\sigma\\
                     &= (f(\sigma g))u,  &&&&\text{ por composición }\\
    \end{align}

y entonces :math:`(\rho_g) f = f (\sigma g)`. Esto es válido para todo :math:`g \in G`. Se dice que una función :math:`f` que satisface :math:`(\rho_g) f = f (\sigma g)` *interviene* las representaciones :math:`\rho` y :math:`\sigma`.

.. important::

    Aquí nuevamente tenemos dos palabras que se usan para describir el mismo concepto: una función *interviene* es lo mismo que un :math:`G`-homomorfismo.

Suponga que :math:`u_{1}`, :math:`u_{2}`, :math:`\dots`, :math:`u_{n}` es una base para :math:`U` y :math:`v_{1}`, :math:`v_{2}`, :math:`\dots`, :math:`v_{m}` es una base para :math:`V`, y sea :math:`A` la matriz de :math:`f` relativa a estas dos bases. Por tanto, :math:`A` es la matriz :math:`m\times n` con :math:`(i, j)`-entrada :math:`a_{ij}` que satisface :math:`fu_{j} = \sum_{i = 1}^{m} a_{ij}v_{i}`. Para cada :math:`g \in G` sea :math:`R_g \in GL (m, \mathbb{C})` la matriz relativa a la base :math:`v_{1}`, :math:`v_{2}`, :math:`\dots`, :math:`v_{m}` de la transformación :math:`v \mapsto gv` del espacio :math:`V`, y sea :math:`Sg \in GL (m, \mathbb{C})` la matriz relativa a la base :math:`u_{1}`, :math:`u_{2}`, :math:`\dots`, :math:`u_{m}` de la transformación :math:`u \mapsto gu` del espacio :math:`U`. Entonces, :math:`R` y :math:`S` son versiones matriciales de las representaciones :math:`\rho` y :math:`\sigma`. Y la versión matricial de la ecuación :math:`(\rho_g)f = f(\sigma g)` es :math:`(R_g)A = A(Sg).`

Definición
~~~~~~~~~~~~~~~~

Si :math:`R` y :math:`S` son representaciones matriciales del grupo :math:`G` de grados :math:`m` y :math:`n` respectivamente, se dice que una matriz :math:`A` de :math:`m × n` interviene :math:`R` y :math:`S` si :math:`(R_g) A = A (Sg)` para todo :math:`g \in G`.

Entonces, una **matriz interventora** es la versión matricial de un :math:`G`-homomorfismo.

.. note::

    - Un mapa lineal es invertible si y solo si su matriz (relativa a cualquier base) es invertible.

    - Es claro que, una matriz :math:`A` solo puede ser invertible si es cuadrada, y esto corresponde al hecho que un mapa :math:`U \to V` solo puede ser invertible si :math:`U` y :math:`V` tienen la misma dimensión.

.. important::

    - Un :math:`G`-homomorfismo :math:`f: U \to V` se llama :math:`G`-isomorfismo si es invertible. La versión matricial de esto es una matriz entrelazada que es invertible.

Ahora, si :math:`A` es invertible, entonces la ecuación :math:`(R_g) A = A (Sg)` se puede reescribir como :math:`R_g = A (Sg) A^{− 1}`, esto significa que las representaciones :math:`R` y :math:`S` son equivalentes, por :ref:`representaciones-matriciales-equivalente` (Ver Sección :doc:`03-representaciones-y-representaciones-matriciales`).

Recíprocamente, si :math:`R` y :math:`S` son equivalentes, de modo que existe una matriz :math:`A` interventora invertible, entonces el mapa lineal :math:`f: U \to V` cuya matriz relativa a nuestras dos bases fijas es :math:`A` es un :math:`G`-isomorfismo.

.. important::

    - Dos :math:`G`-módulos son :math:`G`-isomorfos si y solo si las representaciones matriciales correspondientes (relativas a cualquier base) son equivalentes.

Implementacion en GAP
---------------------------------


.. _GroupSumBSGS:

GroupSumBSGS
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

La función ``GroupSumBSGS(G, summand)`` devuelve :math:`\displaystyle\sum_{g \in G} \text{summand}(g)`

Utiliza una cadena estabilizadora básica por :math:`G` para calcular la suma descrita anteriormente. Este truco requiere que ``summand`` sea una función (en el sentido de **GAP**) que defina un homomorfismo monoide (en el sentido matemático). El cálculo de la cadena estabilizadora asume que :math:`G` es un grupo.

Más precisamente, si tenemos la cadena estabilizadora básica:

.. math::

    \{1\} = G_{1} \leq \ldots \leq G_{n} = G

Atravesamos la cadena desde :math:`G_{1}` a :math:`G_{n}`, usando la suma anterior :math:`G_{i-1}` para construir la suma :math:`G_{i}`. Hacemos esto usando el hecho de que (escribiendo :math:`f` para ``summand``)

.. math::

    \sum_{g \in G_i} f(g) = \sum_{r_j} \left(\sum_{h \in G_{i-1}} f(h)\right) f(r_j)

donde :math:`r_j` son representantes de la clase lateral derecha de :math:`G_ {i-1}` en :math:`G_{i}`.

La condición de ``summand`` se cumple si, por ejemplo, es una representación lineal de un grupo :math:`G`.


.. _LinearRepresentationIsomorphism:

Isomorfismos entre Representaciones Lineales
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Los isomorfismos entre Representaciones Lineales se pueden calcular utilizando la función ``LinearRepresentationIsomorphism( rho, sigma[, rho_cent_basis , sigma_ cent_basis] )`` la cual retorna una matriz :math:`A` o ``fail``

Sean :math:`\rho: G \to GL (V)` y :math:`\sigma: G \to GL (U)`. Si existe un mapa lineal :math:`A: V \to U` tal que :math:`(\sigma g) A = A(\rho_g)` para todo :math:`g \in G`, esta función devuelve uno de esos :math:`A`.

Es decir, que :math:`A` es el isomorfismo o la función que *interviene* las representaciones :math:`\rho` y :math:`\sigma`. :underline:`Si las representaciones no son isomorfas`, se devuelve ``fail``.

Hay tres métodos que podemos usar para calcular un isomorfismo de representaciones lineales, puede seleccionar uno pasando opciones a la función.

    - ``use_kronecker``: asume que las matrices son lo suficientemente pequeñas como para que sus productos Kronecker puedan caber en la memoria. Utiliza :ref:`GroupSumBSGS` y ``KroneckerProduct`` para calcular un elemento del subespacio fijo de :math:`\rho \otimes \sigma^{\ast}`.
    - ``use_orbit_sum``: Encuentra un isomorfismo sumando las órbitas de la acción de :math:`\rho \otimes \sigma^{\ast}` en matrices. Tenga en cuenta que las órbitas pueden ser muy grandes, por lo que esto podría ser tan malo como sumar todo el grupo.
    - El valor predeterminado, suma sobre todo el grupo para calcular la proyección en el subespacio fijo.

.. code-block:: gap
    :caption: función LinearRepresentationIsomorphism
    :name: Ejemplo_LinearRepresentationIsomorphism

    gap> LoadPackage( "RepnDecomp" );
    ────────────────────────────────────────────────────────────────────────────────────────
    Loading  GRAPE 4.8.2 (GRaph Algorithms using PErmutation groups)
    by Leonard H. Soicher (http://www.maths.qmul.ac.uk/~lsoicher/).
    Homepage: https://gap-packages.github.io/grape
    ────────────────────────────────────────────────────────────────────────────────────────
    ────────────────────────────────────────────────────────────────────────────────────────
    Loading  RepnDecomp 1.1.0 (Decompose representations of finite groups into irreducibles)
    by Kaashif Hymabaccus (https://kaashif.co.uk).
    Homepage: https://gap-packages.github.io/RepnDecomp
    ────────────────────────────────────────────────────────────────────────────────────────
    true
    gap> # Ejemplo_LinearRepresentationIsomorphism
    gap> G := SymmetricGroup(4);;
    gap> irreps := IrreducibleRepresentations(G);;
    gap> # rho y tau son isomorfos, solo tienen un orden de bloque diferente
    gap> rho := DirectSumOfRepresentations([irreps[1], irreps[3], irreps[3]]);;
    gap> tau := DirectSumOfRepresentations([irreps[3], irreps[1], irreps[3]]);;
    gap> # tau2 es solo tau con un cambio de base, sigue siendo isomorfo
    gap> B := RandomInvertibleMat(5);;
    gap> tau2 := ComposeHomFunction(tau, x -> B^-1 * x * B);;
    gap> # usando la implementación predeterminada
    gap> M := LinearRepresentationIsomorphism(rho, tau);;
    gap> IsLinearRepresentationIsomorphism(M, rho, tau);
    true
    gap> M := LinearRepresentationIsomorphism(tau, tau2);;
    gap> IsLinearRepresentationIsomorphism(M, tau, tau2);
    true
    gap> # usando la implementación de suma de kronecker
    gap> M := LinearRepresentationIsomorphism(tau, tau2 : use_kronecker);;
    gap> IsLinearRepresentationIsomorphism(M, tau, tau2);
    true
    gap> # usando la implementación de suma de órbitas
    gap> M := LinearRepresentationIsomorphism(tau, tau2 : use_orbit_sum);;
    gap> IsLinearRepresentationIsomorphism(M, tau, tau2);
    true
    gap> # dos irreps distintos no son isomorfos
    gap> M := LinearRepresentationIsomorphism(irreps[1], irreps[2]);
    fail
    gap>


.. _LinearRepresentationIsomorphismSlow:

LinearRepresentationIsomorphismSlow
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Los isomorfismos entre Representaciones Lineales se pueden calcular de manera más lenta con la función ``LinearRepresentationIsomorphismSlow( rho, tau )`` que devuelve una matriz :math:`A` o ``fail``

Da el mismo resultado que LinearRepresentationIsomorphism_, pero esta función usa un método más simple que siempre implica sumar sobre :math:`G`, sin usar :ref:`GroupSumBSGS`. Esto puede resultar útil en algunos casos si resulta difícil calcular un buen ``BSGS``. Sin embargo, para todos los casos que se han probado, es lento (como sugiere el nombre).

.. code-block:: gap
    :caption: función LinearRepresentationIsomorphismSlow
    :name: Ejemplo_LinearRepresentationIsomorphismSlow
    :emphasize-lines: 7-11

    gap> LoadPackage( "RepnDecomp" );
    ...
    ... el resto de código del ejemplo anterior
    ...
    gap> M := LinearRepresentationIsomorphism(irreps[1], irreps[2]);
    fail
    gap> # Ejemplo_LinearRepresentationIsomorphismSlow
    gap> # Siguiendo el ejemplo anterior
    gap> M := LinearRepresentationIsomorphismSlow(rho, tau);;
    gap> IsLinearRepresentationIsomorphism(M, rho, tau);
    true
    gap>





.. _AreRepsIsomorphic:

AreRepsIsomorphic
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

LPodemos probar isomorfismos entre dos Representaciones Lineales mediante la función ``AreRepsIsomorphic( rho, tau)``, que devuelve ``true`` si ``rho`` y ``tau`` son isomorfos como representaciones, ``false`` en caso contrario.

Dado que las representaciones de grupos finitos sobre :math:`\mathbb{C}` están determinadas por sus caracteres, es fácil comprobar si dos representaciones son isomorfas comprobando si tienen el mismo carácter. Intentamos utilizar caracteres siempre que sea posible.

.. code-block:: gap
    :caption: función AreRepsIsomorphic
    :name: Ejemplo_AreRepsIsomorphic
    :emphasize-lines: 7-16

    gap> LoadPackage( "RepnDecomp" );
    ...
    ... el resto de código de los ejemplos anteriores
    ...
    gap> IsLinearRepresentationIsomorphism(M, rho, tau);
    true
    gap> # Ejemplo_AreRepsIsomorphic
    gap> # Siguiendo los ejemplos anteriores
    gap> # Algunas representaciones isomorfas
    gap> AreRepsIsomorphic(rho, tau);
    true
    gap> AreRepsIsomorphic(rho, tau2);
    true
    gap> # rho no es iso a irreps[1] ya que rho es irreps[1] más algunas otras cosas
    gap> AreRepsIsomorphic(rho, irreps[1]);
    false
    gap>

.. _IsLinearRepresentationIsomorphism:

IsLinearRepresentationIsomorphism
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

La función ``IsLinearRepresentationIsomorphism( A, rho, tau)`` devuelve ``true`` si ``rho`` y ``tau`` son :underline:`isomorfos como representaciones con el isomorfismo dado por el mapa lineal` :math:`A`.

Esta función prueba si, para todo :math:`g \in G`, :math:`A (\rho_g) = (\sigma g) A`. Es decir, se devuelve verdadero si y solo sí :math:`A` es el operador entrelazado que lleva :math:`\rho` a :math:`\sigma`. Veamos,

.. code-block:: gap
    :caption: función IsLinearRepresentationIsomorphism
    :name: Ejemplo_IsLinearRepresentationIsomorphism
    :emphasize-lines: 7-14

    gap> LoadPackage( "RepnDecomp" );
    ...
    ... el resto de código de los ejemplos anteriores
    ...
    gap> AreRepsIsomorphic(rho, irreps[1]);
    false
    gap> # Ejemplo_IsLinearRepresentationIsomorphism
    gap> # Ya hemos visto que esta función se usa mucho en ejemplos anteriores.
    gap> # Si dos representaciones son isomorfas, siempre se cumple lo siguiente:
    gap> IsLinearRepresentationIsomorphism(LinearRepresentationIsomorphism(rho, tau), rho, tau);
    true
    gap> # Nota: esta prueba es sensible a las llamados:
    gap> IsLinearRepresentationIsomorphism(LinearRepresentationIsomorphism(rho, tau), tau, rho);
    false
    gap>