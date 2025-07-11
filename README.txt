# 🤖 Assistive Robotics AI Agent

Este repositorio contiene un pipeline de inteligencia artificial diseñado para analizar artículos científicos en PDF y extraer automáticamente información clave sobre brazos robóticos y tipos de gripper. Está orientado a apoyar investigaciones en robótica asistencial, utilizando modelos de lenguaje locales para maximizar la privacidad y el rendimiento.

## 🚀 Funcionalidades principales

- 📄 Lectura automatizada de documentos científicos en PDF  
- 🧠 Segmentación por chunks y detección de idioma  
- 🤖 Extracción inteligente de:
  - Tipos de estructuras de brazo robótico  
  - Tipos de gripper o efector final  
  - Tipo de documento (artículo, tesis, revisión, etc.)  
  - Dominio de aplicación (hogar, salud, industria, etc.)  
- ⚡ Procesamiento paralelo con optimización por **detención anticipada** (early stopping) para acelerar el análisis  

## 📁 Estructura del proyecto

assistive-robotics-ai-agent/  
├── README.md  
├── requirements.txt  
├── .gitignore  
├── notebooks/  
├── Artículos/  

## 🧰 Instrucciones para usarlo en VS Code

### 1. Requisitos previos

- Python 3.10+  
- VS Code con extensiones:  
  - Python  
  - Jupyter  
- Git (opcional)  
- Ollama instalado y funcionando localmente

### 2. Clona el repositorio

```bash
git clone https://github.com/lauravrincong4/assistive-robotics-ai-agent.git
cd assistive-robotics-ai-agent

### 3. Crea y activa un entorno virtual con Conda
conda create -n roboarm-gpu python=3.10
conda activate roboarm-gpu

### 4. Instala las dependencias
pip install -r requirements.txt

### 5. Asegúrate de tener instalado llama-cpp-python con soporte GPU
pip install llama-cpp-python --upgrade

### 6. (Opcional) Instala Jupyter para ejecutar el notebook
pip install notebook
jupyter notebook
Asegúrate de seleccionar el entorno roboarm-gpu como kernel si usas notebooks.

