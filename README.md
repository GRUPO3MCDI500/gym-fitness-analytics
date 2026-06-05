# Análisis global de la industria fitness y gimnasios 2000-2026

## Integrantes

- Wilson Arévalo
- Luis Espinosa
- Mauricio Ortega
- Eduardo Garrido

---

## Descripción del proyecto

Este proyecto corresponde a la Fase 1 del ABP del curso **MCDI500 — Herramientas de software científico** y tiene como propósito iniciar un flujo de trabajo reproducible para analizar la evolución global de la industria fitness y gimnasios entre los años 2000 y 2026.

El análisis se basa en el dataset **World Gym & Fitness Trends 2000-2026**, disponible en formato CSV bajo el archivo `clean_gym_data.csv`. Este conjunto de datos contiene información sobre membresías de gimnasio, participación fitness, ingresos del sector, cantidad de gimnasios, tasa de penetración, PIB per cápita, urbanización, obesidad e inactividad física en distintos países y regiones.

En esta primera fase se define la problemática, se formulan los objetivos, se organiza el repositorio, se configura el entorno inicial de trabajo, se crea el notebook base, se documentan las primeras decisiones técnicas y se implementan validaciones automáticas mediante GitHub Actions.

Además, se incorpora GitHub Models para apoyar la documentación automática de Pull Requests y una Wiki técnica para profundizar las decisiones metodológicas, la trazabilidad del dataset, el flujo reproducible y la gestión de evidencias.

---

## Problemática

La industria fitness y de gimnasios ha crecido de manera desigual a nivel mundial entre 2000 y 2026. Existen diferencias importantes entre países y regiones en cuanto a membresías, número de gimnasios, ingresos del sector, acceso a servicios fitness y participación de la población en actividades físicas.

A partir de esta situación, el proyecto busca comprender qué factores económicos, de acceso y de salud pública se relacionan con el crecimiento y adopción de la industria fitness a nivel global.

Esta problemática requiere un análisis reproducible, ya que el estudio involucra múltiples variables, países, regiones y años. Por ello, el proyecto no solo se enfoca en analizar datos, sino también en documentar cómo se organizan, validan, versionan y reproducen los procesos técnicos asociados al análisis.

---

## Objetivo general

Analizar la evolución global de la industria fitness y gimnasios entre 2000 y 2026, identificando la relación entre el crecimiento del sector, el acceso a gimnasios, las condiciones económicas de los países y los indicadores de salud pública, mediante un flujo de trabajo reproducible apoyado en herramientas científicas colaborativas.

---

## Objetivos específicos

- Identificar las variables principales del dataset y su relación con la problemática del proyecto.
- Organizar una estructura inicial de repositorio que permita mantener trazabilidad y reproducibilidad.
- Implementar un notebook inicial de Fase 1 con carga, exploración y revisión preliminar del dataset.
- Documentar el proceso técnico mediante README, notebook, Wiki y archivos de apoyo.
- Utilizar Git y GitHub para registrar avances mediante commits descriptivos.
- Configurar validaciones automáticas mediante GitHub Actions.
- Ejecutar automáticamente el notebook en CI para comprobar su reproducibilidad.
- Incorporar GitHub Models para generar resúmenes automáticos de Pull Requests.
- Definir criterios iniciales para limpieza, validación y trazabilidad de datos.
- Preparar la base técnica para las siguientes fases del proyecto ABP.

---

## Preguntas de análisis

- ¿Cómo ha evolucionado la cantidad de membresías de gimnasio entre 2000 y 2026?
- ¿Qué países o regiones presentan mayor penetración de gimnasios?
- ¿Existe relación entre PIB per cápita y tasa de penetración de gimnasios?
- ¿Cómo se relacionan la obesidad y la inactividad física con la participación fitness?
- ¿Qué cambios se observan en la industria fitness antes, durante y después del periodo COVID-19?
- ¿Qué variables podrían ser útiles para predecir la penetración de gimnasios en fases posteriores?

---

## Dataset utilizado

| Elemento | Descripción |
|---|---|
| Nombre del dataset | World Gym & Fitness Trends 2000-2026 |
| Archivo utilizado | `clean_gym_data.csv` |
| Fuente | Kaggle |
| Periodo de análisis | 2000-2026 |
| Unidad de análisis | Países y regiones |
| Formato | CSV |
| Ubicación | `data/raw/clean_gym_data.csv` |

