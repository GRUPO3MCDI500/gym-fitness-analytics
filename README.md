# Análisis global de la industria fitness y gimnasios 2000-2026

## Integrantes

- Wilson Arévalo
- Lucas Espinosa
- Eduardo Garrido
- Mauricio Ortega

---

## Descripción del proyecto

Este proyecto corresponde a la Fase 1 del ABP y tiene como propósito iniciar un flujo de trabajo reproducible para analizar la evolución global de la industria fitness y gimnasios entre los años 2000 y 2026.

El análisis se basa en un dataset que contiene información sobre membresías de gimnasio, participación fitness, ingresos del sector, cantidad de gimnasios, tasa de penetración, PIB per cápita, urbanización, obesidad e inactividad física en distintos países y regiones.

En esta primera fase se define la problemática, se formulan los objetivos, se organiza el repositorio, se configura el entorno inicial de trabajo, se crea el notebook base, se documentan las primeras decisiones técnicas y se implementa una validación automática mediante GitHub Actions.

---

## Problemática

La industria fitness y de gimnasios ha crecido de manera desigual a nivel mundial entre 2000 y 2026. Existen diferencias importantes entre países y regiones en cuanto a membresías, número de gimnasios, ingresos del sector, acceso a servicios fitness y participación de la población en actividades físicas.

A partir de esta situación, el proyecto busca comprender qué factores económicos, de acceso y de salud pública se relacionan con el crecimiento y adopción de la industria fitness a nivel global.

---

## Objetivo general

Analizar la evolución global de la industria fitness y gimnasios entre 2000 y 2026, identificando la relación entre el crecimiento del sector, el acceso a gimnasios, las condiciones económicas de los países y los indicadores de salud pública, mediante un flujo de trabajo reproducible apoyado en herramientas científicas colaborativas.

---

## Objetivos específicos

- Identificar las variables principales del dataset y su relación con la problemática del proyecto.
- Organizar una estructura inicial de repositorio que permita mantener trazabilidad y reproducibilidad.
- Implementar un notebook inicial de Fase 1 con carga, exploración y revisión preliminar del dataset.
- Documentar el proceso técnico mediante README, notebook y archivos de apoyo.
- Utilizar Git y GitHub para registrar avances mediante commits descriptivos.
- Configurar una validación inicial mediante GitHub Actions para verificar estructura, dependencias y carga del dataset.
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
| Nombre del dataset | World Gym & Fitness Trends (2000-2026) |
| Archivo utilizado | `clean_gym_data.csv` |
| Fuente | Kaggle |
| Periodo de análisis | 2000-2026 |
| Unidad de análisis | Países y regiones |

---

## Variables principales

El dataset contiene variables relacionadas con industria fitness, economía y salud pública:

| Variable | Descripción general |
|---|---|
| `country` | País registrado en el dataset. |
| `region` | Región geográfica del país. |
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

## Herramientas utilizadas

| Herramienta | Uso dentro del proyecto |
|---|---|
| Python | Lenguaje principal para análisis de datos. |
| Pandas | Carga, manipulación y exploración de datos. |
| NumPy | Apoyo en operaciones numéricas. |
| Matplotlib | Visualización inicial de datos. |
| Jupyter Notebook | Desarrollo del análisis reproducible mediante código y celdas narrativas. |
| Git | Control de versiones local. |
| GitHub | Repositorio remoto y colaboración grupal. |
| GitHub Desktop | Gestión visual de commits, cambios y sincronización con GitHub. |
| GitHub Actions | Validación automática de estructura, dependencias y carga del dataset. |

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
│       └── main.yml
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
```

---

## Reproducibilidad técnica

Para reproducir este proyecto, se recomienda clonar el repositorio, instalar las dependencias declaradas en `requirements.txt` y ejecutar el notebook principal de la Fase 1.

### Instalación de dependencias

Desde la carpeta raíz del repositorio, ejecutar:

```bash
pip install -r requirements.txt
```

### Dependencias principales

El archivo `requirements.txt` contiene las librerías necesarias para ejecutar el notebook:

```text
pandas
numpy
matplotlib
jupyter
notebook
ipykernel
```

### Ejecución del notebook

El notebook principal se encuentra en:

```text
notebooks/F1_Definicion.ipynb
```

Para ejecutarlo:

1. Abrir Anaconda Navigator.
2. Iniciar Jupyter Notebook.
3. Entrar a la carpeta del repositorio `gym-fitness-analytics`.
4. Abrir la carpeta `notebooks`.
5. Ejecutar el archivo `F1_Definicion.ipynb`.
6. Ejecutar las celdas en orden.

El notebook carga el dataset desde la ruta relativa:

```python
from pathlib import Path

