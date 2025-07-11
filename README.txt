Assistive Robotics AI Agent

Este repositorio contiene un pipeline con inteligencia artificial para extraer estructuras de brazo robótico y tipos de gripper desde artículos científicos en PDF. Utiliza modelos locales (llama-cpp-python) y LangChain para apoyar la investigación en robótica asistencial.

Características principales:
- Lectura y segmentación de PDFs científicos
- Análisis por chunks y detección de idioma
- Extracción automática de:
  - Estructura del brazo robótico
  - Tipo de gripper
  - Tipo de documento
  - Aplicación
- Procesamiento paralelo y optimización por detención anticipada

Estructura del proyecto:
assistive-robotics-ai-agent/
├── README.txt
├── requirements.txt
├── .gitignore
├── notebooks/
├── src/
├── models/
└── docs/

Instalación:
conda create -n roboarm-gpu python=3.10
conda activate roboarm-gpu
pip install -r requirements.txt

Nota: asegúrate de tener llama-cpp-python instalado con soporte para GPU (CUDA o Metal).
