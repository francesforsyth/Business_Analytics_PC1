# Scouting LATAM: Identificación de Jugadores Subvalorados mediante Business Analytics ⚽📊

Este proyecto presenta una propuesta analítica integral para un **fondo de inversión deportiva** interesado en capitalizar ineficiencias en el mercado de fichajes de la **Liga 1 Peruana** y el contexto latinoamericano.

---

## 👥 Equipo de Proyecto (Grupo 8)
* **Frances Forsyth** (202320199)
* **Fatima Marquez** (202210592)
* **Rafael Alcandré** (202210012)

**Institución:** Universidad de Ingeniería y Tecnología (UTEC)  
**Curso:** AD3010 Business Analytics | **Profesor:** Alan Morante  
**Fecha:** Mayo, 2026

---

## 🎯 1. Definición del Problema de Negocio
El mercado de transferencias de fútbol en LATAM es asimétrico. Clubes con presupuestos limitados (como los de la Liga 1) a menudo pagan sobreprecios por jugadores basados en "reputación", mientras ignoran talento con métricas superiores.

**El objetivo:** Identificar jugadores cuyos atributos físicos y técnicos superan su valoración de mercado actual en **Transfermarkt**, permitiendo al fondo adquirir activos con alto potencial de revalorización (ROI).

### Preguntas Analíticas de Negocio
* **P1:** ¿Qué jugadores presentan la mayor brecha positiva entre su calidad técnica (FIFA) y su precio de mercado?
* **P2:** ¿En qué posiciones del campo se concentran las mayores oportunidades de inversión?
* **P3:** ¿Cuál es el margen de crecimiento proyectado para jugadores Sub-23?
* **P4:** ¿Existe un castigo económico injustificado hacia el jugador peruano en comparación con sus pares regionales?

---

## 💾 2. Metodología de Datos y Enriquecimiento

### 2.1 Fuentes de Información
1.  **FIFA 24 (Kaggle):** Atributos detallados (ritmo, tiro, pase) para 2,982 jugadores de campo LATAM.
2.  **Transfermarkt:** Datos reales de mercado (precios históricos y actuales).
3.  **World Bank:** GDP per cápita para normalizar el efecto país en la valoración.

### 2.2 Estrategia de Enriquecimiento
Utilizamos un proceso de **Data Blending** para unir el rendimiento (FIFA) con la valoración financiera (Transfermarkt). El ratio clave definido es:
$$\text{Ratio de Oportunidad} = \frac{\text{Valor Estimado FIFA}}{\text{Valor Mercado Transfermarkt}}$$

---

## 📈 3. Análisis Exploratorio de Datos (EDA)

### 3.1 Distribución del Talento Regional
El análisis de *Overall* muestra que, aunque Argentina y Uruguay lideran, Perú mantiene una competitividad sólida con una mediana de 67 puntos.

![Distribución Overall por País](fig1%20overall%20pais.png)
*Figura 1: El talento peruano se encuentra dentro del rango competitivo regional.*

### 3.2 La Ineficiencia del Mercado
Al graficar el Valor FIFA frente al Valor de Mercado, identificamos que la correlación es de apenas $r = 0.574$, lo que confirma la existencia de "gangas".

![FIFA vs Transfermarkt](fig2%20fifa%20vs%20tm.png)
*Figura 2: Dispersión de valoraciones. Los puntos sobre la línea representan activos subvalorados.*

### 3.3 Oportunidades por Posición
Los datos revelan que los **delanteros** y **defensas** son los activos más castigados por el mercado, con ratios de subvaloración de $1.85\text{x}$ y $1.83\text{x}$ respectivamente.

![Brecha por Posición](fig3%20brecha%20posicion.png)
*Figura 3: Análisis de brechas de inversión según la posición en el campo.*

### 3.4 Proyección Sub-23
Identificamos un segmento de 1,015 jóvenes promesas con una capacidad de crecimiento promedio de 12 puntos en su Overall.

![Crecimiento Jóvenes](fig4%20jovenes%20crecimiento.png)
*Figura 4: Potencial de crecimiento vs Valor actual para jugadores menores de 23 años.*

---

## 🇵🇪 4. El Caso de Perú: Hallazgo Crítico
Uno de los descubrimientos más potentes del EDA es que el perfil de habilidades del jugador peruano es **virtualmente indistinguible** del promedio de LATAM en las 6 dimensiones clave.

![Radar Perú vs LATAM](fig5%20radar%20peru.png)
*Figura 5: Superposición de habilidades. El "descuento" del jugador peruano no es técnico, es una falla de mercado.*

Además, controlamos este hallazgo mediante el GDP per cápita, notando que la riqueza del país no dicta necesariamente la calidad técnica del jugador, pero sí influye en su visibilidad.

![GDP vs Overall](fig6%20gdp%20overall.png)
*Figura 6: Relación entre contexto económico del país y rendimiento deportivo.*

---

## 🚀 5. Roadmap: Fase 2 (Modelado Predictivo)
Para la entrega final (PC2), el proyecto escalará hacia:
1.  **Regresión Lineal Múltiple:** Para determinar el "precio justo" de un jugador basado en sus stats.
2.  **Clustering K-means:** Para segmentar el mercado en:
    * *Low-risk Gems* (Seguros)
    * *High-reward Bets* (Apuestas de alto riesgo)
    * *Overpriced Assets* (Evitar compra)
3.  **Time Series Analysis:** Para predecir el momento óptimo de venta (Exit strategy).

---

## ⚠️ 6. Gestión de Riesgos
* **R1 (Match Rate):** Actualmente en el 17%. Se ampliará mediante técnicas de *fuzzy matching* por club y edad.
* **R2 (Sesgo FIFA):** Los atributos de FIFA son estimaciones; se validarán en la Fase 2 con métricas de rendimiento real si la disponibilidad de datos lo permite.

---
**Curso:** AD3010 Business Analytics - UTEC.  
**Entregable:** PC1 - Informe de Propuesta y EDA.

# Datasets
Datasets en el drive --> https://drive.google.com/drive/folders/1vVPE252KF8h7mpV6nG52STV1wfKHRMNI?usp=share_link
