# alzheimers-prediction
🇪🇸 NeuroCheck es un Modelo de ML para predecir Alzheimer analizando 24 factores de riesgo. Detecta la enfermedad antes de síntomas clínicos. Python, CatBoost, FastAPI, Vue.  🇬🇧 AI model predicting Alzheimer's by analyzing 24 risk factors. Detects disease before clinical symptoms. Python, CatBoost, FastAPI, Vue.

# NeuroCheck: Modelo Predictivo de Alzheimer

![Predicción de Alzheimer](https://img.shields.io/badge/IA%20en%20Salud-Predicci%C3%B3n%20de%20Alzheimer-blue)
![Stack Tecnológico](https://img.shields.io/badge/Tecnolog%C3%ADas-Python%20|%20CatBoost%20|%20FastAPI%20|%20Vue-green)
![Estado](https://img.shields.io/badge/Estado-Desplegado-success)

<p align="center">
  <i>"La muerte no llega con la vejez sino con el olvido" - Gabriel García Márquez</i>
</p>

## 🧠 El Problema: El diagnóstico tardío cuesta vidas

**¿Sabías que?** Mientras lees este Readme, al menos 3 personas habrán desarrollado Alzheimer sin siquiera saberlo.

**Más del 50%** de los casos de Alzheimer se diagnostican demasiado tarde, reduciendo dramáticamente la eficacia del tratamiento y la calidad de vida. Solo en América, se proyecta que el número de pacientes con Alzheimer aumentará de 5.8 millones a 13.8 millones para 2050.

Aunque el Alzheimer no tiene cura actualmente, un diagnóstico temprano puede:
- Ralentizar la progresión de la enfermedad
- Mejorar significativamente la calidad de vida del paciente
- Reducir los costos de atención médica
- Permitir intervenciones más efectivas
- Dar a los pacientes y familias más tiempo para prepararse

## 💡 Nuestra Solución: Detección temprana impulsada por IA

NeuroCheck es un modelo de aprendizaje automático que puede predecir el riesgo de Alzheimer antes de que aparezcan los síntomas clínicos. Mediante el análisis de datos demográficos, de estilo de vida, genéticos y clínicos, nuestro sistema identifica patrones que los médicos humanos podrían pasar por alto.

### Beneficios Clave:

- **Evaluación temprana del riesgo**: Identifica pacientes en riesgo años antes del diagnóstico tradicional
- **Accesibilidad**: Interfaz web que no requiere equipos especializados
- **Costo-efectivo**: Reduce la necesidad de procedimientos diagnósticos costosos
- **Información personalizada**: Proporciona recomendaciones de estilo de vida basadas en factores de riesgo individuales
- **Apoyo clínico**: Ayuda a los profesionales de la salud a priorizar pacientes de alto riesgo

## 📊 Conjunto de Datos y Características

Nuestro modelo fue entrenado con un conjunto de datos integral que contiene 74,283 registros de 20 países, con 25 características que incluyen:

### Factores Demográficos
- Edad
- Género
- Nivel de Educación
- Nivel de Ingresos
- Estado Laboral
- Estado Civil
- Residencia Urbana vs Rural

### Factores de Estilo de Vida y Ambientales
- Nivel de Actividad Física
- Estado de Tabaquismo
- Consumo de Alcohol
- Hábitos Alimenticios
- Calidad del Sueño
- Exposición a Contaminación del Aire
- Nivel de Compromiso Social
- Niveles de Estrés

### Factores Médicos y Genéticos
- IMC
- Diabetes
- Hipertensión
- Nivel de Colesterol
- Antecedentes Familiares de Alzheimer
- Factor de Riesgo Genético (APOE-E4)
- Puntuación en Pruebas Cognitivas
- Nivel de Depresión

## 🔬 Metodología

Nuestro enfoque sigue una metodología rigurosa de ciencia de datos:

1. **Recolección y Preprocesamiento de Datos**: 
   - Limpieza y validación exhaustiva de datos
   - Codificación y estandarización de características
   - Análisis de distribución de datos

2. **Análisis Exploratorio de Datos**:
   - Análisis de correlación
   - Evaluación de importancia de características
   - Análisis de distribución
   - Exploración de relaciones multivariadas

3. **Desarrollo y Selección del Modelo**:
   - Prueba de múltiples algoritmos (Random Forest, XGBoost, Gradient Boosting, SVM, etc.)
   - Optimización para alto AUC-ROC y equilibrio entre precisión/sensibilidad
   - Selección de CatBoost por rendimiento superior y manejo de características categóricas

4. **Validación y Pruebas**:
   - División 80/20 de entrenamiento-prueba
   - Validación cruzada para robustez
   - Evaluación con datos no vistos

5. **Despliegue e Integración**:
   - Aplicación web con interfaz de usuario intuitiva
   - API para potencial integración con sistemas de salud
   - Visualización de resultados y recomendaciones personalizadas

## 📈 Resultados y Rendimiento

Después de pruebas exhaustivas de múltiples algoritmos de aprendizaje automático, seleccionamos **CatBoost** como nuestro modelo final basado en su rendimiento superior:

| Métrica | Puntuación |
|--------|-------|
| Precisión (Accuracy) | 72.89% |
| Precisión (Precision) | 71.56% |
| Sensibilidad (Recall) | 74.64% |
| Puntuación F1 | 72.95% |
| **AUC-ROC** | **79.32%** |
| Especificidad | 71.25% |

Priorizamos AUC-ROC como nuestra métrica principal ya que proporciona la mejor evaluación general de la capacidad del modelo para discriminar entre pacientes que desarrollarán Alzheimer y aquellos que no.

## 🌐 Aplicación Web - https://alzheimer-front.onrender.com/

Nuestra solución está desplegada como una aplicación web fácil de usar donde:

1. Los usuarios ingresan información demográfica, de estilo de vida y médica
2. El modelo calcula el riesgo personalizado de Alzheimer
3. El sistema proporciona el nivel de riesgo y el porcentaje de confianza
4. Los usuarios reciben recomendaciones personalizadas de estilo de vida basadas en sus factores de riesgo específicos

### ¡Pruébalo tú mismo!

Visita nuestra aplicación web https://alzheimer-front.onrender.com/ y haz clic en "Iniciar Diagnóstico" para ver el sistema en acción.

### Arquitectura del Sistema

Nuestra solución consta de:

- **Frontend**: Interfaz de usuario basada en React para recopilación de datos y presentación de resultados  
  [Repositorio](https://github.com/DarwingSanchez/alzheimer-front)

- **Backend**: Servicio FastAPI para procesamiento de datos e inferencia del modelo  
  [Repositorio](https://github.com/DarwingSanchez/alzheimer-backend)

- **Web**:
 https://alzheimer-front.onrender.com/
  

- **Pipeline de ML**: Modelo CatBoost para predicción de Alzheimer

## 🛠️ Instalación y Configuración

### Configuración del Frontend

```bash
# Clonar repositorio
git clone https://github.com/DarwingSanchez/alzheimer-front
cd alzheimer-front

# Instalar dependencias
npm install

# Ejecutar servidor de desarrollo
npm start
```

### Configuración del Backend

```bash
# Clonar repositorio
git clone https://github.com/DarwingSanchez/alzheimer-backend
cd alzheimer-backend

# Crear y activar entorno virtual
python3.11 -m venv env
source env/bin/activate  # En Linux/Mac
env\Scripts\activate     # En Windows

# Instalar dependencias
pip install -r requirements.txt

# Configurar entorno
# Crear un archivo .env con SECRET_KEY="tu_clave_secreta"

# Ejecutar el servidor
uvicorn main:app --reload
```

## 👥 Equipo

Nuestro equipo interdisciplinario combina experiencia en salud, ciencia de datos e ingeniería de software:

- **Luisa Fernanda Cárdenas Sierra** - Científica de Datos
- **Darwing Steven Sánchez Londoño** - Desarrollador Full Stack
- **Carlos Andrés Patiño Ibarra** - Ingeniero de Machine Learning
- **Mónica Zuluaga Quintero** - Especialista en Integración Sanitaria

## 🔮 Desarrollo Futuro

Estamos comprometidos a mejorar continuamente nuestra solución:

1. **Mayor Precisión del Modelo**: Incorporar biomarcadores adicionales y datos longitudinales
2. **Aplicación Móvil**: Desarrollar aplicaciones nativas para iOS y Android
3. **Integración con Sistemas de Salud**: Crear APIs para integración con sistemas de historial clínico electrónico
4. **Recomendaciones Ampliadas**: Estrategias de prevención personalizadas más detalladas
5. **Soporte Multilingüe**: Ampliar la accesibilidad a hablantes no hispanohablantes

## 📝 Licencia

Este proyecto está licenciado bajo la Licencia MIT - consulta el archivo LICENSE para más detalles.

## 🙏 Agradecimientos

- Fuente del conjunto de datos: [Alzheimer's Prediction Dataset (Global)](https://www.kaggle.com/datasets/ankushpanday1/alzheimers-prediction-dataset-global) por Ankush Panday
- El proyecto fue inspirado por las palabras de Gabriel García Márquez: "La vida no es la que uno vivió, sino la que uno recuerda y cómo la recuerda para contarla."

---

<p align="center">
  <i>"La memoria es un músculo que debe ejercitarse" - Gabriel García Márquez</i>
</p>

===================================================================================================================================================================================
ENGLISH VERSION
===================================================================================================================================================================================
# NeuroCheck: Alzheimer's Prediction Model

![Alzheimer's Prediction](https://img.shields.io/badge/AI%20in%20Healthcare-Alzheimer's%20Prediction-blue)
![Tech Stack](https://img.shields.io/badge/Tech-Python%20|%20CatBoost%20|%20FastAPI%20|%20React-green)
![Status](https://img.shields.io/badge/Status-Deployed-success)

<p align="center">
  <i>"Death doesn't come with old age, but with forgetfulness" - Gabriel García Márquez</i>
</p>

## 🧠 The Problem: Late Diagnosis Costs Lives

**Did you know?** While you read this presentation, at least 3 people will have developed Alzheimer's disease without knowing it.

**More than 50%** of Alzheimer's cases are diagnosed too late, dramatically reducing treatment efficacy and quality of life. In the Americas alone, the number of Alzheimer's patients is projected to increase from 5.8 million to 13.8 million by 2050.

While Alzheimer's has no cure today, early diagnosis can:
- Slow disease progression
- Significantly improve patient quality of life
- Reduce healthcare costs
- Allow for more effective interventions
- Give patients and families more time to prepare

## 💡 Our Solution: AI-Powered Early Detection

NeuroCheck is a machine learning model that can predict Alzheimer's risk before clinical symptoms appear. By analyzing demographic, lifestyle, genetic, and clinical data, our system identifies patterns that human clinicians might miss.

### Key Benefits:

- **Early Risk Assessment**: Identify patients at risk years before traditional diagnosis
- **Accessibility**: Web-based interface requires no specialized equipment
- **Cost-Effective**: Reduces need for expensive diagnostic procedures
- **Personalized Insights**: Provides lifestyle recommendations based on individual risk factors
- **Clinical Support**: Aids healthcare professionals in prioritizing high-risk patients

## 📊 Dataset & Features

Our model was trained on a comprehensive dataset containing 74,283 records from 20 countries, with 25 features including:

### Demographic Factors
- Age
- Gender
- Education Level
- Income Level
- Employment Status
- Marital Status
- Urban vs Rural Living

### Lifestyle & Environmental Factors
- Physical Activity Level
- Smoking Status
- Alcohol Consumption
- Dietary Habits
- Sleep Quality
- Air Pollution Exposure
- Social Engagement Level
- Stress Levels

### Medical & Genetic Factors
- BMI
- Diabetes
- Hypertension
- Cholesterol Level
- Family History of Alzheimer's
- Genetic Risk Factor (APOE-E4)
- Cognitive Test Score
- Depression Level

## 🔬 Methodology

Our approach follows a rigorous data science methodology:

1. **Data Collection & Preprocessing**: 
   - Thorough data cleaning and validation
   - Feature encoding and standardization
   - Data distribution analysis

2. **Exploratory Data Analysis**:
   - Correlation analysis
   - Feature importance evaluation
   - Distribution analysis
   - Multivariate relationship exploration

3. **Model Development & Selection**:
   - Tested multiple algorithms (Random Forest, XGBoost, Gradient Boosting, SVM, etc.)
   - Optimized for high AUC-ROC and balanced precision/recall
   - Selected CatBoost for superior performance and categorical feature handling

4. **Validation & Testing**:
   - 80/20 train-test split
   - Cross-validation for robustness
   - Evaluation on unseen data

5. **Deployment & Integration**:
   - Web application with intuitive user interface
   - API for potential integration with healthcare systems
   - Results visualization and personalized recommendations

## 📈 Results & Performance

After extensive testing of multiple machine learning algorithms, we selected **CatBoost** as our final model based on its superior performance:

| Metric | Score |
|--------|-------|
| Accuracy | 72.89% |
| Precision | 71.56% |
| Recall | 74.64% |
| F1-Score | 72.95% |
| **AUC-ROC** | **79.32%** |
| Specificity | 71.25% |

We prioritized AUC-ROC as our primary metric as it provides the best overall assessment of the model's ability to discriminate between patients who will develop Alzheimer's and those who won't.

## 🌐 Web Application

Our solution is deployed as a user-friendly web application where:

1. Users enter demographic, lifestyle, and medical information
2. The model calculates personalized Alzheimer's risk
3. The system provides risk level and confidence percentage
4. Users receive personalized lifestyle recommendations based on their specific risk factors

### Try It Yourself!

Visit our web application and click "Start Diagnosis" to see the system in action.

### System Architecture

Our solution consists of:

- **Frontend**: React-based UI for data collection and result presentation  
  [Repository](https://github.com/DarwingSanchez/alzheimer-front)

- **Backend**: FastAPI service for data processing and model inference  
  [Repository](https://github.com/DarwingSanchez/alzheimer-backend)

- **ML Pipeline**: CatBoost model for Alzheimer's prediction

## 🛠️ Installation & Setup

### Frontend Setup

```bash
# Clone repository
git clone https://github.com/DarwingSanchez/alzheimer-front
cd alzheimer-front

# Install dependencies
npm install

# Run development server
npm start
```

### Backend Setup

```bash
# Clone repository
git clone https://github.com/DarwingSanchez/alzheimer-backend
cd alzheimer-backend

# Create and activate virtual environment
python3.11 -m venv env
source env/bin/activate  # On Linux/Mac
env\Scripts\activate     # On Windows

# Install dependencies
pip install -r requirements.txt

# Configure environment
# Create a .env file with SECRET_KEY="your_secret_key"

# Run the server
uvicorn main:app --reload
```

## 👥 Team

Our interdisciplinary team combines expertise in healthcare, data science, and software engineering:

- **Luisa Fernanda Cárdenas Sierra** - Data Scientist
- **Darwing Steven Sánchez Londoño** - Full Stack Developer
- **Carlos Andrés Patiño Ibarra** - Machine Learning Engineer
- **Mónica Zuluaga Quintero** - Healthcare Integration Specialist

## 🔮 Future Development

We're committed to continuously improving our solution:

1. **Enhanced Model Accuracy**: Incorporate additional biomarkers and longitudinal data
2. **Mobile Application**: Develop native mobile apps for iOS and Android
3. **Healthcare System Integration**: Create APIs for integration with EHR systems
4. **Expanded Recommendations**: More detailed personalized prevention strategies
5. **Multilingual Support**: Expand accessibility to non-English speakers

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgements

- Dataset source: [Alzheimer's Prediction Dataset (Global)](https://www.kaggle.com/datasets/ankushpanday1/alzheimers-prediction-dataset-global) by Ankush Panday
- The project was inspired by the words of Gabriel García Márquez: "Life is not what one lived, but what one remembers and how one remembers it in order to recount it."

---

<p align="center">
  <i>"The memory is a muscle that must be exercised" - Gabriel García Márquez</i>
</p>
