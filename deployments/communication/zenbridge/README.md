# ZenBridge: WhatsApp-to-Email Gateway

**ZenBridge** es un servicio de orquestación de comunicaciones diseñado para transformar flujos de mensajería instantánea (WhatsApp Business API) en notificaciones de correo electrónico asíncronas, optimizando la gestión de la atención y reduciendo la fatiga por notificaciones en tiempo real.

## 🧠 Lógica del Sistema

El servicio utiliza **n8n** como motor de ejecución para interceptar webhooks de Meta, procesar el contenido multimedia y de texto, y despacharlos vía SMTP hacia servidores de correo corporativos/personales.

<!--
![Arquitectura de ZenBridge](./assets/zenbridge-workflow.png) 

*(Sugerencia: Aquí coloca la captura de tu flujo de n8n cuando esté terminado)*
-->

## 🛠 Stack Tecnológico

- **Motor de Workflows**: n8n (Self-hosted).
- **API**: WhatsApp Business Cloud API (Meta).
- **Infraestructura**: Docker Containerizado.

## ⚙️ Configuración

Para desplegar este servicio, es necesario configurar las variables de entorno detalladas en `.env.example`:

- `N8N_HOST`: FQDN del servicio (ej. zen-dzamo.duckdns.org).
- `WEBHOOK_URL`: Endpoint público para la recepción de eventos de Meta.
- `GENERIC_TIMEZONE`: Zona horaria del servidor.

## 🚀 Despliegue

```bash
docker-compose up -d
```

