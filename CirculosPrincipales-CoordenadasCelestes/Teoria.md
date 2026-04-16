A continuación, presento la base teórica completa y corregida para la **Práctica 4: Círculos Principales y Coordenadas Celestes**, integrando la información de los libros de **Portilla** (*Elementos de astronomía de posición*) y **Karttunen** (*Fundamental Astronomy*). Se ha verificado cuidadosamente el uso de la notación matemática en LaTeX.

---

# Base Teórica: Práctica 4

### 1. La Bóveda o Esfera Celeste
La astronomía esférica utiliza el concepto de **bóveda celeste**, que es una esfera ilusoria de radio infinito (o adoptado como radio unidad) en cuyo centro se ubica el observador. En esta superficie, las posiciones de los astros se determinan mediante ángulos, permitiendo aplicar las propiedades de la **trigonometría esférica** para calcular direcciones y movimientos aparentes.

### 2. Puntos y Círculos de Referencia Universales
Estos elementos se basan en la extensión de los parámetros físicos de la Tierra hacia el espacio:

*   **Polos Celestes (PNC y PSC):** Son los puntos de intersección del eje de rotación de la Tierra con la esfera celeste.
*   **Ecuador Celeste (EC):** Es el círculo máximo resultante de proyectar el ecuador terrestre sobre la esfera celeste, dividiéndola en los hemisferios norte y sur.
*   **Punto Vernal ($\Upsilon$):** También llamado primer punto de Aries, es el punto donde el Sol cruza el ecuador celeste de sur a norte. Sirve como origen para el sistema de coordenadas ecuatoriales absolutas.
*   **Eclíptica:** Es la trayectoria aparente que describe el Sol en la esfera celeste durante un año debido al movimiento de traslación terrestre.

### 3. Puntos y Círculos de Referencia Locales
Dependen de la ubicación específica del observador y la dirección de la vertical local (plomada):

*   **Cenit ($C$) y Nadir ($C'$):** El cenit es el punto directamente sobre la cabeza del observador; el nadir es el punto diametralmente opuesto.
*   **Horizonte Matemático:** Es el plano perpendicular a la línea cenit-nadir que pasa por el observador.
*   **Meridiano del Observador:** Semicircunferencia máxima que pasa por los polos celestes y el cenit del observador. Cuando un astro cruza esta línea, se dice que está **culminando**.
*   **Vertical de un astro:** Semicircunferencia que va del cenit al nadir pasando por el cuerpo celeste.
*   **Primer Vertical:** Semicircunferencia que une los puntos cardinales Este y Oeste pasando por el cenit.
*   **Almicantarat:** Círculo menor paralelo al horizonte.

### 4. Sistemas de Coordenadas Celestes

#### A. Sistema Horizontal
Utiliza el horizonte como plano fundamental.
*   **Altura ($h$):** Ángulo medido sobre la vertical desde el horizonte hasta el astro. Varía entre $-90^\circ$ y $+90^\circ$.
*   **Distancia cenital ($z$):** Es el complemento de la altura. Su fórmula es:
$$z = 90^\circ - h$$
*   **Acimut ($A$):** Ángulo medido sobre el horizonte. En astronomía moderna se mide comúnmente desde el Norte hacia el Este ($0^\circ$ a $360^\circ$), aunque el libro de Portilla menciona que en algunos contextos se mide desde el Sur.

#### B. Sistemas Ecuatoriales
Utilizan el ecuador celeste como plano de referencia.

1.  **Sistema Ecuatorial Horario:**
    *   **Declinación ($\delta$):** Ángulo medido desde el ecuador hasta el astro sobre su círculo de declinación.
    *   **Ángulo Horario ($H$):** Ángulo medido sobre el ecuador desde el meridiano local hacia el Oeste. Se mide frecuentemente en unidades de tiempo, donde:
$$15^\circ = 1^h$$

2.  **Sistema Ecuatorial Absoluto:**
    *   **Ascensión Recta ($\alpha$):** Ángulo medido sobre el ecuador celeste desde el punto vernal en dirección antihoraria.

### 5. Relaciones Fundamentales para la Práctica

*   **Orientación por Latitud:** La altura del polo norte celeste sobre el horizonte es exactamente igual a la latitud ($\phi$) del observador. La fórmula es:
$$h_{PNC} = \phi$$
*   **Relación Tiempo-Espacio:** El Tiempo Sideral Local ($TSL$) se define como el ángulo horario del punto vernal ($H_\Upsilon$). La conexión con las coordenadas es:
$$TSL = H + \alpha$$
*   **Condición de Culminación:** Un astro alcanza su máxima altura (culminación superior) cuando su ángulo horario es cero ($H = 0^h$). En ese instante:
$$TSL = \alpha$$
