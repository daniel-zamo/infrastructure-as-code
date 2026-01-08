# Infrastructure as Code (IaC) - Managed Services Ecosystem

![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)
![Docker](https://img.shields.io/badge/docker-v26.0+-blue?style=for-the-badge&logo=docker)
![n8n](https://img.shields.io/badge/automation-n8n-red?style=for-the-badge&logo=n8n)
![OS](https://img.shields.io/badge/OS-Debian%2013-A81D33?style=for-the-badge&logo=debian)

Este repositorio centraliza la definición, orquestación y despliegue de la infraestructura de servicios del ecosistema **Balaitus.net**. El proyecto sigue principios de **GitOps** y **IaC** para garantizar la portabilidad y escalabilidad de soluciones sobre entornos Linux modernos.

## 🚀 Arquitectura del Proyecto

La infraestructura está organizada por capas para separar el despliegue de servicios de la lógica de negocio:

- **Deployments**: Orquestación Docker para servicios core (Proxy, Automation Hub, Storage).
- **Automation**: Activos lógicos, incluyendo flujos de integración (Workflows de n8n) y scripts de sistema.
- **Security**: Gestión de identidad, certificados SSL y políticas de endurecimiento.

## 🛠 Tecnologías Principales

- **Orquestación**: Docker & Docker Compose v2.x.
- **Servidor Base**: Debian 13 "Trixie" (OMV 8 compatible).
- **Proxy/SSL**: Nginx Proxy Manager con Let's Encrypt.
- **Automatización**: [n8n](https://n8n.io/) como motor de ejecución principal.

## 📂 Estructura del Repositorio

```text
.
├── automation/
│   └── workflows/       # Lógica distribuida (IA, Notificaciones, Procesamiento)
├── deployments/
│   ├── automation/      # Despliegue de n8n (Automation Hub)
│   ├── proxy/           # Gestión de tráfico e identidad (NPM)
│   └── storage/         # Persistencia y nubes privadas
└── scripts/             # Automatización de tareas de mantenimiento
```

---
*Diseñado bajo estándares de SRE para el despliegue de microservicios autohospedados.*
