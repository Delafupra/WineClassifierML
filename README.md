 Descripción del Proyecto

WineClassifierML es un modelo de clasificación basado en Machine Learning que predice la calidad del vino tinto usando datos químicos.

✅ Objetivo: Predecir si un vino tendrá baja, media o alta calidad con base en sus características químicas.✅ Dataset: Se utilizó el conjunto de datos "winequality-red.csv", que contiene información sobre 1599 vinos tintos con 11 variables químicas, como acidez, alcohol y sulfatos.✅ Modelos utilizados:

Random Forest Classifier 🌲

LightGBM Classifier ⚡
✅ Optimización: Se aplicó RandomizedSearchCV y SMOTE para mejorar la detección de vinos de baja calidad.✅ Evaluación: Se utilizaron métricas como Accuracy, F1-score y Matriz de Confusión para medir el desempeño.

📊 Datos y Análisis Exploratorio

El dataset contiene 12 columnas:

Características químicas: fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, sulphates, alcohol, etc.

Variable objetivo: quality (de 3 a 8, donde 3 es de menor calidad y 8 es de mayor calidad).

Durante el análisis exploratorio (EDA), se descubrieron patrones interesantes:
📌 Los vinos con mayor contenido de alcohol tienden a tener mejor calidad.📌 La acidez volátil tiene una correlación negativa con la calidad (más acidez = menor calidad).📌 El dataset estaba desbalanceado, con muy pocos vinos de calidad baja (clase 3 y 4).

🛠️ Implementación del Modelo

1️⃣ Preprocesamiento de Datos

Se creó una nueva variable categórica quality_category, dividiendo los vinos en baja, media y alta calidad.

Se aplicó StandardScaler para normalizar los datos.

Se crearon nuevas características como total_acidity = fixed_acidity + volatile_acidity.

2️⃣ Entrenamiento de Modelos

Se probaron Random Forest y LightGBM.

Se aplicó GridSearchCV para encontrar los mejores hiperparámetros.

Se utilizó SMOTE para equilibrar las clases y mejorar la predicción de vinos de baja calidad.

3️⃣ Evaluación del Modelo

Métrica

Random Forest

LightGBM

Accuracy

83%

87%

F1-score ponderado

0.83

0.87

Clase 0 (baja calidad) - Recall

0.15

0.15

🔹 LightGBM tuvo el mejor desempeño en general, pero aún hay dificultades para predecir vinos de baja calidad.

💡 Conclusiones y Próximos Pasos

🔹 LightGBM fue el modelo más preciso para predecir la calidad del vino.🔹 El modelo tiene problemas con la clase 0 (baja calidad), por lo que se recomienda recolectar más datos.🔹 Factores clave como el alcohol y los sulfatos influyen directamente en la calidad del vino.

📌 Futuras mejoras:

Obtener más datos de vinos de baja calidad para mejorar la predicción de la clase 0.

Probar modelos como XGBoost o una combinación de modelos (VotingClassifier).

Explorar nuevas características químicas para mejorar la predicción.


📬 Contacto

📌 Desarrollado por: Diego De la Fuente Prats📌 LinkedIn: https://www.linkedin.com/in/diegodelafuenteprats/ 📌 GitHub: Delafupra 📌 Email: diegodelaf18@gmail.com

Si te gustó este proyecto, ¡no olvides darle ⭐ en GitHub! 🚀🍷

