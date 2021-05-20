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



Representaciones y representaciones matriciales
-------------------------------------------------

Sean :math:`U` y :math:`V` espacios vectoriales de dimensión finita sobre el campo :math:`\mathbb{F}`, de dimensiones :math:`m` y :math:`n` respectivamente, y sea :math:`f: U \to V` un mapa lineal. Si :math:`\mathcal{B}` es una base de :math:`U` y :math:`\mathcal{C}` una base de :math:`V`, entonces la matriz de :math:`f` relativa a :math:`\mathcal{B}` y :math:`\mathcal{C}` es la matriz :math:`n \times m` :math:`M_{\mathcal{C B}} (f)` cuya entrada :math:`(i, j)` es el escalar :math:`a_{ij}`, donde

.. math:: 
    
    fu_{j} = \sum_{i = 1}^{n} a_{ij}v_{i} \text{ para todo } j = 1, 2, \dots , m,

:math:`u_{1}`, :math:`u_{2}`, :math:`\dots` , siendo um los vectores que componen la base :math:`\mathcal{B}`, y :math:`v_{1}`, :math:`v_{2}`, :math:`\dots`, :math:`v_{n}` los que componen la base :math:`\mathcal{C}`. Los fundamentos de la conexión entre matrices y transformaciones lineales deberían serle familiares a partir del trabajo de :math:`2^{\circ}` año. Los principales hechos son los siguientes. Al multiplicar el vector de coordenadas relativo a :math:`\mathcal{B}` de un elemento :math:`u \in U` por :math:`M_{\mathcal{C B}} (f)` se obtiene el vector de coordenadas relativo a :math:`\mathcal{C}` de :math:`fu \in V`; es decir, si :math:`u = \sum_{j = 1}^{m} \lambda_{j}u_{j}` entonces :math:`fu = \sum_{i = 1}^{n} \lambda_{i}v_{i}`, donde


Si las bases :math:`\mathcal{B}` y :math:`\mathcal{C}` son fijas, el mapeo :math:`f\to M_{\mathcal{C B}} (f)` es una correspondencia biyectiva entre el conjunto de todos los mapas lineales :math:`U \to V` y el conjunto de todas las matrices :math:`n \times m` sobre :math:`\mathbb{F}`. Si :math:`f: U \to V` y :math:`h: V \to W` son ambos mapas lineales, y :math:`\mathcal{D}` es una base del espacio vectorial :math:`W`, entonces :math:`M_{\mathcal{D B}} (hf) = M_{\mathcal{D C}} (h) M_{\mathcal{C B}} (f)`.

Y de manera similar, si :math:`h` y :math:`f` son dos mapas lineales de :math:`U` a :math:`V`, entonces :math:`M_{\mathcal{C B}} (h + f) = M_{\mathcal{C B}} (h) + M_{\mathcal{C B}} (f)`.

En particular tenemos eso

.. math::

    \begin{align}
        M_{\mathcal{C C}}(hf) &= MC C(h)MC C(f)\\
        M_{\mathcal{C C}}(h + f) &= M_{\mathcal{C C}}(h) + M_{\mathcal{C C}}(f)
    \end{align}

para todas las transformaciones lineales :math:`h, f: V \to V`. Dado que la matriz de la transformación lineal identidad es la matriz identidad, de la primera de estas dos ecuaciones se deduce que una transformación lineal :math:`V \to V` es invertible si y solo si su matriz es relativa a :math:`C` es invertible, y deducimos que :math:`f \mapsto M_{\mathcal{C C}} (f)` es un isomorfismo del grupo de todas las transformaciones lineales invertibles en :math:`V` al grupo de todas las matrices :math:`n \times n` invertibles sobre :math:`\mathbb{F}`.

Definición
-----------------

El grupo de todas las transformaciones lineales invertibles en un espacio vectorial V se llama grupo lineal general :math:`GL(V)` del espacio :math:`V`. El grupo de matrices :math:`d \times d` invertibles sobre :math:`\mathbb{F}` se escribe como :math:`GL(d,\mathbb{F})` y se llama el grupo lineal general de grado :math:`d` sobre :math:`\mathbb{F}`.


Hemos definido una representación (lineal) de :math:`G` en :math:`V` como un homomorfismo :math:`\rho : G \to GL (V)`.

