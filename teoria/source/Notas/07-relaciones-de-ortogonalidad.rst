.. role:: underline
    :class: underline

Relaciones de ortogonalidad
============================

Un poco de escepticismo es algo saludable, y sería natural en esta etapa ser un poco escéptico sobre la utilidad del Lema de Schur. Después de todo, solo se puede aplicar si uno tiene un :math:`G`-homomorfismo o una matriz entrelazada para un par de representaciones irreductibles. Y los homomorfismos son cosas muy especiales: puede que no sean fáciles de encontrar. Afortunadamente, el argumento de promediado utilizado en la demostración del teorema de Maschke proporciona (para grupos finitos) un método general para construirlos.

Lema
-------------

Sea :math:`G` un grupo finito, y sean :math:`R`, :math:`S` representaciones matriciales de :math:`G` de grados :math:`n` y :math:`m` respectivamente. Si :math:`X` es cualquier matriz :math:`n \times m`, entonces :math:`Y = \sum_{g\in G} (Rg) X (S (g^{− 1}))` entrelaza :math:`R` y :math:`S`.

**Demostración:**

Para todo :math:`h \in G`,

.. math::

    \begin{align}
        (Rh)Y &= \sum_{g\in G} (Rh)(Rg)X(S(g−1))\\
              &= \sum_{g\in G} (R(hg))X(S(g^{−1}))(S(h−1))(Sh)\\
              &= \left(\sum_{g\in G} (R(hg))X(S(g^{−1}h^{−1})\right) (Sh)\\
              &= \left(\sum_{g\in G} (Rk)X(S(k−1)\right) (Sh)\\
              &= Y(Sh)
    \end{align}

ya que :math:`k = hg` atraviesa todos los elementos de :math:`G` como lo hace :math:`g`. :math:`\blacksquare`

Supongamos ahora que :math:`R^{(1)}`, :math:`R^{(2)}`), :math:`\dots`, :math:`R^{(s)}` son representaciones matriciales irreductibles del grupo finito :math:`G`, de grados :math:`d_{1}`, :math:`d_{2}`, :math:`\dots`, :math:`d_{s}` respectivamente. Suponga además que :math:`R^{(k)}` y :math:`R^{(l)}` no son equivalentes si :math:`k \not = l`. Escriba :math:`R_{ij}^{(k)}g` para la entrada :math:`(i, j)` de :math:`R^{(k)} g`.

Elija :math:`k` y :math:`l` arbitrariamente del conjunto :math:`\{1, 2, \dots, s\}`, y para :math:`1 \leq m \leq d_{k}` y para :math:`1 \leq n \leq d_{l}` sea :math:`X_{m, n}^{(k, l)}` la matriz :math:`d_{k} \times d_{l}` cuya La entrada :math:`(t, u)` es :math:`0` a menos que :math:`t = m` y :math:`u = n`, en cuyo caso es :math:`1`. En otras palabras, la entrada :math:`(t, u)` de :math:`X_{m, n}^{(k, l)}` es :math:`\delta_{tm}\delta_{un}`. El lema anterior nos dice que la matriz

.. math::

    Y_{m,n}^{(k,l)} = \frac{1}{|G|} \sum_{g\in G} (R^{(k)}g)X_{m, n}^{(k, l)}(R^{(l)}(g^{−1}))

entrelaza :math:`R^{(k)}` y :math:`R^{(l)}`. Por lo tanto, según el lema de Schur, :math:`Y_{m,n}^{(k,l)}` es cero si :math:`k \not = l` (dado que las dos representaciones no son equivalentes en este caso), mientras que :math:`Y_{m,n}^{(k,k)}` debe ser un múltiplo escalar de :math:`I`. Por lo tanto, la entrada :math:`(p, q)` de :math:`Y_{m,n}^{(k,l)}` es :math:`\lambda(k, m, n) \delta_{pq}\delta_{kl}` para algunos :math:`\lambda (k, m, n) \in \mathbb{C}`.

Calculando la entrada :math:`(p, q)` de :math:`Y_{m,n}^{(k,l)}` directamente de la definición, encontramos que

.. math::


    \begin{align}
        \lambda(k, m, n) \delta_{pq}\delta_{kl} &= \frac{1}{|G|} \sum_{g\in G} \left(\sum_{t=1}^{d_{k}} \sum_{u=1}^{d_{l}} (R_{pt}^{(k)}g)\delta_{tm}\delta_{un}(R_{uq}^{(l)}(g^{−1}))\right)\\
                                                &= \frac{1}{|G|} \sum_{g\in G} (R_{pm}^{(k)}g)(R_{nq}^{(l)}(g^{−1})).
    \end{align}

Considerando la entrada :math:`(n, m)` de :math:`Y_{q, p}^{(l, k)}` produce por el mismo cálculo (o cambiando el nombre de las variables anteriores) que

.. math::

    \begin{align}
    \lambda (l,q,p)\delta_{nm}\delta_{kl} &= \frac{1}{|G|} \sum_{g\in G} (R_{nq}^{(l)}g)(R_{pm}^{(k)} (g^{−1}))\\
                                          &= \frac{1}{|G|} \sum_{g\in G} (Rnq(l)(g−1))(Rpm(k)g)
    \end{align}

donde en el último paso simplemente hemos cambiado la variable ficticia de suma de :math:`g` a :math:`g^{−1}`. Pero los lados derechos de las dos últimas fórmulas mostradas son iguales, por lo que concluimos que para todos los valores de :math:`k`, :math:`l`, :math:`m`, :math:`n`, :math:`p` y :math:`q`,

.. math::

    \lambda(k,m,n)\delta_{pq}\delta_{kl} = \lambda(l,q,p)\delta_{nm}\delta_{kl}.

Poniendo :math:`q = p` y :math:`l = k` muestra que :math:`\lambda (k, m, n) = \lambda (k, p, p) \delta_{nm}`, y ahora poniendo :math:`m = n` muestra que :math:`\lambda (k, n, n) = \lambda (k, p, p) = \mu_{k}` depende solo de :math:`k` y no de :math:`p` o :math:`n`. Entonces :math:`\lambda (k, m, n) = \mu_{k}\delta_{nm}`.

El cálculo anterior mostró que

.. math::

    \frac{1}{|G|} \sum_{g\in G} (R_{pm}^{(k)} g)(R_{nq}^{(l)} (g^{−1})) = \mu_{k}\delta_{nm}\delta_{pq}\delta_{kl}\hspace{2cm}(1)

donde :math:`R^{(i)}` son representaciones matriciales irreductibles de :math:`G`, de las cuales no hay dos equivalentes. Tenga en cuenta que :math:`k`, :math:`l`, :math:`m`, :math:`n`, :math:`p` y :math:`q` son variables libres: la ecuación es válida para todos sus valores posibles. Por tanto, podemos calcular los valores de los escalares :math:`\mu k` de la siguiente manera. Ponga :math:`l = k` y :math:`m = n`, y sume la Ecuación :math:`(1)` sobre todos los valores de :math:`n` desde :math:`1` hasta :math:`d_{k}` (el grado de :math:`R^{(k)}`. Después de intercambiar el orden de suma en el lado izquierdo obtenemos

.. math::

    \frac{1}{|G|} \sum_{g\in G} \sum_{n=1}^{dk} (R_{pn}^{(k)} g)(R_{nq}^{(k)} (g^{−1})) = \sum_{n =1}^{d_{k}} \mu_{k}\delta_{pq} = \mu_{k}d_{k}\delta_{pq}.

Pero como :math:`(R^{(k)} g) (R^{(k)} (g^{− 1})) = R^{(k)} (gg^{−1}) = R^{(k)} 1 = I` (para todos los valores de :math:`g`) sabemos que

.. math::

    \sum_{n=1}^{dk} (R_{pn}^{(k)} g)(R_{nq}^{(k)} (g^{−1})) = I_{pq} = \delta_{pq},

y nuestra ecuación anterior se reduce a

.. math::

    \frac{1}{|G|} \sum_{g\in G}\delta_{pq} = \mu_{k}d_{k}\delta_{pq}.

Entonces :math:`\mu k = d_{k}^{-1}`, y la Ecuación :math:`(1)` se convierte en

.. math::

    \frac{1}{|G|} \sum_{g\in G}(R_{pm}^{(k)} g)(R_{nq}^{(l)} (g^{−1})) = d_{k}^{1}\delta_{nm}\delta_{pq}\delta_{kl}\hspace{2cm}(2)

Este resultado básico se conoce como *ortogonalidad de funciones coordenadas*.

.. En el Tutorial 1 se demostró que cada representación matricial de un grupo finito es equivalente a una representación unitaria, que por definición es una representación :math:`R` tal que :math:`Rg` es una matriz unitaria para cada :math:`g \in G`.

Definición (Preguntar)
---------------------------------

Se :math:`R` representación matricial de un grupo finito :math:`G`. Se dice que :math:`R` es una representación unitaria si se cumple que que :math:`Rg` es una matriz unitaria para cada :math:`g \in G`.

.. note::

    Recuerde que se dice que una matriz :math:`M` ser unitaria si su transpuesta conjugada es igual a su inversa; es decir, (:math:`\overline{M}^{t}) M = I`. En el caso de que las entradas de :math:`M` sean números reales, esta condición se convierte en :math:`(M^{t}) M = I`, y se dice que la matriz es ortogonal.
    

Repasemos esta prueba antes de continuar.

Dada una representación matricial :math:`R: G \to GL (d, \mathbb{C})` podemos convertir el espacio vectorial complejo :math:`V = \mathbb{C}^{d}` (que consta de todos los vectores de columna de componente :math:`d`) en un :math:`G`-módulo izquierdo definiendo

.. math::

    gv = (Rg)v (\text{ para todo } g \in G \text{ y } v \in V).

El espacio :math:`V` es, por supuesto, un espacio de producto interno en relación con el producto interno estándar o producto escalar.

.. math::

    \begin{align}
        \left(
            \begin{matrix}
                \lambda_{1}\\
                \lambda_{2}\\
                \vdots     \\
                \lambda_{d}
            \end{matrix}
        \right)
        \cdot
        \left(
            \begin{matrix}
                \mu_{1}\\
                \mu_{2}\\
                \vdots     \\
                \mu_{d}
            \end{matrix}
        \right)
        =
        \overline{\lambda}_{1}\mu_{1}\overline{\lambda}_{2}\mu_{2}\cdots\overline{\lambda}_{d}\mu_{d}
    \end{align}


y como en nuestro primer ensayo del teorema de Maschke, podemos obtener un producto interno :math:`G`-invariante en :math:`V` definiendo

.. math::

    v \ast u = \sum_{g\in G} (gv) \cdot (gu) (\text{ para todo }g \in G \text{ y } v, u \in V).

Ahora elija una base :math:`v_{1}`, :math:`v_{2}`, :math:`\dots` , :math:`v_{d}` de :math:`V` que es ortonormal en relación con este nuevo producto interno, y sea :math:`S` la representación matricial de :math:`G` que produce esta nueva base de :math:`V`. Es decir,

.. math::

    gv_{j} = \sum_{i=1}^{d} (Sg)_{ij}v_{i}

para todo :math:`g\in G` y :math:`j \in \{1, 2,\dots , d\}`. La representación :math:`S` es entonces equivalente a la representación R; de hecho, :math:`Sg = T^{−1} (Rg) T` (para todo :math:`g\in G`), donde :math:`T` es la matriz de transición para cambiar las coordenadas relativas a :math:`v_{1}`, :math:`v_{2}`, :math:`\dots` , :math:`v_{d}` en coordenadas estándar. Específicamente, la :math:`j`-ésima columna de :math:`T` es simplemente el vector de columna :math:`v_{j}`. Además, :math:`S` es una representación unitaria. Para ver esto, observe que la invariancia :math:`G` de :math:`\ast` produce (por definición) que :math:`(gv) \ast (gu) = v \ast u` para todo :math:`u`, :math:`v \in V`, y ahora desde la base :math:`v_{1}`, :math:`v_{2}`, :math:`\dots` , :math:`v_{d}` es ortonormal

.. math::
    
    \begin{align}
        \delta_{jk} &= v_{j} \ast v_{k} = (gv_{j}) \ast (gv_{k})                                                 \\
               &= \left(\sum_{i=1}^{d} (Sg)_{ij}v_{i}\right)\ast \left(\sum_{m=1}^{d} (Sg)_{mk}v_{m} \right) \\
               &= \sum_{i=1}^{d} \sum_{m=1}^{d} \overline{Sg_{ij}}(Sg)_{mk}(v_{i} \ast v_{m})                \\
               &= \sum_{i=1}^{d} \sum_{m=1}^{d} \overline{Sg_{ij}}(Sg)_{mk}\delta_{im}                       \\
               &= \sum_{i=1}^{d} \overline{Sg_{ij}}(Sg)_{ik}                                                 \\
               &= \sum_{i=1}^{d} (\overline{Sg}^{t})_{ji}(Sg)_{ik}
    \end{align}

para todo :math:`j` y :math:`k` y todo :math:`g\in G`. Esto muestra que :math:`\overline{Sg}^{t} Sg = I` para todo :math:`g\in G`, como se requiere.

Volviendo a la Ecuación :math:`(2)`, supongamos ahora que todas las representaciones :math:`R^{(i)}` son unitarias. Entonces para todo :math:`g\in G` y todo :math:`l`,

.. math::

    R^{(l)} (g^{−1}) = (R^{(l)} g)^{−1} = \overline{R(l) g}^{t},
    
y entonces :math:`R_{nq}^{(l)}(g^{−1}) = \overline{R_{qn}^{(l)}g}`. Por tanto, la Ecuación :math:`(2)` se convierte en

.. math::

    \frac{1}{|G|} \sum_{g\in G} (R_{pm}^{(k)}g)R_{qn}^{(l)}g = d_{k}^{-1}\delta_{nm}\delta_{pq}\delta_{kl}.\hspace{2cm}  (3)

Tabular los valores de la función :math:`R_{pm}{(k)}: G \to \mathbb{C}` da un vector fila (llamémoslo temporalmente :math:`x_{kpm}`) que tiene una entrada para cada elemento de :math:`G`. La Ecuación :math:`(3)` nos dice que el producto escalar estándar de :math:`x_{kpm}` y :math:`x_{lqn}` es cero a menos que :math:`k`, :math:`p` y :math:`m` sean (respectivamente) iguales a :math:`l`, :math:`q` y :math:`n`, en cuyo caso el producto escalar es :math:`|G|/d_{k}`. Para cada valor de :math:`k` hay :math:`d_{k}^{2}` posibilidades para el par ordenado :math:`(p, m)` (ya que :math:`p`, :math:`m \in \{1, 2,\dots, d_{k} \}`), por lo que tenemos :math:`\sum_{k = 1}^{s}= d_{k}^{2}` vectores :math:`x_{kpm}` en total. Estos vectores son linealmente independientes ya que son distintos de cero y ortogonales por pares, por lo que abarcan un espacio de dimensión :math:`\sum_{k = 1}^{s}= d_{k}^{2}`. Como están contenidos en el espacio :math:`|G|`-dimensional de los vectores fila con :math:`|G|` componentes, concluimos que

.. math::

    \sum_{k =1}^{2} d_{k}^{2} \leq |G|\hspace{2cm} (4)

siempre que :math:`G` tenga representaciones mutuamente desiguales de grados :math:`d_{1}`, :math:`d_{2}`, :math:`\dots` , :math:`d_{s}`. Por lo tanto, :math:`s \leq | G |`, ya que cada :math:`d_{k}` es al menos :math:`1`, y esto muestra que ningún grupo :math:`G` puede tener más de :math:`|G|` representaciones irreductibles mutuamente desiguales. En particular, hasta la equivalencia, el número de representaciones complejas irreductibles de un grupo finito es finito. (De hecho, como mostraremos en unas pocas conferencias, la igualdad siempre se mantiene en :math:`(4)`).


Ilustremos el resultado anterior para el grupo :math:`G = S_{3}`. Conocemos tres representaciones irreductibles mutuamente desiguales, de grados :math:`1`, :math:`1` y :math:`2`. La suma de los cuadrados de estos grados es :math:`6`, que es igual al orden de :math:`S_{3}`; entonces, en vista de la desigualdad :math:`(4)`, no puede haber una cuarta representación irreductible que no sea equivalente a una de estas tres. Las representaciones de grado :math:`1` son necesariamente unitarias (para un grupo finito), ya que por un lado la representación tiene que ser equivalente a una representación unitaria (ver arriba), y por otro lado una representación de grado :math:`1` no puede ser equivalente a nada más que sí mismo, ya que las matrices :math:`1 \times 1` conmutan. Si identificamos :math:`S_{3}` con el grupo de simetrías de un triángulo equilátero, y coordinamos el plano euclidiano tomando el centroide del triángulo como origen y la recta que pasa por el origen y uno de los vértices como eje :math:`x`, obtenemos un representación de :math:`S_{3}` mediante matrices ortogonales reales. Ahora es muy sencillo calcular los valores de las funciones de coordenadas de nuestras tres representaciones irreducibles y obtener la siguiente tabla.


+------------------------+------------+--------------------+---------------------+----------------+---------------------+---------------------+
| :math:`g`              | :math:`id` | :math:`(1, 2)`     | :math:`(1, 3)`      | :math:`(2, 3)` | :math:`(1, 2, 3)`   | :math:`(1,3, 2)`    |
+========================+============+====================+=====================+================+=====================+=====================+
| :math:`R_{11}^{(1)} g` | :math:`1`  | :math:`1`          | :math:`1`           | :math:`1`      | :math:`1`           | :math:`1`           |
+------------------------+------------+--------------------+---------------------+----------------+---------------------+---------------------+
| :math:`R_{11}^{(2)} g` | :math:`1`  | :math:`-1`         | :math:`-1`          | :math:`-1`     | :math:`1`           | :math:`1`           |
+------------------------+------------+--------------------+---------------------+----------------+---------------------+---------------------+
| :math:`R_{11}^{(3)} g` | :math:`1`  | :math:`-1/2`       | :math:`-1/2`        | :math:`1`      | :math:`-1/2`        | :math:`-1/2`        |
+------------------------+------------+--------------------+---------------------+----------------+---------------------+---------------------+
| :math:`R_{12}^{(3)} g` | :math:`0`  | :math:`\sqrt{3}/2` | :math:`-\sqrt{3}/2` | :math:`0`      | :math:`-\sqrt{3}/2` | :math:`\sqrt{3}/2`  |
+------------------------+------------+--------------------+---------------------+----------------+---------------------+---------------------+
| :math:`R_{21}^{(3)} g` | :math:`0`  | :math:`\sqrt{3}/2` | :math:`-\sqrt{3}/2` | :math:`0`      | :math:`\sqrt{3}/2`  | :math:`-\sqrt{3}/2` |
+------------------------+------------+--------------------+---------------------+----------------+---------------------+---------------------+
| :math:`R_{22}^{(3)} g` | :math:`1`  | :math:`1/2`        | :math:`1/2`         | :math:`-1`     | :math:`-1/2`        | :math:`-1/2`        |
+------------------------+------------+--------------------+---------------------+----------------+---------------------+---------------------+

Aquí, por ejemplo, las últimas cuatro entradas de la segunda columna dicen que la matriz :math:`R^{(3)} (1, 2)` es :math:`\left(\begin{matrix}-1/2 & \sqrt{3}/2\\ \sqrt{3}/2 & 1/2 \end{matrix}\right)`, que es la matriz de la reflexión en el línea que pasa por el origen con pendiente :math:`tan (\pi / 3)`. (Los vértices :math:`1`, :math:`2` y :math:`3` del triángulo son, respectivamente, los puntos con coordenadas :math:`\left(\begin{matrix} x \\ y \end{matrix}\right)` y dadas por :math:`\left(\begin{matrix} 1 \\ 0 \end{matrix}\right)`, :math:`\left(\begin{matrix} -1/2 \\ \sqrt{3}/2 \end{matrix}\right)` y :math:`\left(\begin{matrix} -1/2 \\ -\sqrt{3}/2 \end{matrix}\right)` respectivamente.

Al interpretar los valores de la tabla anterior como las entradas de una matriz de :math:`6 \times 6`, podemos comprobar fácilmente que el producto escalar de dos filas distintas de la matriz es :math:`0`, mientras que el producto escalar de una fila consigo misma es seis (para la primera dos filas) o tres (para las últimas cuatro filas). En general, Ecuación :math:`(2)` dice que la tabla de valores de las funciones de coordenadas es una matriz cuyas filas son mutuamente ortogonales, la longitud de cada fila viene dada por :math:`\sqrt{d / | G |}`, donde :math:`d` es el grado de la representación relevante.

Dividiendo cada fila por su longitud se obtiene una matriz :math:`T (G)` cuyas filas forman un conjunto ortonormal de vectores; las filas de :math:`T (G)` están indexadas por triples :math:`\{(k, p, m) | 1 \leq k \leq s \text{ y } p, m \in \{1, 2,\dots , d_{k}\}\}` y las columnas por elementos de :math:`G`, siendo la :math:`((k, p, m), g)` entrada :math:`\sqrt{d / | G |} R_{p, m}^{(k)} g`. Para :math:`S_{3}` encontramos que

.. math::

    T(S_{3}) =
        \left(
            \begin{matrix}
                1/\sqrt{6}   &1/\sqrt{6}     &1/\sqrt{6}   &1/\sqrt{6}   &1/\sqrt{6}    &1/\sqrt{6}   \\
                1/\sqrt{6}   &−1/\sqrt{6}    &−1/\sqrt{6}  &−1/\sqrt{6}  &1/\sqrt{6}    &1/\sqrt{6}   \\
                1/\sqrt{3}   &−1/2\sqrt{3}   &−1/2\sqrt{3} &1/\sqrt{3}   &−1/2\sqrt{3}  &−1/2\sqrt{3} \\
                0            &1/2            &−1/2         &0            &−1/2          &1/2          \\
                0            &1/2            &−1/2         &0            &1/2           &−1/2         \\
                1/\sqrt{3}   &1/2\sqrt{3}    &1/2\sqrt{3}  &−1/\sqrt{3}  &−1/2\sqrt{3}  &−1/2\sqrt{3} \\
            \end{matrix}
        \right),

que es unitario —ortogonal, de hecho, ya que es real— como se puede comprobar fácilmente.

Una matriz cuadrada :math:`M` es unitaria si y solo si sus columnas forman un conjunto ortonormal de vectores, ya que esta condición es claramente equivalente a la ecuación matricial :math:`(\overline{M}^{t}) M = I`. Dado que esta a su vez es equivalente a :math:`M (\overline{M}^{t}) = I`, que dice que las filas forman un conjunto ortonormal, concluimos que las filas de una matriz cuadrada son ortonormales si y solo si las columnas también lo son. Dado que la igualdad se cumple en :math:`(4)`, de modo que :math:`T (G)` es cuadrado, la ortogonalidad de la columna nos dice que para todo :math:`g`, :math:`h \in G`

.. math::

    \frac{1}{|G|}\sum_{k ,p,m} {d_{k}} \left( \overline{R_{pm}^{(k)} g} \right) (R_{pm}^{(k)} h) = \delta_{gh}.

(Esto es equivalente a la Ecuación :math:`(2)`, pero mucho menos importante en la práctica).