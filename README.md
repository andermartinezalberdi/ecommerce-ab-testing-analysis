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

**Se recomienda detener el experimento y considerar al grupo B como la variante ganadora.**

La variante B incrementa significativamente la conversión sin evidencia de una diferencia significativa en el tamaño promedio de pedido.

[Ver análisis completo en el notebook](notebook/analisis_ab_ecommerce.ipynb)
