.. role:: underline
    :class: underline
    
Representación matricial
========================

Sean :math:`U` y :math:`V` espacios vectoriales de dimensión finita sobre el cuerpo :math:`\mathbb{F}`, de dimensiones :math:`m` y :math:`n` respectivamente, y sea :math:`f: U \to V` un mapa lineal. Si :math:`\mathcal{B}` es una base de :math:`U` y :math:`\mathcal{C}` una base de :math:`V`, entonces la matriz de :math:`f` relativa a :math:`\mathcal{B}` y :math:`\mathcal{C}` es la matriz :math:`M_{\mathcal{C B}} (f)` de orden :math:`n \times m` cuya entrada :math:`(i, j)` es el escalar :math:`a_{ij}`, donde

.. math:: 
    
    f(u_{j}) = \sum_{i = 1}^{n} a_{ij}v_{i} \text{ para todo } j = 1, 2, \dots , m,

tales que :math:`\mathcal{B}=\{u_{1}, u_{2}, \dots, u_{m} \}` y :math:`\mathcal{C} = \{v_{1}, v_{2}, \dots, v_{n}\}`.


- El grupo de todas las transformaciones lineales invertibles en un espacio vectorial :math:`V` se llama grupo lineal general :math:`GL(V)` del espacio :math:`V`.

- El grupo de matrices :math:`d \times d` invertibles sobre :math:`\mathbb{F}` se escribe como :math:`GL(d,\mathbb{F})` y se llama el grupo lineal general de grado :math:`d` sobre :math:`\mathbb{F}`.


Hemos definido una representación (lineal) de :math:`G` en :math:`V` como un homomorfismo :math:`\rho : G \to GL (V)`. Ahora pasamos a definir una *representación matricial* de :math:`G` en :math:`V`.

.. _representacion-matricial:

Representación matricial
--------------------------

Una representación matricial de :math:`G` es un homomorfismo :math:`G\to GL(d,\mathbb{F})`. El entero :math:`d` se llama grado de representación.

Si :math:`\rho` es una representación de :math:`G` en un espacio vectorial :math:`V` de dimensión :math:`d`, y si :math:`\mathcal{C}` es una base de :math:`V`, entonces obtenemos una representación matricial de :math:`G` de grado :math:`d` definiendo :math:`R_g = M_{\mathcal{CC}} (\rho_g)` para cada :math:`g \in G`.

El mapa :math:`R:G\to GL(d,\mathbb{F})` es ciertamente un homomorfismo ya que es la composición del homomorfismo :math:`g \mapsto \rho_g` de :math:`G` a :math:`GL (V)` y el isomorfismo :math:`f \mapsto M_{\mathcal{CC}} (f)` de :math:`GL (V)`a :math:`GL(d,\mathbb{F})`. Por tanto, :math:`R` es una representación matricial, como se afirma.

Recíprocamente, dada una representación matricial :math:`R:G\to GL(d,\mathbb{F})` podemos obtener una representación :math:`\rho: G \to GL (V)` definiendo :math:`\rho_g` como la transformación lineal cuya matriz relativa a :math:`\mathcal{C}` es :math:`R_g`.

.. Cambiar Nota por "La moraleja de esta historia es la siguiente:" 

.. note::

    Una vez que se fija una base de :math:`V`, una representación de :math:`G` sobre :math:`V` es esencialmente lo mismo que una representación matricial de :math:`G` de grado :math:`d = dim V`.

.. _representaciones-matriciales-equivalentes:

Representaciones matriciales equivalentes
-------------------------------------------

Dado que la elección de una base para un espacio vectorial es un asunto algo arbitrario, es natural investigar la relación entre dos representaciones matriciales que se derivan de la misma representación :math:`\rho: G \to GL (V)` eligiendo dos bases diferentes. Entonces suponga que :math:`\mathcal{B}` y :math:`\mathcal{C}` son bases de :math:`V`, y sean :math:`R, S:G\to GL(d,\mathbb{F})` definidas por las fórmulas :math:`R_g = M_{\mathcal{CC}} (\rho_g)` y :math:`S_g = M_{\mathcal{BB}} (\rho_g)`, para todo :math:`g \in G`. Si :math:`T = M_{\mathcal{BC}}(id)` entonces encontramos que para todo :math:`g \in G`,

