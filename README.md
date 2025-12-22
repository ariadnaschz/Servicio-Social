# 🟦 Introducción

La asignación de materias a docentes es un problema recurrente en la planeación académica, ya que debe equilibrar múltiples factores como preferencias, disponibilidad y criterios institucionales. Tradicionalmente, este proceso se realiza de forma manual, lo que puede derivar en asignaciones subóptimas, inconsistencias y una alta carga administrativa.

Este repositorio presenta una solución matemática y computacional a dicho problema, modelándolo como un problema de optimización sobre grafos bipartitos. En particular, la asignación se formula como un emparejamiento máximo ponderado, donde los pesos representan las preferencias de los docentes por determinadas materias.

El proyecto implementa un flujo completo que incluye:

* Limpieza y estandarización de datos.
* Construcción de grafos bipartitos docente–materia.
* Asignación de pesos basada en preferencias.
* Aplicación de algoritmos de emparejamiento máximo.
* Análisis de los resultados obtenidos.

Por motivos de privacidad, los datos reales utilizados en el contexto institucional original no se incluyen en este repositorio. En su lugar, se proporcionan datos de ejemplo anonimizados que permiten reproducir y comprender el funcionamiento del modelo sin comprometer información sensible.

Este trabajo surge como parte de un proyecto de servicio social, y tiene como objetivo demostrar la aplicación de herramientas matemáticas, algoritmos y programación para resolver problemas reales de asignación y optimización.

# 🧠 Metodología

El problema de asignación de materias a docentes se aborda mediante un enfoque de optimización combinatoria, utilizando herramientas de teoría de grafos y análisis de datos. La metodología empleada consta de las siguientes etapas:

# 1️⃣ Recolección y preparación de datos

Los datos de entrada consisten en preferencias de los docentes respecto a las materias disponibles. Cada docente puede indicar un conjunto ordenado de materias, reflejando distintos niveles de prioridad.

Antes de la modelación, los datos pasan por un proceso de:

* Limpieza y eliminación de valores faltantes.
* Normalización de cadenas de texto.
* Estandarización del formato de los datos.
* Transformación de preferencias en valores numéricos (pesos).

Con el fin de preservar la privacidad, en este repositorio se utilizan datos sintéticos anonimizados, que conservan la estructura lógica del problema original.

# 2️⃣ Modelación mediante grafos bipartitos

El problema se modela como un grafo bipartito $G=(U,V,E)$, donde:
* $U$ representa el conjunto de docentes.
* $V$ representa el conjunto de materias (UEAs).
* $E$ es el conjunto de aristas que conectan docentes con materias.

Cada arista $(u,v)\in E$ posee un peso $w(u,v)$, el cual representa el grado de preferencia del docente $u$ por la materia $v$.

# 3️⃣ Construcción de aristas ponderadas

A partir de los datos procesados, se generan aristas únicamente cuando existe una preferencia válida. Los pesos se asignan conforme a criterios definidos (por ejemplo, prioridad alta, media o baja), permitiendo cuantificar las preferencias dentro del modelo matemático.

Este paso traduce la información cualitativa de las preferencias en una representación cuantitativa adecuada para la optimización.

# 4️⃣ Emparejamiento máximo ponderado

El objetivo del modelo es encontrar un subconjunto de aristas $M \subseteq E$ tal que:

* Ningún nodo participe en más de una arista de $M$.
* La suma de los pesos de las aristas en $M$ sea máxima.

Formalmente, se busca maximizar:

$$\max \sum_{(u,v)\in M} w(u,v)$$

Este problema se resuelve mediante algoritmos de emparejamiento máximo ponderado, que garantizan una asignación óptima bajo las restricciones del modelo.

# 5️⃣ Obtención y análisis de resultados

El emparejamiento obtenido proporciona una asignación óptima de materias a docentes, respetando las preferencias y maximizando la satisfacción global del sistema.

Los resultados pueden analizarse para:

* Evaluar el nivel de satisfacción alcanzado.
* Detectar posibles problematicas.
* Ajustar pesos o restricciones en futuros periodos académicos.

# 🎯 Ventajas del enfoque

* Permite automatizar un proceso tradicionalmente manual.
* Proporciona una solución óptima desde el punto de vista matemático.
* Es flexible y adaptable a distintos contextos académicos.
* Facilita la transparencia y reproducibilidad del proceso de asignación.

# 🔎 Nota para el lector

Aunque el proyecto original fue desarrollado en un contexto institucional específico, el modelo presentado es general y reutilizable, pudiendo aplicarse a distintos problemas de asignación y optimización.