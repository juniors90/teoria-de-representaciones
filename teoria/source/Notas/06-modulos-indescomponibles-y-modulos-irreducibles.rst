Módulos Indescomponibles y Módulos Irreducibles
===============================================

.. note::

    - se dice que un espacio vectorial :math:`V` es la suma directa interna de sus subespacios :math:`X` e :math:`Y` si cada elemento de :math:`V` es expresable de forma única en la forma :math:`x + y` con :math:`x \in X` e :math:`y \in Y`. A esto lo llamamos una descomposición directa de :math:`V`, y escribimos :math:`V = X \oplus Y`.
    - se dice que :math:`X` e :math:`Y` son subespacios complementarios de :math:`V`. Se ve fácilmente que si :math:`V = X \oplus Y` entonces :math:`V / X \simeq Y`, un isomorfismo :math:`Y \to V / X` dado por :math:`y \mapsto y + X` para todo :math:`y \in Y`. (El símbolo ":math:`\simeq`" significa "es isomorfo a".)

En términos de bases, una descomposición directa de un espacio vectorial equivale a dividir una base en dos partes; por tanto, si :math:`V = X \oplus Y` entonces si :math:`x_{1}`, :math:`x_{2}`, :math:`\dots` , :math:`x_{n}` es una base de :math:`X` e :math:`y_{1}`, :math:`y_{2}`, :math:`\dots`, :math:`y_{n}` es una base de :math:`Y`  entonces :math:`x_{1}`, :math:`x_{2}`, :math:`\dots` , :math:`x_{n}`, :math:`y_{1}`, :math:`y_{2}`, :math:`\dots`, :math:`y_{n}` es una base de :math:`V`. Es un teorema básico de la teoría del espacio vectorial que una base de un subespacio siempre puede extenderse a una base de :math:`V`. Por lo tanto, si :math:`X` es un subespacio de :math:`V` y :math:`x_{1}`, :math:`x_{2}`, :math:`\dots` , :math:`x_{n}` es una base de :math:`X`, entonces existen :math:`x_{n + 1}`, :math:`x_{n + 2}`, :math:`\dots`, :math:`x_{d}` tal que :math:`x_{1}`, :math:`x_{2}`, :math:`\dots` , :math:`x_{d}` es una base de :math:`V`. El subespacio :math:`Y` de :math:`V` que está generado por :math:`x_{n + 1}`, :math:`x_{n + 2}`, :math:`\dots` , :math:`x_{d}` es entonces complementario de :math:`X`, y obtenemos el hecho importante de que para cada subespacio :math:`X` de un espacio vectorial :math:`V` hay un subespacio :math:`Y` de :math:`V` tal que :math:`V = X \oplus Y`. De hecho, generalmente hay muchos subespacios :math:`Y` que complementan un :math:`X` dado.

El concepto de descomposición directa se generaliza fácilmente a los :math:`G`-módulos. Un :math:`G`-módulo V es la suma directa del módulo :math:`G` de :math:`X` e :math:`Y` si :math:`X` e :math:`Y` son :math:`G`-submódulos de :math:`V` y :math:`V = X \oplus Y` como espacios vectoriales.

Si :math:`V = X \oplus Y` (donde :math:`X` e :math:`Y` son :math:`G`-submódulos) entonces :math:`Y \simeq_{G} V / X`, donde hemos adjuntado un subíndice :math:`G` al signo de isomorfismo para indicar que este es un :math:`G`-isomorfismo (un isomorfismo de :math:`G`-módulos). Como antes, el mapeo :math:`\psi` de :math:`Y` a :math:`V/X` dado por :math:`\psi y = y + X` es un isomorfismo. Ya sabemos que se trata de un isomorfismo de espacio vectorial, por lo que solo debemos comprobar que respeta la :math:`G`-acción. Esto es inmediato a partir de la definición de la acción de :math:`G` sobre :math:`X/Y`: para todo :math:`y \in Y` y :math:`g\in G`,

.. math::

    \psi (gy) = gy + X = g(y + X) = g(\psi y).

Sin embargo, no está del todo claro que para cada :math:`G`-submódulo :math:`X` de un :math:`G`-módulo :math:`V` haya un submódulo complementario. Dado que un submódulo es *a fortiori* un subespacio vectorial, habrá un subespacio complementario, pero entre todos estos complementos, ¿hay uno que sea invariante en :math:`G`? (Tenga en cuenta que se dice que el subespacio vectorial de un :math:`G`-módulo es invariante en :math:`G` si y solo si está cerrado bajo la :math:`G`-acción; por lo tanto, un subespacio invariante en :math:`G` de :math:`V` es lo mismo que un :math:`G`-submódulo de :math:`V`).

