.. role:: underline
    :class: underline

Representaciones por Permutacion y Acciones
==============================================

Introducción
------------

Para comprender las notas del curso se deben tener nociones de

- Teoría de Grupos
- Álgebra lineal

En matemáticas, la palabra "representación" significa básicamente "función de preservación de la estructura". Por lo tanto, en la "Teoría de Grupos" una representación es un homomorfismo.

Pero, más concretamente, debería ser un homomorfismo de un objeto (grupo o anillo) que se está intentando estudiar a otro que es de alguna forma más concreto y por tanto, de un salto, más fácil de entender. Los dos tipos de grupos más simples son,

1. el grupo de todas las permutaciones de un conjunto arbitrario y,

2. el grupo de todas las transformaciones lineales invertibles en un espacio vectorial arbitrario.

Entonces, para los grupos, las representaciones más comúnmente estudiadas son las representaciones por permutación y las representaciones lineales.

Representaciones por Permutación y Acciones
-----------------------------------------------

Representación por permutación de un grupo
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Una representación por permutación de un grupo :math:`G` en un conjunto :math:`S` es un homomorfismo de :math:`G` al grupo de permutaciones de :math:`S`.

Representación lineal de un grupo
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    
Una representación lineal de un grupo :math:`G` en un espacio vectorial :math:`V` es un homomorfismo de :math:`G` al grupo de todas las transformaciones lineales invertibles de :math:`V`.


A menos que esté calificado con algún otro adjetivo, "representación" generalmente significa "representación lineal", por lo que este curso se ocupará de las representaciones lineales de grupos. Por lo general, restringiremos nuestra atención a grupos finitos y espacios vectoriales sobre el cuerpo complejo, ya que esto simplifica las cosas y proporciona una teoría más completa. Si bien sería posible lanzarnos de inmediato al desarrollo de esta teoría, primero dedicaremos un poco de tiempo a familiarizarnos con algunos pequeños grupos finitos, para luego poder ver cómo se aplica la teoría en ejemplos particulares.

- El fundador del tema fue Ferdinand Georg Frobenius (1849-1917), quien descubrió las asombrosas propiedades básicas de los caracteres grupales irreductibles y las publicó en una serie de artículos en la década de 1890.
- Su alumno, Issai Schur, fue otro que hizo muchas contribuciones tempranas importantes al tema.
- En su forma moderna, el tema debe mucho a las contribuciones de Emmy Noether (en la década de 1920), cuyo trabajo forma la base de lo que ahora se llama "álgebra moderna".
- Sobre esta base, Richard Brauer desarrolló la teoría de la representación modular, en la que se estudian las representaciones sobre cuerpos de características distintas de cero y se relacionan con representaciones complejas.

.. _accion-de-un-grupo-sobre-un-conjunto:

Acción de un grupo sobre un conjunto
------------------------------------

Una acción de un grupo :math:`G` sobre un conjunto :math:`S` es una función :math:`(g, s) \mapsto gs` de :math:`G \times S` a :math:`S` tal que
    
    :math:`(i)` :math:`(gh)s = g(hs)` para todo :math:`g, h \in G`, :math:`s \in S`,

    :math:`(i)` :math:`1s = s` para todo :math:`s \in S`, donde :math:`1` es el elemento identidad de :math:`G`.

.. note::

    - Habitualmente usaremos la notación ":math:`1`" para el elemento de identidad de un grupo abstracto, aunque si la operación de grupo se escribe como ":math:`+`" entonces usaremos ":math:`0`" para la identidad. Para un grupo de transformaciones de un conjunto, el elemento identidad será la función identidad del conjunto a sí mismo, y esto lo denotaremos por ":math:`id`". La matriz de identidad se indicará con ":math:`I`"

    - Una acción de :math:`G` sobre :math:`S` puede ser vista como "una regla para multiplicar elementos de :math:`S` por elementos de :math:`G`", tal que el resultado es otro elemento de :math:`S`.



Acciones de Grupos
----------------------

Hemos definido los conceptos de una acción de un grupo :math:`G` sobre un conjunto :math:`S` y de una representación de permutación de :math:`G` sobre :math:`S`. De hecho, estos dos conceptos son esencialmente equivalentes.

