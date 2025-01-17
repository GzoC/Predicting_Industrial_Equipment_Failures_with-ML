# **Predicción de Fallos en Equipos Industriales con Machine Learning**

Este proyecto utiliza técnicas de machine learning para predecir fallos en equipos industriales basándose en datos de sensores y características del equipo. El modelo optimizado final ayuda a identificar patrones que preceden a los fallos, permitiendo un mantenimiento predictivo más eficiente.

---

## **Estructura del Proyecto**

```
Predicting_Industrial_Equipment_Failures_with-ML/
├── data/
│   └── machine_failure_data.csv      # Dataset de fallos en equipos
├── notebook/
│   └── predicting_industrial_equipment_failures_with-ml.ipynb
├── results/
│   └── confusion_matrix.png          # Matriz de confusión generada
│   └── feature_importance.png        # Gráfico de importancia de características
├── README.md                         # Descripción del proyecto
└── .gitignore                        # Archivos y carpetas ignorados por Git
```

---

## **Descripción del Problema**

En un entorno industrial, los fallos de equipos pueden causar retrasos, pérdidas económicas y riesgos de seguridad. Este proyecto utiliza datos históricos de sensores para entrenar modelos de machine learning que predicen fallos antes de que ocurran, facilitando decisiones de mantenimiento predictivo.

---

## **Tecnologías Utilizadas**

- **Lenguaje**: Python 3.8+
- **Librerías Principales**:
  - `pandas` (manipulación de datos)
  - `numpy` (operaciones matemáticas)
  - `scikit-learn` (modelado y evaluación)
  - `seaborn` y `matplotlib` (visualización)
- **Entorno**:
  - Jupyter Notebook
  - Anaconda Environment

---

## **Flujo del Proyecto**

1. **Carga y Limpieza de Datos**:
   - Se cargó el dataset `machine_failure_data.csv`.
   - Se manejaron valores nulos y duplicados para garantizar datos limpios.

2. **Análisis Exploratorio**:
   - Se exploraron las distribuciones de las variables y su relación con la variable objetivo (`failure`).
   - Se generaron gráficos como histogramas y mapas de calor de correlaciones.

3. **Preparación de Datos**:
   - Transformación de datos categóricos mediante **One-Hot Encoding**.
   - Escalado de características para modelos sensibles a magnitudes.

4. **Modelado**:
   - Se entrenaron y evaluaron los siguientes modelos:
     - Regresión Logística
     - Árbol de Decisión
     - Random Forest
   - Se optimizaron hiperparámetros de Random Forest mediante **GridSearchCV**.

5. **Evaluación**:
   - Se generaron métricas de desempeño:
     - Precisión
     - Recall
     - F1-Score
   - Se visualizó la matriz de confusión y la importancia de características.

6. **Conclusiones y Recomendaciones**:
   - Random Forest optimizado tuvo el mejor desempeño con una precisión del **90%** en los datos de prueba.
   - Variables clave como `temp_sensor` y `vibration_sensor` fueron determinantes en las predicciones.

---

## **Resultados Clave**

| Modelo                  | Precisión en Prueba |
|-------------------------|---------------------|
| Regresión Logística     | 84.80%             |
| Árbol de Decisión       | 86.50%             |
| Random Forest (Base)    | 88.20%             |
| Random Forest (Optimizado) | 90.00%          |

---

## **Visualizaciones Generadas**

### Matriz de Confusión

![Matriz de Confusión](./results/confusion_matrix.png)

### Importancia de Características

![Importancia de Características](./results/feature_importance.png)

---

## **Requisitos para Reproducir**

1. Clona este repositorio:
   ```bash
   git clone https://github.com/XXXXXXX/Predicting_Industrial_Equipment_Failures_with-ML.git
   cd Predicting_Industrial_Equipment_Failures_with-ML
   ```

2. Crea y activa un entorno virtual:
   ```bash
   python -m venv p_i_e_f_w-ML
   source p_i_e_f_w-ML/bin/activate  # En Linux/Mac
   .\p_i_e_f_w-ML\Scripts\activate   # En Windows
   ```

3. Instala las dependencias:
   ```bash
   pip install -r requirements.txt
   ```

4. Abre el notebook en Jupyter:
   ```bash
   jupyter notebook notebook/predicting_industrial_equipment_failures_with-ml.ipynb
   ```

---

## **Recomendaciones Futuras**

1. Expandir el dataset para reducir el desbalance de clases.
2. Implementar modelos más avanzados como **XGBoost** o **LightGBM**.
3. Automatizar el flujo completo de datos y modelado mediante **pipelines**.
4. Validar el modelo en entornos de producción reales.

---

## **Contribuciones**

Las contribuciones son bienvenidas. Si deseas contribuir, por favor abre un **Issue** o un **Pull Request** en el repositorio.

---