En general, no es cierto que para cada grupo :math:`G` y cada :math:`G`-módulo :math:`V`, cada subespacio invariante :math:`G` tenga un complemento :math:`G`-invariante. Por ejemplo, considere el grupo :math:`G` que consta de todas las matrices :math:`2 \times 2` sobre :math:`\mathbb{F}` de la forma :math:`\left(\begin{matrix}1&\lambda\\0&1\end{matrix}\right)`, donde :math:`\lambda` es arbitrario. De hecho, :math:`G` es isomorfo al grupo aditivo de :math:`F` a través del mapeo :math:`\phi : \lambda \mapsto \left(\begin{matrix}1&\lambda\\0&1\end{matrix}\right)` este mapeo es claramente biyectivo, y

.. math::

    \phi (\lambda + \mu) = \left(\begin{matrix}1&\lambda + \mu\\0&1\end{matrix}\right) = \left(\begin{matrix}1&\lambda\\0&1\end{matrix}\right)  \left(\begin{matrix}1&\mu\\0&1\end{matrix}\right) = \phi (\lambda) + \phi (\mu)

Pero lo que es más importante en la actualidad es que el espacio :math:`V` de todos los vectores columna de dos componentes es un :math:`G`-módulo que tiene solo un submódulo propio, a saber, el subespacio :math:`X` que consta de todos los vectores de dos componentes cuyo segundo componente es :math:`0`. que :math:`U` es otro submódulo distinto de cero de :math:`V`. Entonces :math:`U` contiene un vector de columna :math:`x` y distinto de cero. Dado que :math:`U` está cerrado bajo esa acción de :math:`G`, deducimos que


.. math::

    \left(\begin{matrix}x + \lambda y\\ y\end{matrix}\right) =  \left(\begin{matrix}1 & \lambda\\ 0 & 1\end{matrix}\right) \left(\begin{matrix} x\\ y\end{matrix}\right)\in U


para todo :math:`\lambda \in \mathbb{F}`, y por cierre de :math:`U` bajo resta

.. math::

    \left(\begin{matrix}\lambda y\\ 0\end{matrix}\right) = \left(\begin{matrix}x + \lambda y\\ y\end{matrix}\right) - \left(\begin{matrix} x\\ y\end{matrix}\right)\in U


para todo :math:`\lambda \in \mathbb{F}`. En particular, si :math:`y \not= 0` entonces al tomar :math:`\lambda = y^{−1}` deducimos que :math:`U` contiene :math:`\left(\begin{matrix}1\\0\end{matrix}\right)`, y por lo tanto (por cierre bajo multiplicación escalar) todos los vectores cuyo segundo componente es :math:`0`. En el Por otro lado, si :math:`y = 0` entonces :math:`x` debe ser diferente de cero (ya que asumimos que :math:`\left(\begin{matrix}x\\y\end{matrix}\right)` es diferente de cero), y se sigue la misma conclusión, ya que ahora los múltiplos escalares de :math:`\left(\begin{matrix}x\\y\end{matrix}\right)` dan todos los vectores que son cero en el segundo componente. Entonces, el submódulo :math:`U` contiene :math:`X` (que ya es suficiente para mostrar que :math:`U` no puede ser un complemento de :math:`X`). Si :math:`U` no es igual a :math:`X`, entonces debe contener algún vector que sea distinto de cero en el segundo componente, y dado que este vector junto con :math:`\left(\begin{matrix}1\\0\end{matrix}\right)` (que está en :math:`X` y por lo tanto en :math:`U`) abarcan :math:`V`, se sigue que :math:`U` es igual a la totalidad de :math:`V`.

Definición
-----------------

Se dice que un :math:`G`-módulo :math:`V` es indecomponible si no puede expresarse como una suma directa de dos submódulos distintos de cero.

Definición
----------------------------

Se dice que un :math:`G`-módulo :math:`V` es irreducible si no tiene más submódulos que él mismo y el submódulo cero.

Hemos dado anteriormente un ejemplo de un módulo :math:`V` que es indecomponible pero no irreductible. Como espacio vectorial, :math:`V` es bidimensional y tiene un submódulo que es unidimensional como espacio vectorial; esto muestra que :math:`V` no es irreductible. Pero como :math:`V` no tiene otros submódulos no triviales, no puede expresarse como una suma directa de dos submódulos no triviales; por tanto, es indescomponible.

El primer resultado principal de la teoría de la representación que pretendemos demostrar es el famoso teorema de Maschke que afirma que si el grupo :math:`G` es finito y el orden de :math:`G` es distinto de cero como elemento de :math:`\mathbb{F}`, entonces todo :math:`G`-módulo indecomponible es irreducible. :math:`\ast`


.. note::

    :math:`\ast` ¿Cómo podría ser cero el orden de :math:`G`  en :math:`\mathbb{F}`? El punto es que algunos cuerpos satisfacen ecuaciones inusuales como :math:`1 + 1 = 0` o :math:`1 + 1 + 1 = 0`. Por lo tanto, puede ser que un número entero :math:`n` distinto de cero se convierta en cero cuando se interpreta como un elemento de :math:`\mathbb{F}`. Si esto sucede, entonces el mínimo de tales el entero positivo se denomina **característica** de :math:`\mathbb{F}`. La hipótesis del teorema de Maschke puede reformularse de la siguiente manera: :math:`G` debe ser finito y la característica de :math:`\mathbb{F}` no debe ser un divisor de :math:`|G|`. Entonces, por ejemplo, si tomamos :math:`G` como el grupo :math:`S_{3}` de orden :math:`6` y :math:`\mathbb{F}` como los números enteros módulo :math:`3`, entonces :math:`1 + 1 + 1 = 0`, de donde :math:`6 = 0` en :math:`\mathbb{F}`, y el teorema de Maschke no se aplicaría.

