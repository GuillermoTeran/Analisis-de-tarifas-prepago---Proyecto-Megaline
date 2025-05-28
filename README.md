# Análisis de planes tarifarios de prepago para Megaline
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

