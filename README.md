# Challenge Alura Agente 

## Agente IA para Análisis de Entregas

## 📋 Tabla de Contenidos

- [Descripción del Proyecto](#-descripción-del-proyecto)
- [Características](#-características)
- [Tecnologías Utilizadas](#-tecnologías-utilizadas)
- [Estructura del Proyecto](#-estructura-del-proyecto)
- [Instalación y Configuración Local](#-instalación-y-configuración-local)
- [Despliegue en Render](#-despliegue-en-render)
- [Uso de la Aplicación](#-uso-de-la-aplicación)
- [Variables de Entorno](#-variables-de-entorno)


## 🎯 Descripción del Proyecto

Este proyecto consiste en un **agente de inteligencia artificial** que permite a cualquier persona colaboradora hacer preguntas en lenguaje natural sobre un dataset de entregas, obteniendo respuestas directas sin necesidad de abrir documentos o escribir consultas complejas.

El agente está construido para resolver un problema real: **la pérdida de horas buscando información dentro de archivos**. Ahora, cualquier usuario puede preguntar:

> *"¿Cuál fue el tiempo promedio de entrega en marzo de 2022?"*
> 
> *"¿Qué categoría de producto tuvo más entregas?"*
> 
> *"¿Cómo afecta el clima a los tiempos de entrega?"*

Y obtener respuestas inmediatas en lenguaje natural.

---

## ✨ Características

### 💬 Chat Interactivo con IA
- **Preguntas en lenguaje natural**: Haz preguntas sobre los datos sin necesidad de saber SQL o programación.
- **Respuestas inmediatas**: El agente procesa tu pregunta y devuelve una respuesta clara y concisa.
- **Historial de conversación**: Mantén un registro de todas tus interacciones.

### 📊 Análisis de Datos en Tiempo Real
- **Métricas clave**: Visualiza el total de entregas, tiempo promedio, número de categorías y experiencia promedio de los colaboradores.
- **Estadísticas descriptivas**: Distribuciones por categoría, clima, tráfico y experiencia.
- **Filtros dinámicos**: Filtra los datos por rango de fechas y categoría de producto.

### 📈 Visualizaciones Interactivas
- **Tiempo de entrega por categoría**: Gráfico de barras con el tiempo promedio por categoría de producto.
- **Evolución temporal**: Línea de tiempo con las entregas diarias y media móvil de 7 días.
- **Relación experiencia vs tiempo**: Scatter plot que muestra la relación entre los años de experiencia y el tiempo de entrega.
- **Mapa de calor de correlaciones**: Matriz de correlación entre variables numéricas.
- **Distribución de tiempos**: Histograma interactivo con estadísticas detalladas.

### 🗃️ Explorador de Datos
- **Visualización de datos**: Navega por el dataset con opciones de filtrado de columnas.
- **Descarga de CSV**: Exporta los datos filtrados en formato CSV para análisis externos.

### 📝 Generador de Reportes
- **Resumen ejecutivo**: Métricas clave y distribuciones principales.
- **Análisis de rendimiento**: Evaluación de los colaboradores y condiciones óptimas.
- **Tendencias temporales**: Patrones diarios y por hora.
- **Análisis de factores**: Impacto del clima y tráfico en los tiempos de entrega.

---

## 🛠️ Tecnologías Utilizadas

| Tecnología | Versión | Propósito |
|------------|---------|-----------|
| **Python** | 3.11.7 | Lenguaje de programación principal |
| **Streamlit** | 1.43.0 | Framework para la interfaz web |
| **LangChain** | 0.3.24 | Framework para construir agentes de IA |
| **OpenAI** | 0.3.24 | Modelo GPT-3.5-turbo para procesamiento de lenguaje natural |
| **Pandas** | 2.2.2 | Manipulación y análisis de datos |
| **Plotly** | 5.22.0 | Visualizaciones interactivas |
| **Matplotlib** | 3.10.0 | Visualizaciones estáticas |
| **Seaborn** | 0.13.2 | Visualizaciones estadísticas |
| **Python-dotenv** | 1.0.1 | Gestión de variables de entorno |
| **Render** | - | Plataforma de despliegue (PaaS) |

---

## 📁 Estructura del Proyecto
```

  proyecto-agente-ia/
  │
  ├── .env # Variables de entorno (no subir a GitHub) 
  ├── .gitignore # Archivos ignorados por Git 
  ├── Procfile # Comando de inicio para Render opcional, puedes cargarlo directamente
  ├── README.md # Este archivo
  ├── requirements.txt # Dependencias del proyecto
  ├── runtime.txt # Versión de Python para Render opcional, render lo carga automaticamente
  │
  ├── app.py # Aplicación Streamlit principal
  ├── agente.py # Lógica del agente de IA
  ├── procesador.py # Procesamiento de documentos
  ├── utils.py # Funciones utilitarias
  │
  ├── data/ # Datos del proyecto
  │ ├── datos_entregas.csv # Dataset de entregas
  │ └── resumen_dataset.csv # Resumen estadístico
  │
  ├── figuras/ # Visualizaciones generadas
  │ ├── tiempos_entrega.png
  │ ├── experiencia_rendimiento.png
  │ ├── analisis_temporal.png
  │ └── analisis_geografico.png
  │
  └── notebooks/ # Notebooks de exploración
  └── exploracion.ipynb

```

---

## 🔧 Instalación y Configuración Local

### Requisitos Previos
- Python 3.11 o superior instalado
- Cuenta de Groq (para obtener tu API key)
- Git (opcional, para clonar el repositorio)

### Pasos para Instalación

1. **Clonar el repositorio**
```
git clone https://github.com/tu-usuario/proyecto-agente-ia.git
cd proyecto-agente-ia

```

Crear y activar entorno virtual

Windows:

```
python -m venv venv
venv\Scripts\activate

```
macOS/Linux:

```
python3 -m venv venv
source venv/bin/activate

```
## Instalar dependencias

```
pip install -r requirements.txt
Configurar variables de entorno

```

# Crear archivo .env y agregar tu API key

```
echo "API_KEY=tu-api-key-aqui" > .env

```


## Descargar el dataset

- Archivo datos_entregas.csv


## Ejecutar la aplicación localmente

```
streamlit run app.py

```

## Abrir en el navegador

Ve a http://localhost:8501

## 🚀 Despliegue en Render

## Paso 1: Preparar el Código

Asegúrate de tener los siguientes archivos en la raíz del proyecto:


✅ app.py - Aplicación principal

✅ requirements.txt - Dependencias

✅ Procfile - Comando de inicio

✅ runtime.txt - Versión de Python

Contenido del Procfile:

```
web: streamlit run app.py --server.port=$PORT --server.address=0.0.0.0 --server.headless=true

```

## Paso 2: Subir a GitHub

✅  Crea un repositorio en GitHub (público o privado)

✅  Sube todos los archivos del proyecto

## Paso 3: Desplegar en Render

Crear cuenta en Render (es gratis, puedes usar GitHub)

Crear un nuevo Web Service:

Haz clic en "New +" → "Web Service"

Conecta tu repositorio de GitHub

Selecciona el repositorio proyecto-agente-ia

Configuración del servicio:

Name: agente-ia-entregas (o el nombre que quieras)

Branch: main

Runtime: Python 3

Build Command: pip install -r requirements.txt

Start Command: El Procfile se usará automáticamente

Configurar variables de entorno:

Ve a la sección "Environment Variables"

Agrega:

Key: API_KEY

Value: sk-... (tu clave)

Haz clic en "Add Environment Variable"

Crear el servicio:

Haz clic en "Create Web Service"

Espera de 3 a 5 minutos mientras Render construye y despliega tu app

Acceder a tu aplicación:

Una vez completado, verás la URL

💻 Uso de la Aplicación
1. Configuración Inicial
Carga el dataset: Haz clic en "📂 Cargar Dataset" en la barra lateral.

Configura tu API key: Ingresa tu OpenAI API key en la barra lateral.

Espera la inicialización: El agente se cargará automáticamente.

2. Pestaña "💬 Chat con Agente"
Haz preguntas en lenguaje natural:

Ejemplos de preguntas:

"¿Cuál es el tiempo promedio de entrega?"

"¿Qué categoría de producto tiene más entregas?"

"¿Cómo afecta el clima al tiempo de entrega?"

"¿Cuál es el mejor día para hacer entregas?"

"¿Qué colaboradores tienen mejor rendimiento?"

3. Pestaña "📊 Análisis de Datos"
Visualiza estadísticas y distribuciones:

Métricas clave (total entregas, tiempo promedio, etc.)

Distribución por categoría de producto

Distribución por clima

Nivel de tráfico y experiencia de colaboradores

4. Pestaña "📈 Visualizaciones"
Selecciona entre diferentes tipos de visualización:

Tiempo de entrega por categoría

Evolución temporal de entregas

Relación experiencia vs tiempo

Mapa de calor de correlaciones

Distribución de tiempos

5. Pestaña "🗃️ Datos"
Explora los datos sin procesar:

Selecciona columnas específicas

Ajusta el número de filas a mostrar

Descarga el dataset en CSV con los filtros aplicados

6. Pestaña "📝 Reportes"
Genera reportes automáticos:

Resumen Ejecutivo: Métricas clave y distribuciones

Análisis de Rendimiento: Evaluación de colaboradores y condiciones

Tendencias Temporales: Patrones diarios y por hora

Análisis de Factores: Impacto de clima y tráfico

## 💻 Uso de la Aplicación

1. Configuración Inicial
Carga el dataset: Haz clic en "📂 Cargar Dataset" en la barra lateral.

Configura tu API key: Ingresa tu OpenAI API key en la barra lateral.

Espera la inicialización: El agente se cargará automáticamente.

2. Pestaña "💬 Chat con Agente"
Haz preguntas en lenguaje natural:

Ejemplos de preguntas:

"¿Cuál es el tiempo promedio de entrega?"

"¿Qué categoría de producto tiene más entregas?"

"¿Cómo afecta el clima al tiempo de entrega?"

"¿Cuál es el mejor día para hacer entregas?"

"¿Qué colaboradores tienen mejor rendimiento?"

3. Pestaña "📊 Análisis de Datos"
Visualiza estadísticas y distribuciones:

Métricas clave (total entregas, tiempo promedio, etc.)

Distribución por categoría de producto

Distribución por clima

Nivel de tráfico y experiencia de colaboradores

4. Pestaña "📈 Visualizaciones"
Selecciona entre diferentes tipos de visualización:

Tiempo de entrega por categoría

Evolución temporal de entregas

Relación experiencia vs tiempo

Mapa de calor de correlaciones

Distribución de tiempos

5. Pestaña "🗃️ Datos"
Explora los datos sin procesar:

Selecciona columnas específicas

Ajusta el número de filas a mostrar

Descarga el dataset en CSV con los filtros aplicados

6. Pestaña "📝 Reportes"
Genera reportes automáticos:

Resumen Ejecutivo: Métricas clave y distribuciones

Análisis de Rendimiento: Evaluación de colaboradores y condiciones

Tendencias Temporales: Patrones diarios y por hora

Análisis de Factores: Impacto de clima y tráfico

## 🔐 Variables de Entorno
Variable	Descripción	Obligatoria	Ejemplo
OPENAI_API_KEY	API key de OpenAI para el modelo GPT	✅ Sí	sk-...
MODEL_NAME	Modelo de OpenAI a utilizar	❌ No	gpt-3.5-turbo
TEMPERATURE	Temperatura del modelo (0-1)	❌ No	0.1
MAX_TOKENS	Máximo de tokens en respuesta	❌ No	1000


