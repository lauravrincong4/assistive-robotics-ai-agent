# 🤖 Assistive Robotics AI Agent

Este repositorio contiene un pipeline de inteligencia artificial diseñado para analizar artículos científicos en PDF y extraer automáticamente información clave sobre brazos robóticos y tipos de gripper. Está orientado a apoyar investigaciones en robótica asistencial, utilizando modelos de lenguaje locales para maximizar la privacidad y el rendimiento.

## 🚀 Funcionalidades principales

- 📄 Lectura automatizada de documentos científicos en PDF
- 🧠 Segmentación por chunks y detección de idioma
- 🎯 Extracción inteligente de:
  - Tipos de estructuras de brazo robótico
  - Tipos de gripper o efector final
  - Tipo de documento (artículo, tesis, revisión, etc.)
  - Dominio de aplicación (hogar, salud, industria, etc.)
- ⚡ Procesamiento paralelo con **detención anticipada** (early stopping) para acelerar el análisis

---

## 🗂️ Estructura del proyecto

```
assistive-robotics-ai-agent/
├── README.md               # Descripción del proyecto
├── requirements.txt        # Dependencias necesarias
├── .gitignore              # Archivos ignorados por Git
├── notebooks/              # Cuadernos Jupyter (análisis, pruebas)
├── src/                    # Código fuente del agente
├── models/                 # Modelos locales si se usan
└── docs/                   # Documentación adicional
```

---

## 💻 Instrucciones para usarlo en VS Code

### 1. Requisitos previos

- Tener instalado [Python 3.10+](https://www.python.org/)
- Tener [VS Code](https://code.visualstudio.com/) con extensiones recomendadas:
  - Python
  - Jupyter
- Tener [Git](https://git-scm.com/) instalado y configurado (opcional)
- Tener [Ollama](https://ollama.com/) instalado y corriendo localmente

### 2. Clona el repositorio

```bash
git clone https://github.com/lauravrincong4/assistive-robotics-ai-agent.git
cd assistive-robotics-ai-agent
```

### 3. Crea y activa un entorno virtual con Conda

```bash
conda create -n roboarm-gpu python=3.10
conda activate roboarm-gpu
```

### 4. Instala las dependencias

```bash
pip install -r requirements.txt
```

### 5. Abre el proyecto en VS Code

Desde la terminal:

```bash
code .
```

> Asegúrate de seleccionar el entorno `roboarm-gpu` como kernel si usas notebooks.

---

## ⚙️ Ejemplo de uso

Puedes ejecutar el pipeline desde un Jupyter Notebook en `notebooks/` o usar scripts desde `src/` como este:

```python
from langchain_ollama import OllamaLLM

llm = OllamaLLM(model="llama2")
respuesta = llm.invoke("¿Qué estructuras de brazo robótico son más comunes?")
print(respuesta)
```

---

## 🧠 Consideraciones adicionales

- Este proyecto puede funcionar **100% offline** con modelos locales como `llama-cpp-python`
- Se recomienda usar modelos ligeros (`llama2:7b`, `mistral`, `gemma`) si no cuentas con una GPU potente
- Puedes activar la detención anticipada en el código para acelerar el procesamiento masivo de PDFs
