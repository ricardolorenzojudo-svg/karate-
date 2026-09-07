# 🥋 Karate Do Shotokan · Asistente Virtual del Dojo

Asistente virtual con IA (sistema RAG) para el dojo de Karate Do Shotokan de Ricardo Lorenzo.

## 🌐 Portal

https://ricardolorenzojudo-svg.github.io/karate/

La página redirige al asistente servido desde n8n (webhook `portal-karate`).

## 🏗️ Arquitectura

- **n8n**: workflow "Asistente Karate Chat" (AI Agent + Vector Store Tool).
- **Qdrant**: colección `karate_docs` (768 dimensiones, distancia Cosine).
- **Ollama**: embeddings con `nomic-embed-text`.
- **Groq**: modelo de lenguaje del agente.
- **Ingesta de datos**: script Python `ingesta_karate.py` (ruta local `C:\Karate\`).

## 📚 Biblioteca de conocimiento

Apuntes propios del dojo y temario oficial por grados (kyu a dan):
kihon, katas Shotokan, kumite, reglamento, Dojo Kun y etiqueta.

Los documentos se gestionan como `.txt` en `C:\Users\USER\Documents\karate-docs`,
con el grado como prefijo en el nombre del archivo
(`6kyu_...`, `3kyu_...`, `1dan_...`, `general_...`).

## 🔧 Mantenimiento

1. Añadir o actualizar documentos `.txt` en la carpeta `karate-docs`.
2. Ejecutar la ingesta: `python C:\Karate\ingesta_karate.py`
3. Si se modificó el HTML del portal o el System Message, publicar el workflow en n8n.

## 👤 Autor

Creado por Ricardo Lorenzo · Ricardo Lorenzo Karate Do Shotokan