De manera similar, una representación matricial de :math:`G` es un homomorfismo :math:`G\to GL(d,\mathbb{F})`; el entero d se llama grado de representación. Si :math:`\rho` es una representación de :math:`G` en un espacio vectorial :math:`V` de dimensión :math:`d`, y si :math:`\mathcal{C}` es una base de :math:`V`, entonces obtenemos una representación matricial de :math:`G` de grado :math:`d` definiendo :math:`Rg = M_{\mathcal{CC}} (\rho g)` para cada :math:`g \in G` El mapa :math:`R:G\to GL(d,\mathbb{F})` es ciertamente un homomorfismo ya que es el compuesto del homomorfismo :math:`g \mapsto \rho g` de :math:`G` a :math:`GL (V)` y el isomorfismo :math:`f \mapsto M_{\mathcal{CC}} (f)` de :math:`GL (V)`a :math:`GL(d,\mathbb{F})`. Por tanto, :math:`R` es una representación matricial, como se afirma. Por el contrario, dada una representación matricial :math:`R:G\to GL(d,\mathbb{F})` podemos obtener una representación :math:`\rho: G \to GL (V)` definiendo :math:`\rho g` como la transformación lineal cuya matriz relativa a :math:`\mathcal{C}` es :math:`Rg`. La moraleja de esta historia es la siguiente: una vez que se fija una base de :math:`V`, una representación de :math:`G` sobre :math:`V` es esencialmente lo mismo que una representación matricial de :math:`G` de grado :math:`d = dim V`.

Dado que la elección de una base para un espacio vectorial es un asunto algo arbitrario, es natural investigar la relación entre dos representaciones matriciales que se derivan de la misma representación :math:`\rho: G \to GL (V)` eligiendo dos bases diferentes. Entonces suponga que :math:`\mathcal{B}` y :math:`\mathcal{C}` son bases de :math:`V`, y sean :math:`R, S:G\to GL(d,\mathbb{F})` definidas por las fórmulas :math:`Rg = M_{\mathcal{CC}} (\rho g)` y :math:`Sg = M_{\mathcal{BB}} (ρg)`, para todo :math:`g \in G`. Si :math:`T = M_{\mathcal{BC}}(id)` entonces encontramos que para todo :math:`g \in G`,

.. math::

    T(Rg) = M_{\mathcal{BC}}(id)M_{\mathcal{CC}}(\rho g) = M_{\mathcal{BC}}((id)(\rho g)) = M_{\mathcal{BC}}((\rho g)(id)) = M_{\mathcal{BB}}(\rho g)M_{\mathcal{BC}}(id) = (Sg)T.

Dado que :math:`M_{\mathcal{BC}}(id) M_{\mathcal{CB}} (id) = M_{\mathcal{BB}}(id) = I`. Similarmente :math:`M_{\mathcal{CB}} (id) M_{\mathcal{BC}} (id) = M_{\mathcal{CC}}(id) = I`, vemos que la matriz :math:`T` es invertible. Por tanto, :math:`Sg = T(Rg) T^{−1}` para todo :math:`g \in G`.

Definición
-----------------

Se dice que las representaciones matriciales :math:`R, S:G\to GL(d,\mathbb{F})` son equivalentes si existe :math:`T \in GL(d,\mathbb{F})` tal que :math:`Sg = T(Rg) T^{−1}` para todo :math:`g \in G`.


Algunas representaciones del grupo simétrico de grado 3
-----------------------------------------------------------------

Sea :math:`\sigma` una permutación de :math:`\{1, 2,\dots , n\}`. Si :math:`V` es un espacio vectorial (sobre cualquier campo :math:`\mathbb{F}`) con base :math:`v_{1}, v_{2},\dots , v_{n}` entonces hay una transformación lineal :math:`p_{\sigma}: V \to V` tal que :math:`v_{i}\mapsto v_{\sigma j}` para cada :math:`j`. Es decir, :math:`p_{\sigma}v_{j} = \sum_{i=1}^{n} \delta_{i\sigma j} v_{i}`. Por tanto, la matriz de :math:`p_{\sigma}` relativa a la base :math:`v_{1}, v_{2},\dots , v_{n}` es la matriz :math:`P_{\sigma}` cuya entrada :math:`(i, j)` es :math:`\delta_{i} \sigma_{j}`. Llamamos :math:`P_{\sigma}` a la matriz de permutación correspondiente a :math:`\sigma`. Es trivial comprobar a partir de la definición que si :math:`\sigma` y :math:`\tau` son permutaciones de :math:`\{1, 2,\dots , n\}` entonces :math:`p_{\sigma \tau} = p_{\sigma}p_{\tau}`: de hecho, para todo :math:`j` tenemos

