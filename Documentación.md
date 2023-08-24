# Olympic Data Analysis

En esta implementación, exploré la aplicación de la regresión lineal manual para predecir si los atletas ganarían medallas en los Juegos Olímpicos. 
Utilicé un conjunto de datos históricos de los Juegos Olímpicos, que abarca desde Atenas 1896 hasta Río 2016. El objetivo era comprender cómo las 
características individuales de los atletas, como su edad, altura, peso y género, podrían influir en sus posibilidades de ganar una medalla.

## Pasos Realizados
#### Carga y Preprocesamiento de Datos: 
Comencé cargando el conjunto de datos en un DataFrame de Pandas. Realicé una limpieza inicial para manejar los valores nulos, cambiándolos por las medias de sus columnas para conservar la estructura
y finalmente convertí los tipos de datos según fuera necesario.

#### Definición de la Función de Hipótesis: 
Creé la función de hipótesis que se utiliza en la regresión lineal para estimar las probabilidades de ganar una medalla en función de las características del atleta.

#### Optimización con Gradiente Descendente: 
Implementé el método de gradiente descendente para ajustar los coeficientes de regresión y reducir el error entre las predicciones y los resultados reales. 
Esto permitió que el modelo se adaptara a los datos de entrenamiento.

#### Sigmoid y Clasificación: 
Utilicé la función sigmoid para transformar las predicciones continuas en valores de probabilidad entre 0 y 1. 
Luego, establecí un umbral para clasificar a los atletas en dos categorías: "Gana Medalla" o "No Gana Medalla", según la probabilidad estimada.

#### Cálculo del Error Cuadrático Medio: 
En cada época durante el entrenamiento, calculé el error cuadrático medio (MSE) para evaluar la calidad del modelo y entender cómo mejoraba con cada iteración.

#### Interpretación de Coeficientes: 
Una vez finalizado el entrenamiento, analicé los coeficientes finales de la regresión. Estos coeficientes permitieron entender qué características 
tenían un mayor impacto en la probabilidad de ganar una medalla.

#### Predicción en un Nuevo Conjunto de Datos: 
Finalmente, utilicé el modelo entrenado para realizar predicciones en el mismo conjunto de datos de atletas, solo eliminando la columna de medallas.
Estas predicciones se basaron en las características de los atletas y proporcionaron una estimación de sus posibilidades de ganar medallas.

## Intentos de implementación y Oportunidad
Durante el proceso de exploración y análisis de los datos históricos de los Juegos Olímpicos, se llevaron a cabo varios intentos que no resultaron en predicciones exitosas. 
Uno de estos intentos involucró la incorporación de un dataset de atletas de la NBA con la esperanza de predecir si algún jugador ganaría una medalla olímpica. Sin embargo, este intento no tuvo éxito.
A pesar de las expectativas iniciales, este resultado subraya la importancia de considerar cuidadosamente la calidad y la pertinencia de los datos al realizar análisis y predicciones.

## Resultados

El modelo final no mostró mejoras significativas después de las iteraciones y ajustes realizados. El MSE no era lo suficientemente bajo para garantizar una 
alta precisión en la predicción. Es importante señalar que la calidad del conjunto de datos, con una gran cantidad de variables categóricas, limitó la capacidad de predicción del modelo.

Utilizar métricas de evaluación más completas para medir el rendimiento del modelo.

#### Feature Engineering: 
Explorar más características relevantes y realizar análisis de su impacto en la predicción. A pesar de que el dataset no contaba con los datos necesarios para realizar una predicción buena, debo decir que habría sido más interesante 
analisarlo si tuviera datos como: Experiencia previa en los Juegos Olímpicos, Clasificación previa en campeonatos mundiales, Características físicas específicas (envergadura, la fuerza, la agilidad)