DATA_PATH = Path("../data/raw/clean_gym_data.csv")
```

Esta ruta permite que el notebook funcione correctamente siempre que se respete la estructura del repositorio.

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
- Resumen estadístico inicial.
- Función simple de exploración.
- Primeras visualizaciones.
- Decisiones técnicas iniciales.
- Vinculación con el mapa conceptual.
- Proyección para fases posteriores.

---

## Control de versiones

El proyecto utiliza Git y GitHub para mantener trazabilidad de los avances. Los commits deben ser descriptivos y representar cambios específicos del proyecto.

### Ejemplos de commits realizados o esperados

```text
Crear estructura inicial del repositorio
Agregar dataset original de gimnasios
Crear notebook inicial de Fase 1
Actualizar README del proyecto
Agregar archivo de dependencias iniciales
Agregar mapa conceptual técnico
Agregar workflow de CI para Fase 1
Validar funcionamiento inicial de CI
Agregar informe técnico de Fase 1
```

---

## Estrategia de ramas del repositorio

Para organizar el trabajo colaborativo y evitar modificar directamente la rama principal `main`, se definió una estrategia de ramas basada en componentes del proyecto. Cada rama tiene un propósito específico y permite desarrollar, validar y documentar cambios antes de integrarlos a la versión principal del repositorio.

La rama `main` se mantiene como la versión estable del proyecto. Los cambios se trabajan primero en ramas secundarias tipo `feature/`, luego se validan mediante GitHub Actions y finalmente se integran a `main` mediante Pull Request, siempre que las validaciones sean exitosas.

### Rama principal

| Rama | Uso |
|---|---|
| `main` | Contiene la versión estable del proyecto. En esta rama se mantiene la estructura validada del repositorio, el README actualizado, el notebook principal, el dataset, la documentación y los archivos de configuración ya revisados. |

### Ramas de trabajo implementadas

| Rama | Uso principal | Archivos o carpetas asociadas |
|---|---|---|
| `feature/actualizar-notebook-f1` | Actualización del notebook principal de Fase 1. | `notebooks/F1_Definicion.ipynb` |
| `feature/actualizar-readme` | Mejora de la documentación principal del proyecto. | `README.md` |
| `feature/documentacion-fase1` | Incorporación de documentos de apoyo, mapa conceptual, anexos y evidencias. | `docs/`, `reports/fase1/` |
| `feature/ci-cd` | Modificación y prueba del workflow de integración continua. | `.github/workflows/main.yml` |
| `feature/dataset-validacion` | Revisión del dataset y sus validaciones iniciales. | `data/` |

---

## Uso de las ramas implementadas

### `feature/actualizar-notebook-f1`

Esta rama se utiliza para realizar modificaciones sobre el notebook principal de la Fase 1.

**Uso esperado:**

- Agregar o corregir celdas Markdown.
- Actualizar la problemática, objetivos o preguntas de análisis.
- Corregir la carga del dataset.
- Agregar revisiones iniciales de columnas, tipos de datos, nulos o duplicados.
- Incorporar visualizaciones preliminares.
- Verificar que el notebook se ejecute sin errores.

**Validación asociada:**

- Verifica que el notebook exista en `notebooks/F1_Definicion.ipynb`.
- Verifica que el dataset siga disponible en `data/raw/clean_gym_data.csv`.
- Comprueba que las dependencias estén declaradas en `requirements.txt`.
- Comprueba que el dataset pueda cargarse correctamente con Python y Pandas.

### `feature/actualizar-readme`

Esta rama se utiliza para modificar la documentación principal del proyecto.

**Uso esperado:**

- Mejorar la descripción del proyecto.
- Agregar o corregir integrantes.
- Documentar problemática, objetivos y preguntas de análisis.
- Explicar la estructura del repositorio.
- Incluir instrucciones para ejecutar el notebook.
- Documentar el uso de GitHub Actions y CI/CD.
- Agregar información sobre reproducibilidad técnica.

**Validación asociada:**

- Verifica que el archivo `README.md` exista.
- Verifica que la estructura general del repositorio no se vea afectada.
- Verifica que el resto de archivos necesarios para reproducibilidad sigan presentes.

### `feature/documentacion-fase1`

Esta rama se utiliza para incorporar documentos de apoyo, anexos, evidencias y archivos relacionados con la documentación formal de la Fase 1.

**Uso esperado:**

- Agregar el mapa conceptual final.
- Agregar evidencias del repositorio.
- Incorporar capturas del workflow de GitHub Actions.
- Guardar evidencias del notebook ejecutado.
- Agregar referencias o documentos complementarios.
- Preparar anexos técnicos del informe.

**Validación asociada:**

- Verifica que la carpeta `docs` exista.
- Verifica que la carpeta `reports` exista.
- Verifica que los archivos principales del proyecto se mantengan disponibles.
- Verifica que los cambios de documentación no rompan la estructura base del repositorio.

### `feature/ci-cd`

Esta rama se utiliza para modificar y probar la configuración de integración continua mediante GitHub Actions.

**Uso esperado:**

- Ajustar el workflow de GitHub Actions.
- Validar que el CI se ejecute en ramas `feature/`.
- Revisar que se instalen correctamente las dependencias.
- Verificar la carga automática del dataset.
- Confirmar que el workflow detecte errores de estructura.
- Mantener una validación automática antes de integrar cambios a `main`.

**Validación asociada:**

El workflow `CI - Validacion Fase 1` ejecuta las siguientes comprobaciones:

- Descarga el repositorio.
- Configura Python 3.11.
- Instala las dependencias desde `requirements.txt`.
- Verifica la existencia de archivos clave:
  - `README.md`
  - `requirements.txt`
  - `data/raw/clean_gym_data.csv`
  - `notebooks/F1_Definicion.ipynb`
- Verifica la existencia de carpetas clave:
  - `data`
  - `notebooks`
  - `docs`
  - `reports`
- Carga el dataset mediante Pandas.
- Comprueba que el dataset tenga filas y columnas.
- Valida que existan las columnas principales esperadas.

### `feature/dataset-validacion`

Esta rama se utiliza para trabajar cambios relacionados con el dataset y sus validaciones iniciales.

**Uso esperado:**

- Verificar que el dataset original esté correctamente ubicado.
- Confirmar que el archivo `clean_gym_data.csv` no haya sido modificado accidentalmente.
- Revisar columnas principales.
- Preparar posibles validaciones futuras sobre estructura, tipos de datos o valores faltantes.
- Mantener separado el dataset original de futuras versiones procesadas.

**Validación asociada:**

- Verifica que exista el archivo `data/raw/clean_gym_data.csv`.
- Verifica que el archivo pueda ser leído correctamente con Pandas.
- Verifica que el dataset no esté vacío.
- Verifica que estén presentes las columnas principales esperadas, como `country`, `region`, `year`, `gym_memberships`, `gdp_per_capita_usd`, `obesity_rate`, entre otras.

---

## Flujo de trabajo implementado

El flujo de trabajo actual se organiza de la siguiente forma:

```text
main
│
├── feature/actualizar-notebook-f1
├── feature/actualizar-readme
├── feature/documentacion-fase1
├── feature/ci-cd
└── feature/dataset-validacion
```

Cada rama se utiliza para un tipo de cambio específico. Una vez que los cambios están listos, se realiza un commit descriptivo y se hace push a GitHub. Luego, GitHub Actions ejecuta automáticamente las validaciones configuradas en `.github/workflows/main.yml`.

Si las validaciones pasan correctamente, los cambios pueden integrarse a `main` mediante Pull Request. Si las validaciones fallan, se corrigen los errores en la misma rama y se realiza un nuevo commit hasta obtener un resultado exitoso.

---

## CI/CD con GitHub Actions

Se implementó un workflow de integración continua mediante GitHub Actions, ubicado en:

```text
.github/workflows/main.yml
```

Este workflow se ejecuta automáticamente ante cada actualización en la rama `main`, en ramas `feature/` y en Pull Requests dirigidos a `main`.

El workflow cumple las siguientes funciones:

- Descarga el repositorio.
- Configura Python 3.11.
- Instala las dependencias desde `requirements.txt`.
- Verifica la estructura mínima del repositorio.
- Comprueba la existencia de `README.md`, `requirements.txt`, el dataset y el notebook.
- Carga el dataset `clean_gym_data.csv` mediante Python y Pandas.
- Verifica que el dataset contenga filas y columnas.
- Valida la presencia de las columnas principales esperadas.

### Evidencia CI/CD

| Elemento | Detalle |
|---|---|
| Workflow | CI - Validacion Fase 1 |
| Job | validar-proyecto |
| Archivo | `.github/workflows/main.yml` |
| Evento de ejecución | push a `main`, push a ramas `feature/` y Pull Request hacia `main` |
| Estado esperado | exitoso |

La implementación de CI/CD permite detectar errores tempranos de estructura, dependencias o carga del dataset, aportando a la reproducibilidad técnica del proyecto.

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
- Registro de dependencias en `requirements.txt`.
- Uso de Git/GitHub para trazabilidad.
- Implementación de validación automática mediante GitHub Actions.
- Organización de ramas de trabajo para separar cambios y validar actualizaciones antes de integrarlas a `main`.

Quedan proyectados para fases posteriores:

- Limpieza y transformación completa de datos.
- Análisis exploratorio más profundo.
- Visualizaciones comparativas entre países y regiones.
- Análisis del periodo pre y post COVID-19.
- Interpretación de resultados.
- Posible modelación predictiva de la tasa de penetración de gimnasios.

---

## Estado del proyecto

**Fase actual:** Fase 1 - Implementación inicial del entorno reproducible y documentación técnica.

En esta fase se define la problemática, se organiza el repositorio, se configura el entorno inicial, se crea el notebook de definición, se documentan las primeras decisiones técnicas, se implementan ramas de trabajo y se valida automáticamente la estructura del proyecto mediante GitHub Actions.

---

## Referencias iniciales

Mishra, A. (2026). *World Gym & Fitness Trends (2000-2026)* [Conjunto de datos]. Kaggle.

pandas development team. (2024). *pandas documentation*. https://pandas.pydata.org/docs/

Python Software Foundation. (2024). *Python documentation*. https://docs.python.org/3/

Project Jupyter. (2024). *Jupyter documentation*. https://docs.jupyter.org/

GitHub Docs. (2024). *GitHub Docs*. https://docs.github.com/