.. important::

    **Supongamos que** :math:`\phi: G \to Sym (S)` es una representación de permutación de :math:`G`. Entonces :math:`\phi g` es una permutación de :math:`S` para :math:`g \in G`, y para cada :math:`x\in S` podemos definir :math:`gx\in S` mediante la fórmula :math:`gx = (\phi g)x`. Dado que :math:`\phi` es un homomorfismo, tenemos que :math:`\phi (gh) = (\phi g) (\phi h) `para todo :math:`g, h \in G`, y dado que el producto de las permutaciones :math:`\phi g` y :math:`\phi h` es por definición su compuesto (:math:`\phi h` seguido de :math:`\phi g`), sigue que

    .. math::

        (gh)x = (\phi (gh))x = ((\phi g)( \phi  h))x = ( \phi g)(( \phi h)x) = ( \phi g)(hx) = g(hx)

    para todo :math:`x \in S`. Esto muestra que se satisface *la primera propiedad* en la definición de una :ref:`accion-de-un-grupo-sobre-un-conjunto`.

    Además, dado que un homomorfismo de grupo necesariamente lleva el elemento de identidad al elemento de identidad, debemos tener que :math:`\phi 1 = id`, y por lo tanto

    .. math::

        1x = (\phi 1)x = id(x) = x

    para todo :math:`x \in S`. Luego, se satisface la segunda propiedad en :ref:`accion-de-un-grupo-sobre-un-conjunto`. Por lo tanto, tenemos una acción de :math:`G` sobre :math:`S`.

    **Recíprocamente**, si tenemos una acción de :math:`G` sobre :math:`S`, entonces para cada :math:`g \in G` podemos definir una función :math:`\phi g: S \to S` por :math:`(\phi g) x = gx`. Entonces para todo :math:`g, h \in G` y :math:`x \in S` tenemos que

    .. math::

        ((\phi g) (\phi h)) x = (\phi g) ((\phi h) x) = (\phi g) (hx) = g (hx) = (gh) x = (\phi (gh)) x,

    y por lo tanto :math:`(\phi g) (\phi h) = \phi (gh)`. Además, :math:`\phi 1 = id`, ya que

    .. math::

        (\phi 1)x = 1x = x = id(x)

    para todo :math:`x \in S`. Se deduce que :math:`(\phi g) (\phi (g^{−1})) = id = (\phi (g^{−1})) (\phi g)`, por lo que las funciones :math:`\phi g` y :math:`\phi (g^{−1})` son inversas a entre sí, lo que significa que ambos son biyectivos. Entonces :math:`\phi` es una función de :math:`G` a :math:`Sym (S)`, y como ya hemos demostrado que preserva la multiplicación, se deduce que :math:`\phi` es una representación de permutación.

Es una práctica bastante común entre los algebristas, especialmente los teóricos de grupos, que las funciones se escriban como operadores de derecha en lugar de operadores de izquierda. En otras palabras, el valor de la función :math:`f` en el elemento :math:`x` se escribe como :math:`xf` en lugar de :math:`f(x)`. Aunque esto es puramente una cuestión de notación, tiene ramificaciones. En particular, el compuesto :math:`fg` de dos funciones :math:`f` y :math:`g` se define mediante la regla :math:`x(fg) = (xf)g` si :math:`f` y :math:`g` se escriben como operadores de la derecha, mientras que para los operadores de la izquierda la fórmula correspondiente para :math:`fg` es :math:`(fg) ( x) = f (g (x))`. Según la convención del operador correcto, :math:`fg` significa :math:`f` seguida de :math:`g`; bajo la convención del operador de la izquierda significa :math:`g` seguido de :math:`f`. Como hay contextos en los que aparecen simultáneamente los operadores de la derecha y los de la izquierda, tenemos que poder trabajar con ambas convenciones. En consecuencia, definimos una acción correcta de un grupo :math:`G` sobre un conjunto :math:`S` como una función :math:`(x, g) \mapsto xg` de :math:`S \times G` a :math:`S` tal que :math:`x1 = x` y :math:`x (gh) = (xg) h` para todos :math:`g, h \in G` y todo :math:`x \in S`. Si uno escribiera las permutaciones de uno como operadores derechos en lugar de operadores izquierdos, y de hecho para las permutaciones, la convención del operador derecho es más común que la convención del operador izquierdo, entonces una representación de permutación de :math:`G` sobre :math:`S` sería esencialmente lo mismo que una acción correcta de :math:`G` sobre :math:`S`.

