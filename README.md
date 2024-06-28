# Prototipo-flow

## Introducción
Este proyecto se centra en el análisis de flujo no invasivo en reactores químicos industriales utilizando técnicas de aprendizaje profundo y flujo óptico. El objetivo es desarrollar una herramienta que permita monitorear y optimizar el funcionamiento de estos reactores, mejorando la eficiencia y reduciendo costos operativos.

## Objetivo
- Desarrollar un sistema basado en deep learning para el cálculo del flujo óptico en reactores electroquímicos, con el fin de mejorar la precisión en el análisis de la distribución del flujo y optimizar el rendimiento de los reactores.

## Metodología
### Enfoque Inicial
El primer enfoque del proyecto utilizó una combinación de algoritmos clásicos de cálculo de flujo óptico como Gunnar Farneback. Estos algoritmos, aunque efectivos en la obtención de vectores de flujo óptico, generaban resultados con un considerable nivel de ruido. Para abordar este problema, se implementó una red neuronal autoencoder con capas convolucionales diseñada para aprender a remover este ruido y obtener vectores de flujo óptico codificados con menos ruido.
![Red Propuesta](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/Prototipo_unet.png)

### Arquitectura del Modelo
La red propuesta es un autoencoder con capas convolucionales. La estructura del modelo comienza con 32 características y se expande a 128 antes de reducirse nuevamente. Este enfoque permite capturar características de diferentes niveles de complejidad del flujo óptico.

* **Capas Convolucionales**: Se utilizan para extraer características espaciales del flujo.
* **Activaciones ReLU**: Introducen no linealidades en el modelo, permitiendo que aprenda relaciones más complejas.
A continuación se muestra la arquitectura de la red propuesta:

![Red Propuesta](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/red_propuesta_.png)

## Entrenamiento
**Algoritmo de Optimización**: El modelo se entrenó utilizando el algoritmo Adam, conocido por su eficiencia en el ajuste de parámetros.

**Tasa de Aprendizaje**: Se utilizó una tasa de aprendizaje de $1\times 10^{-4}$, equilibrando la rapidez del entrenamiento con la estabilidad del mismo.

**Historial de Entrenamiento**: A continuación se muestra el historial de entrenamiento del modelo:

![Entrenamiento](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/Entrenamiento.png)

## Resultados
Los resultados obtenidos son visual y numericamente satisfactorios, mostrando la capacidad del modelo para generar imágenes de flujo óptico con ruido reducido.

Pérdida de Entrenamiento: $1.3740 \times 10^{-4}$
MSE de Entrenamiento: $1.3740 \times 10^{-4}$
Pérdida de Validación: $1.3466 \times 10^{-4}$
MSE de Validación: $1.346 \times 10^{-4}$
Estos resultados indican que el modelo tiene un buen rendimiento en términos de minimización de la pérdida y del error cuadrático medio, tanto en el conjunto de entrenamiento como en el de validación.

![Resultado 1](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/Resultado1.png)
![Resultado 2](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/Resultado2.png)
![Resultado 3](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/Resultado3.png)
![Resultado 4](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/Resultado4.png)
![Resultado 5](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/Resultado5.png)

Ventajas de RAFT:
Mejora visual del flujo óptico.
Resultados visuales más claros y detallados.

## Implementación de RAFT
Para mejorar aún más los resultados, se adoptó un enfoque utilizando el modelo RAFT. Este enfoque ha demostrado ser más robusto y preciso, mejorando la calidad del análisis de flujo sin necesidad de cálculos adicionales de flujo óptico.

A continuación se muestran algunos de los resultados visuales obtenidos con el modelo RAFT:

| Flujo óptico| Flujo óptico procesado por la red|
|:------------------------------:|:----------------------------------------------:|
| ![GIF de Resultados 1](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/bifurcado_o.gif) | ![GIF de Resultados 2](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/bifurcado.gif) |

| Flujo óptico| Flujo óptico procesado por la red|
|:------------------------------:|:----------------------------------------------:|
| ![GIF de Resultados 2](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/canalizado_o.gif) | ![GIF de Resultados 2](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/canalizado.gif) |

| Flujo óptico| Flujo óptico procesado por la red|
|:------------------------------:|:----------------------------------------------:|
| ![GIF de Resultados 3](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/original_o.gif) | ![GIF de Resultados 2](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/original.gif) |

## Demo app


![Demoa app](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/Resultado1.png)
