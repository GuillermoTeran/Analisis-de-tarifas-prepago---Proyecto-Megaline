# Análisis de tarifas prepago para Megaline

## ES Español

**Rol:** Analista de Datos  
**Tecnologías:** Python (pandas, numpy, matplotlib, seaborn, scipy), Jupyter Notebook

### Descripción del proyecto  
Como analista de datos para Megaline, un operador de telecomunicaciones, realicé un análisis de clientes para comparar el rendimiento de sus dos planes prepago: Surf y Ultimate. El objetivo principal fue determinar cuál plan genera mayores ingresos para optimizar el presupuesto publicitario. Se trabajó con datos de 500 clientes y su uso en llamadas, mensajes y datos durante 2018.

### Objetivos del análisis  
- Preprocesar y limpiar múltiples fuentes de datos relacionadas con usuarios, llamadas, mensajes, internet y planes tarifarios.  
- Calcular ingresos mensuales por cliente, considerando límites y cargos adicionales.  
- Analizar el comportamiento de los usuarios por plan.  
- Realizar pruebas estadísticas para determinar diferencias significativas entre ingresos por plan y región geográfica.

### Preparación y limpieza de datos  
Archivos analizados:  
- megaline_users.csv: datos demográficos y plan de cada usuario.  
- megaline_calls.csv: duración y fechas de llamadas.  
- megaline_messages.csv: cantidad de SMS enviados.  
- megaline_internet.csv: uso mensual de internet.  
- megaline_plans.csv: detalles de tarifas (límites y costos).

Tareas realizadas:  
- Conversión de columnas a tipos adecuados (datetime, int, str).  
- Cálculo del volumen mensual de minutos, SMS y datos por cliente.  
- Identificación y corrección de valores atípicos o inconsistentes.  
- Redondeo de llamadas y datos según reglas de facturación.  
- Cálculo de ingresos mensuales sumando cuota mensual y cargos adicionales.

### Análisis exploratorio  
- Minutos de llamadas: usuarios de Surf superan el límite con más frecuencia, generando cargos extras.  
- SMS: bajo uso general; mayoría no supera límites.  
- Datos móviles: Surf tiene límite menor (15 GB); muchos usuarios lo exceden.  
- Se calcularon promedios, varianza y desviación estándar por tarifa, visualizados con histogramas.

### Pruebas estadísticas  
Hipótesis evaluadas:

**Hipótesis 1:**  
- H₀: No hay diferencia significativa en ingresos promedio entre Surf y Ultimate.  
- H₁: Sí existe diferencia significativa.

**Hipótesis 2:**  
- H₀: No hay diferencia significativa en ingresos promedio entre NY-NJ y otras regiones.  
- H₁: Sí existe diferencia significativa.

Método:  
Prueba t para dos muestras independientes, α = 0.05.

Resultados:  
- Diferencia significativa entre ingresos de Surf y Ultimate, confirmando mayor rentabilidad de uno.  
- No se encontró evidencia suficiente para diferencias por región.

### Conclusiones clave  
- Aunque Ultimate tiene cuota mensual mayor, Surf genera más cargos adicionales, especialmente en datos, equilibrando o superando ingresos.  
- Patrones de uso distintos entre planes orientan decisiones promocionales.  
- Análisis estadístico sustenta estrategias de marketing basadas en ingresos reales.

### Herramientas utilizadas  
- Python: pandas, numpy, matplotlib, seaborn, scipy  
- Jupyter Notebook para documentación y presentación  
- Técnicas de EDA, ingeniería de características, limpieza y análisis estadístico

### Impacto del proyecto  
El análisis permitió a Megaline entender qué tarifa maximiza ingresos según comportamiento real de clientes, mejorando la asignación del presupuesto publicitario y diseñando estrategias personalizadas de adquisición y retención.

---

# Analysis of prepaid rates for Megaline

## US English

**Role:** Data Analyst  
**Technologies:** Python (pandas, numpy, matplotlib, seaborn, scipy), Jupyter Notebook

### Project description  
As a data analyst for Megaline, a telecommunications operator, I conducted a customer analysis to compare the performance of its two prepaid plans: Surf and Ultimate. The main goal was to determine which plan generates more revenue to optimize the advertising budget. Data from 500 customers was analyzed including usage of calls, messages, and data throughout 2018.

### Analysis objectives  
- Preprocess and clean multiple data sources related to users, calls, messages, internet, and rate plans.  
- Calculate monthly revenue per customer considering plan limits and additional charges.  
- Analyze user behavior by plan.  
- Use statistical tests to detect significant differences in average revenue by plan and geographic region.

### Data preparation and cleaning  
Files analyzed:  
- megaline_users.csv: demographic data and user plan.  
- megaline_calls.csv: call durations and dates.  
- megaline_messages.csv: SMS sent.  
- megaline_internet.csv: monthly internet usage.  
- megaline_plans.csv: rate plan details (limits and costs).

Tasks performed:  
- Converted columns to appropriate data types (datetime, int, str).  
- Calculated monthly volume of minutes, SMS, and data per customer.  
- Identified and corrected outliers or inconsistent values.  
- Rounded calls and data per Megaline billing rules.  
- Calculated monthly revenue including monthly fee and extra charges.

### Exploratory analysis  
- Call minutes: Surf users exceed limits more often, generating extra charges.  
- SMS: low overall usage; most users stay within limits.  
- Mobile data: Surf has lower limit (15 GB); many users exceed it.  
- Calculated averages, variance, and standard deviation by plan and visualized with histograms.

### Statistical tests  
Hypotheses tested:

**Hypothesis 1:**  
- H₀: No significant difference in average revenue between Surf and Ultimate.  
- H₁: Significant difference exists.

**Hypothesis 2:**  
- H₀: No significant difference in average revenue between NY-NJ and other regions.  
- H₁: Significant difference exists.

Method:  
Two-sample independent t-test, α = 0.05.

Results:  
- Statistically significant revenue difference between Surf and Ultimate, confirming one is more profitable.  
- Insufficient evidence to conclude revenue differences between regions.

### Key conclusions  
- Ultimate has higher monthly fee, but Surf generates more additional charges (notably data), balancing or exceeding revenue.  
- Different usage patterns between plans guide promotional decisions.  
- Statistical analysis provides strong basis to prioritize marketing strategies based on actual revenue.

### Tools used  
- Python: pandas, numpy, matplotlib, seaborn, scipy  
- Jupyter Notebook for documentation and presentation  
- EDA, feature engineering, data cleaning, and statistical analysis

### Project impact  
This analysis helped Megaline identify which plan maximizes revenue based on real customer behavior, enabling better advertising budget allocation and tailored acquisition and retention strategies.