Si el conjunto :math:`S` sobre el que actúa un grupo no es solo un conjunto, sino un conjunto con alguna estructura adicional, entonces es natural preguntarse si la acción conserva la estructura. Así, por ejemplo, una acción izquierda de un grupo :math:`G` en un espacio vectorial :math:`V` significa implícitamente una acción izquierda de :math:`G` en el conjunto :math:`V` tal que :math:`g (u + v) = gu + gv` y :math:`g (\lambda v) = \lambda (gv)` para todo :math:`u, v \in V` y todos los escalares :math:`\lambda` y todo :math:`g \in G`.

Una acción izquierda de :math:`G` sobre :math:`V` es entonces esencialmente lo mismo que un homomorfismo de :math:`G` al grupo de todas las transformaciones lineales invertibles en :math:`V` (donde las transformaciones lineales se escriben como operadores izquierdos).

También podemos hablar de una acción de un grupo sobre otro grupo. Es común usar una convención de operadores correctos y escribir los operadores como exponentes. Siguiendo esta convención, una acción de un grupo :math:`A` sobre otro grupo :math:`G` es una función :math:`(g, \alpha) \mapsto g^{\alpha}` de :math:`G \times A` a :math:`G` tal que se satisfacen las siguientes propiedades:

    :math:`(i)` :math:`(g^{\alpha})^{\beta} = g^{\alpha \beta}` para todo :math:`g \in G` y :math:`\alpha, \beta \in A`,
    
    :math:`(ii)` :math:`g^{1} = g` para todo :math:`g \in G` (donde :math:`1` es el elemento identidad de :math:`A`),
    
    :math:`(iii)` :math:`(gh)^{\alpha} = g^{\alpha} h^{\alpha}` para todo :math:`g, h \in G` y :math:`\alpha \in A`.

Recuerde que un subgrupo normal :math:`K` de un grupo :math:`G` es un subgrupo de :math:`G` tal que :math:`g^{-1}kg \in K` para todo :math:`g \in G` y :math:`k\in K`. Es un teorema básico importante de la teoría de grupos que si :math:`K` es normal en :math:`G` entonces hay es una acción de :math:`G` sobre :math:`K` definida por :math:`k^{g} = g^{−1}kg` para todo :math:`g \in G` y :math:`k\in K`. Es una cuestión sencilla comprobar que se satisfacen las tres propiedades anteriores. Por ejemplo, si :math:`k_{1}, k_{2} \in K` y :math:`g \in G` entonces

.. math::

    (k_{1}k_{2})^{g} = g^{−1}k_{1}k_{2}g = (g^{−1}k_{1}g)(g^{−1}k_{2}g) = k_{1}^{g}k_{2}^{g}.

Si :math:`G` y :math:`H` son grupos, el producto directo externo de :math:`G` y :math:`H` es el conjunto

.. math::

    G \times H = \{ (g, h) | g \in G, h \in H \},

equipado con la multiplicación definida por :math:`(g_{1}, h_{1}) (g_{2}, h_{2}) = (g_{1}g_{2}, h_{1}h_{2})`. Se comprueba fácilmente que :math:`G \times H` es un grupo con esta operación.

Suponga que :math:`S` y :math:`T` son subgrupos de :math:`G` tales que :math:`S\cap T = \{ 1 \}`, y suponga también que :math:`st = ts` para todo :math:`s\in S` y :math:`t\in T`. Se define una función :math:`f` del producto directo externo :math:`S \times T` a :math:`G` por :math:`f (s, t) = st` para todo :math:`s\in S` y :math:`t\in T`. Claramente :math:`f` es un homomorfismo:

