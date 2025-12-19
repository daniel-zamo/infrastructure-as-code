# Infrastructure as Code (IaC) - Managed Services Ecosystem

Este repositorio centraliza la definición, orquestación y despliegue de la infraestructura de servicios del ecosistema **Balaitus.net**. El proyecto sigue principios de **GitOps** y **IaC** para garantizar la portabilidad y escalabilidad de las soluciones sobre entornos Linux (Debian/OpenMediaVault).

## 🚀 Arquitectura del Proyecto

La infraestructura está organizada por dominios funcionales, permitiendo una gestión modular de los contenedores Docker y sus configuraciones asociadas.

- **Deployments**: Definiciones de servicios (Docker Compose) categorizados por su propósito (Comunicación, Proxy, Almacenamiento).
- **Automation**: Scripts de mantenimiento y flujos de integración.
- **Security**: Políticas de endurecimiento (hardening) y gestión de certificados SSL.

## 🛠 Tecnologías Principales

- **Orquestación**: Docker & Docker Compose.
- **Servidor Base**: Debian GNU/Linux (OMV 7).
- **Proxy/SSL**: Nginx Proxy Manager con Let's Encrypt.
- **Automatización**: n8n (Workflow Automation).

## 📂 Estructura del Repositorio

```text
.
├── deployments/
│   ├── communication/   # Pasarelas de mensajería y flujos de notificación
│   ├── proxy/           # Gestión de tráfico e identidad (NPM)
│   └── storage/         # Persistencia de datos y nubes privadas
└── scripts/             # Automatización de tareas de sistema y despliegue
```

