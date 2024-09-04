# Proyecto de Ciencia de Datos Aplicada en la Industria Inmobiliaria

Este repositorio está destinado a estudiantes de ciencia de datos aplicada. Detalla un proceso completo de desarrollo de un proyecto de ciencia de datos, que abarca desde la preparación de los datos hasta la implementación de modelos de predicción. Es una guía práctica para comprender proyectos de ciencia de datos del mundo real, enfocado en la **industria inmobiliaria**.

## Descripción del Proyecto

El objetivo del proyecto es construir un modelo que permita predecir la **probabilidad de compra** de propiedades por parte de los clientes, basándose en un conjunto de datos relacionados con transacciones inmobiliarias y comportamiento de los clientes. Se incluyen las siguientes fases del proyecto:

1. **Recopilación y preparación de datos**: Carga y limpieza de datos desde una base de datos SQLite.
2. **Creación de nuevas características (features)**: Desarrollo de variables clave como `Salario_MarcaClase`, `TOTALVENTAS`, `TOTALMONTOVENDIDO`, entre otras.
3. **Imputación de valores faltantes**: Tratamiento de valores nulos o faltantes en variables críticas como `EstadoCivil` y `InteresMetraje`, usando técnicas supervisadas.
4. **Análisis de Clústeres (K-means)**: Segmentación de clientes utilizando clustering para identificar patrones y tendencias.
5. **Modelo Supervisado (Random Forest)**: Predicción de la probabilidad de compra de propiedades usando un modelo de clasificación.
6. **Visualización**: Uso de gráficos interactivos para analizar las diferencias en los clústeres y visualizar las probabilidades de compra.

## Estructura del Proyecto

### 1. Preparación de los datos
- **Carga y limpieza**: Los datos se obtienen de una base de datos SQLite, realizando las transformaciones necesarias para preparar los datos para el análisis.
- **Imputación**: Se corrigen los valores faltantes en variables importantes como `EstadoCivil`, usando un modelo de Árbol de Decisión para imputar valores en función de otras características.
- **Creación de características**: Variables adicionales son creadas a partir de los datos brutos, como `InteresMetraje_MarcaClase` y `Salario_MarcaClase`.

### 2. Análisis de Clústeres (K-means)
- **Segmentación de clientes**: Se usa el algoritmo K-means para agrupar clientes basándose en variables como `TOTALVENTAS`, `TOTALMONTOVENDIDO` y `Salario_MarcaClase`.
- **Visualización de clústeres**: Gráficos interactivos muestran las diferencias entre los clústeres, ayudando a interpretar las características que definen a cada grupo de clientes.

### 3. Modelo Supervisado (Random Forest)
- **Modelo de clasificación**: Se construye un modelo de Random Forest para predecir la probabilidad de que un cliente realice una compra de propiedad.
- **Matriz de confusión**: Se utiliza para evaluar el rendimiento del modelo.
- **Probabilidades de compra**: Se obtienen y visualizan las probabilidades de compra para cada cliente, lo que facilita la toma de decisiones en la estrategia de ventas.

### 4. Visualización Interactiva con Plotly
- **Gráficos de cuadrantes**: Se usan gráficos tipo cuadrantes para comparar variables como `TOTALMONTOVENDIDO` con las probabilidades de compra.
- **Gráficos de dispersión y boxplots**: Visualizaciones interactivas que permiten explorar las diferencias entre clústeres y probabilidades de compra.

## Requisitos

Este proyecto utiliza **Python** y requiere las siguientes librerías:

- `pandas`
- `scikit-learn`
- `plotly`
- `matplotlib`
- `sqlite3`
- `seaborn` (opcional)

Puedes instalar todas las dependencias ejecutando:

```bash
pip install -r requirements.txt

