# Proyecto2
Proyecto de ML con análisis exploratorio de 4 datasets y modelo para predecir precios de automóviles. Incluye limpieza de datos, visualizaciones y solución de problemas de regresión. Dataset principal de UCI.
# Proyecto 2: Análisis Inicial y Selección de Problema

## Descripción
Este proyecto realiza un análisis exploratorio (EDA) de cuatro conjuntos de datos para identificar problemáticas relevantes en machine learning. Se seleccionó el dataset de automóviles (Dataset 2) para desarrollar un modelo de predicción de precios.

## Conjuntos de Datos Analizados

1. **Dataset 1: Propiedades inmobiliarias**  
   - **Fuente**: Por definir  
   - **Tamaño**: 128 filas × 8 columnas  
   - **Variables**: 6 numéricas (Price, SqFt, Bedrooms, etc.) y 2 categóricas (Brick, Neighborhood)  
   - **Dominio**: Bienes raíces  

2. **Dataset 2: Características de automóviles** *(SELECCIONADO)*  
   - **Fuente**: UCI Machine Learning Repository  
   - **Tamaño**: 205 filas × 26 columnas  
   - **Variables**: 5 numéricas, 5 enteras y 16 categóricas (make, fuel-type, price, etc.)  
   - **Dominio**: Automotriz  

3. **Dataset 3: Calidad de vinos**  
   - **Fuente**: UCI Wine Quality Dataset  
   - **Tamaño**: 1,143 filas × 13 columnas  
   - **Variables**: 11 numéricas (acidez, alcohol, etc.) y 2 enteras (quality, Id)  
   - **Dominio**: Industria vitivinícola  

4. **Dataset 4: Ventas minoristas**  
   - **Fuente**: Por definir  
   - **Tamaño**: 440 filas × 8 columnas  
   - **Variables**: 8 enteras (Fresh, Milk, Grocery, etc.)  
   - **Dominio**: Retail  

---

## Resumen del EDA Inicial

### Hallazgos Comunes
- **Dataset 1**: Datos limpios sin valores nulos. Variables numéricas con distribuciones normales y sesgadas.
- **Dataset 2**: Presencia de variables numéricas almacenadas como objetos (price, horsepower). Alto potencial predictivo.
- **Dataset 3**: Datos completos sin nulos. Variable "quality" podría usarse para clasificación.
- **Dataset 4**: Todos valores enteros. Posible aplicación de clusterización para segmentación de clientes.

### Hallazgos Clave por Dataset
1. **Dataset 2 (Automóviles)**:  
   - Variables críticas: `price` (target), `horsepower`, `engine-size`  
   - Problemas de formato: 16 columnas como objetos requieren preprocesamiento  
   - Correlaciones fuertes: `engine-size` vs `price` (0.87), `horsepower` vs `price` (0.81)  

---

## Problema Seleccionado
### Dataset Elegido
- **Nombre**: Características y precios de automóviles (Dataset 2)  
- **Razón de elección**:  
  - Datos completos (205 registros)  
  - Variables técnicas claramente relacionadas con el precio  
  - Oportunidad para limpieza y conversión de datos  

### Problema a Abordar
- **Tipo**: **Regresión** (predictivo)  
- **Objetivo**: Predecir el precio de automóviles basado en características técnicas y especificaciones.  
- **Relevancia**:  
  - Modelo útil para compradores y vendedores en el mercado automotriz  
  - Permite identificar features que más impactan en el valor  
- **Desafíos**:  
  - Conversión de variables numéricas almacenadas como texto (`price`, `horsepower`)  
  - Manejo de variables categóricas (`make`, `fuel-type`) con one-hot encoding  

---

## Instrucciones para Ejecutar
```bash```
git clone [URL-del-repositorio]
pip install pandas matplotlib seaborn numpy jupyter
jupyter notebook EDA/EDA_dataset2.ipynbv 


##Autores

Milimar Ramos