From now on, unless otherwise stated, the scalar field for each vector space we deal with will b e C, the complex field. And all the vector spaces will be finite dimensional.

Teorema de Maschke
---------------------

Sea :math:`G` un grupo finito, :math:`V` un :math:`G`-módulo y :math:`U` un :math:`G`-submódulo de :math:`V`. Entonces hay un submódulo :math:`W` de :math:`V` tal que :math:`V = U \oplus W`.


De acuerdo con la definición de "irreductible" dada en la Lección 6, se dice que un módulo es reducible si tiene un submódulo propio distinto de cero. Se dice que un módulo es completamente reducible si para cada submódulo hay un submódulo complementario. El teorema de Maschke dice que cada módulo para un grupo finito :math:`|G|` (sobre un cuerpo tal que :math:`|G|\not = 0`) es completamente reducible, por lo que el teorema también se conoce como el Teorema de la reducibilidad completa.

Si ha trabajado completamente en los ejercicios del Tutorial 1, entonces ya habrá probado el Teorema de Maschke. Esa prueba es la siguiente:

- El primer paso es notar que es posible definir un producto interno en el espacio :math:`V`. Es decir, existe una función :math:`(u, v) \mapsto u \cdot v` de :math:`V \times V` a :math:`\mathbb{C}` tal que

    :math:`(i)` :math:`u \cdot (\lambda v + \mu w) = \lambda (u \cdot v) + \mu (u \cdot w)` para todo :math:`u`, :math:`v`, :math:`w \in V` y :math:`\lambda, \mu \in \mathbb{C}`,
    
    :math:`(ii)` :math:`u \cdot v = \overline{v \cdot u}` para todo :math:`u`, :math:`v \in V` (donde la línea superior indica conjugación compleja),
    
    :math:`(iii)` :math:`u \cdot u` es un número real y positivo para todo :math:`u \not = 0, u\in V` (y es :math:`0` si :math:`u = 0`).

De hecho, si :math:`v_{1}`, :math:`v_{2}`, :math:`\dots`, :math:`v_{n}` es cualquier base de :math:`V`, entonces existe un producto interno tal que :math:`v_{i} \cdot v_{j} = \delta_{ij}` para todo :math:`i` y :math:`j`. Explícitamente, si :math:`u = \sum_{i} \lambda_{i}v_{i}` y :math:`v = \sum_{i} \mu_{i}v_{i}` entonces :math:`u \cdot v = \sum_{i} \overline{\lambda_{i}}\mu_{i}`.


Verifiquemos las propiedades que debe cumplir el producto interno. Sean :math:`u`, :math:`v`, :math:`w \in V`; :math:`\alpha, \beta \in \mathbb{C}`. Luego :math:`u = \sum_{i} \lambda_{i}v_{i}`, :math:`v = \sum_{i} \mu_{i}v_{i}` y :math:`w = \sum_{i} \alpha_{i}v_{i}`


    :math:`(i)`
        
        .. math::

            \begin{align}
                u \cdot \left(\alpha v+\beta w\right) &= \left(\sum_{i} \lambda_{i}v_{i}\right)\cdot \left(\alpha\left(\sum_{i} \mu_{i}v_{i}\right)+\beta \left(\sum_{i} \alpha_{i}v_{i}\right)\right)                                                               \\
                                                      &= \left(\sum_{i} \lambda_{i}v_{i}\right)\cdot\left(\sum_{i} \left(\alpha \mu_{i}+ \beta \alpha_{i}\right)v_{i}\right)                                                                                             \\
                                                      &= \sum_{i} \overline{\lambda_{i}}\left(\alpha \mu_{i} + \beta \alpha_{i}\right)                                                                                                                               \\
                                                      &= \alpha\left(\sum_{i} \overline{\lambda_{i}}\mu_{i}\right) + \beta \left(\sum_{i} \overline{\lambda_{i}}\alpha_{i}\right)                                                                                    \\
                                                      &= \alpha\left(\left(\sum_{i} \lambda_{i}v_{i}\right) \cdot \left(\sum_{i} \mu_{i}v_{i}\right)\right) + \beta \left(\left(\sum_{i} \lambda_{i}v_{i}\right) \cdot \left(\sum_{i} \alpha_{i}v_{i}\right)\right)  \\
                                                      &= \alpha\left(u \cdot v\right) + \beta \left(u \cdot w\right)
            \end{align}                                        

    :math:`(ii)`

        .. math::

            \begin{align}
                u \cdot v &= \left(\sum_{i} \lambda_{i}v_{i}\right)\cdot \left(\sum_{i} \mu_{i}v_{i}\right)   \\
                          &= \sum_{i} \overline{\lambda_{i}} \mu_{i}                                          \\
                          &= \overline{\overline{\sum_{i} \overline{\lambda_{i}} \mu_{i}}}                    \\
                          &= \overline{\sum_{i} \overline{\overline{\lambda_{i}} \mu_{i}}}                    \\
                          &= \overline{\sum_{i} \lambda_{i} \overline{\mu_{i}}}                               \\
                          &= \overline{v \cdot u}
            \end{align}   

    :math:`(iii)`

        .. math::

            \begin{align}
                u \cdot u &= \left(\sum_{i} \lambda_{i}v_{i}\right)\cdot \left(\sum_{i} \lambda_{i}v_{i}\right) = \sum_{i} \overline{\lambda_{i}} \lambda_{i} = \sum_{i} |\lambda_{i}|^{2} \geq 0 \text{ y } \\
                u \cdot u &  \Leftrightarrow \lambda_{i} = 0, \forall i=1,2,\dots,n \Leftrightarrow  \overline{v \cdot u} \Leftrightarrow u=0
            \end{align} 



