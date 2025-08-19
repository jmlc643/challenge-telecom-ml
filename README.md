# 📊 Modelo Predictivo de Churn para Telecomunicaciones

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-green.svg)](https://scikit-learn.org/)
[![Status](https://img.shields.io/badge/Status-En%20Desarrollo-yellow.svg)]()

## 🎯 Descripción del Proyecto

Este proyecto desarrolla un **modelo predictivo de Machine Learning** capaz de identificar qué clientes de telecomunicaciones tienen mayor probabilidad de cancelar sus servicios (churn). El objetivo es ayudar a las empresas de telecomunicaciones a implementar estrategias proactivas de retención de clientes.

## 🔍 Problema de Negocio

- **Desafío**: La alta tasa de cancelación de servicios en el sector telecomunicaciones
- **Impacto**: Pérdida de ingresos y aumento en costos de adquisición de nuevos clientes
- **Solución**: Modelo predictivo para identificar clientes en riesgo de churn antes de que cancelen

## 📋 Características del Dataset

- **Tamaño**: 7,043 registros de clientes
- **Variables**: 18 características después del preprocesamiento
- **Distribución de Churn**: 26.54% (1,869 cancelaciones vs 5,174 retenciones)

### Variables Principales:
- **Demográficas**: Edad (SeniorCitizen), Partner, Dependents
- **Servicios**: InternetService, PhoneService, OnlineSecurity, TechSupport
- **Contractuales**: Contract, tenure, PaymentMethod, PaperlessBilling
- **Financieras**: Charges.Monthly

## 🛠️ Metodología

### 1. **Análisis Exploratorio de Datos (EDA)**
- Identificación de variables relevantes
- Análisis de distribuciones y correlaciones
- Detección de patrones de churn

### 2. **Preprocesamiento de Datos**
- **Eliminación de variables irrelevantes**: customerID, gender, variables derivadas
- **Codificación de variables categóricas**: Label Encoding para variables binarias
- **Balanceo de clases**: SMOTE para equilibrar la distribución de churn
- **Estandarización**: Normalización de variables continuas (tenure, Charges.Monthly)

### 3. **Análisis de Correlación**
- Matriz de correlación para identificar relaciones entre variables
- Detección de multicolinealidad
- Selección de features más predictivas

## 📊 Hallazgos Principales

### Variables más correlacionadas con Churn:
1. **Contract (0.397)** - Tipo de contrato (mes a mes vs anual)
2. **tenure (0.352)** - Antigüedad del cliente
3. **Charges.Monthly (0.193)** - Cargos mensuales
4. **PaperlessBilling (0.192)** - Facturación electrónica
5. **OnlineSecurity (0.171)** - Servicios de seguridad online

### Insights Clave:
- Clientes con **contratos mes a mes** tienen 42.71% de churn vs 2.83% en contratos de 2 años
- **Clientes nuevos** (0-12 meses) presentan 47.68% de churn
- **Fiber optic** internet tiene mayor churn (41.89%) que DSL (18.96%)
- **Electronic check** como método de pago correlaciona con 45.29% de churn

## 🔧 Tecnologías Utilizadas

```python
# Librerías principales
pandas              # Manipulación de datos
numpy               # Operaciones numéricas
scikit-learn        # Machine Learning
imblearn            # Balanceo de clases (SMOTE)
matplotlib          # Visualización
seaborn             # Visualización estadística
```

## 📁 Estructura del Proyecto

```
challenge-telecom-ml/
│
├── datos_tratados.csv          # Dataset preprocesado
├── main.ipynb                  # Notebook principal con análisis completo
├── README.md                   # Este archivo
│
└── notebooks/
    └── exploratory_analysis/   # Análisis exploratorio detallado
```

## 🚀 Cómo Ejecutar el Proyecto

### Prerrequisitos
```bash
Python 3.8+
Jupyter Notebook
```

### Instalación
```bash
# Clonar el repositorio
git clone https://github.com/jmlc643/challenge-telecom-ml.git
cd challenge-telecom-ml

# Instalar dependencias
pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn jupyter
```

### Ejecución
```bash
# Abrir Jupyter Notebook
jupyter notebook main.ipynb
```

## 📈 Resultados del Balanceo

- **Dataset Original**: 7,043 filas
- **Dataset Balanceado**: 10,348 filas
- **Muestras Sintéticas**: 3,305 filas generadas por SMOTE
- **Distribución Final**: 50% No Churn / 50% Churn

## 🎯 Próximos Pasos

1. **Entrenamiento de Modelos**:
   - Random Forest
   - Gradient Boosting
   - SVM
   - Redes Neuronales

2. **Evaluación de Performance**:
   - Métricas: Accuracy, Precision, Recall, F1-Score, AUC-ROC
   - Validación cruzada
   - Análisis de importancia de features

3. **Optimización**:
   - Hyperparameter tuning
   - Feature engineering
   - Ensemble methods

4. **Implementación**:
   - API para predicciones en tiempo real
   - Dashboard de monitoreo
   - Sistema de alertas

## 📊 Métricas de Éxito

- **Precisión objetivo**: > 85%
- **Recall para Churn**: > 80%
- **F1-Score**: > 0.82
- **Reducción de falsos negativos**: Minimizar clientes en riesgo no detectados

## 👥 Contribuciones

Las contribuciones son bienvenidas. Por favor:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📝 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

## 📧 Contacto

**Proyecto Link**: [https://github.com/jmlc643/challenge-telecom-ml](https://github.com/jmlc643/challenge-telecom-ml)

---

⭐ **Si este proyecto te resulta útil, no olvides darle una estrella en GitHub!** ⭐