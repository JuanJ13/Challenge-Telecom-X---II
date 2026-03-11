# Análisis de Evasión de Clientes (Churn) - Telecom X II

## 1. Descripción del Proyecto

Este proyecto de Ciencia de Datos tiene como objetivo identificar los patrones de comportamiento que motivan la cancelación de servicios (*Churn*) en la operadora **Telecom X**. A través de modelos de Machine Learning y análisis estadístico, evaluamos variables críticas como el tipo de contrato, la antigüedad (*tenure*) y la calidad del servicio técnico para proponer estrategias de retención basadas en datos.

## 2. Metodología de Análisis

El flujo de trabajo siguió el ciclo de vida de ciencia de datos, desde la ingesta hasta el modelado:

* **Consolidación:** Integración de fuentes de datos mediante técnicas de normalización y limpieza.
* **Preprocesamiento:** Manejo de datos categóricos con `OneHotEncoder` y escalado de variables numéricas con `StandardScaler`.
* **Análisis Estadístico:** Identificación de correlaciones clave mediante mapas de calor y visualización de distribuciones.
* **Modelado Predictivo:** Comparación de modelos (**Decision Tree** y **KNN**) para evaluar la capacidad de clasificación, utilizando métricas como F1-Score y Matrices de Confusión.

## 3. Principales Hallazgos

* **Vulnerabilidad Inicial:** Los clientes con menos de 10 meses de antigüedad representan el segmento de mayor riesgo de fuga.
* **Impacto Tecnológico:** Se detectó una alta tasa de deserción vinculada al servicio de **Fibra Óptica**, sugiriendo áreas de mejora en la calidad del servicio.
* **Correlación de Pagos:** El método de pago electrónico presenta una correlación relevante con la tasa de abandono, indicando fricciones en la experiencia de usuario digital.

## 4. Estrategias de Retención (Data-Driven)

Basado en los resultados del modelo, se propone a la gerencia:

1. **Programa de Onboarding (0-10 meses):** Fidelización proactiva durante la etapa crítica de riesgo.
2. **Auditoría Técnica:** Revisión de los niveles de servicio y soporte técnico en usuarios de fibra óptica.
3. **Optimización de Pagos:** Simplificación de procesos en el portal de pagos electrónicos para reducir la fricción.

## 5. Tecnologías Utilizadas

* **Lenguaje:** Python 3.x
* **Librerías de Procesamiento:** `pandas`, `numpy`
* **Modelado:** `scikit-learn` (Pipeline,DecisionTreeClassifier, KNN)
* **Visualización:** `matplotlib`, `seaborn`

## 6. Resultados del Modelo

El modelo **Random Forest** demostró ser la herramienta más robusta para capturar relaciones no lineales, permitiendo identificar variables como `Contract_Month-to-month` y `tenure` como los principales *drivers* de la cancelación.