.. math::

    p_{\sigma \tau}v_{j} = v_{(\sigma \tau)j} = v_{\sigma (\tau j)} = p_{\sigma}(v_{\tau j}) = p_{\sigma}(p_{\tau}v_{j}) = (p_{\sigma}p_{\tau})v_{j},

y como los mapas lineales :math:`p_{\sigma \tau}` y pσpτ tienen el mismo efecto en todos los elementos de la base :math:`v_{1}, v_{2},\dots , v_{n}` se deduce que son iguales. Tenga en cuenta también que si :math:`id` es la permutación de identidad, entonces :math:`p_{id}` es la transformación de identidad de :math:`V`. Por lo tanto, se deduce que :math:`p_{\sigma}` es invertible para todo :math:`\sigma \in S_{n}`, y :math:`p: S_{n} \to GL (V)` definido por :math:`p\sigma = p_{\sigma}` es una representación de :math:`S_{n}`. Según la teoría general que hemos descrito, cualquier elección de una base de :math:`V` da lugar a una representación matricial :math:`S_{n} \to GL (n,\mathbb{F})` correspondiente a la representación :math:`p`. Por supuesto, si tomamos la decisión obvia y usamos la base :math:`v_{1}, v_{2},\dots , v_{n}`, la representación matricial que obtenemos viene dada por :math:`\sigma \mapsto P_{\sigma}`.

Cuando se escribe explícitamente en el caso :math:`n = 3`, la representación matricial que hemos descrito anteriormente es la siguiente:

.. math::

    \begin{align}
        id &\mapsto
        \left(
            \begin{matrix}
                1 & 0 & 0 \\
                0 & 1 & 0 \\
                0 & 0 & 1 
            \end{matrix}
        \right)
        &&&
        (1,3) &\mapsto
        \left(
            \begin{matrix}
                0 & 0 & 1 \\
                0 & 1 & 0 \\
                1 & 0 & 0 
            \end{matrix}
        \right)
        &&&
        (1,2,3) &\mapsto
        \left(
            \begin{matrix}
                0 & 0 & 1 \\
                1 & 0 & 0 \\
                0 & 1 & 0 
            \end{matrix}
        \right)
        \\[0.2cm]
        (1,2) &\mapsto
        \left(
            \begin{matrix}
                0 & 1 & 0 \\
                1 & 0 & 0 \\
                0 & 0 & 1 
            \end{matrix}
        \right)
        &&&
        (2,3) &\mapsto
        \left(
            \begin{matrix}
                1 & 0 & 0 \\
                0 & 0 & 1 \\
                0 & 1 & 0 
            \end{matrix}
        \right)
        &&&
        (1,3,2) &\mapsto
        \left(
            \begin{matrix}
                0 & 1 & 0 \\
                0 & 0 & 1 \\
                1 & 0 & 0 
            \end{matrix}
        \right)
    \end{align}


Dado que :math:`det (AB) = det A det B` siempre que :math:`A` y :math:`B` son matrices :math:`d \times d`, vemos que si :math:`R: g \mapsto Rg` es una representación matricial del grado :math:`d` de cualquier grupo :math:`G`, entonces :math:`g \mapsto det (Rg)` es una representación matricial del grado :math:`1` del grupo :math:`G`. Al aplicar esta observación a la representación anterior de :math:`S_{3}` se obtiene la representación dada por

.. math::

    \begin{align}
        id &\mapsto 1
        &&&
        (1,3) &\mapsto -1
        &&&
        (1,2,3) &\mapsto 1
        \\[0.2cm]
        (1,2) &\mapsto -1
        &&&
        (2,3) &\mapsto -1
        &&&
        (1,3,2) &\mapsto 1
    \end{align}


Esta representación se puede describir alternativamente mediante la regla de que las permutaciones pares se asignan a :math:`1` y las permutaciones impares a :math:`-1`. Hay otra representación aún más obvia de :math:`S_{3}` de grado :math:`1`: está dada por :math:`\sigma \mapsto 1` para todo :math:`\sigma \in S_{3}`. (Por supuesto, esto funciona de la misma manera para cualquier grupo :math:`G`. La representación dada por :math:`g \mapsto 1` para todo :math:`g` se llama la representación :math:`1`, o la representación principal, de :math:`G`).

Haciendo uso de la terminología introducida en la lección :math:`3`, podemos llamar al espacio tridimensional V con base :math:`v_{1}`, :math:`v_{2}`, :math:`v_{3}` un módulo :math:`S_{3}`. La acción :math:`S_{3}` viene dada por :math:`\sigma v_{j} = v_{\sigma j}` para todo :math:`\sigma \in S_{3}` y todo :math:`j \in \{1, 2, 3\}`. Es bastante fácil ver que el subconjunto :math:`U` de :math:`V` definido por

