# Proyecto_9_Pozos_Petroleo / Oil wells

# Descripción del proyecto / Project Description

SPA:

Trabajas en la compañía de extracción de petróleo OilyGiant. Tu tarea es encontrar los mejores lugares donde abrir 200 pozos nuevos de petróleo.

Para completar esta tarea, tendrás que realizar los siguientes pasos:

   - Leer los archivos con los parámetros recogidos de pozos petrolíferos en la región seleccionada: calidad de crudo y volumen de reservas.
   - Crear un modelo para predecir el volumen de reservas en pozos nuevos.
   - Elegir los pozos petrolíferos que tienen los valores estimados más altos.
   - Elegir la región con el beneficio total más alto para los pozos petrolíferos seleccionados.

Tienes datos sobre muestras de crudo de tres regiones. Ya se conocen los parámetros de cada pozo petrolero de la región. Crea un modelo que ayude a elegir la región con el mayor margen de beneficio. Analiza los beneficios y riesgos potenciales utilizando la técnica bootstrapping.

EN:

You work in the oil extraction company OilyGiant. Your task is to find the best places to open 200 new oil wells.

To complete this task, you will need to perform the following steps:

   - Read files with parameters collected from oil wells in the selected region: oil quality and volume of reserves.
   - Create a model to predict the volume of reserves in new wells.
   - Choose the oil wells that have the highest estimated values.
   - Choose the region with the highest total profit for the selected oil wells.

You have data on oil samples from three regions. You already know the parameters of each oil well in the region. Create a model to help choose the region with the highest profit margin. Analyse the potential benefits and risks using the bootstrapping technique.


# Condiciones / Conditions :

SPA:

   - Solo se debe usar la regresión lineal para el entrenamiento del modelo.
   - Al explorar la región, se lleva a cabo un estudio de 500 puntos con la selección de los mejores 200 puntos para el cálculo del beneficio.
   - El presupuesto para el desarrollo de 200 pozos petroleros es de 100 millones de dólares.
   - Un barril de materias primas genera 4.5 USD de ingresos. El ingreso de una unidad de producto es de 4500 dólares (el volumen de reservas está expresado en miles de barriles).
   - Después de la evaluación de riesgo, mantén solo las regiones con riesgo de pérdidas inferior al 2.5%. De las que se ajustan a los criterios, se debe seleccionar la región con el beneficio promedio más alto.

Los datos son sintéticos: los detalles del contrato y las características del pozo no se publican.

EN: 

   - Only linear regression can be used for model training.
   - When exploring the region, a 500-point survey is carried out with the best 200 points selected for the calculation of the benefit.
   - The budget for the development of 200 oil wells is $100 million.
   - One barrel of raw materials generates 4.5 USD of revenue. The revenue from one unit of product is USD 4500 (the volume of reserves is expressed in thousands of barrels).
   - After the risk assessment, keep only regions with a risk of loss of less than 2.5%. Of those that fit the criteria, select the region with the highest average profit.

The data are synthetic: contract details and well characteristics will not be published.

# Descripción de datos / Data description

SPA:

Los datos de exploración geológica de las tres regiones se almacenan en archivos:

   - 'geo_data_0.csv.'
   - 'geo_data_1.csv.'
   - 'geo_data_2.csv.'
   - 'id' — identificador único de pozo de petróleo
   - f0, f1, f2 — tres características de los puntos (su significado específico no es importante, pero las características en sí son significativas)
   - 'product' — volumen de reservas en el pozo de petróleo (miles de barriles).

EN:

Geological exploration data from the three regions are stored in files:

   - 'geo_data_0.csv.'
   - 'geo_data_1.csv.'
   - 'geo_data_2.csv.'
   - 'id' — unique oil well identifier
   - f0, f1, f2 — three characteristics of the points (their specific meaning is not important, but the characteristics themselves are significant)
   - 'product' — volume of reserves in the oil well (thousands of barrels).

# Instrucciones del proyecto / Project instructions

