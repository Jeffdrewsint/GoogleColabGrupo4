# GoogleColabGrupo4
Tratamiento de Datos Google Colab/ Python
# Detección de Fraude en Tarjetas de Crédito

## Introducción

La detección de fraude en tarjetas de crédito es un problema crítico en la industria financiera. Este proyecto explora un dataset real para entender las características de las transacciones fraudulentas y legítimas, y construye un modelo predictivo para su detección.

---

## Dataset

Se utiliza el dataset **Credit Card Fraud Detection** de Kaggle con 284,807 transacciones y 31 variables, incluyendo 28 variables anonimadas (V1 a V28), además de tiempo, monto y clase (fraude o no).

El dataset presenta un fuerte desbalance, con solo el 0.17% de las transacciones clasificadas como fraude.

---

## Análisis Exploratorio

- Confirmamos ausencia de valores nulos y desbalance de clases.
- Visualizamos la distribución de montos, tiempos y clases.
- Identificamos variables con correlación significativa con la clase fraude (V17, V14, V12, V10).
- Observamos patrones interesantes en los montos y momentos de las transacciones.

---

## Modelado Predictivo

Para evaluar la capacidad predictiva de las variables, se construyó un modelo de **Regresión Logística** usando scikit-learn, con las siguientes características:

- Se tomó una muestra estratificada para entrenamiento y prueba (70%-30%).
- Se aplicó escalamiento de la variable `Amount` y `Time` (las demás variables ya estaban PCA-transformadas).
- Se usaron métricas adaptadas para desbalance: matriz de confusión, recall, precisión, F1-score y ROC-AUC.

### Resultados

| Métrica             | Valor   |
|---------------------|---------|
| Accuracy            | 99.92%  |
| Precision (fraude)  | 86.00%  |
| Recall (fraude)     | 61.00%  |
| F1-score (fraude)   | 72.00%  |
| ROC-AUC             | 95.60%  |

**Matriz de Confusión:**

*Interpretación:*  
El modelo logra un alto nivel de exactitud general y un buen desempeño en la detección de fraudes, con una precisión del 86% y un recall del 61% para la clase fraude. Esto significa que identifica correctamente la mayoría de fraudes, aunque todavía deja escapar algunos (falsos negativos). El valor de ROC-AUC de 0.956 indica un buen poder discriminativo.

---

## Conclusiones

- El dataset presenta un fuerte desbalance que impacta el recall para fraudes.
- La Regresión Logística es capaz de obtener resultados sólidos, con buena precisión y un ROC-AUC alto.
- El recall puede mejorarse aplicando técnicas como *oversampling* (SMOTE), *undersampling* o modelos más complejos (árboles de decisión, XGBoost, redes neuronales).
- Las visualizaciones y análisis estadísticos ayudan a entender el comportamiento de las transacciones y a guiar la selección de variables.

---

**Herramientas Utilizadas**
-Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Plotly)
-Jupyter Notebook / Google Colab
-GitHub para control de versiones


--
## Referencias

- Dataset: [Credit Card Fraud Detection - Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud)  
- Documentación scikit-learn: https://scikit-learn.org

---

## Autor

- Jefferson A. Gaibor
- Jonathan Briceño
- Saul Contreras



