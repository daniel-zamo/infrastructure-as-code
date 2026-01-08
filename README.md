# Infrastructure as Code (IaC) - Managed Services Ecosystem

![License](https://img.shields.io/badge/license-MIT-green)
![Docker](https://img.shields.io/badge/docker-v24.0+-blue?logo=docker)
![n8n](https://img.shields.io/badge/automation-n8n-red?logo=n8n)
![OS](https://img.shields.io/badge/OS-Debian%2012-A81D33?logo=debian)

Este repositorio centraliza la definición, orquestación y despliegue de la infraestructura de servicios del ecosistema **Balaitus.net**. El proyecto sigue principios de **GitOps** y **IaC** para garantizar la portabilidad y escalabilidad de las soluciones sobre entornos Linux (Debian/OpenMediaVault).

## 🚀 Arquitectura del Proyecto

Organizada por capas para separar la infraestructura del despliegue lógico:

- **Deployments**: Orquestación Docker para servicios core (Proxy, Automation, Storage).
- **Automation**: Lógica de negocio y flujos de integración (Workflows de n8n, Scripts).

## 🛠 Tecnologías Principales

- **Orquestación**: Docker & Docker Compose.
- **Servidor Base**: Debian GNU/Linux (OMV 7).
- **Proxy/SSL**: Nginx Proxy Manager con Let's Encrypt.
- **Automatización**: n8n (Workflow Automation).

## 📂 Estructura del Repositorio

```text
.
├── automation/
│   └── workflows/       # Flujos lógicos (IA, Notificaciones, Procesamiento)
├── deployments/
│   ├── automation/      # Despliegue de n8n (Automation Hub)
│   ├── proxy/           # Nginx Proxy Manager & SSL
│   └── storage/         # Persistencia de datos
└── scripts/             # Tareas de mantenimiento de sistema
```

## ⚖️ Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