El archivo se mantiene en `data/raw/` para conservar una copia original sin modificaciones. En fases posteriores, cualquier versión transformada o procesada deberá almacenarse en `data/processed/`, manteniendo la trazabilidad entre el dato original y las versiones derivadas.

---

## Variables principales

El dataset contiene variables relacionadas con industria fitness, economía, territorio y salud pública:

| Variable | Descripción general |
|---|---|
| `country` | País registrado en el dataset. |
| `region` | Región geográfica asociada al país. |
| `year` | Año del registro. |
| `gym_memberships` | Cantidad de membresías de gimnasio. |
| `fitness_participation_rate` | Tasa de participación en actividades fitness. |
| `total_health_club_revenue_usd` | Ingresos totales de la industria fitness en USD. |
| `number_of_gyms` | Número de gimnasios registrados. |
| `gym_penetration_rate` | Tasa de penetración de gimnasios. |
| `urban_population_percentage` | Porcentaje de población urbana. |
| `obesity_rate` | Tasa de obesidad. |
| `gdp_per_capita_usd` | PIB per cápita en USD. |
| `population_total` | Población total del país. |
| `average_membership_cost_usd` | Costo promedio de membresía en USD. |
| `insufficient_physical_activity_pct` | Porcentaje de actividad física insuficiente. |

---

## Dimensiones de análisis

Las variables del dataset permiten estudiar la problemática desde tres dimensiones principales.

### 1. Industria fitness

Incluye variables como:

- `gym_memberships`
- `fitness_participation_rate`
- `total_health_club_revenue_usd`
- `number_of_gyms`
- `gym_penetration_rate`
- `average_membership_cost_usd`

Estas variables permiten observar el crecimiento del sector, la adopción de gimnasios, la participación fitness y los ingresos asociados a la industria.

### 2. Economía y territorio

Incluye variables como:

- `gdp_per_capita_usd`
- `urban_population_percentage`
- `population_total`
- `country`
- `region`
- `year`

Estas variables permiten comparar países y regiones, observando si las condiciones económicas o urbanas se relacionan con el acceso a servicios fitness.

### 3. Salud pública

Incluye variables como:

- `obesity_rate`
- `insufficient_physical_activity_pct`
- `fitness_participation_rate`
- `gym_penetration_rate`

Estas variables permiten explorar relaciones entre actividad física, obesidad, inactividad física y participación fitness.

---

## Herramientas utilizadas

| Herramienta | Uso dentro del proyecto |
|---|---|
| Python | Lenguaje principal para análisis de datos. |
| Pandas | Carga, manipulación y exploración del dataset. |
| NumPy | Apoyo en operaciones numéricas. |
| Matplotlib | Visualización inicial de datos. |
| Jupyter Notebook | Desarrollo del análisis reproducible mediante código y celdas narrativas. |
| Git | Control de versiones local. |
| GitHub | Repositorio remoto y colaboración grupal. |
| GitHub Desktop | Gestión visual de commits, ramas y sincronización. |
| GitHub Actions | Validación automática de estructura, dependencias, dataset y notebook. |
| GitHub Models | Generación automática de resúmenes técnicos en Pull Requests. |
| GitHub Wiki | Documentación técnica ampliada del proyecto. |

---

## Justificación técnica de herramientas

El uso de estas herramientas responde a la necesidad de construir un flujo reproducible, trazable y colaborativo.

- **Python y Pandas** permiten cargar, revisar y transformar el dataset de forma programática, evitando procesos manuales difíciles de replicar.
- **Jupyter Notebook** permite integrar código, resultados, visualizaciones y explicación metodológica en un mismo documento ejecutable.
- **Git y GitHub** permiten registrar la evolución del proyecto mediante commits, ramas y Pull Requests.
- **requirements.txt** permite reconstruir el entorno de ejecución con las dependencias necesarias.
- **GitHub Actions** permite validar automáticamente que la estructura, dependencias, dataset y notebook funcionen correctamente.
- **GitHub Models** permite documentar automáticamente el impacto técnico de los cambios realizados en Pull Requests.
- **GitHub Wiki** permite ampliar la documentación técnica sin sobrecargar el README.

Esta combinación de herramientas permite que el proyecto no dependa exclusivamente del computador local de un integrante, sino que pueda ejecutarse, revisarse y validarse desde un entorno común.

---

## Estructura del repositorio

```text
gym-fitness-analytics/
│
├── README.md
├── requirements.txt
├── .gitignore
├── .gitattributes
│
├── .github/
│   └── workflows/
│       ├── main.yml
│       └── ai-pr-summary.yml
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
        ├── informe_tecnico_fase1.pdf
        └── evidencias/
```

