# Proyecto_Salary_Prediction
## CONTENIDO 📑
[1 - Objetivo 🎯](#O)<br />
[2 - Preparación de los datos 🛠️](#PR)<br />
[3 - Machine Learning 🤖](#ML)<br />
 
## 1 - OBJETIVO 🎯<a name="O"/>   
💥 Cargar, limpiar y preparar los datos para su buena adecuación para el proceso de machine learning. <br />
💥 Encontrar el modelo de machine learning que menor error (RMSE) proporcione en la predicción de salarios de trabajos de Data. <br />
💥 Realizar una predicción con el formato concreto para la competición de Kaggle con los compañeros del bootcamp. <br />

## 2 - PREPARACIÓN DE LOS DATOS 🛠️ <a name="PR"/> 
⤵️ Cargamos los archivos CSV de Data y Test (convertimos a dataframe).<br />

❌ Eliminamos registros considerados Outliers. <br />

🧩 Unimos (concatenamos) los dataframes de Data y Test.<br />

💼 Recategorizamos JOB_TITLE agrupando los trabajos en: Data Analyst, Data Scientist, Data Engineer.<br />

🌍 Limpiamos la columna COMPANY_LOCATION quedándonos con los 20 paises más repetidos y recategorizando en "others" el resto.<br />

🪙 Añadimos datos nuevos al dataframe incluyendo el SALARIO_MEDIO por país.<br />

🔢 Limpiamos los datos y añadimos el CÓDIGO del país.<br />

🤔 Calculamos nueva columna con un FACTOR que representa en qué proporción es superior el salario de Data Scientist y Data Engineer a Data Analyst ( asumimos un 15% y 20% de media en el mundo respectivamente).<br />

💰 Creamos nueva columna con SALARIO_MEDIO_PONDERADO donde multiplicamos el salario medio del país por el factor proporcional anterior.<br />

⚙️ Aplicamos Get Dummies (creamos 90 columnas).<br />

## 3 - MACHINE LEARNING 🤖<a name="ML"/> 
▶️ Creamos una función para aplicar Machine Learning que nos inicializa, entrena y calcula errores de 18 modelos: <br />

&emsp; &emsp;• Linear Regression (LinReg)<br />
&emsp; &emsp;• Least Absolute Shrinkage and Selection Operator (Lasso) <br />
&emsp; &emsp;• Ridge Regression (Ridge) <br />
&emsp; &emsp;• Elastic Net Regression (Elastic)<br />
&emsp; &emsp;• Logistic Regression (LogReg)<br />
&emsp; &emsp;• Random Forest Regressor (RFR)<br />
&emsp; &emsp;• Extra Trees Regressor (ETR)<br />
&emsp; &emsp;• Support Vector Regression (SVR)<br />
&emsp; &emsp;• Click Through Rate (CTR)<br />
&emsp; &emsp;• Extreme Gradient Boosting (XGBR)<br />
&emsp; &emsp;• Gradient Boosting Regressor (GBR)<br />
&emsp; &emsp;• Light Gradient Boosted Machine (LGBMR)<br />
&emsp; &emsp;• Gaussian Naive Bayes (GNB)<br />
&emsp; &emsp;• Linear Model Bayesian Ridge (RegBR)<br />
&emsp; &emsp;• K-Nearest Neighbors (KNN)<br />
&emsp; &emsp;• Catboost Regressor (Cat)<br />
&emsp; &emsp;• Stochastic Gradient Descent Regressor (SGD)<br />
&emsp; &emsp;• Kernel Ridge Regression (KerRid)<br />

‼️ Detectamos que el modelo que minimiza el error es KernelRidge.<br />

⤴️ Calculamos predicciones con KernelRidge, creamos archivo de sample y subimos los datos.<br />

