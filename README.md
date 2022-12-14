# Proyecto_Salary_Prediction
## CONTENIDO 馃搼
[1 - Objetivo 馃幆](#O)<br />
[2 - Preparaci贸n de los datos 馃洜锔廬(#PR)<br />
[3 - Machine Learning 馃](#ML)<br />
 
## 1 - OBJETIVO 馃幆<a name="O"/>   
馃挜 Cargar, limpiar y preparar los datos para su buena adecuaci贸n para el proceso de machine learning. <br />
馃挜 Encontrar el modelo de machine learning que menor error (RMSE) proporcione en la predicci贸n de salarios de trabajos de Data. <br />
馃挜 Realizar una predicci贸n con el formato concreto para la competici贸n de Kaggle con los compa帽eros del bootcamp. <br />

## 2 - PREPARACI脫N DE LOS DATOS 馃洜锔? <a name="PR"/> 
猡碉笍 Cargamos los archivos CSV de Data y Test (convertimos a dataframe).<br />

鉂? Eliminamos registros considerados Outliers. <br />

馃З Unimos (concatenamos) los dataframes de Data y Test.<br />

馃捈 Recategorizamos JOB_TITLE agrupando los trabajos en: Data Analyst, Data Scientist, Data Engineer.<br />

馃實 Limpiamos la columna COMPANY_LOCATION qued谩ndonos con los 20 paises m谩s repetidos y recategorizando en "others" el resto.<br />

馃獧 A帽adimos datos nuevos al dataframe incluyendo el SALARIO_MEDIO por pa铆s.<br />

馃敘 Limpiamos los datos y a帽adimos el C脫DIGO del pa铆s.<br />

馃 Calculamos nueva columna con un FACTOR que representa en qu茅 proporci贸n es superior el salario de Data Scientist y Data Engineer a Data Analyst ( asumimos un 15% y 20% de media en el mundo respectivamente).<br />

馃挵 Creamos nueva columna con SALARIO_MEDIO_PONDERADO donde multiplicamos el salario medio del pa铆s por el factor proporcional anterior.<br />

鈿欙笍 Aplicamos Get Dummies (creamos 90 columnas).<br />

## 3 - MACHINE LEARNING 馃<a name="ML"/> 
鈻讹笍 Creamos una funci贸n para aplicar Machine Learning que nos inicializa, entrena y calcula errores de 18 modelos: <br />

&emsp; &emsp;鈥? Linear Regression (LinReg)<br />
&emsp; &emsp;鈥? Least Absolute Shrinkage and Selection Operator (Lasso) <br />
&emsp; &emsp;鈥? Ridge Regression (Ridge) <br />
&emsp; &emsp;鈥? Elastic Net Regression (Elastic)<br />
&emsp; &emsp;鈥? Logistic Regression (LogReg)<br />
&emsp; &emsp;鈥? Random Forest Regressor (RFR)<br />
&emsp; &emsp;鈥? Extra Trees Regressor (ETR)<br />
&emsp; &emsp;鈥? Support Vector Regression (SVR)<br />
&emsp; &emsp;鈥? Click Through Rate (CTR)<br />
&emsp; &emsp;鈥? Extreme Gradient Boosting (XGBR)<br />
&emsp; &emsp;鈥? Gradient Boosting Regressor (GBR)<br />
&emsp; &emsp;鈥? Light Gradient Boosted Machine (LGBMR)<br />
&emsp; &emsp;鈥? Gaussian Naive Bayes (GNB)<br />
&emsp; &emsp;鈥? Linear Model Bayesian Ridge (RegBR)<br />
&emsp; &emsp;鈥? K-Nearest Neighbors (KNN)<br />
&emsp; &emsp;鈥? Catboost Regressor (Cat)<br />
&emsp; &emsp;鈥? Stochastic Gradient Descent Regressor (SGD)<br />
&emsp; &emsp;鈥? Kernel Ridge Regression (KerRid)<br />

鈥硷笍 Detectamos que el modelo que minimiza el error es KernelRidge.<br />

猡达笍 Calculamos predicciones con KernelRidge, creamos archivo de sample y subimos los datos.<br />

