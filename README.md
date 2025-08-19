# 📊 TelecomX - Parte 2: Predicción de Cancelación de Clientes

Este repositorio contiene el análisis y modelado predictivo de cancelación de clientes (*churn*) para una empresa de telecomunicaciones. Se aplicaron técnicas de preprocesamiento, balanceo de clases, normalización, y modelos supervisados para identificar patrones de abandono.

---

## 📁 Archivos

- `TelecomX_parte_2.ipynb`: Notebook principal con todo el flujo de trabajo.
- `datos_normalizados.csv`: Dataset tratado desde la Parte 1.
- `README.md`: Este archivo.

---

## 🧪 Dataset

- **Observaciones**: 7,032 clientes
- **Variables**: 21 columnas tras limpieza
- **Variable objetivo**: `Churn` (0 = No canceló, 1 = Canceló)

---

## ⚙️ Flujo de trabajo

1. **Carga y limpieza de datos**
   - Eliminación de columnas irrelevantes (`customerID`)
   - One-Hot Encoding para variables categóricas

2. **Análisis exploratorio**
   - Distribución de `Churn`
   - Correlación entre variables
   - Visualizaciones dirigidas (contrato, cargos, antigüedad)

3. **Preprocesamiento**
   - Balanceo con SMOTE
   - Normalización con `StandardScaler`

4. **Modelado**
   - Regresión Logística (con y sin SMOTE)
   - Random Forest (con y sin SMOTE)

5. **Evaluación**
   - Métricas: Accuracy, Precision, Recall, F1-score
   - Matriz de confusión
   - Comparación gráfica de modelos

---

## 📈 Resultados

| Modelo                      | Accuracy | Precision | Recall | F1-score |
|----------------------------|----------|-----------|--------|----------|
| Regresión Logística        | 0.80     | 0.70      | 0.58   | 0.63     |
| Regresión Logística + SMOTE| 0.78     | 0.66      | 0.65   | 0.65     |
| Random Forest              | 0.79     | 0.68      | 0.59   | 0.63     |
| Random Forest + SMOTE      | 0.77     | 0.64      | 0.67   | 0.65     |

✅ **Mejor modelo en recall**: Random Forest + SMOTE  
✅ **Mejor equilibrio general**: Regresión Logística + SMOTE

---

## 🔍 Variables más influyentes

- `customer.tenure`: mayor antigüedad reduce el churn
- `account.Contract_Month-to-month`: contratos mensuales aumentan el riesgo
- `account.Charges.Monthly`: cargos altos correlacionan con cancelación
- `internet.OnlineSecurity_No`, `internet.TechSupport_No`: falta de servicios técnicos influye negativamente

---

## 🎯 Recomendaciones estratégicas

- Incentivar contratos a largo plazo
- Programas de fidelización para nuevos clientes
- Revisión de precios y percepción de valor
- Fortalecer soporte técnico y seguridad online

---

## 🚀 Cómo ejecutar

1. Clona el repositorio:
   ```bash
   git clone https://github.com/jordano-crt/TelecomX-parte-2-challenge.git
2.Abre el notebook en Google Colab

3.Ejecuta todas las celdas para reproducir el análisis.
