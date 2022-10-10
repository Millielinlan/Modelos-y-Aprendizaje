# Identificación Cáncer de Mama 

## Cáncer de Mama en Ecuador
  En el año 2020 fallecieron más del 29% de las mujeres que presentaron diagnóstico de Cáncer de mama en Ecuador. En el año en mención se diagnosticaron 3563 casos, por lo que un diagnóstico temprano es de vital importancia hoy en día.
  Se estima que el 13% de los casos a nivel mundial puede evitarse, por lo que se debe tener en cuenta las recomendaciones de los especialistas, quienes insisten en que cuando la enfermedad se presenta en familiares, la probabilidad de padecerla aumenta entre el 5% al 10%.

Proyecto Modelos y Aprendizajes
El presente trabajo se realizó utilizando el dataset "wdbc.data" de la UC que fue descargado del siguiente link: https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)

El dataset consta de 569 casos cada uno con 30 variables, que se dividen en:
          Casos Benignos: 357 que corresponde al 63%
          Casos Malignos: 212 que corresponde al 37%
          
Para esto se realizó un conteo junto con el gráfico correspondiente.

   ![image](https://user-images.githubusercontent.com/115441451/194828347-03e426c2-28d8-45a2-b975-9fecd5928a4a.png)


 
Se procedió a revisar el dataset, verificando el tipo de datos de las columnas, las mismas que poseen tipo de dato numérico excepto la variable objetivo “diagnosis”. Se validó también que no existieron campos vacíos.

   ![image](https://user-images.githubusercontent.com/115441451/194828412-837ccbed-1e78-43e3-b181-078dcf6675ed.png)


Se categoriza la variable objetivo con los valores: 1 maligno y 0 benigno y se elimina la columna “Id”.

![image](https://user-images.githubusercontent.com/115441451/194829627-b996a95f-ffb1-4688-b81c-4855bb9e0ff8.png)



Se utilizó el 75% del dataset para training de los modelos utilizados y 25% para test. Se utilizó una función para obtener el accuracy de los modelos tanto en training como test y se graficó la matriz de confusión.

   ![image](https://user-images.githubusercontent.com/115441451/194828531-612962c9-f11e-440f-8851-26c6ae9b76cb.png)


Se evaluaron los siguientes modelos, teniendo el accuracy con el mayor porcentaje entre los modelos utilizados. Adicionalmente, se registran 3 modelos con el 100% de accuracy en training.

![image](https://user-images.githubusercontent.com/115441451/194829846-435d8732-e7c6-4ab9-9ec6-a73fa539f661.png)


En el caso de los modelos SVC y SGD se obtienen los mejores resultados:

•	En el caso del modelo SGDClassifier, la matriz de confusión presenta:
	 o	1 caso clasificado como “Maligno” y que corresponde a un caso “Benigno, y
	 o	3 casos clasificados como “Benigno” y que corresponden a casos “Malignos”.
	 Adicional, presenta accuracy del 97% en test.
	 
![image](https://user-images.githubusercontent.com/115441451/194831155-615185d2-99b2-4d3f-966d-053cab18bcb0.png)


 •	En el caso del modelo SVC, la matriz de confusión presenta:
     	o	3 casos clasificados como “Maligno” y que corresponde a casos “Benigno”, y
 	o	1 caso clasificado como “Benigno” y que corresponde a un caso “Maligno”.
      	Adicional, presenta también accuracy del 97% en test.
	
![image](https://user-images.githubusercontent.com/115441451/194831465-d7ff5f82-5173-43d4-9e14-9db061f35455.png)
  

• En el caso del modelo LogisticRegression, la matriz de confusión presenta:
        o	0 casos clasificados como “Maligno” y que corresponde a caso “Benigno”, y
        o	2 casos clasificados como “Benigno” y que corresponde a un caso “Maligno”.
	Adicional, presenta accuracy del 98% en test.
	
![image](https://user-images.githubusercontent.com/115441451/194831532-253d4346-0cad-4f91-8bfd-210ff9063c9d.png)


	 
Personalmente, utilizaría el modelo SVC, por cuanto presenta la matriz de confusión con un caso maligno clasificado como benigno. Si bien, es cierto que en conteo general de los errores cometidos los otros modelos no presentan malos número, optaría por el modelo SVC debido a que es el que menor cantidad de casos malignos mal clasificados tiene. 
Si bien perseguimos obtener la menor cantidad de casos mal clasificados en ambos, un caso mal clasificado como maligno tiene menor impacto que un caso clasificado como benigno cuando no lo es.

![image](https://user-images.githubusercontent.com/115441451/194830207-35ff6d40-0dc7-4814-a08d-523a48fab95d.png)



Muchas Gracias por la retroalimentación. 

Saludos
