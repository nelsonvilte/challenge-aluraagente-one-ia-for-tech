# Challenge Alura Agente 

## Agente IA para Análisis de Entregas

## 📋 Tabla de Contenidos

- [Descripción del Proyecto](#-descripción-del-proyecto)
- [Características](#-características)
- [Tecnologías Utilizadas](#-tecnologías-utilizadas)
- [Estructura del Proyecto](#-estructura-del-proyecto)


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

proyecto-agente-ia/
│
├── .env # Variables de entorno (no subir a GitHub)
├── .gitignore # Archivos ignorados por Git
├── Procfile # Comando de inicio para Render
├── README.md # Este archivo
├── requirements.txt # Dependencias del proyecto
├── runtime.txt # Versión de Python para Render
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


---

## 🔧 Instalación y Configuración Local

### Requisitos Previos
- Python 3.11 o superior instalado
- Cuenta de Qroq (para obtener tu API key)
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