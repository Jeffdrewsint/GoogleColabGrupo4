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
- Se aplicó escalamiento de la variable Amount y normalización de otras variables.
- Se usaron métricas adaptadas para desbalance: matriz de confusión, recall, precisión, F1-score y ROC-AUC.

### Resultados

| Métrica           | Valor   |
|-------------------|---------|
| Accuracy          | XX.XX%  |
| Precision (fraude) | XX.XX%  |
| Recall (fraude)    | XX.XX%  |
| F1-score (fraude)  | XX.XX%  |
| ROC-AUC           | XX.XX%  |

*Interpretación:*  
El modelo logra identificar correctamente un porcentaje importante de fraudes (recall alto), aunque con algunos falsos positivos, lo que es crucial para minimizar pérdidas económicas.

---

## Conclusiones

- El dataset tiene características que permiten diferenciar transacciones fraudulentas, pero su fuerte desbalance requiere técnicas específicas.
- La Regresión Logística, aunque simple, es un buen punto de partida para la detección de fraude.
- Visualizaciones y análisis estadísticos apoyan la selección de variables y comprensión del fenómeno.
- Futuras mejoras podrían incluir modelos más complejos, técnicas de balanceo y validación cruzada.

---

## Referencias

- Dataset: https://www.kaggle.com/mlg-ulb/creditcardfraud
- Documentación scikit-learn: https://scikit-learn.org

---

## Autor

- Jefferson A. Gaibor
- Jonathan Briceño
- Saul Contreras



