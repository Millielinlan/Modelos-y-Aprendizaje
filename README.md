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

    ![image](https://user-images.githubusercontent.com/115441451/194829077-724b1a02-79fd-4215-a549-a2659d3ccce9.png)


Se utilizó el 75% del dataset para training de los modelos utilizados y 25% para test. Se utilizó una función para obtener el accuracy de los modelos tanto en training como test y se graficó la matriz de confusión.

   ![image](https://user-images.githubusercontent.com/115441451/194828531-612962c9-f11e-440f-8851-26c6ae9b76cb.png)


Se evaluaron los siguientes modelos, teniendo el accuracy con el mayor porcentaje entre los modelos utilizados. Adicionalmente, se registran 3 modelos con el 100% de accuracy en training.
 
    ![image](https://user-images.githubusercontent.com/115441451/194828576-e80719e1-6baa-4f1d-9c69-e798d83f87e6.png)


En el caso de los modelos SVC y SGD se obtienen los mejores resultados:

    •	En el caso del modelo SGDClassifier, la matriz de confusión presenta:
      o	1 caso clasificado como “Maligno” y que corresponde a un caso “Benigno, y
      o	3 casos clasificados como “Benigno” y que corresponden a casos “Malignos”
    Adicional, presenta accuracy del 97% en test.
    
    ![image](https://user-images.githubusercontent.com/115441451/194828673-49f00f3c-7a24-439c-a502-a08eadc5d243.png)

 

    •	En el caso del modelo SVC, la matriz de confusión presenta:
      o	3 casos clasificados como “Maligno” y que corresponde a casos “Benigno”, y
      o	1 caso clasificado como “Benigno” y que corresponde a un caso “Maligno”
    Adicional, presenta también accuracy del 97% en test.
 
    ![image](https://user-images.githubusercontent.com/115441451/194828729-01a9070d-92dd-4c9a-8523-fc105cb4021f.png)


      • En el caso del modelo LogisticRegression, la matriz de confusión presenta:
        o	0 casos clasificados como “Maligno” y que corresponde a caso “Benigno”, y
        o	2 casos clasificados como “Benigno” y que corresponde a un caso “Maligno”
        Adicional, presenta accuracy del 98% en test.
        
        ![image](https://user-images.githubusercontent.com/115441451/194828759-bbdc9ddc-7346-4233-a7de-c5e1afba2a7b.png)

	 
Personalmente, utilizaría el modelo SVC, por cuanto presenta la matriz de confusión con un caso maligno clasificado como benigno. Si bien, es cierto que en conteo general de los errores cometidos los otros modelos no presentan malos número, optaría por el modelo SVC debido a que es el que menor cantidad de casos malignos mal clasificados tiene. 
Si bien perseguimos obtener la menor cantidad de casos mal clasificados en ambos, un caso mal clasificado como maligno tiene menor impacto que un caso clasificado como benigno cuando no lo es.

        ![image](https://user-images.githubusercontent.com/115441451/194829154-59560c12-c884-4c9e-9307-a1c75129fc96.png)


Muchas Gracias por la retroalimentación. 

Saludos
