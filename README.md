# Análisis de  tarifas prepago para Megaline

## ES Español

Descripción del proyecto:

Como analista de datos para Megaline, un operador de telecomunicaciones, llevé a cabo un análisis de clientes para comparar el rendimiento de sus dos planes prepago: Surf y Ultimate. El objetivo principal era determinar cuál de los dos planes genera mayores ingresos, con el fin de optimizar la asignación del presupuesto publicitario.

Se trabajó con datos de 500 clientes, incluyendo sus patrones de uso durante 2018 en llamadas, mensajes y consumo de datos.

## Objetivos del análisis:
Preprocesar y limpiar múltiples fuentes de datos relacionadas con usuarios, llamadas, mensajes, internet y planes tarifarios.

Calcular los ingresos mensuales por cliente, teniendo en cuenta los límites incluidos en cada plan y los cargos adicionales.

Analizar el comportamiento de los usuarios de cada plan.

Utilizar pruebas estadísticas para determinar si existen diferencias significativas entre ingresos medios por plan y por región geográfica.

## Preparación y limpieza de datos
Archivos analizados:

megaline_users.csv: datos demográficos y plan de cada usuario.

megaline_calls.csv: duración y fechas de llamadas.

megaline_messages.csv: cantidad de SMS enviados.

megaline_internet.csv: uso mensual de internet.

megaline_plans.csv: detalles de cada tarifa (límites y costos).

Tareas realizadas:

Conversión de columnas a tipos de datos adecuados (datetime, int, str, etc.).

Cálculo del volumen mensual de minutos, SMS y datos por cliente.

Identificación y corrección de valores atípicos o inconsistentes.

Redondeo de llamadas y datos según las reglas de facturación de Megaline.

Cálculo de ingresos mensuales por cliente, sumando cargos adicionales y la cuota mensual.

## Análisis exploratorio
Se analizó el uso mensual promedio de cada servicio:

Minutos de llamadas: los usuarios del plan Surf superan más a menudo el límite, generando cargos adicionales.

Mensajes SMS: muy poco uso general; la mayoría de usuarios no supera los límites.

Datos móviles: plan Surf tiene un límite más bajo (15 GB), y muchos usuarios exceden ese umbral.

Se calcularon promedios, varianza y desviación estándar para cada tipo de uso por tarifa, y se representaron mediante histogramas.

## Pruebas estadísticas
Se plantearon y evaluaron las siguientes hipótesis:

### Hipótesis 1:
H₀ (nula): No hay diferencia significativa entre los ingresos promedio de los planes Surf y Ultimate.

H₁ (alternativa): Hay una diferencia significativa entre los ingresos promedio de los planes.

### Hipótesis 2:
H₀ (nula): No hay diferencia significativa en los ingresos promedio entre usuarios del área de NY-NJ y otras regiones.

H₁ (alternativa): Hay una diferencia significativa en los ingresos promedio entre regiones.

### Método aplicado:
Prueba de hipótesis de dos muestras independientes (t-test), con un valor de α = 0.05.

### Resultados:

Se encontró una diferencia estadísticamente significativa en los ingresos entre Surf y Ultimate, confirmando que uno de los planes es más rentable.

No se encontró evidencia suficiente para afirmar que los ingresos difieren significativamente entre NY-NJ y otras regiones.

## Conclusiones clave:
Aunque el plan Ultimate tiene una cuota mensual mayor, el plan Surf genera más cargos adicionales, especialmente en consumo de datos, lo que puede equilibrar o incluso superar los ingresos.

Existen patrones de uso distintos entre planes, lo que puede orientar decisiones sobre la promoción de cada tarifa.

El análisis estadístico proporciona bases sólidas para priorizar estrategias de marketing basadas en ingresos reales generados.

## Herramientas utilizadas:
Python: pandas, numpy, matplotlib, seaborn, scipy

Jupyter Notebook: para documentación y presentación del análisis

Técnicas de EDA, ingeniería de características, limpieza de datos y análisis estadístico

## Impacto del proyecto:
Este análisis ayudó a Megaline a entender qué tarifa maximiza los ingresos en función del comportamiento real de sus clientes, permitiendo una mejor asignación del presupuesto de publicidad y el diseño de estrategias personalizadas de adquisición y retención.


# Analysis of  prepaid rates for Megaline

## US English

Project description:

As a data analyst for Megaline, a telecommunications operator, I conducted a customer analysis to compare the performance of its two prepaid plans: Surf and Ultimate. The main objective was to determine which of the two plans generates the most revenue in order to optimize the allocation of the advertising budget.

We worked with data from 500 customers, including their usage patterns during 2018 in terms of calls, messages, and data consumption.

## Analysis objectives:
Preprocess and clean multiple data sources related to users, calls, messages, internet, and rate plans.

Calculate monthly revenue per customer, taking into account the limits included in each plan and additional charges.

Analyze the behavior of users of each plan.

Use statistical tests to determine if there are significant differences between average revenue per plan and geographic region.

## Data preparation and cleaning
Files analyzed:

megaline_users.csv: demographic data and plan for each user.

megaline_calls.csv: duration and dates of calls.

megaline_messages.csv: number of SMS messages sent.

megaline_internet.csv: monthly internet usage.

megaline_plans.csv: details of each rate (limits and costs).

Tasks performed:

Conversion of columns to appropriate data types (datetime, int, str, etc.).

Calculation of monthly volume of minutes, SMS, and data per customer.

Identification and correction of outliers or inconsistent values.

Rounding of calls and data according to Megaline's billing rules.

Calculation of monthly revenue per customer, adding additional charges and the monthly fee.

## Exploratory analysis
The average monthly usage of each service was analyzed:

Call minutes: Surf plan users exceed the limit more often, generating additional charges.

SMS messages: very little overall usage; most users do not exceed the limits.

Mobile data: the Surf plan has a lower limit (15 GB), and many users exceed that threshold.

Averages, variance, and standard deviation were calculated for each type of usage by rate and represented by histograms.

## Statistical tests
The following hypotheses were proposed and evaluated:

### Hypothesis 1:
H₀ (null): There is no significant difference between the average revenues of the Surf and Ultimate plans.

H₁ (alternative): There is a significant difference between the average revenues of the plans.

### Hypothesis 2:
H₀ (null): There is no significant difference in average revenues between users in the NY-NJ area and other regions.

H₁ (alternative): There is a significant difference in average revenues between regions.

### Method applied:
Two-sample independent hypothesis test (t-test), with a value of α = 0.05.

### Results:

A statistically significant difference in revenue was found between Surf and Ultimate, confirming that one of the plans is more profitable.

There was insufficient evidence to conclude that revenue differs significantly between NY-NJ and other regions.

## Key conclusions:
Although the Ultimate plan has a higher monthly fee, the Surf plan generates more additional charges, especially for data consumption, which can balance or even exceed revenue.

There are different usage patterns between plans, which can guide decisions about promoting each rate.

Statistical analysis provides a solid basis for prioritizing marketing strategies based on actual revenue generated.

## Tools used:
Python: pandas, numpy, matplotlib, seaborn, scipy

Jupyter Notebook: for documentation and presentation of the analysis

EDA techniques, feature engineering, data cleaning, and statistical analysis

## Project impact:
This analysis helped Megaline understand which rate maximizes revenue based on the actual behavior of its customers, allowing for better allocation of the advertising budget and the design of customized acquisition and retention strategies.

