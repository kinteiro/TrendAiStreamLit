# [trendaiapp.streamlit.app](https://trendaiapp.streamlit.app)
# Proyecto de Streamlit con GPT-4 Vision y carga a S3

Este proyecto utiliza Streamlit junto con GPT-4 Vision para crear una aplicación web interactiva que permite ingestar manualmente imágenes desde la app a un bucket de S3 para su posterior analálisis o bien crear una descripcion detallada para la ayuda de generar un copywriting de dicha imagen

## Descripción del proyecto

El objetivo de este proyecto es aprovechar las capacidades de GPT-4 Vision para realizar tareas de procesamiento de imágenes y visión artificial de manera sencilla y accesible a través de una interfaz web. Los usuarios podrán cargar imágenes, aplicar el algoritmo  gpt4-ision, visualizar los resultados en tiempo real y cargarlos a S3

## Estructura de archivos

A continuación se muestra la lista de archivos presentes en este directorio:

- `streamplitapp.py`: Archivo principal que contiene el código de la aplicación Streamlit.
- `OpenAiPromptAPI_GPT4_Vision.py`: Sript que implementa las funcionalidades de GPT-4 Vision para dar respuesta como texto.
- `OpenAiTaggingPrompt_GPT4_Vision.py`: Sript que implementa las funcionalidades de GPT-4 con un promt adaptado para generar etiquetas y guardarlas en un archivo .csv en un bucket de S3
- `s3_service.py`: Módulo que proporciona funciones para la carga de archivos a un bucket de S3.
- `requirements.txt`: Archivo que especifica las dependencias del proyecto.
- `image_description_promt y image_tagging_prompt`: Prompts en formato txt para ambos scripts, uno decriptivo y otro para generar tags
- `.streamlit/secrets.toml`: secretos para configurar streamlit en local y deployed en la nube de streamlit con claves de AWS y OpenAI

## Instrucciones de uso

1. Asegúrate de tener todas las dependencias instaladas. Puedes revisar el archivo `requirements.txt` para obtener la lista completa de dependencias y sus versiones. Tambien necesitas los secretos en una estructur `.streamlit/secrets.toml`
2. Ejecuta el archivo `streamplitapp.py` para iniciar la aplicación Streamlit.
3. En la interfaz web, carga una imagen utilizando el botón correspondiente..
4. Visualiza los resultados obtenidos y, si lo deseas, guarda los resultados en un bucket de S3 utilizando el botón de carga.