.. math::

    U = \{ \lambda_{1} v_{1} + \lambda_{2}v_{2} + \lambda_{3}v_{3} | \lambda_{1} + \lambda_{2} + \lambda_{3} = 0 \}

es un :math:`S_{3}`-submódulo de :math:`V`. Para probar esto, basta con mostrar que U está cerrado bajo la suma y la multiplicación escalar, y también cerrado bajo la acción de los elementos de :math:`S_{3}`. Esto se deja como ejercicio para el alumno. El alumno también puede comprobar que :math:`u_{1} = v_{1} - v_{2}` y :math:`u_{2} = v_{2} - v_{3}` forman una base para :math:`U`, y las matrices relativas a esta base de las transformaciones de :math:`U` correspondientes a los diversos elementos de :math:`S_{3}` son las siguientes:

.. math::

    \begin{align}
        id &\mapsto
        \left(
            \begin{matrix}
                1 & 0 \\
                0 & 1 
            \end{matrix}
        \right)
        &&&
        (1,3) &\mapsto
        \left(
            \begin{matrix}
                0  & -1 \\
                -1 & 0 
            \end{matrix}
        \right)
        &&&
        (1,2,3) &\mapsto
        \left(
            \begin{matrix}
                0 & -1 \\
                1 & -1  
            \end{matrix}
        \right)
        \\[0.2cm]
        (1,2) &\mapsto
        \left(
            \begin{matrix}
                -1 & 1 \\
                0  & 1  
            \end{matrix}
        \right)
        &&&
        (2,3) &\mapsto
        \left(
            \begin{matrix}
                1 & 0 \\
                1 & -1 
            \end{matrix}
        \right)
        &&&
        (1,3,2) &\mapsto
        \left(
            \begin{matrix}
                -1 & 0 \\
                -1 & 0 
            \end{matrix}
        \right)
    \end{align}



Así hemos obtenido una representación matricial de :math:`S_{3}` de grado :math:`2`.

Supongamos, para mayor precisión, que el campo :math:`\mathbb{F}` (el campo escalar para :math:`V` y el campo de coeficientes para nuestras matrices) es :math:`\mathbb{C}`, el campo de números complejos. Las dos representaciones de :math:`S_{3}` de grado :math:`1` y la representación de :math:`S_{3}` de grado :math:`2` que hemos descrito anteriormente son todas representaciones irreductibles de :math:`S_{3}`, en un sentido que definiremos en breve. Además, resulta que cualquier representación compleja irreducible de :math:`S_{3}` tiene que ser equivalente a una de estas tres. Los principales teoremas de la teoría de la representación que discutiremos en este curso nos dicen en principio cómo una representación compleja arbitraria de un grupo finito :math:`G` puede expresarse en términos de representaciones complejas irreducibles, y cuántas clases de equivalencia de representaciones complejas irreducibles tiene un grupo finito. No existe un método uniforme conocido para construir las representaciones irreductibles de un grupo finito arbitrario y, en consecuencia, el principal problema práctico de la teoría de la representación es encontrar descripciones elegantes de las representaciones irreductibles de varias clases importantes de grupos finitos. En verdad, no hay muchas clases de grupos para los que se haya logrado este objetivo, pero los grupos simétricos constituyen una clase para la que se ha descubierto una teoría completa. Se espera que se describa parte de esta teoría antes del final de este curso.

Centralizers and conjugacy
-------------------------------------------------

Proposición
~~~~~~~~~~~~~~~~~~~~~

Sea :math:`G` un grupo y :math:`g\in G`. Entonces el conjunto :math:`C_{G} (g) = \{x \in G | xg = gx \}` es un subgrupo de :math:`G`.

**Demostración:**

Debemos demostrar que :math:`1 \in C_{G} (g)`, que :math:`x^{-1} \in C_{G} (g)` siempre que :math:`x \in C_{G} (g)`, y que :math:`xy \in C_{G} (g)` siempre que :math:`x, y \in C_{G} (g)`. Todos estos son triviales.

- Dado que la propiedad definitoria del elemento identidad es que :math:`1g` y :math:`g1` son iguales a :math:`g`, tenemos :math:`1g = g1` y, por tanto, :math:`1 \in C_{G} (g)`.

