**Baird, D. C.** (1991). ***Experimentación***: Una introducción a la teoría de mediciones y al diseño de experimentos (2ª ed.). México: **Prentice-Hall**,. ISBN: 968-880-223-9.


# 2-7 MÉTODO GENERAL PARA LA INCERTIDUMBRE EN FUNCIONES DE UNA SOLA VARIABLE

De la sección anterior, las diferencias finitas $\delta z$ y $\delta x$ se pueden expresar en términos de la derivada $dz/dx$. Por lo tanto, podemos obtener el valor de $\delta z$ usando primero las técnicas normales para obtener $dz/dx$ en la siguiente forma:

$$\frac{dz}{dx} = \frac{d(f(x))}{dx}$$

y escribiendo después:

$$\delta z = \frac{d(f(x))}{dx} \delta x \tag{2-1}$$

Este es un procedimiento relativamente simple, y funcionará bien en los casos para los cuales el planteamiento de diferencias finitas llevaría a una excesiva complejidad algebraica. Así, por ejemplo, si

$$z = \frac{x}{(x^2 + 1)}$$

entonces:

$$\frac{dz}{dx} = \frac{x^2 + 1 - x \cdot 2x}{(x^2 + 1)^2}$$
$$= \frac{1 - x^2}{(1 + x^2)^2}$$

y finalmente:

$$\delta z = \frac{1 - x^2}{(1 + x^2)^2} \delta x$$

Este cálculo habría sido muy complicado con cualquier otro planteamiento. Más aún, nos da una expresión general para $\delta z$ en función de $x$ y $\delta x$; cualquier valor deseado en particular puede obtenerse haciendo $x = x_0$. Usemos ahora estas técnicas para evaluar incertidumbres de algunas funciones comunes.

### a) Potencias

Consideremos:

$$z = x^n$$
$$\frac{dz}{dx} = nx^{n-1}$$
$$\delta z = nx^{n-1} \delta x$$

Lo significativo de este resultado se hace un poco más obvio cuando se expresa en términos de la incertidumbre relativa. Así,

$$\frac{\delta z}{z} = n \frac{\delta x}{x}$$

Por lo tanto, cuando se evalúan potencias, la **incertidumbre relativa del resultado es la incertidumbre relativa de la cantidad original multiplicada por la potencia respectiva**. Esto será válido tanto para potencias como para raíces, de modo que la precisión disminuye si una cantidad se eleva a potencias y mejora al sacar raíces. Esta situación debe vigilarse con cuidado en un experimento que implique potencias. Cuanto más alta es la potencia, mayor será la necesidad de una alta precisión inicial.

### b) Funciones trigonométricas

Sólo trabajaremos un ejemplo, ya que los demás se pueden tratar de manera semejante. Consideremos:

$$z = \text{sen } x$$

Aquí se cumple:

$$\frac{dz}{dx} = \cos x$$

y

$$\delta z = (\cos x) \delta x$$

Este es un caso en el que el método elemental de insertar $x_0 \pm \delta x$ muestra más claramente el resultado. Utilizando la aproximación $\cos \delta x = 1$, obtenemos:

$$\delta z = \cos x \text{ sen } \delta x$$

lo que muestra que la $\delta x$ en el resultado anterior es en realidad $\text{sen } \delta x$ en el límite, para ángulos pequeños. Sólo en el caso de una incertidumbre muy grande podrá ser significativa esta diferencia, pero es mejor entender la naturaleza del resultado. Es claro que **$\delta x$ deberá expresarse en radianes**. Este resultado normalmente tendrá una aplicación directa cuando se trate de aparatos como los espectrómetros.

### c) Funciones logarítmicas y exponenciales

Consideremos:

$$z = \log x$$

Aquí,

$$\frac{dz}{dx} = \frac{1}{x}$$

y

$$\delta z = \frac{1}{x} \delta x$$

La incertidumbre relativa se puede calcular como de costumbre. Si

$$z = e^x$$
$$\frac{dz}{dx} = e^x$$

y entonces:

$$\delta z = e^x \delta x$$

Este es un caso importante, ya que las funciones exponenciales ocurren frecuentemente en la ciencia y la ingeniería. Estas funciones pueden hacerse muy sensibles al exponente cuando toma valores mucho mayores que la unidad, y la incertidumbre $\delta z$ puede volverse muy grande. Esto le parecerá familiar, por ejemplo, a cualquiera que haya observado las fluctuaciones de corriente en un diodo termoiónico que resultan de variaciones muy pequeñas en la temperatura del filamento.

Como se dijo antes, este método puede aplicarse fácilmente a cualquier función no enumerada arriba evaluando la derivada respectiva y usando la ecuación 2-1.




# 2-9 MÉTODO GENERAL PARA LA INCERTIDUMBRE EN FUNCIONES DE DOS O MÁS VARIABLES

Los últimos dos ejemplos, tratados por el método elemental, sugieren que, una vez más, el **cálculo diferencial** puede ofrecer una **simplificación considerable** a este tratamiento. Es claro que, si tenemos:

$$z = f(x, y)$$

la cantidad apropiada para calcular $\delta z$ es la **diferencial total** $dz$, que está dada por:

$$dz = \frac{\partial f}{\partial x} dx + \frac{\partial f}{\partial y} dy \tag{2-2}$$

