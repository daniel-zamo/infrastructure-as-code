# Automation Hub: Multi-Service Orchestration Engine

![Status](https://img.shields.io/badge/status-active-success)
![Category](https://img.shields.io/badge/category-automation-red)
![Stack](https://img.shields.io/badge/stack-n8n--docker-blue?logo=n8n)

Este despliegue constituye el núcleo de automatización del ecosistema. Diseñado bajo principios de **infraestructura inmutable** y **seguridad por defecto**, este motor orquesta flujos críticos que van desde la integración de mensajería (WhatsApp/Email) hasta el procesamiento de datos mediante IA.

## 🚀 Capacidades de la Plataforma
- **ZenBridge Engine**: Transformación de flujos asíncronos de WhatsApp Business API a SMTP.
- **AI-Ops Pipeline**: Procesamiento de exámenes AZ-104 mediante modelos de visión (Gemini).
- **System Integrity**: Gestión centralizada de errores y limpieza automática de base de datos.

## 🛠 Especificaciones Técnicas
- **Core**: n8n (Containerized).
- **Runtime Hardening**: Ejecución con usuario no-root, límites de recursos (CPU/RAM) y persistencia optimizada en SQLite.
- **Observability**: Integración con un *Global Error Handler* para monitoreo de fallos en workflows.

## ⚙️ Despliegue
1. Clone este repositorio.
2. Copie el archivo de ejemplo y configure sus variables:
   ```bash
   cp .env.example .env
   ```

3. Inicie el stack:
   ```bash
   docker compose up -d
   ```

## 🔒 Consideraciones de Seguridad

El despliegue fuerza permisos estrictos en los archivos de configuración (`N8N_ENFORCE_SETTINGS_FILE_PERMISSIONS`) y utiliza cookies seguras para entornos de producción tras un Reverse Proxy.