Fije un producto interno :math:`(u, v) \mapsto u \cdot v` en :math:`V`, y defina otra función :math:`V \times V \to \mathbb{C}` mediante la fórmula :math:`u \ast v = \sum_{x\in G} xu \cdot xv`.

Es fácil demostrar que se satisfacen las propiedades :math:`(i)`, :math:`(ii)` y :math:`(iii)` anteriores, de modo que :math:`\ast` también es un producto interno.

    :math:`(i)`

        .. math::

            \begin{align}
                u \ast \left(\alpha v+\beta w\right) &= \sum_{x\in G} xu\cdot x\left(\alpha v + \beta w\right)                                              \\
                                                     &= \sum_{x\in G} xu\cdot \left(\alpha \left(xv\right) + \beta \left(xw\right)\right)                   \\
                                                     &= \sum_{x\in G}\left( \alpha (xu\cdot xv) +\beta (xu\cdot xw) \right)                                 \\
                                                     &= \alpha \left( \sum_{x\in G} xu\cdot xv \right) +\beta \left(\sum_{x\in G} xu\cdot xw)\right)        \\                              \\
                                                     &= \alpha(u \ast v) + \beta (u \ast w)
            \end{align} 

    :math:`(ii)`

        .. math::

            \begin{align}
                u \ast v &= \sum_{ x\in G} xu\cdot xv                                       \\
                          &= \overline{ \overline{\sum_{x\in G} xu\cdot xv }}                  \\
                          &= \overline{ \sum_{x\in G} \overline{ xu\cdot xv }}                 \\
                          &= \overline{ \sum_{i} \lambda_{i} \overline{\mu_{i}}}               \\
                          &= \overline{v \cdot u}
            \end{align} 

    :math:`(iii)`

        .. math::

            \begin{align}
                u \ast u &= \sum_{x\in G} xu \cdot xu = \sum_{i} || xu ||^{2} \geq 0 \text{ y } \\
                u \ast u &  \Leftrightarrow ||xu|| = 0, \forall x \in G \Leftrightarrow  xu = 0 \forall x\in G (\text{en particular para } x=1) \Leftrightarrow u=0.
            \end{align} 

Además, es :math:`G`-invariante, en el sentido de que :math:`gu \ast gv = u \ast v` para todo :math:`u`, :math:`v \in V` y todo :math:`g\in G`, ya que

.. math::

    gu \ast gv = \sum_{x\in G} x(gu) \cdot x(gv) = \sum_{x\in G}(xg)u \cdot (xg)v =\sum_{y\in G} yu \cdot yv = u \ast v

(donde hemos utilizado el hecho de que cuando :math:`x` atraviesa todos los elementos de :math:`G`, también lo hace :math:`y = xg`, ya que :math:`x \mapsto xg` es una biyección :math:`G \to G`). Ahora definimos :math:`W` como el complemento ortogonal de :math:`U` relativo a este nuevo producto interno:

.. math::
    
    W = U^{\bot} = \{v \in V | u \ast v = 0 \text{ para todo } u \in U\}.
    
Entonces :math:`V = U \oplus W`. (Es una propiedad general de los espacios de producto internos que si :math:`U` es cualquier subespacio, entonces todo el espacio es la suma directa :math:`U \oplus U^{\bot}`.) Solo tenemos que demostrar que :math:`W` es un :math:`G`-submódulo de :math:`V`, y como ya sabemos que es un subespacio solo tenemos que demostrar que si :math:`w ∈ W` y :math:`g\in G` entonces :math:`gw \in W`. Pero esto es fácil: si :math:`u \in U` entonces :math:`u \ast gw = g^{−1}u \ast w = 0` ya que :math:`w \in U^{\bot}` y :math:`g^{−1}u \in U` (ya que :math:`U` es un :math:`G`-módulo); por tanto, :math:`gw \in U^{\bot}` (ya que :math:`u 'ast gw = 0` para todo :math:`u\in U`).

