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

Tipo de contrato

El análisis muestra que el tipo de contrato es el factor más determinante en la evasión:

Contrato month-to-month: ≈ 43% de churn

Contrato one year: ≈ 11% de churn

Contrato two year: ≈ 3% de churn

Los contratos mensuales presentan una tasa de evasión significativamente mayor, lo que sugiere que la falta de compromiso a largo plazo facilita la decisión de abandono.

2️⃣ Antigüedad del cliente (tenure)

Los clientes que abandonan la empresa tienen, en promedio, una menor antigüedad, lo que indica que el churn ocurre principalmente en las primeras etapas de la relación con el cliente.

3️⃣ Cargos mensuales

Los clientes con churn presentan cargos mensuales ligeramente más altos, lo que puede indicar una percepción de bajo valor frente al costo del servicio.

4️⃣ Servicios adicionales

La ausencia de servicios adicionales como Tech Support se asocia a mayores tasas de churn, sugiriendo que el valor agregado contribuye a la retención.

📌 Calidad de los datos

Se identificaron 224 registros sin información de churn, los cuales se mantuvieron como valores nulos para evitar introducir supuestos no fundamentados. Estos registros no fueron considerados en los análisis comparativos.

🎯 Conclusión general

El churn en Telecom X está fuertemente asociado a contratos flexibles, baja antigüedad y menor valor percibido del servicio. Estos factores deben ser priorizados en futuras estrategias de retención y en modelos predictivos de evasión.

🚀 Recomendaciones

Incentivar la migración desde contratos mensuales a contratos de mayor duración

Implementar estrategias de retención temprana para clientes nuevos

Reforzar la oferta de servicios adicionales

Utilizar el dataset limpio para desarrollar modelos predictivos de churn


