# 🌱 Factores que determinan el contenido de materia orgánica en los suelos agrícolas de Colombia  
**Análisis numérico mediante modelos de regresión penalizada Ridge y Lasso**

---

## 📘 Descripción general

Este proyecto aplica **modelos de regresión penalizada (Ridge y Lasso)** para analizar los factores que influyen en el **contenido de materia orgánica (MO)** en los suelos agrícolas de Colombia.  

La **materia orgánica**, determinada por el método **Walkley & Black**, es un indicador fundamental de la **fertilidad del suelo**, reflejando su capacidad para retener nutrientes, agua y sostener actividad biológica.  

El estudio busca comprender cómo las **propiedades químicas** (N, P, K, Ca, Mg, pH, conductividad eléctrica) y las **condiciones físicas** (drenaje, topografía, riego) afectan este parámetro esencial para la sostenibilidad agrícola.

---

## 🎯 Objetivo del proyecto

**Objetivo general:**  
Evaluar cómo los elementos químicos y las condiciones físicas del suelo influyen sobre el contenido de materia orgánica, utilizando técnicas de regresión penalizada Ridge y Lasso.

**Objetivos específicos:**
- Identificar las variables químicas y físicas más relacionadas con la fertilidad del suelo.  
- Aplicar modelos Ridge y Lasso para reducir colinealidad y mejorar la predicción de la MO.  
- Comparar el desempeño de ambos modelos en términos de error y estabilidad.  
- Interpretar los resultados para proponer lineamientos de manejo sostenible del suelo.

---

## ⚙️ Metodología

1. **Fuente de datos:**  
   Resultados de análisis de laboratorio de suelos en Colombia, con variables físico-químicas y de manejo (pH, fósforo, calcio, magnesio, potasio, sodio, drenaje, riego, topografía, etc.).

2. **Limpieza y procesamiento:**  
   - Estandarización de variables numéricas  
   - Codificación de variables categóricas (one-hot encoding)  
   - Eliminación de valores faltantes o “No indica”

3. **Modelos aplicados:**
   - 📈 **Regresión Ridge:** controla multicolinealidad penalizando la magnitud de los coeficientes.  
   - 🧮 **Regresión Lasso:** realiza selección automática de variables al penalizar la suma absoluta de los coeficientes.

4. **Evaluación:**
   - Validación cruzada (k-fold)  
   - Métricas: R² ajustado, RMSE, MAE  
   - Comparación Ridge vs Lasso para interpretar estabilidad y parsimonia del modelo.

---

## 📊 Variables consideradas

| Tipo | Variables | Descripción |
|------|------------|-------------|
| **Dependiente** | `Materia_organica` | Porcentaje determinado por el método Walkley & Black |
| **Químicas** | `pH`, `Fósforo`, `Potasio`, `Calcio`, `Magnesio`, `Sodio`, `Conductividad_electrica` | Propiedades químicas del suelo |
| **Físicas** | `Drenaje`, `Riego`, `Topografía` | Condiciones de manejo del terreno |
| **Opcionales** | `Cultivo`, `Departamento` | Contexto agrícola o regional |

---



## 🧰 Herramientas utilizadas

- **Lenguaje:** R 
- **Librerías:**  
  - `glmnet` (R)  
  - `tidyverse`, `pandas`, `matplotlib`, `seaborn`  
- **Técnicas:** Estandarización, Validación cruzada, Selección automática de variables  
- **Visualizaciones:** gráficos de coeficientes, comparaciones de error y dispersión predicha/real

---
