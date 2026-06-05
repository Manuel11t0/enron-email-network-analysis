# Enron Email Network Analysis

Este proyecto realiza un análisis de redes sociales usando la red de correos electrónicos de Enron.  
El objetivo principal es estudiar cómo se conectan los empleados dentro de la red, identificar nodos importantes y analizar qué tan robusta es la estructura de comunicación.

## Descripción

En este proyecto se trabaja con un archivo `.mtx` que contiene interacciones de correo electrónico entre empleados de Enron.  
A partir de estos datos se construye una red no dirigida usando `NetworkX`, donde:

- Cada nodo representa un empleado.
- Cada arco representa una interacción por correo electrónico entre dos empleados.

Aunque el archivo contiene origen y destino, la red se analiza como no dirigida, ya que el interés principal es estudiar la existencia de comunicación entre empleados.

## Tecnologías utilizadas

- Python
- Pandas
- NumPy
- NetworkX
- Matplotlib
- Google Colab

## Objetivos del proyecto

- Cargar y explorar los datos de correos electrónicos.
- Construir una red no dirigida.
- Analizar la estructura general de la red.
- Identificar nodos con mayor y menor grado.
- Calcular métricas importantes de conectividad.
- Analizar la resiliencia de la red.
- Detectar nodos de articulación y arcos puente.
- Calcular medidas de centralidad.
- Visualizar la red usando diferentes criterios.

## Análisis realizado

Durante el proyecto se realizan los siguientes pasos:

1. Importación de librerías.
2. Carga manual del archivo `.mtx`.
3. Lectura del archivo en un DataFrame.
4. Revisión básica de los datos.
5. Construcción de la red no dirigida.
6. Análisis de nodos, arcos, componentes y densidad.
7. Visualización general de la red.
8. Cálculo del grado de los nodos.
9. Visualización de nodos según su grado.
10. Cálculo del diámetro de la red.
11. Cálculo del promedio de caminos más cortos.
12. Verificación de si la red es bipartita.
13. Análisis de la distribución del grado.
14. Identificación de nodos de articulación.
15. Identificación de arcos puente.
16. Cálculo de centralidades.
17. Análisis de robustez de la red.
18. Exportación de resultados a archivos CSV.

## Métricas utilizadas

El proyecto calcula diferentes métricas de análisis de redes, entre ellas:

- Grado de los nodos
- Densidad de la red
- Diámetro
- Promedio de caminos más cortos
- Componentes conexas
- Nodos de articulación
- Arcos puente
- Centralidad de grado
- Centralidad de cercanía
- Centralidad de intermediación
- Centralidad eigenvector
- PageRank

## Centralidades analizadas

Se calculan varias medidas de centralidad para identificar empleados importantes dentro de la red:

- **Centralidad de grado:** mide cuántas conexiones directas tiene cada nodo.
- **Centralidad de cercanía:** mide qué tan rápido puede llegar un nodo al resto de la red.
- **Centralidad de intermediación:** identifica nodos que funcionan como puentes entre otros empleados.
- **Centralidad eigenvector:** detecta nodos conectados con otros nodos importantes.
- **PageRank:** mide la importancia de cada nodo tomando en cuenta la estructura general de conexiones.

## Archivos generados

El proyecto exporta dos archivos CSV con resultados importantes:

```text
grados_nodos_enron.csv
centralidades_enron.csv
