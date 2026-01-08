# AZ-104 Exam Simulator: AI-Driven Automation

![n8n](https://img.shields.io/badge/Logic-n8n-red?logo=n8n)
![AI](https://img.shields.io/badge/Model-Gemini%201.5%20Flash-blue?logo=google-gemini)
![Cloud](https://img.shields.io/badge/Target-Microsoft%20Azure-0089D6?logo=microsoft-azure)

## 📖 Descripción del Proyecto

Este workflow resuelve la "deuda de aprendizaje" en certificaciones técnicas. Utiliza **IA Multimodal** para procesar capturas de pantalla del examen AZ-104 y generar una base de conocimientos estructurada en Google Sheets.

### 🧠 Capacidades de la IA (Prompt Engineering)

El sistema actúa como un **Senior Azure Architect** realizando:

1. **Análisis de Recursos**: Identificación de componentes de Azure (VNet, RBAC, DNS).
2. **Descarte Lógico**: Explicación técnica de por qué los distractores son incorrectos.
3. **Validación de Documentación**: Referencias directas a Microsoft Learn.

## 🛠 Stack Tecnológico

- **Motor**: n8n (Self-hosted en Debian 13).
- **LLM**: Google Gemini 2.5 Flash (via API).
- **Persistence**: Google Sheets API.

## 🚀 Cómo utilizarlo

1. **Importación**: Carga el archivo `workflow.json` en tu instancia de n8n.
2. **Credenciales**: Configura `Google Gemini API` y `Google Sheets OAuth2`.
3. **Preparación**: Crea una Google Sheet con los encabezados: `Date`, `Question_File`, `Explanation`.
4. **Trigger**: Accede a la URL del `Form Trigger` y sube tu captura.

---

*Este proyecto forma parte de la infraestructura de servicios gestionados de Balaitus.net.*
