### ¿Qué determina el precio de un seguro de automóvil?

**Fernando Santiago Sanchez Sarmiento**

#### Resumen ejecutivo
Cada vez que uno adquiere una póliza de seguros para un automóvil se pregunta si el costo de la prima es justo y se encuentra en el promedio del mercado y mejor aún si está por debajo del promedio.
En el mercado las empresas aseguradoras para definir sus precios de las primas tienen diferentes estratégicas, unas se enfocan en el alcance de las coberturas, otras en proporcionar servicios adicionales y otras mas audaces en el comportamiento del conductor. Este proyecto tomará la información que las aseguradoras consideran relevantes hoy en día para realiza la cotización a sus clientes. 
El producto final de este proyecto es la creación de un modelo para predicir el precio de una póliza de seguros y saber cuáles son los principales factores que impactan en este precio que constituye la base de la creación de un startup que seguidamente buscará socios inversionistas para la creación de una aplicación Web y móvil.
#### Fundamento
Las personas antes de adquirir o renovar una póliza de seguro de automóvil desearían saber si van a pagar el precio justo para el alcance de la cobertura y servicios que se ofrece. Para ello el cliente o futuro asegurado puede contar con la información necesaria para tomar una decisión, conociendo cuales son las características mas importantes que definen el precio de una póliza. Con este conocimiento podrían negociar con las aseguradoras y ajustar estas características para obtener un precio al alcance de su presupuesto de ser necesario.  
#### Pregunta de investigación
Cuales son las principales características en la determinación del precio de un seguro de automóvil por parte de las empresas aseguradoras. Esta información será útil para un cliente nuevo o antiguo que quisiera renovar su póliza.
#### Fuentes de datos
Los datos que se utilizarán para responder las pregunta son los datos de ingreso a los cotizadores más los datos de respuesta de estas aplicaciones. Los datos de entrada fueron preparados tratando de cubrir los diversos tipos de automóviles, marcas, modelos y fechas de fabricación entre otros datos relevantes y como respuesta de las aplicaciones obtuvimos un tipo de tarifa, valor comercial del vehículo, la cobertura, servicios adicionales y el costo de la prima.
Estos son los datos de entrada.<br>
•	Nombre de la persona que solicita el seguro.<br>
•	Fecha de nacimiento
•	Documento de identidad
•	Placa (opcional)
•	Dirección
•	Año de fábrica del vehículo
•	Uso del vehículo
Esta es la información de salida de la aplicación en línea
•	Precio comercial del vehículo
•	Plan que ofrece la aseguradora
•	Cobertura de la póliza que depende del plan ofrecido.
•	Servicios adicionales
•	Historial de siniestralidad del conductor. (*)

(*) En la etapa de entendimiento de los datos se verificará si estos datos son necesarios para el análisis.
#### Metodología
Para predecir el precio de una póliza de automóvil y determinar los principales factores que influyen en este precio, emplearemos técnicas de Machine Learning supervisado (regresión) y análisis de importancia de características.
Para seleccionar el modelo para predecir el valor de la prima probaremos los modelos:  Regresión lineal regularizada, que es muy interpretativa y nos permitirá obtener coeficientes asociados a cada característica para identificar los factores mas importantes. Y usaremos la regularización Lasso para manejar colinealidad o muchas características irrelevantes.
Random Forest, que captura relaciones no lineales entre las características y el precio. También, permite obtener la importancia de las características.
Gradient Boosting XGBoost, es un modelo más avanzado y potente que los árboles simples y ofrecen medidas precisas de importancia de características. 
#### Resultados
1.	Mejor modelo es Lasso que tiene el menor MAE (37.11), lo que indica que, en promedio, las predicciones del modelo están más cerca de los valores reales que los otros modelos.
2.	También tiene menor MSE (5,390.79), mostrando que penaliza menos los errores grandes comparado con los otros modelos.
3.	Lasso alcanza un R² de 0.9985, indicando que explica el 99.85% de la varianza en los datos. Este es el valor más alto entre los tres modelos, sugiriendo un ajuste excelente.
4.	Lasso es el modelo más rápido de entrenar (58.96 segundos), siendo significativamente más eficiente que RandomForest y XGBRegressor.
5.	Con relación al análisis de Lasso, la característica más importante es el Valor comercial: 1,935.67 con mayor influencia positiva en el modelo, Modelo_target: 409.79 representa una fuerte relación positiva y las interacciones cuadráticas y combinaciones: Ano de fabrica^2 Modelo_target y Ano de fabrica Modelo_target tienen coeficientes altos, indicando que las interacciones son importantes.
6.	La Permutation Importance en el modelo Lasso muestra que la característica Modelo_target tiene la mayor importancia (0.992), lo que confirma que esta característica tiene un gran impacto en las predicciones. Valor comercial también es importante (0.176), aunque con menor peso en comparación con Modelo_target. Las variables categóricas como Aseguradora_Mapfre Perú y Plan de seguro tienen menor impacto

#### Próximos pasos
Una vez obtenido el modelo de predicción de precio de una póliza de automóviles se buscará socios inversionistas quienes deben de financiar una aplicación web y móvil.
Seguidamente, debemos ejecutar todos los pasos que sigue una empresa emergente (Startup) para lanzar su producto o servicio al mercado, como la realización de un MVP para probarlo cuanto antes en el mercado.
Como resultado de estas pruebas o experimentos con el usuario podremos identificar nuevos insights que podríamos incluir en la solución previa evaluación.
Paralelamente, podríamos ir mejorando el modelo con las siguientes actividades:
1. Para mejorar el análisis se debe incrementar los datos de entrenamiento. Esto requiere de mayor esfuerzo considerando que el ingreso de los datos en el cotizador se realiza de forma manual.
2. Realizar pruebas para la selección de la mejor técnica de transformación de características categóricas a numéricas de tal forma de evitar los problemas de multidimensionalidad y overfitting.
3. Considerar otras características que impactan en el precio de la póliza que no se encuentra en la cotización que genera la aplicación en línea, como son descuentos adicionales por no haber sufrido siniestros importantes en el último año, para el caso de renovaciones.

#### Esquema del proyecto

- [Enlace al cuaderno 1]()
- [Enlace al cuaderno 2]()
- [Enlace al cuaderno 3]()

##### Contacto e información adicional