---

## Función de las carpetas principales

| Carpeta | Uso |
|---|---|
| `data/raw/` | Contiene el dataset original sin modificaciones. |
| `data/processed/` | Guardará versiones procesadas o limpias del dataset en fases posteriores. |
| `notebooks/` | Contiene notebooks reproducibles del análisis. |
| `src/` | Guardará scripts reutilizables en fases futuras. |
| `outputs/figures/` | Guardará gráficos generados durante el análisis. |
| `outputs/tables/` | Guardará tablas derivadas del análisis. |
| `docs/` | Contiene documentación de apoyo, mapa conceptual y referencias técnicas. |
| `reports/fase1/` | Contiene informe técnico y evidencias de la Fase 1. |
| `.github/workflows/` | Contiene workflows de GitHub Actions. |

---

## Reproducibilidad técnica

Para reproducir este proyecto, se recomienda clonar el repositorio, instalar las dependencias declaradas en `requirements.txt` y ejecutar el notebook principal de la Fase 1.

### Instalación de dependencias

Desde la carpeta raíz del repositorio:

```bash
pip install -r requirements.txt
```

### Dependencias principales

El archivo `requirements.txt` contiene:

```text
pandas>=2.0.0
numpy>=1.24.0
matplotlib>=3.7.0
jupyter>=1.0.0
notebook>=7.0.0
ipykernel>=6.0.0
nbconvert>=7.0.0
```

### Ejecución local del notebook

El notebook principal se encuentra en:

```text
notebooks/F1_Definicion.ipynb
```

Para ejecutarlo localmente:

1. Abrir Jupyter Notebook o JupyterLab.
2. Entrar a la carpeta del repositorio.
3. Abrir la carpeta `notebooks`.
4. Ejecutar el archivo `F1_Definicion.ipynb`.
5. Ejecutar las celdas en orden.

El notebook carga el dataset desde la ruta relativa:

```python
from pathlib import Path

DATA_PATH = Path("../data/raw/clean_gym_data.csv")
```

Esta ruta permite que el notebook funcione correctamente siempre que se respete la estructura del repositorio.

---

## Flujo reproducible del proyecto

El flujo reproducible se organiza en la siguiente secuencia:

```text
Definición del problema
        ↓
Adquisición y organización del dataset
        ↓
Exploración inicial
        ↓
Limpieza y preparación de datos
        ↓
Análisis exploratorio
        ↓
Visualización de resultados
        ↓
Interpretación y documentación
        ↓
Versionamiento y validación automática
```

Cada etapa cumple una función específica:

| Etapa | Propósito |
|---|---|
| Definición | Delimitar problemática, objetivos y preguntas de análisis. |
| Adquisición | Incorporar el dataset en `data/raw/`. |
| Exploración | Revisar dimensiones, columnas, tipos, nulos y duplicados. |
| Limpieza | Definir criterios para tratar datos faltantes, duplicados y valores atípicos. |
| Análisis | Comparar países, regiones, años y relaciones entre variables. |
| Visualización | Generar gráficos y tablas interpretables. |
| Documentación | Registrar decisiones, hallazgos y configuraciones. |
| Validación | Verificar estructura, dataset y notebook mediante GitHub Actions. |

---

## Notebook Fase 1

El archivo `F1_Definicion.ipynb` contiene:

- Contexto del proyecto.
- Problemática.
- Objetivo general y objetivos específicos.
- Preguntas centrales de análisis.
- Descripción del dataset.
- Herramientas utilizadas.
- Carga inicial de librerías.
- Carga del dataset desde `data/raw`.
- Revisión de dimensiones del dataset.
- Revisión de columnas.
- Revisión de tipos de datos.
- Revisión de valores nulos.
- Revisión de duplicados.
- Resumen estadístico inicial.
- Función simple de exploración.
- Primeras visualizaciones.
- Decisiones técnicas iniciales.
- Vinculación con el mapa conceptual.
- Proyección para fases posteriores.

---

## Ejecución automática del notebook en CI

Como mejora de reproducibilidad, el notebook se ejecuta automáticamente mediante GitHub Actions usando `nbconvert`.

El workflow ejecuta el notebook desde la carpeta `notebooks/` para que la ruta relativa al dataset funcione correctamente.

Comando utilizado:

```bash
jupyter nbconvert --to notebook --execute F1_Definicion.ipynb --output F1_Definicion_ejecutado.ipynb --ExecutePreprocessor.timeout=300 --ExecutePreprocessor.kernel_name=python3
```

