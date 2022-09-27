# Proyecto_Salary_Prediction
-------------------------------------------------------------------------------------------------------------------------
En este repositoria se añadirán las actualizaciones del proyecto de predicción de salarios.
-------------------------------------------------------------------------------------------------------------------------
Cargamos Data y Test.
-------------------------------------------------------------------------------------------------------------------------
Eliminamos Outliers.
-------------------------------------------------------------------------------------------------------------------------
Concatenamos Data-Test para transformaciones de datos.
-------------------------------------------------------------------------------------------------------------------------
Recategorizamos job_title agrupando los trabajos en: Data Analyst, Data Scientist, Data Engineer.
-------------------------------------------------------------------------------------------------------------------------
Limpiamos la columna company_location quedándonos con los 20 paises más repetidos y recategorizando en "others" el resto.
-------------------------------------------------------------------------------------------------------------------------
Añadimos nuevos datos: Salario medio por país.
-------------------------------------------------------------------------------------------------------------------------
Limpiamos los nuevos datos, añadimos lo código por país (nuevos datos).
-------------------------------------------------------------------------------------------------------------------------
Calculamos en qué % es superior Data Scientist y Data Engineer a Data Analyst (15% y 20%).
-------------------------------------------------------------------------------------------------------------------------
Creamos nueva columna con el salario medio añadido anteriormente multiplicando por el factor según el trabajo.
-------------------------------------------------------------------------------------------------------------------------
Aplicamos Get Dummies (creamos 90 columnas).
-------------------------------------------------------------------------------------------------------------------------
Creamos una función para aplicar Machine Learning que nos inicializa, entrena y calcula errores de 18 modelos: 'LinReg', 'Lasso', 'Ridge', 'Elastic', 'LogReg', 'RFR', 'ETR', 'SVR', 'CTR', 'XGBR', 'GBR', 'LGBMR', 'GNB', 'RegBR', 'KNN', 'Cat', 'SGD', 'KerRid'.
-------------------------------------------------------------------------------------------------------------------------
Detectamos que el modelo que minimiza el error es KernelRidge.
-------------------------------------------------------------------------------------------------------------------------
Calculamos predicciones con KernelRidge, creamos archivo de sample y subimos los datos.
-------------------------------------------------------------------------------------------------------------------------
