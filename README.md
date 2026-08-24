# CV Analyzer

Aplicación web que evalúa currículums usando inteligencia artificial. Analiza CVs en PDF contra un puesto de trabajo específico y proporciona una evaluación objetiva con porcentaje de ajuste.

## Instalación

### Crear entorno virtual

```bash
python -m venv .venv
source .venv/bin/activate
```

### Instalar dependencias

Con **pip**:

```bash
pip install streamlit langchain-openai PyPDF2 pydantic python-dotenv
```

Con **uv**:

```bash
uv pip install streamlit langchain-openai PyPDF2 pydantic python-dotenv
```

## Variables de entorno

1. Copia el archivo `example.env` como `.env`:
   ```bash
   cp example.env .env
   ```

2. Edita el archivo `.env` con tus datos reales:
   ```env
   OPENAI_API_KEY=tu-api-key-aqui
   ```

El archivo `.env` contiene información sensible y está excluido del repositorio.

## Ejecución

```bash
streamlit run app.py
```
