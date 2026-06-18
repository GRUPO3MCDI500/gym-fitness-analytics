# Fase 3 - Núcleo algorítmico, eficiencia y POO

## Proyecto

Análisis global de la industria fitness y gimnasios 2000-2026.

## Objetivo de la Fase 3

Implementar el núcleo algorítmico del sistema utilizando programación estructurada, recursiva y orientada a objetos, incorporando mediciones de complejidad temporal y espacial, validaciones técnicas y documentación reproducible mediante Jupyter Notebooks.

## Relación con fases anteriores

En Fase 1 se configuró el entorno reproducible, se organizó el repositorio y se documentó la estructura inicial del proyecto.

En Fase 2 se implementó el pipeline de obtención, limpieza y transformación de datos.

En Fase 3 se reutilizan los datos procesados y se amplía el proyecto hacia algoritmos, mediciones de complejidad y principios de Programación Orientada a Objetos.

## Dataset requerido

Entrada raw:

```text
data/raw/clean_gym_data.csv
```

Salida procesada:

```text
data/processed/gym_data_processed.csv
```

## Orden de ejecución

```text
1. F3_01_Preprocesamiento.ipynb
2. F3_02_Algoritmos.ipynb
3. F3_03_Mediciones.ipynb
4. F3_04_Nucleo_POO.ipynb
5. F3_05_Integrador_Resultados.ipynb
```

## Descripción de notebooks

| Notebook | Propósito |
|---|---|
| F3_01_Preprocesamiento.ipynb | Limpieza, transformación, validación y exportación del dataset procesado. |
| F3_02_Algoritmos.ipynb | Implementación de algoritmos estructurados, recursivos y exploración de grafos. |
| F3_03_Mediciones.ipynb | Medición de tiempo, memoria y comparación de implementaciones. |
| F3_04_Nucleo_POO.ipynb | Implementación de clases, herencia, encapsulamiento y polimorfismo. |
| F3_05_Integrador_Resultados.ipynb | Integración de resultados y soporte al informe técnico. |

## Algoritmos implementados

| Algoritmo | Tipo | Complejidad temporal | Complejidad espacial |
|---|---|---|---|
| Ranking iterativo | Estructurado | O(n log n) | O(n) |
| Máximo iterativo | Estructurado | O(n) | O(1) |
| Máximo recursivo con slicing | Recursivo | O(n) | O(n) |
| Máximo recursivo optimizado | Recursivo optimizado | O(n) | O(log n) |
| Promedio manual por región | Estructurado | O(n) | O(k) |
| Promedio Pandas por región | Pandas groupby | O(n) aprox. | O(k) |
| DFS recursivo sobre grafo regional | Recursivo / grafos | O(V + E) | O(V) |

## Programación Orientada a Objetos

El notebook `F3_04_Nucleo_POO.ipynb` implementa:

- `DatasetFitness`
- `AlgoritmoBase`
- `RankingFitness`
- `MaximoFitness`
- `PromedioRegionalFitness`
- `MedidorComplejidad`
- `ExperimentoAlgoritmico`

Se aplican:

- Encapsulamiento.
- Herencia.
- Polimorfismo.
- Alta cohesión.
- Bajo acoplamiento.
- Métodos documentados.

## Dependencias

```text
pandas==2.2.2
numpy==1.26.4
matplotlib==3.9.2
jupyter==1.1.1
notebook==7.2.2
ipykernel==6.29.5
nbconvert==7.16.4
```

## Ejecución

Desde la raíz del proyecto:

```bash
jupyter notebook
```

Luego abrir los notebooks en el orden indicado.

## Evidencias recomendadas

Guardar capturas en:

```text
reports/fase3/evidencias/
```

Evidencias sugeridas:

```text
01_preprocesamiento.png
02_algoritmos.png
03_mediciones.png
04_grafico_tiempo.png
05_grafico_memoria.png
06_nucleo_poo.png
07_integrador.png
08_commits.png
09_readme_f3.png
```

## Referencias

- Cormen, T. H., Leiserson, C. E., Rivest, R. L., & Stein, C. (2022). Introduction to algorithms.
- Python Software Foundation. Python documentation.
- The pandas development team. Pandas documentation.
- Project Jupyter. Jupyter documentation.
- Material docente Fase 3, MCDI500.