La idea clave en esta demostración es crear un objeto :math:`G`-invariante, en este caso un producto interno, sumando las transformadas :math:`G` de un objeto arbitrario. Este es un tema que se repetirá en varios puntos de este curso. A menudo, además de sumar sobre :math:`G`, dividimos por :math:`| G |`, de modo que el proceso puede considerarse como un promedio de los efectos de los elementos de :math:`G`. Ahora daremos una segunda prueba del teorema de Maschke; esta prueba puede aplicarse sin cambios si el cuerpo complejo se reemplaza por cualquier cuerpo en el que :math:`| G | \not = 0`. La idea clave de promediar permanece.


Dado el :math:`G`-módulo :math:`V` y el submódulo :math:`U`, elija un subespacio vectorial arbitrario :math:`Z` de :math:`V` que sea complementario a :math:`U`. Por lo tanto, como espacio vectorial :math:`V = U \oplus Z`, pero esto generalmente no será una descomposición del :math:`G`-módulo. Ahora, para cada :math:`z \in Z` y :math:`g\in G`, el elemento :math:`gz \in V` se puede dividir de manera única en un componente en :math:`U` y un componente en :math:`Z`; para que podamos escribir

.. math::

    \begin{equation}
        gz = \tau gz + \sigma gz\hspace{3cm} (1)
    \end{equation}

donde :math:`\tau_{g}: Z \to U` y :math:`\sigma_{g}: Z \to Z` son mapas lineales. Tenga en cuenta que tomando :math:`g = 1` da :math:`gz = z`; por tanto, :math:`\tau_{1}z = 0` y :math:`\sigma_{1}z = z`.

Sea :math:`h \in  G` y aplicando :math:`h` a ambos lados de la Ecuación :math:`(1)` y compare el resultado con la ecuación obtenida al reemplazar :math:`g` por :math:`hg` en la Ecuación :math:`(1)`:

.. math::
    
    \begin{align}
        \tau_{hg}z + \sigma_{hg}z &= (hg)z = h(gz) \\
                                  &= h(\tau_{g}z + \sigma_{g}z) \\
                                  &= h(\tau_{g}z) + h(\sigma_{g}z) \\
                                  &= h(\tau_{g}z) + (\tau_{h}(\sigma_{g}z) + \sigma_{h}(\sigma_{g}z))\hspace{2cm}(2)
    \end{align}

donde en el último paso hemos aplicado la Ecuación :math:`(1)` con :math:`g` reemplazar por :math:`h` y :math:`z` por :math:`\sigma_{g}z`. Dado que :math:`\tau_{g}z \in U` y :math:`U` es un :math:`G`-submódulo, se deduce que :math:`h (\tau_{g}z) \in U`, por lo que comparando los componentes :math:`U` y :math:`Z` de la primera y última expresión en la Ecuación :math:`(2)` da

.. math::

    \tau_{hg}z = h(\tau_{g}z) + \tau_{h}(\sigma_{g}z)\hspace{3cm} (3)

así como :math:`\sigma_{hg}z = \sigma_{h} (\sigma_{g}z)`. Tenga en cuenta que tomando :math:`h = g^{−1}` aquí se obtiene que :math:`\sigma_{(g^{−1})} = \sigma_{g}^{− 1}`, ya que :math:`\sigma_{1} = id`, y si ahora reemplazamos :math:`z` por :math:`\sigma_{g}^{− 1} z = \sigma_{hg}^{−1} (\sigma_{h}z)` en la Ecuación :math:`(3)` obtenemos

.. math::

    \tau_{hg}(\sigma_{hg}^{−1}(\sigma_{h}z)) = h(\tau_{g}(\sigma_{g}^{−1}z)) + \tau_{h}z. \hspace{2cm}(4)

Es la Ecuación :math:`(4)` a la que aplicamos la idea de promediar: sumarlo sobre todo :math:`g \in G` da

.. math::

    \sum_{g\in G} \tau_{hg}(\sigma_{hg}^{−1}(\sigma_{h}z)) = h\left(\sum_{g\in G} \tau_{g} (\sigma_{g}^{−1}z)\right) + |G|\tau_{h}z,

y ahora dividiendo por :math:`|G|` da

.. math::

    \eta (\sigma_{h}z) = h(\eta z) + \eta_{h}z,\hspace{2cm}(5)

donde hemos definido :math:`\eta: Z \to U` por

.. math::

    \eta z = \frac{1}{|G|} \sum_{g\in G} \tau_{g} (\sigma_{g}^{−1}z).

(El punto crucial es que si :math:`h \in G` es fijo, entonces :math:`\eta z' = \frac{1}{|G|} \sum_{g\in G} \tau_{hg} (\sigma_{hg}^{−1}z')` para todo :math:`z' \in Z`, ya que hg atraviesa todos los elementos de :math:`G` como lo hace :math:`g`.)

