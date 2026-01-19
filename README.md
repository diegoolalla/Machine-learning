# Machine Learning Práctica 2 - Pump it Up Competition

## Descripción del Proyecto

Este proyecto participa en el concurso **"Pump it Up: Data Mining the Water Table"** de DrivenData.org, donde el objetivo es predecir el estado funcional de bombas de agua en Tanzania.

### Clases a Predecir
- **functional**: La bomba funciona correctamente
- **non functional**: La bomba no funciona
- **functional needs repair**: La bomba funciona pero necesita reparación

### Características del Dataset
- ~60,000 bombas de agua en el conjunto de entrenamiento
- 40 variables (mixtas: numéricas y categóricas)
- Problemas típicos: valores faltantes, alta cardinalidad, desbalanceo de clases

## Estructura del Repositorio

```
Machine-learning-practica-2/
├── README.md                          # Este archivo
├── pump_it_up_competition.ipynb       # Notebook principal del proyecto
├── requirements.txt                   # Dependencias de Python
├── .gitignore                         # Archivos a ignorar en Git
└── [data files]                       # Archivos CSV (no versionados)
```

## Instrucciones de Instalación

### 1. Clonar el Repositorio

```bash
git clone https://github.com/diegoolalla/Machine-learning-practica-2.git
cd Machine-learning-practica-2
```

### 2. Crear Entorno Virtual (Recomendado)

```bash
# Usando venv
python -m venv venv

# Activar en Windows
venv\Scripts\activate

# Activar en Linux/Mac
source venv/bin/activate
```

### 3. Instalar Dependencias

```bash
pip install -r requirements.txt
```

### 4. Descargar los Datos

1. Visitar: https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/
2. Registrarse o iniciar sesión
3. Ir a la sección "Data" y descargar:
   - `train_values.csv` - Características de entrenamiento
   - `train_labels.csv` - Etiquetas de entrenamiento
   - `test_values.csv` - Características de prueba
4. Colocar los archivos CSV en el directorio raíz del proyecto

### 5. Ejecutar el Notebook

```bash
jupyter notebook pump_it_up_competition.ipynb
```

## Contenido del Notebook

El notebook está organizado en las siguientes secciones:

1. **Importación de Librerías y Configuración**
   - Setup inicial del ambiente de trabajo

2. **Carga de Datos**
   - Lectura de archivos CSV
   - Exploración inicial

3. **Exploración de Datos (EDA)**
   - Análisis de la variable objetivo
   - Detección de valores faltantes
   - Análisis de cardinalidad
   - Estadísticas descriptivas
   - Visualizaciones

4. **Preprocesamiento y Feature Engineering**
   - Limpieza de datos
   - Manejo de valores faltantes
   - Encoding de variables categóricas
   - Creación de nuevas características
   - Reducción de cardinalidad

5. **Entrenamiento de Modelos**
   - Random Forest
   - XGBoost
   - LightGBM
   - Manejo de desbalanceo de clases
   - Validación cruzada

6. **Evaluación y Comparación**
   - Métricas de rendimiento
   - Matrices de confusión
   - Importancia de características

7. **Predicciones y Submission**
   - Generación de predicciones finales
   - Creación de archivo de submission
   - Instrucciones para subir al concurso

8. **Conclusiones y Recomendaciones**
   - Insights de negocio
   - Recomendaciones para el mantenimiento de bombas
   - Próximos pasos

## Resultados

### Modelo Final
- **Algoritmo**: [Se determina automáticamente el mejor durante la ejecución]
- **Accuracy en Validación**: [Se reporta al ejecutar el notebook]
- **Score del Concurso**: [Actualizar después de la submission]

### Características Más Importantes
El notebook identifica automáticamente las características más importantes para la predicción, lo cual ayuda a:
- Priorizar la recolección de datos
- Enfocar recursos de mantenimiento
- Mejorar la toma de decisiones

## Aspectos Destacados del Proyecto

### 1. Manejo de Desbalanceo de Clases
- Uso de `class_weight='balanced'` en los modelos
- Implementación de SMOTE disponible para pruebas
- Métricas específicas por clase

### 2. Procesamiento de Alta Cardinalidad
- Reducción de categorías poco frecuentes
- Target encoding y frequency encoding
- Agrupación inteligente de categorías

### 3. Feature Engineering
- Extracción de características temporales
- Creación de variables geográficas derivadas
- Edad de las bombas
- Distancia a centros poblados

### 4. Orientación a Negocio
- Explicaciones claras en cada sección
- Insights prácticos para la gestión de mantenimiento
- Visualizaciones interpretables
- Recomendaciones accionables

## Tecnologías Utilizadas

- **Python 3.8+**
- **pandas**: Manipulación de datos
- **numpy**: Operaciones numéricas
- **scikit-learn**: Modelos de ML y preprocesamiento
- **XGBoost**: Gradient boosting avanzado
- **LightGBM**: Gradient boosting eficiente
- **imbalanced-learn**: Manejo de desbalanceo
- **matplotlib/seaborn**: Visualizaciones
- **Jupyter Notebook**: Ambiente interactivo

## Métricas de Evaluación

El concurso usa **Classification Rate** (accuracy) como métrica principal, pero el notebook también reporta:
- Precision, Recall, F1-Score por clase
- Matrices de confusión
- Distribución de predicciones

## Próximos Pasos para Mejorar

1. **Optimización de Hiperparámetros**
   - Grid Search
   - Random Search
   - Bayesian Optimization

2. **Feature Engineering Avanzado**
   - Interacciones entre variables
   - Transformaciones no lineales
   - Agregaciones geográficas

3. **Ensemble Methods**
   - Voting Classifier
   - Stacking
   - Blending

4. **Técnicas de Balanceo Avanzadas**
   - ADASYN
   - SMOTE variants
   - Cost-sensitive learning

## Contribuciones

Este proyecto es parte de la práctica de Machine Learning. Sugerencias y mejoras son bienvenidas.

## Autor

Diego Olalla

## Licencia

Este proyecto es de código abierto y está disponible para fines educativos.

## Referencias

- [DrivenData - Pump it Up Competition](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/)
- [Scikit-learn Documentation](https://scikit-learn.org/)
- [XGBoost Documentation](https://xgboost.readthedocs.io/)
- [LightGBM Documentation](https://lightgbm.readthedocs.io/)

---

**Nota**: Para ejecutar el notebook correctamente, asegúrate de haber descargado los archivos de datos del concurso y colocarlos en el directorio del proyecto.
