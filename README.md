# Ajuste de Hiperparámetros con RandomForestClassifier

**Redactado por:** Sofía Andrea Cruz Durán.

--------
Este proyecto implementa técnicas de ajuste de hiperparámetros aplicadas al modelo `RandomForestClassifier` usando el dataset Heart Disease UCI. El objetivo principal fue comparar el desempeño de tres enfoques de entrenamiento:

1. Modelo baseline (hiperparámetros por defecto).
2. Búsqueda aleatoria (`RandomizedSearchCV`).
3. Optimización bayesiana (`Optuna`).

### 📊 DATASET:  *Heart Disease UCI*
- Fuente: Kaggle
- Observaciones: 918
- Variables predictoras: 11 (mixtas: numéricas y categóricas)
- Variable objetivo: `HeartDisease` (0 = no, 1 = sí)

## 🧪 Metodología

- División del dataset en entrenamiento y prueba (80/20).
- Preprocesamiento de variables categóricas con `ColumnTransformer` y `OneHotEncoder`.
- Validación cruzada con 5 folds.
- Evaluación mediante la métrica **ROC AUC**.

## 📈 Resultados

### ROC AUC promedio en validación cruzada (entrenamiento):

- Baseline: 0.9222  
- Random Search: 0.9289  
- Optuna: 0.9296  

### ROC AUC en conjunto de prueba:

- Baseline: 0.9314  
- Random Search: 0.9272  
- Optuna: 0.9289  

## ✅ Conclusiones

- El modelo baseline fue más competitivo desde el inicio.
- Las técnicas de ajuste ofrecieron mejoras leves pero no determinantes.
- Optuna mostró un enfoque eficiente para la optimización de hiperparámetros.