Tomaremos esta diferencial y la trataremos como una **diferencia finita** $\delta z$ que se puede calcular a partir de las incertidumbres $\delta x$ y $\delta y$. Esto es:

$$\delta z = \frac{\partial f}{\partial x} \delta x + \frac{\partial f}{\partial y} \delta y$$

y las derivadas $\partial f / \partial x$ y $\partial f / \partial y$ normalmente se calcularán con los valores $x_0$ y $y_0$, para los que se necesita $\delta z$. Podemos encontrar que, dependiendo de la función $f$, el signo de $\partial f / \partial x$ o $\partial f / \partial y$ resulte ser negativo. En ese caso, utilizando nuestro **requisito pesimista** para el valor máximo de $\delta z$, **escogeremos los valores negativos apropiados para $\delta x$ o $\delta y$**, obteniendo de ahí una **contribución total positiva** a la suma.

### a) Producto de dos o más variables

Supongamos que:

$$z = xy$$

Para usar la ecuación 2-2 necesitamos los valores de $\partial z / \partial x$ y $\partial z / \partial y$. Estos son:

$$\frac{\partial z}{\partial x} = y \quad \text{y} \quad \frac{\partial z}{\partial y} = x$$

Por lo que el valor de $\delta z$ está dado por:

$$\delta z = y \delta x + x \delta y$$

La significación de este resultado se ve con más claridad cuando se convierte a la **incertidumbre relativa**:

$$\frac{\delta z}{z} = \frac{\delta x}{x} + \frac{\delta y}{y}$$

Así pues, cuando la cantidad deseada es el **producto de dos variables**, la **incertidumbre relativa es la suma de las incertidumbres relativas de las componentes**.

El caso más general de una función compuesta, que se encuentra muy comúnmente en la física, implica un **producto algebraico** que tiene componentes elevadas a **diferentes potencias**.

Sea:

$$z = x^a y^b$$

en donde $a$ y $b$ pueden ser positivas o negativas, enteras o fraccionarias. En ese caso la formulación se **simplifica de manera significativa tomando los logaritmos** de ambos lados antes de diferenciar. Así:

$$\log z = a \log x + b \log y$$

de donde, diferenciando implícitamente, se obtiene:

$$\frac{dz}{z} = a \frac{dx}{x} + b \frac{dy}{y}$$

Como de costumbre, tomamos las diferenciales como diferencias finitas, y obtenemos:

$$\frac{\delta z}{z} = a \frac{\delta x}{x} + b \frac{\delta y}{y}$$

Nótese que este proceso da la **incertidumbre relativa de manera directa**, y eso con frecuencia es conveniente. Si se requiere la **incertidumbre absoluta** $\delta z$, se puede evaluar simplemente multiplicando la incertidumbre relativa por el valor calculado $z_0$, que normalmente está disponible. Esta forma de **diferenciación implícita** sigue siendo el procedimiento más sencillo, aun cuando la misma $z$ esté elevada a alguna potencia. Porque, si la ecuación es:

$$z^2 = xy$$

es innecesario reescribirla como:

$$z = x^{1/2} y^{1/2}$$

y partir de ahí, porque, si sacamos logaritmos:

$$2 \log z = \log x + \log y$$

de donde:

$$2 \frac{\delta z}{z} = \frac{\delta x}{x} + \frac{\delta y}{y}$$

lo que da $\delta z/z$, como se requería.

### b) Cocientes

Estos se pueden tratar como productos, en los cuales algunas de las **potencias son negativas**. Como antes, el valor máximo de $\delta z$ se obtendrá **despreciando los signos negativos** de la diferencial y combinando todos los términos en **forma aditiva**.

Si se encuentra una función distinta a las ya enumeradas, funciona por lo general alguna forma de diferenciación. Con frecuencia es conveniente diferenciar una ecuación en **forma implícita**, evitando así el requisito de calcular explícitamente la cantidad desconocida en función de las otras variables. Por ejemplo, consideremos la ecuación para **lentes delgadas**:

$$\frac{1}{f} = \frac{1}{o} + \frac{1}{i}$$

en donde la distancia focal $f$ es función de las cantidades medidas la distancia al objeto $o$ y la distancia a la imagen $i$. Podemos diferenciar la ecuación implícitamente, y obtenemos:

$$-\frac{df}{f^2} = -\frac{do}{o^2} - \frac{di}{i^2}$$

Es posible ahora calcular de manera directa $df/f$, y con más facilidad que si se escribe $f$ explícitamente como función de $o$ e $i$ y se diferencia. De esta forma podemos preparar una fórmula para la incertidumbre en la que se pueden insertar directamente todas las incógnitas. **Asegúrese de que se usen los signos adecuados** para que todas las contribuciones a la incertidumbre se sumen para dar los **límites extremos de posibilidad** del resultado.

Cuando la función sea tan grande y complicada que no se pueda obtener un valor general de $\delta z$, siempre podemos tomar los valores medidos $x_0, y_0$, etc., y encontrar $z_0$. Podemos entonces trabajar con dos resultados diferentes, uno utilizando los valores numéricos propios de $x_0 + \delta x, y_0 + \delta y$ (o $y_0 - \delta y$, si es el adecuado), etc., para obtener uno de los valores extremos de $z$, y el otro utilizando $x_0 - \delta x$, etc. Esos dos valores corresponderán a los límites de $z$, y así sabremos el valor de $\delta z$.
