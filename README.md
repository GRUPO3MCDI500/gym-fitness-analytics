# Análisis global de la industria fitness y gimnasios 2000-2026

## Integrantes

- Wilson Arévalo
- Lucas Espinosa
- Integrante 3: __________________________
- Integrante 4: __________________________

---

## Descripción del proyecto

Este proyecto corresponde a la Fase 1 del ABP y tiene como propósito iniciar un flujo de trabajo reproducible para analizar la evolución global de la industria fitness y gimnasios entre los años 2000 y 2026.

El análisis se basa en un dataset que contiene información sobre membresías de gimnasio, participación fitness, ingresos del sector, cantidad de gimnasios, tasa de penetración, PIB per cápita, urbanización, obesidad e inactividad física en distintos países y regiones.

En esta primera fase se define la problemática, se formulan los objetivos, se organiza el repositorio, se configura el entorno inicial de trabajo, se crea el notebook base y se documentan las primeras decisiones técnicas del proyecto.

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

## CI/CD con GitHub Actions

Se implementó un workflow de integración continua mediante GitHub Actions, ubicado en:

```text
.github/workflows/main.yml
```

Este workflow se ejecuta automáticamente ante cada actualización en la rama `main` y cumple las siguientes funciones:

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
| Evento de ejecución | push a la rama `main` |
| Estado esperado | exitoso |

La implementación de CI/CD permite detectar errores tempranos de estructura, dependencias o carga del dataset, aportando a la reproducibilidad técnica del proyecto.

---
## Resumen automático de Pull Requests con GitHub Models

Además del workflow principal de CI/CD, se implementó un workflow complementario basado en **GitHub Models** para apoyar la documentación automática de los cambios realizados mediante Pull Requests.

Este workflow se encuentra en:

```text
.github/workflows/ai-pr-summary.yml
```

Su objetivo es generar automáticamente un resumen técnico cada vez que se abre, actualiza o reabre un Pull Request dirigido a la rama `main`.

### Funcionamiento general

El flujo de trabajo se ejecuta bajo el siguiente proceso:

```text
Pull Request hacia main
        ↓
GitHub Actions ejecuta el workflow AI - Resumen de Pull Request
        ↓
Se identifican los archivos modificados
        ↓
Se clasifica el tipo de cambio realizado
        ↓
GitHub Models genera un resumen técnico automático
        ↓
El resumen se publica como comentario en el Pull Request
        ↓
El resumen también se guarda como artifact descargable
```

### Qué analiza el workflow

El workflow revisa los archivos modificados en el Pull Request y clasifica el cambio según el tipo de componente afectado:

| Tipo de cambio        | Archivos o carpetas relacionadas        |
| --------------------- | --------------------------------------- |
| Notebook              | `notebooks/F1_Definicion.ipynb`         |
| Documentación         | `README.md`                             |
| Dataset               | `data/` y `data/raw/clean_gym_data.csv` |
| CI/CD                 | `.github/workflows/`                    |
| Documentación técnica | `docs/`                                 |
| Informe o evidencias  | `reports/`                              |

### Contenido del resumen generado

El resumen automático generado por GitHub Models incluye:

* Tipo de cambio detectado.
* Archivos modificados.
* Impacto técnico del cambio.
* Relación del cambio con la Fase 1 del proyecto.
* Riesgos o puntos de atención.
* Validaciones recomendadas.
* Observación final sobre si el Pull Request parece seguro para fusionarse con `main`, siempre que las validaciones pasen.

### Dónde se puede ver el resumen

El resumen generado por la IA puede revisarse en tres lugares:

| Ubicación                     | Descripción                                                                            |
| ----------------------------- | -------------------------------------------------------------------------------------- |
| Comentario en el Pull Request | El workflow publica o actualiza automáticamente un comentario dentro del Pull Request. |
| Logs de GitHub Actions        | El resumen se imprime en el paso `Mostrar resumen en logs`.                            |
| Artifact descargable          | El archivo `resumen_ai.md` se guarda como artifact bajo el nombre `resumen-ai-pr`.     |

### Checklist automático de revisión

El workflow también agrega un checklist automático para apoyar la revisión del Pull Request antes de fusionarlo a `main`. Este checklist puede incluir verificaciones como:

```text
- El workflow principal CI - Validacion Fase 1 está en verde.
- El Pull Request fue revisado antes de fusionarse a main.
- Los cambios son coherentes con el objetivo de Fase 1.
- La estructura del repositorio se mantiene ordenada.
- El notebook F1_Definicion.ipynb fue ejecutado sin errores, si fue modificado.
- El README mantiene formato y contenido actualizado, si fue modificado.
- El dataset mantiene columnas y estructura esperada, si fue modificado.
- Los workflows funcionan correctamente, si se modificó CI/CD.
- La documentación técnica y el mapa conceptual están actualizados, si se modificó docs/.
- Los anexos o informe de Fase 1 están correctamente ubicados, si se modificó reports/.
```

### Relación con la reproducibilidad

La incorporación de GitHub Models fortalece la trazabilidad y documentación del proyecto, ya que cada Pull Request recibe una explicación automática sobre los cambios realizados y su posible impacto técnico.

Este workflow no reemplaza al CI/CD principal, sino que lo complementa. Mientras el workflow `CI - Validacion Fase 1` verifica estructura, dependencias, dataset y columnas principales, el workflow `AI - Resumen de Pull Request` apoya la revisión documental y colaborativa mediante una síntesis generada automáticamente.

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

En esta fase se define la problemática, se organiza el repositorio, se configura el entorno inicial, se crea el notebook de definición, se documentan las primeras decisiones técnicas y se valida automáticamente la estructura del proyecto mediante GitHub Actions.

---

## Referencias iniciales

Mishra, A. (2026). *World Gym & Fitness Trends (2000-2026)* [Conjunto de datos]. Kaggle.

pandas development team. (2024). *pandas documentation*. https://pandas.pydata.org/docs/

Python Software Foundation. (2024). *Python documentation*. https://docs.python.org/3/

Project Jupyter. (2024). *Jupyter documentation*. https://docs.jupyter.org/

GitHub Docs. (2024). *GitHub Docs*. https://docs.github.com/
