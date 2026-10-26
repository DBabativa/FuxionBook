# FuxionBook
FuxionBook — Plataforma SaaS de Agendamiento Multicanal y Automatización de Citas

**FuxionBook** es una plataforma tecnológica bajo modelo **SaaS (Software as a Service)** diseñada para centralizar, automatizar y escalar la gestión de citas de profesionales independientes, comercios locales y microempresas en Colombia (incluyendo despliegues piloto como *BarberSanti*).

El proyecto resuelve la fragmentación de canales de atención y reduce activamente la tasa de inasistencias (*no-shows*) mediante sincronización en tiempo real con **Google Calendar API (OAuth 2.0)** y flujos automatizados de recordatorios a través de **WhatsApp** y **correo electrónico**.

## 🚀 Arquitectura Modular (Tiered Pricing Model)

El sistema está estructurado en tres niveles de madurez digital para adaptarse al tamaño operativo de cada negocio:

| Característica / Nivel | Módulo 1: Básico (Starter) | Módulo 2: Intermedio (Professional) | Módulo 3: Avanzado (Enterprise / Custom) |
| :--- | :--- | :--- | :--- |
| **Audiencia Objetivo** | Freelancers y profesionales independientes | Pequeños negocios y consultorios (1 a 5 colaboradores) | Negocios consolidados, centros médicos, spas y franquicias |
| **Canales de Captura** | Formulario web simplificado y correo electrónico | Web interactiva + **WhatsApp** (Webhook / Chatbot en n8n) | Omnicanal (Web, WhatsApp, Correo, Widget para Instagram/Redes) |
| **Sincronización de Agenda** | Google Calendar API (1 agenda única) | Google Calendar + Panel administrativo web multi-agenda | Sincronización bidireccional multi-plataforma (Google / Outlook) |
| **Recordatorios y Reducción de No-Shows** | Confirmación inicial automática por correo | Recordatorios automáticos 24h y 2h antes (WhatsApp + Correo) con botón de confirmación/cancelación | Secuencias personalizadas y encuestas post-servicio automatizadas |
| **Dominio e Identidad** | Subdominio compartido (`fuxionbook.app`) | Subdominio personalizado con marca blanca básica | Dominio propio (`.com` / `.co`), SSL y UI/UX a medida |
| **Pagos y Analítica** | Gestión esencial sin costo de servidor | Catálogo de servicios con duraciones y precios diferenciados | Pasarelas de pago (**Wompi, Mercado Pago, PayU**) y Dashboard de KPIs |

## 🛠️ Stack Tecnológico e Integraciones

* **Frontend & Interfaz de Usuario:** HTML5, CSS3, JavaScript (ES6+), diseño responsive orientado a conversión y reserva rápida.
* **Backend & Persistencia:** Lógica de negocio modular, gestión de disponibilidad horaria y base de datos relacional (**MySQL**).
* **APIs y Autenticación:** Integración con **Google Calendar API** mediante protocolo **OAuth 2.0** para creación, actualización y bloqueo automático de bloques horarios.
* **Automatización y Mensajería:** Flujos de trabajo basados en eventos (*webhooks*) e integración con **n8n** para notificaciones transaccionales por correo y WhatsApp.
