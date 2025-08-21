# Dashboards
## Catalogo Dashboards

Comparto dos proyectos de dashboards realizados en Power BI.

- En resumen, los dashboards demuestran un uso sofisticado de la inteligencia de negocios, desde la estructuración de los datos hasta la aplicación de medidas DAX complejas para el análisis de tendencias, el ranking de productos y la evaluación del desempeño. Estas son herramientas esenciales para la toma de decisiones estratégicas.


  - [Dashboard 1: ElectroMas](ElectroMas.pdf)
  - [Dashboard 2: NexoPlanet](NexoPlanet.pdf)

- Análisis de Fórmulas y Medidas DAX
    - Las métricas y los gráficos presentados no son simples datos brutos, sino que son el resultado de la aplicación de medidas y fórmulas DAX que permiten un análisis más profundo.

- Cálculos de Agregación Básicos:

    - Ingresos y Ganancias: Estas medidas (Revenue, Profit, Cost) son el resultado de una función de agregación (SUM) sobre las columnas de la tabla de hechos.

    - Transacciones: El número total de transacciones se calcula con una función de conteo (COUNT o COUNTROWS).

- Cálculos de Relación (Ratios):

    - Rentabilidad (Profitability): Esta es una medida clave calculada como una relación entre las ganancias y los ingresos. La fórmula DAX probable sería DIVIDE([Profit], [Revenue]).

- Análisis de Tiempo (Time Intelligence):

    - Cálculos de Tendencia: En el dashboard de "Nexo Planet", las métricas de tendencia ("Prev period Revenue Trend") son un claro ejemplo de la inteligencia de tiempo de DAX. Estas medidas se calculan comparando el período actual con el anterior. La fórmula DAX probable utilizaría funciones como CALCULATE y PREVIOUSPERIOD.

- Análisis de Ranking y Top N:

    - Top 5 Productos y Top 10 Marcas: Estos gráficos son el resultado de funciones de ranking que identifican los elementos con el mejor desempeño. Las fórmulas DAX para esto a menudo utilizan TOPN o RANKX para clasificar y luego filtrar los resultados. Por ejemplo, TOPN(5, ALL('Products'), [Total Sales]).

- Análisis Geográfico:

    - Transacciones por Ciudad y País: Los gráficos de mapas y barras que muestran la distribución de ventas por ubicación requieren la aplicación de filtros de contexto a las medidas, como CALCULATE([Total Transactions], 'Geography'[City] = "Tokyo").