Esta validación permite comprobar que:

- El notebook existe.
- Las dependencias están instaladas.
- El dataset se encuentra en la ruta esperada.
- Las rutas relativas funcionan.
- Las celdas se ejecutan sin errores.
- El notebook no depende de un entorno local específico.
- El análisis inicial puede reproducirse en un entorno limpio.

El kernel se fuerza a `python3` para evitar errores asociados a kernels locales de Anaconda u otros entornos.

---

## Control de versiones

El proyecto utiliza Git y GitHub para mantener trazabilidad de los avances. Los commits deben ser descriptivos y representar cambios específicos.

### Ejemplos de commits

```text
Crear estructura inicial del repositorio
Agregar dataset original de gimnasios
Crear notebook inicial de Fase 1
Actualizar README del proyecto
Agregar archivo de dependencias iniciales
Agregar mapa conceptual técnico
Agregar workflow de CI para Fase 1
Ejecutar notebook en CI
Corregir kernel de ejecucion del notebook en CI
Agregar resumen automatico de PR con GitHub Models
Agregar informe tecnico de Fase 1
Documentar Wiki del proyecto
```

---

## Estrategia de ramas

La rama `main` se mantiene como la versión estable del proyecto. Los cambios se trabajan primero en ramas secundarias tipo `feature/`, luego se validan mediante GitHub Actions y finalmente se integran a `main` mediante Pull Request.

### Rama principal

| Rama | Uso |
|---|---|
| `main` | Contiene la versión estable del proyecto. Solo debe recibir cambios revisados y validados. |

### Ramas implementadas

| Rama | Propósito | Archivos o carpetas asociadas |
|---|---|---|
| `feature/actualizar-notebook-f1` | Actualizar y mejorar el notebook principal de la Fase 1. | `notebooks/F1_Definicion.ipynb` |
| `feature/actualizar-readme` | Mejorar la documentación principal del repositorio. | `README.md` |
| `feature/documentacion-fase1` | Incorporar documentos, evidencias, anexos y material de apoyo de la Fase 1. | `docs/`, `reports/fase1/` |
| `feature/ci-cd` | Ajustar y probar la configuración de integración continua. | `.github/workflows/main.yml` |
| `feature/dataset-validacion` | Revisar la ubicación, estructura y validación inicial del dataset. | `data/`, `data/raw/clean_gym_data.csv` |
| `feature/github-models-pr-summary` | Implementar resumen automático de Pull Requests con GitHub Models. | `.github/workflows/ai-pr-summary.yml` |

### Flujo de trabajo con ramas

```text
main
│
├── feature/actualizar-notebook-f1
├── feature/actualizar-readme
├── feature/documentacion-fase1
├── feature/ci-cd
├── feature/dataset-validacion
└── feature/github-models-pr-summary
```

Procedimiento recomendado:

1. Actualizar `main`.
2. Crear una rama `feature/` según el tipo de cambio.
3. Realizar modificaciones.
4. Hacer commit con mensaje descriptivo.
5. Hacer push de la rama.
6. Crear Pull Request hacia `main`.
7. Esperar validaciones de GitHub Actions.
8. Revisar el resumen automático generado por GitHub Models.
9. Integrar a `main` solo si las validaciones pasan.

---

## CI/CD con GitHub Actions

Se implementó un workflow de integración continua mediante GitHub Actions, ubicado en:

```text
.github/workflows/main.yml
```

Nombre del workflow:

```text
CI - Validacion Fase 1
```

El workflow se ejecuta automáticamente en:

- Push a `main`.
- Push a ramas `feature/**`.
- Pull Requests hacia `main`.

### Validaciones realizadas

El workflow principal realiza las siguientes comprobaciones:

- Descarga el repositorio.
- Muestra la estructura inicial del proyecto.
- Configura Python 3.11.
- Instala las dependencias desde `requirements.txt`.
- Ejecuta el notebook `F1_Definicion.ipynb` mediante `nbconvert`.
- Verifica la existencia de `README.md`.
- Verifica la existencia de `requirements.txt`.
- Verifica la existencia de `data/raw/clean_gym_data.csv`.
- Verifica la existencia de `notebooks/F1_Definicion.ipynb`.
- Verifica la existencia de carpetas principales.
- Carga el dataset mediante Pandas.
- Verifica que el dataset tenga filas y columnas.
- Valida la presencia de las columnas principales esperadas.

### Columnas validadas

