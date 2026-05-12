### **1. Contexto: El Cielo Deformado**

Cuando miramos al cielo, suponemos que lo que vemos está exactamente donde parece estar. Sin embargo, la atmósfera terrestre actúa como una lente compleja y dinámica entre nosotros y el cosmos. Al igual que un lápiz parece quebrarse cuando se sumerge en un vaso con agua, la luz de las estrellas, los planetas y el Sol se curva al atravesar las capas de aire de nuestra atmósfera.

Este fenómeno no es solo una curiosidad óptica: tiene implicaciones profundas para la astronomía observacional. Hace que el Sol salga antes y se ponga después de lo que la geometría predice, hace que las estrellas titilen o centelleen y, lo más crítico para la ciencia, desplaza la posición aparente de los objetos celestes.

Si un astrónomo ignora la atmósfera, sus mapas del cielo serían erróneos. En esta práctica, dejaremos de ver la atmósfera como un obstáculo invisible y comenzaremos a medirla, **cuantificando** cómo deforma nuestra visión del universo y aprendiendo a corregir estos efectos para obtener datos precisos.

---

### **2. Objetivos de Aprendizaje**

Al **finalizar** esta práctica, el estudiante estará en capacidad de:

*   Entender el fenómeno físico de la refracción y cómo se **manifiesta específicamente** en las observaciones astronómicas (centelleo, desplazamiento de posición y deformación geométrica).
*   **Cuantificar experimentalmente** el achatamiento del disco solar o lunar en función de su altura sobre el horizonte.
*   **Analizar** la discrepancia entre la posición real y la posición aparente de un objeto celeste utilizando herramientas de simulación y cálculo.
*   **Aplicar** modelos matemáticos básicos para corregir las coordenadas de una estrella afectadas por la atmósfera.

---

### **3. Materiales y Herramientas**

*   Cámara digital o cámara de celular con buena resolución.
*   Trípode o soporte **fijo** para la cámara.
*   **¡IMPORTANTE!** Filtro solar **certificado** (si se va a observar el Sol). Si se observa la Luna, no es necesario.
*   Software de planetario **Stellarium** instalado en computador o dispositivo móvil.
*   Software de procesamiento de imágenes simple (puede ser ImageJ, Python, o incluso herramientas de medición en pantalla).
*   Cinta métrica, transportador o inclinómetro (puede ser una app del celular) para medir la altura aproximada si no se usa Stellarium en tiempo real.
*   Libreta de apuntes.

---

### **4. Principio Científico: La Luz en un Medio Alabeado**

#### **4.1. La Refracción de Ondas**
La refracción ocurre cuando una onda cambia de medio de propagación, alterando su velocidad y, en consecuencia, su dirección. En el caso de la luz de las estrellas, los rayos viajan desde el vacío del espacio e ingresan a la atmósfera terrestre. Dado que la atmósfera no es uniforme (su densidad cambia con la altura y la temperatura), los rayos de luz se curvan continuamente hacia la **superficie**, no únicamente cuando ingresan.

#### **4.2. Manifestaciones Observables**
En astronomía, este fenómeno causa varios efectos notables:

