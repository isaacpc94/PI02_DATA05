# PI02_DATA05
PI02 dataton machine learning
Pasos para el modelado:

-  Se hizo un EDA de los datos, encontrando valores unicos para cada feature.
-  Se convierte valores categóricos a numericos cada feature aplicando "One hot encoder", "label encoder"
-  Se aplica un escalado a las features como MinMax y StandardScaler.
-  Se obtiene un Dataframe con solo valores numéricos(no se considera el feature "pacient_id") del cual se obtendrán 6 tipos de muestra:<br>
    Las 3 primeras muestras presenta outliers en el feature "Admission_Deposit".
    - Dataframe con todas las features
    - Dataframe excluyendo las featues con un factor de correlacion <0.1
    - Dataframe excluyendo las featues con un factor de correlacion <0.01<br>

    Las 3 ultimas muestras no presentan outliers en el feature "Admission_Deposit".
    - Dataframe con todas las features
    - Dataframe excluyendo las featues con un factor de correlacion <0.1
    - Dataframe excluyendo las featues con un factor de correlacion <0.01<br>

