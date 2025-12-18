# Challenge-Telecom-X
Desafío Alura One
Análisis de Evasión de Clientes (Churn) - Telecom X 🚀
📋 Descripción del Proyecto
Este proyecto fue desarrollado como parte de un desafío para la empresa Telecom X. El objetivo principal fue realizar un proceso completo de ETL (Extract, Transform, Load) y un Análisis Exploratorio de Datos (EDA) sobre la base de datos de clientes para identificar las causas principales de la evasión (Churn).

Los resultados de este análisis sirven como base para que el equipo de Ciencia de Datos desarrolle modelos predictivos precisos.

🛠️ Tecnologías Utilizadas
Python 3.x

Pandas: Manipulación y limpieza de datos.

Matplotlib & Seaborn: Visualización de datos y análisis estadístico.

Google Colab: Entorno de desarrollo.

GitHub: Versionamiento de código.

📂 Estructura del Proceso
1. Extracción (Extract)
Los datos fueron obtenidos directamente desde una API en formato JSON. Se utilizó la librería pandas para la ingesta inicial de la información.

2. Transformación (Transform)
Esta fue la etapa más crítica del proyecto, donde se realizaron las siguientes tareas:

Normalización de datos: Se "aplanaron" columnas anidadas (customer, phone, internet, account) que contenían diccionarios internos.

Limpieza de tipos: Se convirtió la columna TotalCharges_account de tipo object a float64.

Tratamiento de nulos: Se identificaron y trataron valores faltantes mediante la coherción de errores y la imputación lógica (clientes nuevos con cargos en 0).

Binarización: Se transformaron las variables categóricas clave (como Churn) a formato numérico (0/1) para facilitar el análisis estadístico.

3. Análisis Exploratorio (EDA)
Se realizó un análisis de correlación para identificar los factores que más influyen en la salida de los clientes.

📈 Hallazgos Principales
Tras el análisis de correlación, se identificaron los siguientes patrones:

Factores de Riesgo (Churn alto):

Contratos Mes a Mes: Es el mayor predictor de fuga.

Internet por Fibra Óptica: Presenta una tasa de evasión superior a otras tecnologías.

Falta de servicios adicionales: La ausencia de Soporte Técnico y Seguridad en Línea aumenta la probabilidad de salida.

Factores de Retención (Lealtad):

Antigüedad (Tenure): A mayor tiempo en la empresa, menor es el riesgo de churn.

Contratos a Largo Plazo: Los contratos a dos años son la herramienta de retención más efectiva.
