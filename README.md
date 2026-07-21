# analysis-everpeak
# 📊 EverPeak Retail Analysis – Sprint 6 & 7

Este repositorio contiene el proyecto de análisis exploratorio de datos (EDA), limpieza y tratamiento de atípicos para la empresa de e-commerce **EverPeak – SilverBasket**, desarrollado como parte del programa de Analista de Datos en TripleTen.

El objetivo principal es auditar la calidad de los datos transaccionales, construir un pipeline de limpieza reproducible y generar insights estratégicos para el área de operaciones y mercadotecnia.

---

## 📂 Contenido del Repositorio

- `Sprint07_Webinar11_students_version.ipynb`: Notebook principal con el flujo completo de análisis:
  - Carga y diagnóstico estructural del dataset.
  - Limpieza de datos (tratamiento de *sentinels*, nulos y conversión de tipos).
  - Feature Engineering (Segmentación por volumen y método de pago).
  - Análisis de distribuciones y detección formal de outliers.
  - Winsorización al percentil 99 (`p99`) para estabilizar métricas ejecutivas.

---

## ▶️ Cómo ejecutar el Notebook en Google Colab

Puedes abrir e interactuar directamente con el notebook sin necesidad de instalar entornos locales utilizando el siguiente botón:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/tatianabr67-DA/analysis-everpeak/blob/main/Sprint07_Webinar11_students_version.ipynb)

> **Nota:** Si prefieres abrirlo desde la interfaz de Google Colab:
> 1. Ve a [colab.research.google.com](https://colab.research.google.com).
> 2. Pestaña **GitHub** $\rightarrow$ Escribe el usuario: `tatianabr67-DA`.
> 3. Selecciona el repositorio `tatianabr67-DA/analysis-everpeak` y la rama `main`.
> 4. Haz clic sobre el archivo `Sprint07_Webinar11_students_version.ipynb`.

---

## 📘 Cómo reproducir el análisis

1. Abre el notebook usando el enlace superior de Colab o clonando el repositorio localmente.
2. Ejecuta las celdas de forma secuencial (`Shift + Enter`).
3. El script carga automáticamente los datos y ejecuta el pipeline de limpieza y visualizaciones con `Pandas`, `NumPy`, `Matplotlib` y `Seaborn`.

---

## 🛠️ Herramientas Utilizadas

- **Lenguaje:** Python 3
- **Librerías de Procesamiento:** Pandas, NumPy
- **Visualización de Datos:** Matplotlib, Seaborn
- **Entorno & Versionado:** Google Colab, GitHub

---

## 💡 Hallazgos y Conclusiones Clave

- **Estabilización de Métricas:** Se detectó un sesgo positivo (*right-skewed*) significativo en el valor de las órdenes (`order_value`). La aplicación de Winsorización (cap al $P_{99}$) permitió proteger la representatividad de compras VIP sin permitir que valores extremos distorsionaran la media del negocio.
- **Segmentación Operativa:** Mediante la función `.apply(axis=1)`, se dividió la cartera en 4 cuadrantes comerciales según edad y volumen de compra, optimizando el canal de atención para clientes de alto volumen (*High Volume*).

---
*Proyecto desarrollado por **Denisse Tatiana Baltazar Romero** – Analista de Datos Junior.*