.. math::

    f((s_{1}, t_{1})(s_{2}, t_{2})) = f(s_{1}s_{2}, t_{1}t_{2}) = (s_{1}s_{2})(t_{1}t_{2}) = (s_{1}t_{1})(s_{2}t_{2}) = f(s_{1}, t_{1})f(s_{2}, t_{2}).

También es fácil demostrar que :math:`f` es inyectiva: si :math:`f (s, t) = 1` entonces :math:`st = 1`, y entonces :math:`s = t^{− 1} \in S \cap T = {1}`, de donde :math:`(s, t) = (1 , 1)`, que es el elemento de identidad de :math:`S \times T`. Por tanto, el núcleo de :math:`f` es trivial, por lo que :math:`f` es inyectivo, como se afirma. Si también es el caso de que :math:`G = ST`, de modo que cada elemento de :math:`G` es expresable en la forma :math:`st` con :math:`s\in S` y :math:`t\in T`, entonces se deduce que :math:`f` es un isomorfismo de :math:`S \times T` a :math:`G`.


Definición
-------------

Se dice que un grupo :math:`G` es el producto directo interno de :math:`S` y :math:`T` si :math:`S` y :math:`T` son subgrupos de :math:`G` tales que :math:`S\cap T = \{ 1 \}` y :math:`ST = G`, y :math:`st = ts` para todo :math:`s\in S` y :math:`t\in T`.

Si :math:`S` y :math:`T` son subgrupos de :math:`G` tales que :math:`S\cap T = \{ 1 \}` y :math:`G = ST`, entonces la condición adicional de que :math:`st = ts` para todos :math:`s\in S` y :math:`t\in T` es equivalente a la condición de que :math:`S` y :math:`T` son ambos subgrupos normales. Pues suponga que :math:`S` y :math:`T` son ambos normales, y sean :math:`s\in S` y :math:`t\in T`.

- La normalidad de :math:`T` implica que :math:`s^{− 1}ts \in T`, y por tanto :math:`t^{−1}s^{− 1}ts \in T`.

- Por otro lado, la normalidad de :math:`S` implica que :math:`t^{−1}s^{−1}t \in S`, de donde :math:`t^{−1}s^{−1}ts \in S`. Entonces :math:`t^{−1}s^{−1}ts \in S \cap T = \{1\}`, de modo que :math:`t^{−1}s^{−1}ts = 1`, y :math:`ts = st`.

Por el contrario, si asumimos que los elementos de :math:`S` y :math:`T` conmutan entonces para :math:`s\in S` y :math:`t, t_{0}\in T` tenemos que :math:`(st)^{−1}t_{0} (st)^{−1} = t^{−1}s^{−1}t_{0}st = t^{− 1}t_{0}t \in T`. Pero como :math:`G = ST` cada elemento de :math:`G` es expresable en la forma :math:`st`, y se sigue que :math:`g^{−1}tg \in T` para todo :math:`g\in G` y :math:`t_{0} \in T`; es decir, :math:`T` es normal. Del mismo modo, :math:`S` también es normal.

Si un grupo :math:`S` tiene una acción sobre otro grupo :math:`T`, entonces podemos definir un producto semidirecto :math:`S \ltimes T` de :math:`S` y :math:`T` de la siguiente manera. Los elementos de :math:`S \ltimes T` son pares ordenados :math:`(s, t)` (donde :math:`s\in S` y :math:`t\in T`).

La multiplicación de pares ordenados está definida por la regla

.. math::

    (s_{1}, t_{1}) (s_{2}, t_{2}) = (s_{1}s_{2}, t_{1}^{s_{2}}t_{2}).

Se deja como ejercicio para que el alumno demuestre que se satisfacen los axiomas del grupo.

Un grupo :math:`G` es un producto semidirecto interno de sus subgrupos :math:`S` y :math:`T` si :math:`G = ST` y :math:`S \cap T = \{1\}`, y el subgrupo :math:`T` es normal. En estas circunstancias, :math:`S` tiene una acción sobre :math:`T` dada por :math:`t^{s} = s^{−1}ts` para todo :math:`s\in S` y :math:`t\in T`, y ahora es una rutina comprobar que :math:`(s, t) \mapsto st` proporciona un isomorfismo de :math:`S \ltimes T` a :math:`G`.
