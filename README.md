# PROYECTO INDIVIDUAL #2 : MACHINE LEARNING


<p align="center">
<img src="https://raw.githubusercontent.com/isaacpc94/PI02_DATA05/main/images/MChospital.jpg"  height=300><br>

# DESCRIPCION DEL PROYECTO :

El siguiente proyecto tiene como objetivo predecir si un paciente estará hospitalizado más de 8 dias o no, por lo cual se cuenta con una data de 90000 registros, para el cual se aplicó modelos de clasificación en busca de obtener métricas "recall" y "accuracy" mayor a 70%.<br>
<br>

# FEATURE ENGINEER :

-  Se carga el archivo "hospitalizacions_test.csm en la carpeta "Archivos train y test".
-  Se hizo un EDA de los datos, no encontrnado duplicados ni valores "Null".
-  Se encuentra los valores unícos para cada feature con el fin de conocer si son categóricos o numéricos.
<br>
<br>

# FEATURE ENCODING :
-  Se convierte valores categóricos a numericos cada feature aplicando "One hot encoder", "label encoder"
-  Se aplica un escalado a las features como MinMax y StandardScaler.
-  El feature "patientid" no se considera ya que so en su mayoria unicos y no se les puede relacionar con el objetivo que es la columna "Stay (in days)"
-  Se obtiene un Dataframe con solo valores numéricos y se obtendrán 6 tipos de muestra:<br>
    Las 3 primeras muestras presenta outliers en el feature "Admission_Deposit".
    - Dataframe con todas las features
    - Dataframe excluyendo las featues con un factor de correlacion <0.1
    - Dataframe excluyendo las featues con un factor de correlacion <0.01<br>

    Las 3 ultimas muestras no presentan outliers en el feature "Admission_Deposit".
    - Dataframe con todas las features
    - Dataframe excluyendo las featues con un factor de correlacion <0.1
    - Dataframe excluyendo las featues con un factor de correlacion <0.01<br>
<br>

# MODELING:
- Se divide el Dataframe en una muestra de 70% para entrenamiento y 30 % para testeo.
- Se busca los mejores hiperparámetros con scoring = "accuracy "para los modelos de "DecisionTreeClassifier" y "KNeighborsClassifier"
- De todas las pruebas la primera prueba es la mejor con los siguientes hiperparemtros:
    - 'criterion': 'gini' 
    - 'max_depth': 22
- Este modelo tiene  un "accuracy > 75% y un "recall" > 80% , lo cual supera el objetivo.
<p align="center">
<img src="https://raw.githubusercontent.com/isaacpc94/PI02_DATA05/main/images/resultadoML.jpg"  height=100><br>


# PREDICTION : 

- En la carpeta "pred", esta el archivo "csv" con la prediccion para el archivo "hospitalizaciones_test.csv"

