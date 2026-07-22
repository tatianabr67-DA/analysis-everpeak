# 📊 Análisis Exploratorio y Segmentación de Clientes — ConnectaTel

## 🎯 Objetivo del Proyecto
El objetivo principal de este proyecto es analizar el comportamiento de consumo de los clientes de la empresa de telecomunicaciones **ConnectaTel** para identificar patrones de uso, evaluar la distribución demográfica y segmentar la cartera de usuarios. Este análisis proporciona recomendaciones estratégicas orientadas a reducir el riesgo de cancelación (*churn*) y optimizar las ofertas comerciales.

---

## 📁 Datasets Utilizados
El análisis combina tres fuentes de datos principales:
- `plans.csv`: Información sobre los planes actuales (precios, minutos, mensajes y MB incluidos, además de costos extra).
- `users.csv`: Datos demográficos y de registro de los usuarios (ID, nombre, edad, ciudad, fecha de registro, plan contratado y fecha de cancelación).
- `calls.csv` / `messages.csv` / `internet.csv`: Registros de consumo mensual por cliente.

---

## 🛠️ Etapas del Análisis
1. **Preparación y Limpieza de Datos:**
   - Tratamiento de valores ausentes en variables clave (`city`, `churn_date`).
   - Identificación e imputación de registros atípicos (llamadas de 0 minutos y datos cero).
   - Unificación de datasets mediante integraciones relacionales (`merge`).
2. **Análisis Exploratorio de Datos (EDA):**
   - Cálculo de estadísticas descriptivas (tendencia central, dispersión e IQR).
   - Identificación de sesgos y distribuciones de consumo.
3. **Segmentación de Clientes:**
   - **Segmentación por Uso (`grupo_uso`):** Clasificación en *Bajo uso*, *Uso medio* y *Alto uso* con evaluación condicional vectorizada (`np.select`).
   - **Segmentación Demográfica (`grupo_edad`):** Clasificación por cohortes (*Joven*, *Adulto*, *Adulto Mayor*).
4. **Visualización y Reporte Ejecutivo:**
   - Gráficos de barras etiquetados (`sns.countplot`) para comunicación ejecutiva.
   - Diagnóstico final y recomendaciones de negocio orientadas a la retención y migración de planes.

---

## 🚀 Guía de Reproducción y Ejecución

Para explorar el proyecto y ejecutar el código interactivo:

1. **Apertura Directa en Google Colab:**
   - Haz clic en el botón **Open in Colab** ubicado en la parte superior del notebook [`S7_Version_Estudiante_Project_ConnectaTel.ipynb`](./S7_Version_Estudiante_Project_ConnectaTel.ipynb).
2. **Ejecución del Código:**
   - Ejecuta las celdas en orden secuencial (`Shift + Enter` o clic en el icono de reproducción).
   - Asegúrate de contar con las librerías `pandas`, `numpy`, `matplotlib` y `seaborn` (ya preinstaladas en el entorno de Colab).

---

## 💡 Principales Conclusiones
- **Predominio del Uso Medio:** El 73.58% de los usuarios mantiene un consumo moderado, constituyendo el núcleo operativo de la empresa.
- **Riesgo de Cancelación:** Se aisló un 19.45% de clientes con bajo consumo, identificándolos como público prioritario para campañas de reactivación.
- **Perfil Demográfico Maduro:** El 81% de la base se concentra en Adultos (50.45%) y Adultos Mayores (30.55%), sugiriendo la necesidad de simplificar la oferta comercial de voz y soporte.