Sea :math:`W = \{z + \eta z | z \in Z \}`, y sea :math:`w \in W` arbitrario. Elija :math:`z \in Z` tal que :math:`w = z + \eta z`. Entonces para todo :math:`h \in G`,

.. math::

    hw = hz + h(\eta z) = hz + (\eta(\sigma_{h}z) − \tau_{h}z)

(por la Ecuación :math:`(5)`), y ahora usando la Ecuación :math:`(1)` deducimos que

.. math::

    hw = \sigma_{h}z + \eta(\sigma_{h}z) \in W.


Dado que esto es válido para todo :math:`w \in W` y :math:`h \in G`, hemos demostrado que :math:`W` está cerrado bajo la :math:`G`-acción . También es un subespacio vectorial de :math:`V` ya que es la imagen del mapa lineal :math:`z \mapsto z + \eta z` de :math:`Z` a :math:`V`. Por lo tanto, :math:`W` es un submódulo :math:`G` de :math:`V`. Si :math:`v \in V` entonces, para algunos :math:`u \in U` y :math:`z \in Z`,

.. math::

    v = u + z = (u − \eta z) + (z + \eta z) \in U + W,

ya que :math:`\eta z \in U` y :math:`z + \eta z \in W`. Además, :math:`U \cap W = \{0\}`, ya que si :math:`u \in U` y :math:`u = z + \eta z` para algún :math:`z \in Z` entonces

.. math::

    z = u − \eta z \in U \cap Z = \{0\},

mostrando que :math:`z = 0` y, por tanto, :math:`u = 0`. Por tanto, el submódulo :math:`W` es complementario de :math:`U`, como se requiere.



Como siempre en este tema, es posible reformular las demostraciones usando matrices en lugar de transformaciones lineales. A veces, los resultados se vuelven más fáciles de entender de esta manera y, a veces, más difíciles. Y, a menudo, diferentes personas no están de acuerdo sobre cuál es más fácil. De todos modos, repasemos la prueba anterior en términos de matriz. Comenzamos eligiendo una base :math:`v_{1}`, :math:`v_{2}`,:math:`\dots` , :math:`v_{n}` para el submódulo :math:`U` de :math:`V`, y luego extendiéndolo a una base :math:`v_{1}`, :math:`v_{2}`,:math:`\dots` , :math:`v_{n+m}` de V. Para :math:`g \in G` sea :math:`Qg` la matriz :math:`(n + m) \times (n + m)` cuya :math:`(i, j)`-ésima entrada :math:`Q_{ij}g` está definida por

.. math::

    gv_{j} = \sum{i=1}^{n+m}(Q_{ij}g)v_{i}.

Es decir, sea :math:`Qg` es la matriz de la transformación :math:`v \mapsto gv` relativa a nuestra base elegida. Observe que si :math:`1 \leq j \leq n` entonces :math:`v_{j} \in U` y entonces :math:`gv_{j} \in U`, y se sigue que :math:`gv_{j}` es una combinación lineal de :math:`v_{1}`, :math:`v_{2}`,:math:`\dots` , :math:`v_{n}`. Por tanto, los coeficientes :math:`Q_{ij}g` son cero para :math:`n + 1 \leq i \leq n + m` y :math:`1 \leq j \leq n`. Entonces tenemos una descomposición en bloque de la matriz sea :math:`Qg` como

    Qg = \left(\begin{matrix}Rg & Tg\\ 0 & Sg\end{matrix}\right)  \text{ para todo } g \in G

donde :math:`Rg` y :math:`Sg` son matrices respectivamente :math:`n \times n` y :math:`m \times m`, y :math:`Tg` es :math:`n \times m`. Esto puede verse como la versión matricial de reducibilidad; más precisamente, una representación matricial de :math:`G` es reducible si es equivalente a una representación matricial que tiene una estructura de bloque como en la Ecuación :math:`(8)`. Si el subespacio de :math:`V` generado por :math:`v_{n+1}`, :math:`v_{n+2}`, :math:`\dots` , :math:`v_{m}` fuera un :math:`G`-submódulo, entonces :math:`gv_{n + j}` sería una combinación lineal de :math:`v_{n+1}`, :math:`v_{n+2}`, :math:`\dots` , :math:`v_{m}`, y los coeficientes :math:`Q_{ij}g` serían cero para :math:`i \leq n` y :math:`j \geq n`; la matriz :math:`Tg` sería :math:`0` para todo :math:`g`. Por tanto, una representación matricial es descomponible si es equivalente a una de la forma :math:`g \mapsto \left(\begin{matrix}Rg & Tg\\ 0 & Sg\end{matrix}\right)`, y la forma matricial del teorema de Maschke es que una representación de la forma dada por la Ecuación :math:`(8)` es equivalente a una representación de la misma forma con todos los :math:`Tg` cero.

