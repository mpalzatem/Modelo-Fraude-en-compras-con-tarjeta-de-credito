**MODELOS**

Para la identificación de la probabilidad de fraude en tarjetas de créditos en diferentes comercios en Estados Unidos desde el 1 de enero de 2019
 hasta el 31 de diciembre de 2020, se utilizará dos modelos de clasificación, el primero fue del tipo KNN Means para analizar su correlación significativa  
y el segundo es el modelo Neuronal Madaline para realizar el pronóstico

**BASES DE DATOS**

La base original contenía más de mil datos e información de diversos estados, pero esta se modificó a la información de los comercios del estado de Florida, por lo que esta 
se redujo a 226 datos. Además, las variables cualitativas se modificaron en cuantitativas para poder trabajarlas en los modelos. 

**ANÁLISIS DE LOS RESULTADOS**


Para analizar la base de datos 'Data Fraud', la cual contiene información sobre casos de fraude en tarjetas de crédito en diferentes comercios en Estados Unidos, decidimos(en el Estado de Florida) seleccionamos las siguientes variables: 'gender','category','city','state','job','amt'y 'is_fraud'.

***Modelo KNN MEANS***
Inicialmente, se desarrolló un modelo KNN de clasificación, en el cual utilizamos como variable de salida 'is_fraud'; donde 0 es que no hubo fraude y 1 que sí lo hubo. Inicialmente con este modelo, quisimos analizar la correlación entre las variables para identificar si había una relación importante entre ellas, sin embargo, las gráficas nos muestran que ninguna se correlaciona significativamente entre sí, aunque si podemos ver que la variable que mejor puede diferenciar los datos es la de ciudad.

Luego procedimos a analizar los resultados de la evaluación del modelo, los cuales revelan que la precisión del modelo es 71.68%, lo cual es refleja un buen desempeño del modelo, pero no muy significativo. Así mismo, la sensibilidad es del 67.24%, lo que indica que el modelo logra identificar un porcentaje significativo de transacciones fraudulentas, pero que aún hay un margen de error por mejorar en la detección de fraude.

Por otro lado, la especificidad del 76.36% tiene una buena capacidad para distinguir transacciones legítimas, aunque igualmente existe el riesgo de clasificar erróneamente algunas como fraudulentas.

Finalmente, se analizaron los datos de un usuario aleatorio para conocer su clasificación dentro de un grupo, con la información: 1,6,0,0,10,1000; lo que significa que es un usuario femenino, la categoría de la compra es 'Personal care', ciudad West Palm Beach, estado de Florida, que el trabajo del usuario es health physicist y el valor de la transacción fue 1000 USD.

A lo que se encontró que pertenecería a un grupo 5, el cual, según los datos analizados demuestra que una persona con esas características socioeconómicas tiene una probabilidad del 100% de cometer fraude.


***MODELO NEURONAL MADALINE***

El segundo modelo utilizado, fue el modelo neuronal MADALINE, el cual nos sirve para realizar un pronóstico. Para este caso se tomó como variable (continua) de salida, la cual es 'amt'; monto de la transacción, y se tomó como valor de epoch 1000 y batch size de 26, teniendo en cuenta que es el 10% de los datos.



Teniendo en cuenta los resultados nos damos cuenta que hay una correlación positiva moderada (0.263978). Luego al observar los coeficientes de efectos independientes se puede observar que las variable categoría y ciudad, representan un impacto significativo en el modelo, ya que tienen mayor peso en él.

En cuanto a la discrepancia de las medias (que es de aproximadamente 4.6819) indica que hay diferencias notables entre las medias de los grupos en el conjunto de datos y que los datos están subestimados. Y la discrepancia entre dispersiones es de aproximadamente 73.82.

En la última gráfica se puede evidenciar que la distribución es desigual, donde el 1 que es representado por el color naranja tiene un menor recuento que el 0 que es representado por azul, el cual alcanza más de 60.
