# Guía para Agentes — CV Analyzer

## Inicio Rápido

- Ejecutar: `streamlit run app.py`
- Configurar: Copiar `example.env` como `.env` y rellenar los valores
- Instalar dependencias: `pip install streamlit langchain-openai PyPDF2 pydantic python-dotenv`

## Arquitectura

- Entry point: `app.py` → `ui/streamlit_ui.py:main()`
- Cadena IA: `services/cv_evaluator.py` (LangChain, modelo `gpt-4o-mini`, temperature 0.2)
- Extracción PDF: `services/pdf_processor.py` (PyPDF2)
- Templates de prompts: `prompts/cv_prompts.py`
- Modelo de datos: `models/cv_model.py` (Pydantic `AnalisisCV`)

## Convenciones

- **Todo el codebase está en Español**: nombres de funciones, variables, comentarios, strings UI y prompts están en español.
- **Las respuestas del LLM también deben ser en Español** al trabajar con este repositorio.
- No hay tests ni configuración de linting.
- No hay archivos `__init__.py` — las importaciones dependen del comportamiento de CWD de Streamlit.

## Problemas Conocidos

- No hay problemas conocidos actualmente.

## Seguridad

- **PROHIBIDO LEER EL ARCHIVO `.env`**: Este archivo contiene claves secretas (API keys). Bajo ninguna circunstancia el asistente de IA debe leer, mostrar o procesar el contenido de este archivo.
- **PROHIBIDO MOSTRAR CLAVES**: Nunca mostrar, registrar o transmitir claves API o credenciales en mensajes, logs o salidas.
- Si necesitas verificar la configuración, consulta `example.env` que contiene valores de ejemplo.