Dado que :math:`Rg` tiene :math:`(i, j)`-ésima entrada :math:`Q_{ij}g` para :math:`i`, :math:`j \in \{1, 2 ,\dots , n\}` vemos que :math:`Rg` es la matriz relativa a :math:`v_{1}`, :math:`v_{2}`, :math:`\dots` , :math:`v_{n}` de la transformación :math:`u \mapsto gu` de :math:`U`. Note también que :math:`v_{n + 1} + U`, :math:`v_{n + 2} + U` ,:math:`\dots` , :math:`v_{n + m} + U` es una base para el módulo de cociente :math:`V/U`, y dado que

.. math::

    g(v_{n+j} + U) = \left(\sum_{i =1}^{n+m} (Q_{i,n+j-g)v_{i}\right) + U = \sum_{i =1}^{m}(Q_{n+i,n+j}g)(v_{n+i} + U),

y :math:`Q_{n + i, n + j}g` es la :math:`(i, j)`-ésima entrada de :math:`Sg`, vemos que :math:`Sg` es la matriz de :math:`v + U \mapsto g(v + U)` en relación con la base anterior de :math:`V/U`.


Dado que :math:`g \mapsto Qg` es una representación matricial de :math:`G`, la Ecuación :math:`(8)` da

.. math::


    \begin{align}
        \left(\begin{matrix}R(hg) & T(hg)\\ 0 & S(hg) \end{matrix}\right) &= Q(hg)                                                           \\
                        &= (Qg)(Qh)                                                                                                          \\
                        &= \left(\begin{matrix}Rh & Th\\ 0 & Sh \end{matrix}\right)\left(\begin{matrix}Rg & Tg\\ 0 & Sg \end{matrix}\right)  \\
                        &= \left(\begin{matrix}(Rh)(Rg) & (Rh)(Tg)+(Th)(Sg)\\ 0 & (Sh)(Sg) \end{matrix}\right),
    \end{align}

que confirma las fórmulas :math:`R(hg) = (Rh)(Rg)` y :math:`S(hg) = (Sh)(Sg)` (que ya sabíamos ya que :math:`R` y :math:`S` son versiones matriciales de las representaciones de :math:`G` en :math:`U` y :math:`V/U` ), y también nos permite deducir que :math:`T(hg) = (Rh)(T g) + (T h)(Sg)`. Por lo tanto, a la derecha multiplicando por :math:`(Sg)^{−1} = S(hg){−1}(Sh)`,

.. math::

    (T(hg)S(hg))^{−1}(Sh) = (Rh)((T g)(Sg)^{−1}) + Th,\hspace{3cm}(9)

que es la matriz análoga de Ecuación :math:`(4)`. Promediando sobre :math:`g \in G` esto da

.. math::

    E(Sh) = (Rh)E + Th \text{ para todo }h \in G,

donde hemos definido :math:`E =\frac{1}{| G |} \sum_{g\in G} (Tg) (Sg)^{−1}`. Por lo tanto, obtenemos la siguiente ecuación matricial:

.. math::

    \left(\begin{matrix}Rh & Th\\ 0 & Sh \end{matrix}\right)\left(\begin{matrix}I & E\\ 0 & I \end{matrix}\right) = \left(\begin{matrix}I & E\\ 0 & I \end{matrix}\right)\left(\begin{matrix}Rh & 0\\ 0 & Sh \end{matrix}\right) \text{ para todo }h \in G.

Equivalentemente

.. math::

    \left(\begin{matrix}I & E\\ 0 & I \end{matrix}\right)^{-1}\left(\begin{matrix}Rh & Th\\ 0 & Sh \end{matrix}\right)\left(\begin{matrix}I & E\\ 0 & I \end{matrix}\right) = \left(\begin{matrix}Rh & 0\\ 0 & Sh \end{matrix}\right) \text{ para todo }h \in G.

de modo que la representación :math:`Q` sea equivalente a la suma diagonal de las representaciones :math:`R` y :math:`S`, según queríamos.

Habiendo hecho el Teorema de Maschke, procedamos inmediatamente al otro teorema principal de este curso: el Lema de Schur. Llamarlo Lema, como es tradicional, contradice su importancia. Pero como corresponde a un Lema, su demostración es fácil.

.. _version-uno:

Lema de Schur (Versión 1).
-----------------------------

Sean :math:`U`, :math:`V` dos :math:`G`-módulos irreducibles y :math:`\phi: U \to V` un :math:`G`-homomorfismo. Entonces :math:`\phi` es un :math:`G`-isomorfismo o el mapa cero.

**Demostración:**

Según parte del primer teorema del isomorfismo, :math:`ker \phi` es un :math:`G`-submódulo de :math:`U`. Pero:math:`U` es irreducible, por lo que no tiene submódulos propios no triviales. Por lo tanto, :math:`ker \phi = U` o :math:`ker \phi = \{0\}`.

- Si :math:`ker \phi = U` entonces :math:`\phi` es el mapa cero, que es una de las posibilidades permitidas en el enunciado del teorema.

- En el caso alternativo, :math:`\phi` es *inyectivo*, ya que :math:`ker \phi = \{0\}`. Ahora, otra parte del primer teorema del isomorfismo nos dice que :math:`im \phi` es un submódulo de :math:`V`, por lo que la irreductibilidad de :math:`V` nos dice que :math:`im \phi` es :math:`\{0\}` o :math:`V`. Si es :math:`\{0\}` entonces nuevamente :math:`\phi` debe ser el mapa cero, y como ya hemos excluido este caso, deducimos que :math:`im \phi = V`. Entonces :math:`\phi` es tanto *sobreyectiva* como *inyectiva*, y por lo tanto es un isomorfismo, como se requiere. :math:`^{\ast}` :\math:`\blacksquare`

.. note::

    :math:`\ast` Se me acaba de ocurrir que la definición de "irreductible" debería haber incorporado el supuesto de que un módulo irreducible tiene que ser distinto de cero. Asumiremos esto de ahora en adelante.

Por tanto, parecería que el Lema de Schur no es gran cosa. Sin embargo, dedicaremos bastante tiempo a derivar consecuencias y reformulaciones del resultado, muchas de las cuales son bastante sorprendentes. La verdad es que el supuesto de irreductibilidad es muy fuerte. Así, los módulos irreductibles son objetos bastante especiales y, como veremos, tienen algunas propiedades sorprendentes.

Primero, debemos derivar la forma matricial de la declaración anterior:

.. _version-dos:

Lema de Schur (Versión 2)
--------------------------------------

Sean :math:`R: G \to GL(n,\mathbb{F})` y :math:`S: G \to GL(m,\mathbb{F})` representaciones matriciales irreductibles de :math:`G`, y sea :math:`X` una matriz :math:`n \times m` que entrelaza :math:`R` y :math:`S`. Entonces :math:`X = 0` o :math:`X` es invertible.


Esto se sigue inmediatamente del :ref:`version-uno`, en vista de nuestra discusión de los :math:`G`-homomorfismos y las matrices entrelazadas en la Lección 5. Tenga en cuenta que, por supuesto, el caso :math:`G` invertible solo puede surgir si :math:`n = m` (que en términos de módulo dice que si :math:`U` y :math:`V` son isomorfos tienen la misma dimensión que :math:`\mathbb{F}`).

.. important::

    Cabe señalar que todo lo dicho hasta ahora es totalmente general. Nuestra suposición de que se puede prescindir de :math:`\mathbb{F} = \mathbb{C}`, el grupo :math:`G` no tiene que ser finito y los módulos :math:`U` y :math:`V` no tienen que ser de dimensión finita sobre :math:`\mathbb{F}`. Hemos usado solo el primer teorema del isomorfismo (y de hecho solo casos de eso) y la definición de irreductibilidad. Sin embargo, para el siguiente resultado, hacemos uso de la suposición de que el cuerpo es :math:`\mathbb{C}`.



Lema de Schur (Version 3)
--------------------------------------

Sea :math:`R: G \to GL (d, \mathbb{C})` una representación matricial irreducible de :math:`G`, y suponga que :math:`X` es una matriz a :math:`d \times d` tal que :math:`(Rg) X = X (Rg)` para todo :math:`g \in G`. Entonces :math:`X = \lambda I` para algunos :math:`\lambda \in \mathbb{C}`.

**Demostración:**

Elija :math:`\lambda` para que sea un valor propio de :math:`X`. Debido a que el campo fundamental es :math:`\mathbb{C}`, y todo polinomio no constante con coeficientes en :math:`\mathbb{C}` tiene una raíz en :math:`\mathbb{C}`, el polinomio característico de :math:`X` tiene al menos una raíz :math:`\lambda \in \mathbb{C}`, por lo que un :math:`\lambda` adecuado ciertamente existe. Por definición, det :math:`(X - \lambda I) = 0`, y la matriz :math:`X - \lambda I` no es invertible. Ahora para todo :math:`g \in G`,

.. math::

    (X − \lambda I)(Rg) = X(Rg) − \lambda(Rg) = (Rg)X − \lambda(Rg) = (Rg)(X − \lambda I),

ya que :math:`X` conmuta con cada :math:`Rg`. Por lo tanto, :math:`X - \lambda I` conmuta con cada :math:`Rg`, y según el :ref:`version-dos` anterior se deduce que :math:`X - \lambda I` es invertible o cero. Por la elección de :math:`\lambda` no es invertible; entonces :math:`X = \lambda I`, según sea necesario.

La versión modular de esta declaración es que si :math:`V` es un :math:`G`-módulo irreducible de dimensión finita sobre :math:`\mathbb{C}` y :math:`\phi: V \to V` es un :math:`G`-homomorfismo, entonces :math:`\phi` es un múltiplo escalar del mapa de identidad. La suposición aquí de que :math:`V` es de dimensión finita es necesaria ya que los espacios vectoriales de dimensión infinita admite operadores lineales que no tienen valores propios.

No habrá escapado a la atención del lector alerta que, en nuestra tercera forma del Lema de Schur, :math:`\mathbb{C}` podría ser reemplazado por cualquier campo algebraicamente cerrado.

