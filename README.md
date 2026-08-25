# E-commerce A/B Testing & Revenue Analysis

Análisis de un experimento A/B para una tienda online, orientado a priorizar oportunidades de crecimiento y determinar qué variante genera mejores resultados de negocio.

## Objetivo

El proyecto busca responder dos preguntas principales:

1. ¿Qué hipótesis de crecimiento debería priorizar el equipo de marketing?
2. ¿La variante B del experimento A/B genera una mejora significativa frente al grupo A?

Para responderlas se utilizaron los frameworks **ICE y RICE**, análisis exploratorio, detección de valores atípicos y pruebas estadísticas no paramétricas.

## Resultados principales

- La priorización mediante **RICE** situó la hipótesis 7 como la iniciativa con mayor potencial.
- Se identificaron **58 usuarios presentes en ambos grupos**, que fueron excluidos para evitar contaminación del experimento.
- Después de eliminar valores atípicos, el grupo B obtuvo una **conversión 18.9% superior** al grupo A.
- La diferencia de conversión fue estadísticamente significativa (`p-value = 0.00702`).
- No se encontraron diferencias significativas en el tamaño promedio de pedido (`p-value = 0.82203`).
- Se detectó un pedido excepcional de **19,920.4** que estaba distorsionando inicialmente los resultados del grupo B.

## Decisión de negocio



## Datos

El análisis utiliza tres datasets:

- `hypotheses_us.csv`: hipótesis de crecimiento y métricas necesarias para calcular ICE y RICE.
- `orders_us.csv`: transacciones, usuarios, fechas, ingresos y grupo experimental.
- `visits_us.csv`: visitas diarias registradas para los grupos A y B.

Los datasets fueron proporcionados como parte de un ejercicio de formación del programa de Data Analyst de TripleTen y no se redistribuyen públicamente en este repositorio.

Más información sobre los archivos esperados en [`data/README.md`](data/README.md).

## Metodología

El análisis se desarrolló en las siguientes etapas:

1. Revisión y preparación de los datos.
2. Identificación y exclusión de usuarios presentes en ambos grupos.
3. Priorización de hipótesis mediante **ICE y RICE**.
4. Análisis de ingresos, conversión y tamaño promedio de pedido.
5. Detección de valores atípicos mediante percentiles.
6. Comparación estadística de los grupos mediante la prueba de **Mann–Whitney U**.
7. Repetición del análisis después de eliminar anomalías.
8. Formulación de una recomendación de negocio basada en los resultados.

## Herramientas

- Python
- pandas
- NumPy
- Matplotlib
- SciPy
- Jupyter Notebook / Google Colab
- GitHub

**Se recomienda detener el experimento y considerar al grupo B como la variante ganadora.**

La variante B incrementa significativamente la conversión sin evidencia de una diferencia significativa en el tamaño promedio de pedido.

[Ver análisis completo en el notebook](notebook/analisis_ab_ecommerce.ipynb)


## Visualizaciones clave

### 1. Priorización de hipótesis con RICE

La metodología RICE permite incorporar el alcance potencial de cada iniciativa y modifica de forma relevante el orden de prioridad frente a ICE.

![Priorización RICE](images/priorizacion_rice.png)

### 2. Ingreso acumulado por grupo

El grupo B presenta un crecimiento superior en ingresos acumulados, aunque se observa un incremento abrupto asociado a pedidos de valor atípico.

![Ingreso acumulado](images/ingreso_acumulado.png)

### 3. Conversión después de eliminar anomalías

Una vez eliminados los usuarios con comportamiento anómalo, el grupo B mantiene una conversión aproximadamente **18.9% superior** al grupo A.

![Conversión filtrada](images/conversion_filtrada.png)


## Estructura del repositorio

```text
ecommerce-ab-testing-analysis/
│
├── data/
│   └── README.md
│
├── images/
│   ├── priorizacion_rice.png
│   ├── ingreso_acumulado.png
│   └── conversion_filtrada.png
│
├── notebook/
│   └── analisis_ab_ecommerce.ipynb
│
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
