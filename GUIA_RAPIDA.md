# Guía Rápida - Pump it Up Competition

## ¿Qué es este proyecto?

Este es un proyecto de Machine Learning que participa en el concurso **"Pump it Up: Data Mining the Water Table"** de DrivenData.org. El objetivo es predecir el estado funcional de bombas de agua en Tanzania usando técnicas de clasificación multiclase.

## Pasos para Ejecutar el Proyecto

### 1️⃣ Obtener los Datos

**IMPORTANTE**: Los datos NO están incluidos en este repositorio. Debes descargarlos:

1. Ve a: https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/
2. Crea una cuenta o inicia sesión
3. Ve a la pestaña "Data"
4. Descarga estos 3 archivos:
   - `train_values.csv`
   - `train_labels.csv`
   - `test_values.csv`
5. Coloca los archivos en el mismo directorio que el notebook

### 2️⃣ Instalar Dependencias

```bash
pip install -r requirements.txt
```

Esto instalará:
- pandas, numpy, matplotlib, seaborn
- scikit-learn, xgboost, lightgbm
- jupyter notebook
- imbalanced-learn

### 3️⃣ Abrir el Notebook

```bash
jupyter notebook pump_it_up_competition.ipynb
```

### 4️⃣ Ejecutar el Notebook

1. En Jupyter, selecciona "Cell" > "Run All" o ejecuta celda por celda
2. El proceso tomará varios minutos (depende de tu máquina)
3. Al final se generará un archivo `submission.csv`

### 5️⃣ Subir Resultados al Concurso

1. Ve a: https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/submissions/
2. Haz clic en "Submit Predictions"
3. Sube el archivo `submission.csv`
4. Espera a que se procese (1-2 minutos)
5. Verás tu score en el leaderboard

### 6️⃣ Registrar el Score

1. Copia tu score del leaderboard
2. En el notebook, ve a la última sección
3. Actualiza la variable `competition_score` con tu score
4. Re-ejecuta esa celda para ver el análisis

## ¿Qué Contiene el Notebook?

### Sección 1: Configuración
- Importación de librerías necesarias
- Configuración de visualizaciones

### Sección 2: Carga de Datos
- Lectura de archivos CSV
- Verificación de dimensiones

### Sección 3: Análisis Exploratorio (EDA)
- Distribución de clases (desbalanceo)
- Valores faltantes y problemáticos
- Variables categóricas de alta cardinalidad
- Estadísticas de variables numéricas
- **Visualizaciones**: gráficos de distribución, matrices

### Sección 4: Preprocesamiento
- Limpieza de valores faltantes
- Feature engineering (edad de bombas, distancias)
- Encoding de variables categóricas
- Reducción de cardinalidad

### Sección 5: Modelado
- Entrenamiento de 3 modelos:
  - Random Forest
  - XGBoost
  - LightGBM
- Manejo de desbalanceo con class weights
- Evaluación con métricas (accuracy, F1, confusion matrix)
- Análisis de importancia de features

### Sección 6: Predicciones
- Generación de predicciones finales
- Creación de archivo submission.csv
- Instrucciones para subir al concurso

### Sección 7: Conclusiones
- Insights de negocio
- Recomendaciones prácticas
- Score del concurso

## Problemas Comunes y Soluciones

### Error: "FileNotFoundError"
**Causa**: No has descargado los datos
**Solución**: Sigue el paso 1️⃣ para descargar los archivos CSV

### Error: "ModuleNotFoundError"
**Causa**: Faltan dependencias
**Solución**: Ejecuta `pip install -r requirements.txt`

### Error: "Kernel died"
**Causa**: Posible falta de memoria
**Solución**: Cierra otras aplicaciones o reduce el tamaño del modelo

### El notebook tarda mucho
**Normal**: El entrenamiento puede tomar 5-15 minutos dependiendo de tu máquina

## Mejoras Posibles

Si quieres mejorar el score:

1. **Hyperparameter Tuning**: Usar GridSearchCV o RandomizedSearchCV
2. **Feature Engineering**: Crear más variables derivadas
3. **Ensemble**: Combinar predicciones de múltiples modelos
4. **SMOTE**: Aplicar oversampling en lugar de solo class weights
5. **Deep Learning**: Probar redes neuronales

## Entrega del Proyecto

Para entregar este proyecto debes incluir:

1. ✅ **Este repositorio** con el notebook
2. ✅ **Notebook ejecutado** (con outputs visibles)
3. ✅ **Screenshot del score** del concurso
4. ✅ **Archivo submission.csv** generado

## Recursos Adicionales

- **Concurso**: https://www.drivendata.org/competitions/7/
- **Scikit-learn**: https://scikit-learn.org/
- **XGBoost**: https://xgboost.readthedocs.io/
- **Pandas**: https://pandas.pydata.org/

## Soporte

Si tienes problemas:
1. Revisa esta guía completa
2. Verifica que descargaste los datos correctamente
3. Asegúrate de tener todas las dependencias instaladas
4. Revisa los mensajes de error cuidadosamente

---

**¡Buena suerte con el concurso! 🚀**
