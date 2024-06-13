# Prototipo-flow

## Introducción
Este proyecto se centra en el análisis de flujo no invasivo en reactores químicos industriales utilizando técnicas de aprendizaje profundo y flujo óptico.

## Objetivos
- Desarrollar un sistema basado en deep learning para analizar la distribución del flujo en reactores electroquímicos.

## Metodología
- La red propuesta es un autoencoder con capas convolucionales que comienza con 32 características y se expande a 128 antes de reducirse.
- Utiliza activaciones ReLU para introducir no linealidades.

![Red Propuesta](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/red_propuesta_.png)

## Entrenamiento
- Se entrenó la red utilizando el algoritmo Adam con una tasa de aprendizaje de 1x10^-4.
- Aquí se muestra el historial de entrenamiento:

![Entrenamiento](https://github.com/DanielAntonioGJ/Prototipo-flow/blob/main/Kits19_subset_UNet_training_history.png)

## Resultados
- Los resultados del entrenamiento muestran una pérdida de 1.3740x10^-4 y un MSE de 1.3740x10^-4.
- La validación muestra una pérdida de 1.3466x10^-4 y un MSE de 1.346x10^-4.

## Uso del Modelo
- Instrucciones para usar el modelo entrenado para hacer predicciones en nuevos datos.

## Contribuciones
- Se invita a la comunidad a reportar issues y sugerir mejoras.

## Referencias
- [1] L. Arenas and J. Smith, “Critical analysis of electrode materials for electrochemical applications,” Journal of Electrochemical Science, 2020.
- [2] J. Escudero-González, P. Amparo Lopez-Jimenez, “Redox cell hydrodynamic modelling: Towards real improved geometry based on CFD analysis,” Engineering Applications of Computational Fluid Mechanics, 2014.