```text
country
region
year
gym_memberships
fitness_participation_rate
total_health_club_revenue_usd
number_of_gyms
gym_penetration_rate
urban_population_percentage
obesity_rate
gdp_per_capita_usd
population_total
average_membership_cost_usd
insufficient_physical_activity_pct
```

### Evidencia CI/CD

| Elemento | Detalle |
|---|---|
| Workflow | CI - Validacion Fase 1 |
| Job | validar-proyecto |
| Archivo | `.github/workflows/main.yml` |
| Eventos | push a `main`, push a ramas `feature/**` y Pull Requests hacia `main` |
| Estado esperado | exitoso |

---

## Resumen automático de Pull Requests con GitHub Models

Además del workflow principal de CI/CD, se implementó un workflow complementario basado en GitHub Models para apoyar la documentación automática de los cambios realizados mediante Pull Requests.

El workflow se encuentra en:

```text
.github/workflows/ai-pr-summary.yml
```

Nombre del workflow:

```text
AI - Resumen de Pull Request
```

### Funcionamiento general

```text
Pull Request hacia main
        ↓
GitHub Actions ejecuta AI - Resumen de Pull Request
        ↓
Se identifican los archivos modificados
        ↓
Se clasifica el tipo de cambio
        ↓
GitHub Models genera un resumen técnico automático
        ↓
El resumen se publica como comentario en el Pull Request
        ↓
El resumen también se guarda como artifact descargable
```

### Qué analiza el workflow

| Tipo de cambio | Archivos o carpetas relacionadas |
|---|---|
| Notebook | `notebooks/` |
| Documentación | `README.md` |
| Dataset | `data/` |
| CI/CD | `.github/workflows/` |
| Documentación técnica | `docs/` |
| Informe o evidencias | `reports/` |

### Contenido del resumen generado

El resumen automático generado por GitHub Models incluye:

- Tipo de cambio detectado.
- Archivos modificados.
- Impacto técnico del cambio.
- Relación del cambio con la Fase 1.
- Riesgos o puntos de atención.
- Validaciones recomendadas.
- Observación final.
- Checklist automático de revisión.

### Dónde se puede ver el resumen

| Ubicación | Descripción |
|---|---|
| Comentario en el Pull Request | El workflow publica o actualiza automáticamente un comentario dentro del Pull Request. |
| Logs de GitHub Actions | El resumen se imprime en el paso `Mostrar resumen en logs`. |
| Artifact descargable | El archivo `resumen_ai.md` se guarda como artifact bajo el nombre `resumen-ai-pr`. |

---

## Wiki del proyecto

Además del README, el proyecto cuenta con una Wiki técnica para documentar de forma más detallada las decisiones metodológicas y técnicas del flujo reproducible.

Páginas implementadas o sugeridas:

- `Home`
- `Contexto del proyecto`
- `Dataset y variables`
- `Flujo reproducible`
- `Estructura del repositorio`
- `Notebook Fase 1`
- `Control de versiones y ramas`
- `CI/CD con GitHub Actions`
- `GitHub Models`
- `Evidencias y anexos`
- `Riesgos, limitaciones y decisiones técnicas`
- `Referencias`

La Wiki permite profundizar en aspectos que en el README se presentan de forma resumida, tales como criterios de limpieza, justificación de herramientas, trazabilidad del dataset, funcionamiento del CI/CD y gestión de evidencias.

---

## Criterios iniciales de revisión del dataset

Durante la exploración inicial se revisarán:

- Cantidad de filas y columnas.
- Nombres de columnas.
- Tipos de datos.
- Valores nulos.
- Registros duplicados.
- Rango de años disponibles.
- Cantidad de países representados.
- Cantidad de regiones representadas.
- Distribución temporal de registros.
- Valores mínimos y máximos de variables numéricas.
- Posibles valores atípicos.
- Coherencia entre país, región y año.
- Consistencia de columnas esperadas.

---

## Criterios futuros de limpieza

En fases posteriores, la limpieza del dataset deberá considerar:

- No modificar directamente el archivo original ubicado en `data/raw/`.
- Guardar versiones procesadas en `data/processed/`.
- Documentar cada transformación aplicada en el notebook.
- Justificar cualquier eliminación de filas o columnas.
- Revisar valores nulos antes de imputar o excluir.
- Identificar valores atípicos antes de decidir su tratamiento.
- Validar rangos razonables de variables numéricas.
- Revisar consistencia temporal por país y año.
- Mantener trazabilidad entre dataset original y dataset procesado.

---

## Riesgos y limitaciones iniciales