.. math::

    \begin{align}
        T(R_g) &= M_{\mathcal{BC}}(id)M_{\mathcal{CC}}(\rho_g)  \\
              &= M_{\mathcal{BC}}(id(\rho_g))                \\
              &= M_{\mathcal{BC}}((\rho_g) id)                \\
              &= M_{\mathcal{BB}}(\rho_g) M_{\mathcal{BC}}(id)  \\
              &= (S_g)T.
    \end{align}

Dado que

.. math::

    \begin{align}
        M_{\mathcal{BC}}(id) M_{\mathcal{CB}} (id) &= M_{\mathcal{BB}}(id) = I&\text{y}&&M_{\mathcal{CB}} (id) M_{\mathcal{BC}} (id) &= M_{\mathcal{CC}}(id) = I,
    \end{align}
    
vemos que la matriz :math:`T` es invertible. Por tanto, :math:`S_g = T(R_g) T^{−1}` para todo :math:`g \in G`.

.. _definicion-de-representaciones-matriciales-equivalente:

Definición
~~~~~~~~~~~

Se dice que las representaciones matriciales :math:`R, S:G\to GL(d,\mathbb{F})` son equivalentes si existe :math:`T \in GL(d,\mathbb{F})` tal que :math:`S_g = T(R_g) T^{−1}` para todo :math:`g \in G`.


Algunas representaciones del grupo simétrico de grado 3
-----------------------------------------------------------------

Sea :math:`\sigma` una permutación de :math:`\{1, 2,\dots , n\}`. Si :math:`V` es un espacio vectorial (sobre cualquier cuerpo :math:`\mathbb{F}`) con base :math:`v_{1}, v_{2},\dots , v_{n}` entonces hay una transformación lineal :math:`p_{\sigma}: V \to V` tal que :math:`v_{i}\mapsto v_{\sigma j}` para cada :math:`j`. Es decir, :math:`p_{\sigma}v_{j} = \sum_{i=1}^{n} \delta_{i\sigma j} v_{i}`. Por tanto, la matriz de :math:`p_{\sigma}` relativa a la base :math:`v_{1}, v_{2},\dots , v_{n}` es la matriz :math:`P_{\sigma}` cuya entrada :math:`(i, j)` es :math:`\delta_{i} \sigma_{j}`. Llamamos :math:`P_{\sigma}` a la matriz de permutación correspondiente a :math:`\sigma`. Es trivial comprobar a partir de la definición que si :math:`\sigma` y :math:`\tau` son permutaciones de :math:`\{1, 2,\dots , n\}` entonces :math:`p_{\sigma \tau} = p_{\sigma}p_{\tau}`: de hecho, para todo :math:`j` tenemos

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


Dado que :math:`det (AB) = det A det B` siempre que :math:`A` y :math:`B` son matrices :math:`d \times d`, vemos que si :math:`R: g \mapsto R_g` es una representación matricial del grado :math:`d` de cualquier grupo :math:`G`, entonces :math:`g \mapsto det (R_g)` es una representación matricial del grado :math:`1` del grupo :math:`G`. Al aplicar esta observación a la representación anterior de :math:`S_{3}` se obtiene la representación dada por

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

Supongamos, para mayor precisión, que el cuerpo :math:`\mathbb{F}` (el cuerpo escalar para :math:`V` y el cuerpo de coeficientes para nuestras matrices) es :math:`\mathbb{C}`, el cuerpo de números complejos. Las dos representaciones de :math:`S_{3}` de grado :math:`1` y la representación de :math:`S_{3}` de grado :math:`2` que hemos descrito anteriormente son todas representaciones irreductibles de :math:`S_{3}`, en un sentido que definiremos en breve. Además, resulta que cualquier representación compleja irreducible de :math:`S_{3}` tiene que ser equivalente a una de estas tres. Los principales teoremas de la teoría de la representación que discutiremos en este curso nos dicen en principio cómo una representación compleja arbitraria de un grupo finito :math:`G` puede expresarse en términos de representaciones complejas irreducibles, y cuántas clases de equivalencia de representaciones complejas irreducibles tiene un grupo finito. No existe un método uniforme conocido para construir las representaciones irreductibles de un grupo finito arbitrario y, en consecuencia, el principal problema práctico de la teoría de la representación es encontrar descripciones elegantes de las representaciones irreductibles de varias clases importantes de grupos finitos. En verdad, no hay muchas clases de grupos para los que se haya logrado este objetivo, pero los grupos simétricos constituyen una clase para la que se ha descubierto una teoría completa. Se espera que se describa parte de esta teoría antes del final de este curso.