SPA:

   1. Descarga y prepara los datos. Explica el procedimiento.

   2. Entrena y prueba el modelo para cada región en geo_data_0.csv:

       1. Divide los datos en un conjunto de entrenamiento y un conjunto de validación en una proporción de 75:25

       2. Entrena el modelo y haz predicciones para el conjunto de validación.

       3. Guarda las predicciones y las respuestas correctas para el conjunto de validación.

       4. Muestra el volumen medio de reservas predicho y RMSE del modelo.

       5. Analiza los resultados.

       6. Coloca todos los pasos previos en funciones, realiza y ejecuta los pasos 2.1-2.5 para los archivos 'geo_data_1.csv' y 'geo_data_2.csv'.

   3. Prepárate para el cálculo de ganancias:

       1. Almacena todos los valores necesarios para los cálculos en variables separadas.

       2. Dada la inversión de 100 millones por 200 pozos petrolíferos, de media un pozo petrolífero debe producir al menos un valor de 500,000 dólares en unidades para evitar pérdidas (esto es equivalente a 111.1 unidades). Compara esta cantidad con la cantidad media de reservas en cada región.

       3. Presenta conclusiones sobre cómo preparar el paso para calcular el beneficio.

   4. Escribe una función para calcular la ganancia de un conjunto de pozos de petróleo seleccionados y modela las predicciones:

       1. Elige los 200 pozos con los valores de predicción más altos de cada una de las 3 regiones (es decir, archivos 'csv').

       2. Resume el volumen objetivo de reservas según dichas predicciones. Almacena las predicciones para los 200 pozos para cada una de las 3 regiones.

       3. Calcula la ganancia potencial de los 200 pozos principales por región. Presenta tus conclusiones: propón una región para el desarrollo de pozos petrolíferos y justifica tu elección.

  5. Calcula riesgos y ganancias para cada región:

       1. Utilizando las predicciones que almacenaste en el paso 4.2, emplea la técnica del bootstrapping con 1000 muestras para hallar la distribución de los beneficios.

       2. Encuentra el beneficio promedio, el intervalo de confianza del 95% y el riesgo de pérdidas. La pérdida es una ganancia negativa, calcúlala como una probabilidad y luego exprésala como un porcentaje.

       3. Presenta tus conclusiones: propón una región para el desarrollo de pozos petrolíferos y justifica tu elección. ¿Coincide tu elección con la elección anterior en el punto 4.3?
    
EN:

   1. Download and prepare the data. Explain the procedure.
   
   2. Train and test the model for each region in geo_data_0.csv:

      1. Split the data into a training set and a validation set in a ratio of 75:25.
      
      2. Train the model and make predictions for the validation set.

      3. Save predictions and correct answers for the validation set.
  
      4. Displays the average predicted stock volume and RMSE of the model.
  
      5. Analyse the results.
     
      6. Place all previous steps in functions, perform and execute steps 2.1-2.5 for the files ‘geo_data_1.csv’ and ‘geo_data_2.csv’.

   3. Get ready for the profit calculation:

      1. Store all values needed for the calculations in separate variables.
     
      2. Given an investment of 100 million for 200 oil wells, an average oil well must produce at least $500,000 worth of units to avoid losses (this is equivalent to 111.1 units). Compare this amount with the average reserve amount in each region.
     
      3. Show the conclusions on how to prepare the step to calculate the benefit.
     
   4. Write a function to calculate the profit for a set of selected oil wells and model the predictions:

      1. Choose the 200 wells with the highest predicted values from each of the 3 regions (i.e. ‘csv’ files).
     
      2. Summarise the target volume of reserves based on these predictions. Store the predictions for the 200 wells for each of the 3 regions.
     
      3. Calculate the profit potential of the top 200 wells per region. Present your conclusions: propose a region for oil well development and justify your choice.

   5. Calculate risks and gains for each region:

      1. Using the predictions you stored in step 4.2, employ the bootstrapping technique with 1000 samples to find the distribution of benefits.
     
      2. Find the average profit, the 95% confidence interval and the risk of loss. The loss is a negative profit, calculate it as a probability and then express it as a percentage.
     
      3. Show your conclusions: propose a region for the development of oil wells and justify your choice. Does your choice coincide with the previous choice in 4.3?
