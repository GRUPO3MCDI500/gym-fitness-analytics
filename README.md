# Análisis global de la industria fitness y gimnasios 2000-2026

## Integrantes

- Wilson Arévalo
- Integrante 2: __________________________
- Integrante 3: __________________________
- Integrante 4: __________________________

## Descripción del proyecto

Este proyecto corresponde a la Fase 1 del ABP y tiene como propósito iniciar un flujo de trabajo reproducible para analizar la evolución global de la industria fitness y gimnasios entre los años 2000 y 2026.

El análisis se basa en un dataset que contiene información sobre membresías de gimnasio, participación fitness, ingresos del sector, cantidad de gimnasios, tasa de penetración, PIB per cápita, urbanización, obesidad e inactividad física en distintos países y regiones.

## Problemática

La industria fitness y de gimnasios ha crecido de manera desigual a nivel mundial entre 2000 y 2026. Existen diferencias importantes entre países y regiones en cuanto a membresías, número de gimnasios, ingresos del sector, acceso a servicios fitness y participación de la población en actividades físicas.

A partir de esta situación, el proyecto busca comprender qué factores económicos, de acceso y de salud pública se relacionan con el crecimiento y adopción de la industria fitness a nivel global.

## Objetivo general

Analizar la evolución global de la industria fitness y gimnasios entre 2000 y 2026, identificando la relación entre el crecimiento del sector, el acceso a gimnasios, las condiciones económicas de los países y los indicadores de salud pública, mediante un flujo de trabajo reproducible apoyado en herramientas científicas colaborativas.

## Objetivos específicos

- Identificar las variables principales del dataset y su relación con la problemática del proyecto.
- Organizar una estructura inicial de repositorio que permita mantener trazabilidad y reproducibilidad.
- Implementar un notebook inicial de Fase 1 con carga, exploración y revisión preliminar del dataset.
- Documentar el proceso técnico mediante README, notebook y archivos de apoyo.
- Utilizar Git y GitHub para registrar avances mediante commits descriptivos.
- Preparar la base técnica para las siguientes fases del proyecto ABP.

## Dataset utilizado

- Nombre del dataset: World Gym & Fitness Trends (2000-2026)
- Archivo utilizado: clean_gym_data.csv
- Fuente: Kaggle
- Periodo de análisis: 2000-2026
- Unidad de análisis: países y regiones

## Variables principales

El dataset contiene variables relacionadas con industria fitness, economía y salud pública, tales como:

- country
- region
- year
- gym_memberships
- fitness_participation_rate
- revenue_usd
- number_of_gyms
- gym_penetration_rate
- population_urban
- obesity_rate
- gdp_per_capita_usd
- population_total
- avg_membership_cost_usd
- insufficient_physical_activity_pct

## Herramientas utilizadas

- Python: lenguaje principal para análisis de datos.
- Pandas: manipulación y exploración de datos.
- NumPy: operaciones numéricas.
- Matplotlib y Seaborn: visualización de datos.
- Jupyter Notebook: desarrollo del análisis reproducible.
- Git: control de versiones local.
- GitHub: repositorio remoto y colaboración grupal.

## Estructura del repositorio

```text
gym-fitness-analytics/
│
├── README.md
├── requirements.txt
├── .gitignore
├── .gitattributes
│
├── data/
│   ├── raw/
│   │   └── clean_gym_data.csv
│   └── processed/
│       └── .gitkeep
│
├── notebooks/
│   └── F1_Definicion.ipynb
│
├── src/
│   └── .gitkeep
│
├── outputs/
│   ├── figures/
│   │   └── .gitkeep
│   └── tables/
│       └── .gitkeep
│
├── docs/
│   └── mapa_conceptual.pdf
│
└── reports/
    └── fase1/
        └── informe_tecnico_fase1.pdf