El dataset y el proceso de análisis pueden presentar desafíos metodológicos que serán considerados en fases posteriores:

- Posible presencia de datos estimados o modelados para años recientes.
- Diferencias en la calidad de datos entre países.
- Variables económicas o de salud pública provenientes de distintas fuentes.
- Posibles valores atípicos asociados al periodo COVID-19.
- Comparaciones afectadas por diferencias demográficas entre países.
- Riesgo de interpretar correlaciones como causalidad.
- Posibles registros incompletos o inconsistentes.

Estos riesgos serán abordados mediante exploración inicial, documentación de decisiones, limpieza reproducible y validaciones técnicas.

---

## Evidencias y anexos

Las evidencias del proyecto deben organizarse preferentemente en:

```text
reports/fase1/evidencias/
```

Evidencias recomendadas:

| Evidencia | Descripción |
|---|---|
| Mapa conceptual | Evidencia visual del flujo reproducible planificado. |
| Repositorio GitHub | Captura de estructura del repositorio. |
| README actualizado | Evidencia de documentación principal. |
| Notebook ejecutado | Evidencia de carga y exploración inicial. |
| GitHub Actions exitoso | Evidencia de validación automática. |
| Ejecución del notebook en CI | Evidencia del paso `Ejecutar notebook Fase 1`. |
| Pull Requests | Evidencia del proceso de revisión. |
| GitHub Models | Evidencia del resumen automático generado. |
| Historial de commits | Evidencia de trazabilidad. |
| Ramas `feature/` | Evidencia de estrategia colaborativa. |

---

## Vinculación con el mapa conceptual

El mapa conceptual permitió planificar la relación entre problemática, dataset, herramientas científicas, flujo reproducible, documentación técnica y control de versiones.

En esta Fase 1 se materializan los siguientes componentes del mapa:

- Definición de la problemática del proyecto.
- Formulación del objetivo general y objetivos específicos.
- Identificación del dataset y variables principales.
- Organización inicial del repositorio.
- Creación del notebook `F1_Definicion.ipynb`.
- Documentación inicial mediante `README.md`.
- Documentación ampliada mediante Wiki.
- Registro de dependencias en `requirements.txt`.
- Uso de Git/GitHub para trazabilidad.
- Implementación de validación automática mediante GitHub Actions.
- Ejecución automática del notebook mediante `nbconvert`.
- Organización de ramas de trabajo.
- Implementación de resumen automático de Pull Requests mediante GitHub Models.

Quedan proyectados para fases posteriores:

- Limpieza y transformación completa de datos.
- Análisis exploratorio más profundo.
- Visualizaciones comparativas entre países y regiones.
- Análisis del periodo pre y post COVID-19.
- Interpretación de resultados.
- Posible modelación predictiva de la tasa de penetración de gimnasios.

---

## Articulación con fases F1-F4

| Fase | Propósito |
|---|---|
| F1 | Definir problemática, organizar entorno reproducible, crear notebook inicial y documentar decisiones técnicas. |
| F2 | Realizar limpieza, preparación y transformación del dataset. |
| F3 | Ejecutar análisis exploratorio, visualizaciones y comparaciones entre países o regiones. |
| F4 | Interpretar resultados, elaborar conclusiones y evaluar posible modelación predictiva. |

---

## Estado del proyecto

**Fase actual:** Fase 1 - Implementación inicial del entorno reproducible y documentación técnica.

En esta fase se define la problemática, se organiza el repositorio, se configura el entorno inicial, se crea el notebook de definición, se documentan las primeras decisiones técnicas, se implementan ramas de trabajo, se valida automáticamente la estructura del proyecto mediante GitHub Actions, se ejecuta el notebook en CI y se incorpora GitHub Models para mejorar la documentación de Pull Requests.

---

## Referencias iniciales

Mishra, A. (2026). *World Gym & Fitness Trends 2000-2026* [Conjunto de datos]. Kaggle.

pandas development team. (2024). *pandas documentation*. https://pandas.pydata.org/docs/

Python Software Foundation. (2024). *Python documentation*. https://docs.python.org/3/

Project Jupyter. (2024). *Jupyter documentation*. https://docs.jupyter.org/

GitHub Docs. (2024). *GitHub Docs*. https://docs.github.com/

Makridakis, S., Spiliotis, E., & Assimakopoulos, V. (2018). Statistical and machine learning forecasting methods: Concerns and ways forward. *PLoS ONE, 13*(3), e0194889. https://doi.org/10.1371/journal.pone.0194889