- Si :math:`x \in C_{G} (g)` entonces :math:`xg = gx`, y multiplicar esta ecuación a la izquierda y a la derecha por :math:`x^{−1}` da :math:`gx^{−1} = x^{−1}g`, de donde :math:`x^{-1} \in C_{G} (g)`.

- Si :math:`x, y \in C_{G} (g)` entonces :math:`xg = gx` y :math:`yg = gy`, y vemos que

.. math::

    (xy)g = x(yg) = x(gy) = (xg)y = (gx)y = g(xy),

de donde :math:`xy \in C_{G} (g)`, según se requiera.

Definición
~~~~~~~~~~~~~~~~~~~

El subgrupo :math:`C_{G} (g)` definido en la proposición anterior se denomina centralizador en :math:`G` del elemento :math:`g`.

Recuerde que si :math:`H` es un subgrupo de un grupo :math:`G`, entonces para cada :math:`x\in G` el subconjunto :math:`xH = \{ xh | h \in H \}` se llama una clase lateral izquierda de :math:`H` en :math:`G`.

El mapeo :math:`h \mapsto xh` de :math:`H` a :math:`xH` es una biyección, por lo que el número de elementos de la clase lateral :math:`xH` es el mismo que el número de elementos de :math:`G`. Si :math:`x, y \in G` entonces las clases laterales izquierdas :math:`xH` e :math:`yH` coinciden o son disjuntas. Coinciden si :math:`x \in yH` o (de manera equivalente) si :math:`y \in xH`, o (una tercera condición equivalente) si :math:`x^{−1}y \in H`. Además, cada elemento de :math:`G` se encuentra en alguna clase lateral izquierda de :math:`H`: de hecho, :math:`g \in gH.` De ello se deduce que podemos elegir una transversal izquierda, o sistema de representantes de las clases laterales izquierdas, para el subgrupo :math:`H`. Esta es una familia :math:`(x_{i}) i\in I` de elementos de :math:`G` tal que :math:`G` es la unión disjunta de las clases laterales :math:`x_{i}H` para :math:`i \in I`. Suponiendo que el grupo :math:`G` es finito, entonces, por supuesto, el número de clases laterales izquierdas de :math:`H` también es finito. 

El número de clases laterales izquierdas de :math:`H` en :math:`G` se denomina índice de :math:`H` en :math:`G`, denotado por :math:`[G: H]`. Si :math:`n = [G: H]` entonces una transversal izquierda para :math:`H` constará de :math:`n` elementos :math:`x_{1}`, :math:`x_{2}`,:math:`\dots` , :math:`x_{n}`, y dado que :math:`G = x_{1}H \cup x_{2}H \cup \cdots \cup x_{n}H` expresa :math:`G` como la unión disjunta de :math:`n = [G: H]` conjuntos todos los cuales tienen :math:`|H|` elementos, llegamos a la conclusión de que :math:`|G| = [G: H] |H|`.

Supongamos ahora que :math:`H = C_{G} (g)`, donde :math:`g \in G`. Si :math:`x,y \in G` están en la misma clase lateral izquierda de :math:`H`, entonces :math:`y = xh` para algunos:math:`h\in H`, y

.. math::

    ygy^{−1} = (xh)g(xh)^{−1} = x(hg)h^{−1} x^{−1} = x(gh)h^{−1}x^{−1} = xgx^{−1},

ya que :math:`h` está en el centralizador de :math:`g`. Por tanto, hemos demostrado que :math:`ygy^{−1} = xgx^{−1}` siempre que :math:`x`, :math:`y` están en la misma clase lateral izquierda del centralizador. Por el contrario, si :math:`ygy^{−1} = xgx^{−1}` entonces :math:`(x^{−1}y) g = g (x^{− 1}y)`, de modo que :math:`x^{−1}y \in C_{G} (g)`, y por lo tanto :math:`x` e :math:`y` están en la misma clase lateral del centralizador. Así, los elementos de :math:`G` de la forma :math:`xgx^{−1}` están en correspondencia uno a uno con las clases laterales izquierdas de :math:`C_{G} (g)`: si :math:`x_{1}`, :math:`x_{2}`,:math:`\dots` , :math:`x_{n}` es una transversal izquierda, entonces cada elemento de la forma :math:`xgx^{−1}` es igual a uno u otro de los :math:`n` elementos :math:`x_{i}gx_{i}^{-1}`, y estos elementos son todos distintos (ya que corresponden a clases laterales distintas). Estos elementos de la forma :math:`xgx^{−1}` se denominan conjugados de :math:`g` en :math:`G`; hemos demostrado que el número de conjugados de :math:`G` es igual al índice del centralizador de :math:`g`.