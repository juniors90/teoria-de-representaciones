.. role:: underline
    :class: underline

La Representación Regular
============================


Si un grupo :math:`G` tiene una acción izquierda en un conjunto :math:`S`, entonces asociado con cada :math:`g \in G` es una permutación :math:`\sigma_{g}: S \to S` definida por :math:`\sigma_{g}s = gs` para todo :math:`s \in S`. Además, :math:`g \mapsto \sigma_{g}` es un homomorfismo de :math:`G` a el grupo de todas las permutaciones de :math:`S`. También hemos visto que las permutaciones pueden asociarse con matrices de permutaciones. Si :math:`S = \{s_{1}, s_{2}, \dots, s_{d}\}` obtenemos así un homomorfismo :math:`g \mapsto R_g` de :math:`G` al grupo de todas las matrices de permutación :math:`d \times d`, donde la entrada :math:`(i, j)` de :math:`R_g` es :math:`1` si :math:`v_{i} = gv_{j}` y :math:`0` en caso contrario.* En otras palabras , una representación de permutación se convierte en una representación de matriz si uno identifica permutaciones con matrices de permutación. (El :math:`G`-módulo G asociado con esta representación matricial es un espacio vectorial con base en correspondencia biyectiva con los elementos de :math:`S`, actuando los elementos de :math:`G` mediante transformaciones lineales que permutan esta base).

Si consideramos en particular la acción de multiplicación por la izquierda del grupo :math:`G` sobre sí mismo, obtenemos una representación de :math:`G` por :math:`| G | \times | G |` matrices de permutación. Las matrices precisas dependen de un orden elegido de los elementos de :math:`G`. Ilustremos lo que sucede para el grupo :math:`S_{3}`, usando el mismo orden de los elementos que usamos en la tabla de multiplicar dada en la Clase 1:

.. math::

    \begin{align}
        g_{1} &= id, & g_{2} &= ( 1, 2, 3), & g_{3} &= (1, 3, 2), & g_{4} &= (1, 2), & g_{5} &= (1, 3), & g_{6} &= (2, 3).
    \end{align}

La multiplicación por la izquierda por :math:`(1, 2)` intercambia :math:`g_{1}` y :math:`g_{4}` (ya que :math:`(1, 2) id = (1, 2)` y :math:`(1, 2) (1, 2) = id`), y también intercambia los pares :math:`g_{2}`, :math:`g_{6}` y :math:`g_{3}`, :math:`g_{5}`. La matriz que representa :math:`(1, 2)` resulta ser

.. math::

    R(1, 2) =
        \left(
            \begin{matrix}
                0 & 0 & 0 & 1 & 0 & 0 \\
                0 & 0 & 0 & 0 & 0 & 1 \\
                0 & 0 & 0 & 0 & 1 & 0 \\
                1 & 0 & 0 & 0 & 0 & 0 \\
                0 & 0 & 1 & 0 & 0 & 0 \\
                0 & 1 & 0 & 0 & 0 & 0
            \end{matrix}
        \right)


Similarmente

.. math::

    \begin{align}
        R(2, 3) &=
            \left(
                \begin{matrix}
                    0 & 0 & 0 & 0 & 0 & 1 \\
                    0 & 0 & 0 & 0 & 1 & 0 \\
                    0 & 0 & 0 & 1 & 0 & 0 \\
                    0 & 0 & 1 & 0 & 0 & 0 \\
                    0 & 1 & 0 & 0 & 0 & 0 \\
                    1 & 0 & 0 & 0 & 0 & 0
                \end{matrix}
            \right)
        &&&
        R(1, 2, 3) &=
            \left(
                \begin{matrix}
                    0 & 0 & 1 & 0 & 0 & 0 \\
                    1 & 0 & 0 & 0 & 0 & 0 \\
                    0 & 1 & 0 & 0 & 0 & 0 \\
                    0 & 0 & 0 & 0 & 0 & 1 \\
                    0 & 0 & 0 & 1 & 0 & 0 \\
                    0 & 0 & 0 & 0 & 1 & 0
                \end{matrix}
            \right)
    \end{align}


.. note::

    En el caso de una acción correcta de :math:`G` sobre :math:`S`, la matriz de permutación asociada con :math:`g \in G` debe tener :math:`(i, j)`-entrada :math:`1` si :math:`v_{i}g = v_{j}` y :math:`0` en caso contrario, para asegurar que :math:`R(gh)` sea igual a :math:`(R_g)(Rh)` en lugar de :math:`(Rh)(R_g)`.


Los demás son igualmente fáciles de calcular.

La representación :math:`R: G \to GL (|G|,\mathbb{C})` construida de esta manera se llama la representación regular de :math:`G`. En vista del Teorema de Maschke es posible encontrar una matriz :math:`T`; más bien, debería decir que existe una matriz :math:`T`, ya que no está claro cómo encontrar uno, de modo que