1.  **Desplazamiento de la Posición (Elevación Aparente):** Los objetos parecen estar más altos en el cielo de lo que realmente están. Este efecto es máximo en el horizonte (llegando a ser de $\approx 34$ minutos de arco, más que el diámetro del Sol) y nulo en el cenit.
    La corrección aproximada para la refracción $R$ (en minutos de arco) en función de la altura aparente $h$ es:
    $$R['] = \cot \left( h[^\circ] + \frac{7.31}{h[^\circ] + 4.4} \right) \times \left( \frac{P}{101 \text{ kPa}} \right) \times \left( \frac{273}{273 + T} \right) \quad (1)$$
    Donde $P$ es la presión atmosférica en kilopascales y $T$ es la temperatura en grados Celsius.

2.  **Achatamiento del Disco Solar/Lunar:** Como la refracción es más fuerte cerca del horizonte, la parte inferior del Sol se eleva (visualmente) más que la parte superior. Esto comprime la imagen verticalmente, dándole una forma ovalada o achatada.

3.  **Adelanto del Amanecer y Retraso del Atardecer:** Debido a la curvatura de la luz, vemos el Sol antes de que geométricamente cruce el horizonte y lo seguimos viendo después de que ya se ha ocultado. Esto añade aproximadamente 4 minutos extra de luz diurna.


### **5. Procedimiento Experimental**

#### **5.1. Experimento 0: Cuantificación del achatamiento (Deformación)**
**Objetivo:** Medir cómo cambia la geometría de un objeto extenso a diferentes alturas sobre el horizonte.

**¡ADVERTENCIA DE SEGURIDAD!:** Nunca observe ni fotografíe el Sol directamente sin un **filtro solar certificado** adecuado. Esto puede causar daños irreversibles a su vista y a los sensores de su cámara. Si no dispone de filtro, realice este experimento únicamente con la Luna llena.

1.  **Planificación:** Identifique un momento en el que el Sol o la Luna se encuentren muy cerca del horizonte, ya sea durante su salida o puesta.
2.  **Captura de Datos:**
    *   Monte la cámara en el trípode para asegurar la estabilidad de las tomas.
    *   Tome una serie de fotografías del objeto celeste comenzando cuando esté muy cerca del horizonte (altura $h \approx 0^\circ$) y continúe cada 5 o 10 minutos hasta que el astro alcance aproximadamente unos $15^\circ$ o $20^\circ$ de altura.
    *   Para cada fotografía, registre la **hora exacta** y la altura aproximada $h$ (puede apoyarse en Stellarium para obtener la altura precisa ingresando la hora de la captura).
3.  **Procesamiento:**
    *   Cargue las imágenes en su computadora.
    *   Mida el ancho horizontal $W$ (eje paralelo al horizonte) y la altura vertical $h_v$ (eje perpendicular al horizonte) del disco solar o lunar en píxeles utilizando un software de medición.

#### **5.2. Experimento 1: Refracción Diferencial (Simulación y Cálculo)**
**Objetivo:** Comparar las alturas observadas frente a las alturas reales de los astros.

1.  **Selección de Fuentes:** Elija dos estrellas brillantes y conocidas en el software **Stellarium**:
    *   **Fuente de Referencia:** Una estrella ubicada cerca del Cenit (altura $\approx 90^\circ$).
    *   **Fuente de Observación:** Una estrella ubicada cerca del Horizonte (altura $\approx 10^\circ$).
2.  **Configuración:** En el panel de visualización de Stellarium, active y desactive repetidamente la opción de "Atmósfera" (o "Refracción") para observar cómo se desplaza la posición indicada del objeto.
3.  **Medición:**
    *   Anote la altura ($a$) indicada **con atmósfera** ("altura aparente").
    *   Anote la altura ($a$) indicada **sin atmósfera** ("altura geométrica o real").
    *   Calcule la diferencia matemática $\Delta a = a_{aparente} - a_{real}$.
4.  **Repetición:** Realice este procedimiento para tres estrellas distintas situadas a diferentes alturas bajas (por ejemplo: $5^\circ, 15^\circ, 25^\circ$).

---

### **6. Tablas de Datos**

**Tabla 0: Deformación del Disco (Experimento 0)**

| Hora | Altura ($h$) [$^\circ$] | Ancho ($W$) [px] | Alto ($h_v$) [px] | Relación $W/h_v$ |
| :--- | :--- | :--- | :--- | :--- |

**Tabla 1: Desplazamiento de Posición (Experimento 1)**

| Estrella / Fuente | Altura ($a$) Real [Sin atmósfera] | Altura ($a$) Aparente [Con atmósfera] | Diferencia ($a_{ap} - a_{real}$) | Refracción ($R$) [Calculada con Ec. 1] |
| :--- | :--- | :--- | :--- | :--- |

---

### **7. Análisis y Conclusiones**

Responda las siguientes preguntas basándose en sus datos y observaciones experimentales:

1.  **Análisis Gráfico:** Realice una **gráfica** de la relación de aspecto ($W/h_v$) en función del ángulo de elevación ($h$) utilizando los datos registrados en la Tabla 0. ¿Qué tendencia observa en los datos? ¿A qué altura aproximada deja de ser perceptible la deformación geométrica del disco?
2.  **El Observador Distante:** Imagine que una persona situada en Barranquilla (a nivel del mar, con mayor presión atmosférica) observa una estrella cercana al horizonte. Simultáneamente, una persona en Medellín (en la montaña, con menor presión atmosférica) observa la misma estrella. Omitiendo las diferencias de latitud, ¿medirían ambos observadores la misma altura aparente? **Justifique** su respuesta técnica basándose en la ecuación de refracción presentada en la sección teórica.
3.  **Implicaciones Científicas:** ¿Cree usted que los efectos de la refracción atmosférica son despreciables al momento de medir las posiciones de asteroides en el sistema solar con **fines** de cálculo de órbitas? Explique detalladamente por qué un error de apenas unos pocos minutos de arco en la posición podría resultar peligroso para la precisión científica.
4.  **Más allá de lo monocromático (Investigación):** Hasta ahora hemos asumido la luz como un fenómeno único, pero las estrellas emiten radiación en múltiples colores. Consulte e investigue: ¿Cómo se **manifiesta** la refracción atmosférica cuando consideramos que la luz no es monocromática? ¿Se refracta de la misma manera la luz azul que la luz roja? ¿Qué efecto visual particular produciría esta dispersión en una estrella que se encuentra a muy baja altura sobre el horizonte?
