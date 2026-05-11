# RegresionLogistica

Problema:  

Imagina que eres un investigador médico que recopila datos para un estudio. Has recopilado datos sobre un conjunto de pacientes, todos ellos con la misma enfermedad. Durante su tratamiento, cada paciente ha respondido a uno de los 5 medicamentos, el fármaco A, el fármaco B, el fármaco C (de proveedor nacional), el fármaco X y el Y (de proveedor extranjero). 

Parte de tu trabajo consiste en construir un modelo para averiguar qué medicamento podría ser apropiado para un futuro paciente con la misma enfermedad. Los conjuntos de características de este conjunto de datos son la edad, el sexo, la presión arterial y el colesterol de los pacientes, y el objetivo es estudiar el fármaco al que respondió cada paciente. 

De manera particular para este problema, se requiere saber si el medicamento a aplicar es de origen nacional o extranjero.

1. Cargue la base de datos “drugs.csv” en Python e investigue cómo convertir las variables predictoras cualitativas de esta base a una escala numérica mediante la instrucción “preprocessing.LabelEncoder()”. Por ejemplo, si una variable tiene 3 posibles categorías, deberá cambiar sus resultados a 0, 1 o 2.

Se transformaron las variables 'Sex', 'BP' y 'Cholesterol'.

2. Use diversos métodos de optimización para una Regresión Logística para encontrar un algoritmo óptimo de clasificación. Explique cuál sería su recomendación para este caso.

Los métodos de optimización utilizados fueron: 'sag', 'newton-cg', 'liblinear', 'saga' y 'lbfgs'.

En este caso, los métodos de optimización con las mejores precisiones son 'newton-cg' y 'lbfgs', los cuales obtuvieron 95% en precisión.

3. ¿Qué tan eficaz es el algoritmo predictivo escogido? Explique a detalle comentando sobre los indicadores obtenidos mediante el reporte de clasificación correspondiente y la curva ROC.

<img width="560" height="447" alt="image" src="https://github.com/user-attachments/assets/91d3d9c5-34e4-4123-9a90-4809c2afb0d1" />

El algoritmo predictivo escogido (lbfgs) es bastante efectivo, ya que el área debajo de la curva es de 0.90, muy cercano a 1, por lo que se puede considerar que el modelo tiene buena precisión. Por otra parte, el reporte de clasificación muestra una precisión para predecir los casos de fármacos de proveedor nacional de 83% y para proveedor extranjero de 97%. La predicción global o accuracy es de 95%. 