.. math::

    T^{−1}(R_g)T =
        \left(
            \begin{matrix}
                S_{1}g & 0      & 0      & \cdots & 0      \\
                0      & S_{2}g & 0      & \cdots & 0      \\
                0      & 0      & S_{3}g & \cdots & 0      \\
                \vdots & \vdots & \vdots &        & \vdots \\
                0      & 0      & 0      & \cdots & S_{m}g
            \end{matrix}
        \right) \hspace{2cm}(1)

donde :math:`S_{1}`, :math:`S_{2}`, :math:`\dots`, :math:`S_{m}` son algunas representaciones irreductibles de :math:`G`. Nótese que el orden en el que los irreducibles Si ocurren como sumandos diagonales se puede variar alterando la matriz :math:`T`. Por ejemplo, :math:`S_{1}` y :math:`S_{2}` pueden intercambiarse ya que

.. math::

        \left(
            \begin{matrix}
                0      & I      & \cdots & 0      \\
                I      & 0      & \cdots & 0      \\
                \vdots & \vdots &        & \vdots \\
                0      & 0      & \cdots & I
            \end{matrix}
        \right)
        \left(
            \begin{matrix}
                S_{1}g & 0      & \cdots & 0      \\
                0      & S_{2}g & \cdots & 0      \\
                \vdots & \vdots &        & \vdots \\
                0      & 0      & \cdots & S_{m}g
            \end{matrix}
        \right)
        \left(
            \begin{matrix}
                0      & I      & \cdots & 0      \\
                I      & 0      & \cdots & 0      \\
                \vdots & \vdots &        & \vdots \\
                0      & 0      & \cdots & I
            \end{matrix}
        \right)
        = 
        \left(
            \begin{matrix}
                S_{1}g & 0      & \cdots & 0      \\
                0      & S_{2}g & \cdots & 0      \\
                \vdots & \vdots &        & \vdots \\
                0      & 0      & \cdots & S_{m}g
            \end{matrix}
        \right)

y claramente una secuencia de operaciones similares puede producir cualquier orden deseado de los sumandos diagonales. Además, cada Si puede ser reemplazado por cualquier representación a la que sea equivalente: por ejemplo, si :math:`S_{1}' g = X^{−1}(S_{1}g) X` entonces


.. math::

        \left(
            \begin{matrix}
                X      & 0      & \cdots & 0      \\
                0      & I      & \cdots & 0      \\
                \vdots & \vdots &        & \vdots \\
                0      & 0      & \cdots & I
            \end{matrix}
        \right)^{-1}
        \left(
            \begin{matrix}
                S_{1}g & 0      & \cdots & 0      \\
                0      & S_{2}g & \cdots & 0      \\
                \vdots & \vdots &        & \vdots \\
                0      & 0      & \cdots & S_{m}g
            \end{matrix}
        \right)
        \left(
            \begin{matrix}
                X      & 0      & \cdots & 0      \\
                0      & I      & \cdots & 0      \\
                \vdots & \vdots &        & \vdots \\
                0      & 0      & \cdots & I
            \end{matrix}
        \right)
        = 
        \left(
            \begin{matrix}
                S_{1}'g & 0      & \cdots & 0      \\
                0      & S_{2}g & \cdots & 0      \\
                \vdots & \vdots &        & \vdots \\
                0      & 0      & \cdots & S_{m}g
            \end{matrix}
        \right)


para todo :math:`g \in G`. Entonces, si elegimos representaciones irreducibles :math:`R^{(1)}`, :math:`R^{(2)}`, :math:`\dots`, :math:`R^{(s)}` tal que toda representación irreducible de :math:`G` es equivalente a una de las :math:`R^{(k)}`, entonces podemos suponer que cada :math:`S_{j}` en la Ecuación :math:`(1)` anterior coincide con algunos :math:`R^{(k)}`. Por supuesto, una :math:`R^{(k)}` dada podría posiblemente ocurrir varias veces. Para que podamos aplicar las fórmulas de la lección :math:`9`, asumiremos que las :math:`R^{(k)}` son unitarias y mutuamente desiguales. Como veremos pronto, resulta que cada :math:`R^{(k)}` ocurre :math:`d_{k}` veces como un sumando diagonal en la Ecuación :math:`(1)`. Esto significa que el grado de representación del lado derecho en la Ecuación :math:`(1)` es :math:`\sum_{k} d_{k}^{2}` (ya que para cada :math:`k` hay :math:`d_{k}` sumandos de grado :math:`d_{k}`). Como ya se mencionó, esto es igual a :math:`|G|`, que es el grado de representación en el lado izquierdo de la Ecuación :math:`(1)`.