# Dinámica multitemporal de los humedales de El Yali

Caso de estudio de teledetección y análisis de datos ambientales aplicado a tres unidades de humedal de la Región de Valparaíso: Albufera, Laguna Colejuda y Laguna Matanza.

## Informe técnico

[Abrir informe técnico de monitoreo y planificación](documents/Informe_Tecnico_Monitoreo_y_Planificacion_El_Yali.docx)

## Objetivo

Caracterizar la variación estacional del agua abierta y la condición de la vegetación entre 2019 y 2025, integrando observaciones Sentinel-2, índices espectrales y precipitación CHIRPS.

El proyecto busca responder dos preguntas:

1. ¿Cómo cambia la superficie con respuesta espectral de agua entre invierno y verano?
2. ¿Las tres unidades presentan la misma relación entre precipitación, agua abierta y vegetación?

## Enfoque metodológico

![Workflow metodológico desde la pregunta ambiental a la interpretación aplicada](data/results/figura_workflow_metodologico_el_yali.png)

El análisis conecta una pregunta ambiental, observaciones satelitales comparables, indicadores espectrales e interpretación prudente. La incertidumbre se considera de forma transversal: resolución espacial, nubosidad, sensibilidad del umbral MNDWI, píxeles mixtos, geometrías de referencia, escala de la precipitación y ausencia de validación sistemática en terreno.

## Diseño analítico

- composiciones estacionales comparables de Sentinel-2 Surface Reflectance Harmonized;
- enmascaramiento de nubes y sombras mediante la clasificación SCL;
- estimación de agua abierta con MNDWI y análisis de sensibilidad de umbrales;
- evaluación de la condición media de la vegetación mediante NDVI;
- precipitación acumulada estacional obtenida de CHIRPS;
- comparación espacial entre Albufera, Laguna Colejuda y Laguna Matanza;
- estadística descriptiva y correlaciones exploratorias por unidad y temporada;
- validación visual de los resultados espectrales.

## Resultados principales

- La Albufera mantuvo la presencia más persistente de agua abierta durante el periodo analizado.
- Laguna Colejuda presentó una marcada contracción estival y la asociación invernal más consistente entre precipitación y agua abierta.
- Laguna Matanza mostró pulsos de agua abierta concentrados en 2020 y 2024, junto con valores de NDVI que evidencian una respuesta vegetal relevante en años sin agua abierta detectable.
- El análisis desagregado evitó atribuir una única dinámica a humedales con funcionamiento ambiental diferente.

Los valores obtenidos corresponden a sectores analíticos y no constituyen superficies oficiales ni una restitución de límites legales.

### Variación estacional del agua abierta

![Variación estacional del agua abierta en Albufera, Laguna Colejuda y Laguna Matanza](data/results/sector_analysis/serie_agua_abierta_por_sector_cientifica.png)

### Condición espectral media de la vegetación

![Variación del NDVI medio por unidad analítica y temporada](data/results/sector_analysis/serie_ndvi_por_sector_cientifica.png)

### Precipitación invernal y agua abierta

![Relación exploratoria entre precipitación invernal y agua abierta](data/results/sector_analysis/relacion_precipitacion_agua_invierno_cientifica.png)

### Sensibilidad del umbral MNDWI

![Sensibilidad de la superficie de agua al umbral MNDWI](data/results/sector_analysis/sensibilidad_mndwi_por_sector_cientifica.png)

## Cartografía de apoyo a la interpretación

Las siguientes láminas integran la lectura espacial de las composiciones Sentinel-2 y de los indicadores de agua abierta. Se presentan como apoyo a la interpretación temporal y a la priorización de preguntas de seguimiento; no corresponden a delimitaciones oficiales ni a una evaluación de terreno.

### Frecuencia estimada de agua abierta, 2019–2025

![Frecuencia estimada de agua abierta en la Reserva Nacional El Yali](data/results/cartografia/mapa_02_frecuencia_agua_abierta.png)

### Comparación estacional, 2020 y 2024

![Comparación estacional de composiciones Sentinel-2 y agua abierta estimada](data/results/cartografia/mapa_03_comparacion_estacional.png)

### Cambio estimado de agua abierta entre inviernos

![Cambio estimado de agua abierta entre los inviernos de 2020 y 2024](data/results/cartografia/mapa_04_cambio_invernal_2020_2024.png)

### Extensión máxima estimada de agua abierta, 2019–2025

![Extensión máxima estimada de agua abierta en la Reserva Nacional El Yali](data/results/cartografia/mapa_05_extension_maxima_2019_2025.png)

## Contenido

- [Notebook de análisis](notebooks/01_analisis_resultados_el_yali.ipynb): control de calidad, estadística descriptiva y visualizaciones con Python.
- [Informe técnico de monitoreo y planificación](documents/Informe_Tecnico_Monitoreo_y_Planificacion_El_Yali.docx): integración de resultados, cartografía, indicadores de seguimiento, incertidumbre y propuesta de manejo adaptativo.
- [Resultados generales](data/results/): tablas y figuras del análisis temporal agregado.
- [Resultados por sector](data/results/sector_analysis/): indicadores desagregados, sensibilidad MNDWI y relaciones exploratorias con precipitación.
- [Cartografía](data/results/cartografia/): láminas de frecuencia, comparación estacional, cambio y extensión máxima estimada de agua abierta.

## Alcance

Este repositorio presenta un caso de estudio de portafolio. Los resultados permiten reconocer trayectorias diferenciadas entre unidades y formular preguntas para seguimiento, verificación en terreno o manejo adaptativo. Son exploratorios: no reemplazan mediciones en terreno, no constituyen monitoreo oficial ni evaluación ambiental, y no son por sí solos una herramienta para decisiones operacionales.
