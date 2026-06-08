<div align="center">

<img src="assets/icon.png" alt="InmobilarIA" width="120" />

# 🏠 InmobilarIA

### El sistema operativo inteligente para inmobiliarias modernas

**CRM inmobiliario premium con IA integrada — captación, gestión, automatización y cierre en una sola plataforma.**

`IA` · `Multi-tenant` · `Web + Escritorio` · `Dark mode enterprise`

</div>

---

> ⚠️ **Repositorio de presentación (showcase).** Aquí se muestran las **capacidades y la experiencia** del producto.
> **No** contiene código fuente, lógica de negocio ni configuración de despliegue. Ver [Código fuente](#-código-fuente).

---

## ¿Qué es InmobilarIA?

**InmobilarIA** es una plataforma inmobiliaria premium —web y escritorio— que convierte la operativa diaria de una agencia en un flujo inteligente y automatizado. No es un CRM más: es un **sistema operativo inmobiliario** que integra inteligencia artificial en cada etapa del negocio, desde la captación del lead hasta la firma del contrato.

Construida como producto **multi-tenant**, cada agencia opera en un espacio totalmente aislado —datos, usuarios, branding y configuración propios.

---

## 🎯 El problema que resuelve

Las agencias inmobiliarias pierden operaciones por fricción operativa: leads sin seguir, tareas manuales repetitivas, contenido lento de producir y datos dispersos en hojas de cálculo y chats. InmobilarIA centraliza captación, CRM, contenido y cierre en una sola plataforma, y delega en IA el trabajo repetitivo para que el equipo comercial dedique su tiempo a vender.

## 💎 Beneficios

- **Más cierres, menos fricción** — pipeline visual con priorización por IA.
- **Captación 24/7** — agente de WhatsApp que responde y cualifica solo.
- **Contenido en minutos** — anuncios, home staging y vídeo generados con IA.
- **Decisiones con datos** — analítica en tiempo real del embudo comercial.
- **Listo para equipos** — roles, permisos y métricas de rendimiento por agente.

---

## ✨ Funcionalidades de alto nivel

| | |
|---|---|
| 🤖 **IA en todo el flujo** | Lead scoring, asistente comercial, agente de WhatsApp, tasación visual y generación de contenido. |
| 👥 **Gestión de equipo** | Perfiles de agente, asignaciones, rendimiento real y permisos por rol. |
| 🏡 **Mapas inteligentes** | Miles de propiedades en mapa sin lag, con agrupación dinámica. |
| 📄 **Contratos PDF premium** | Documentos corporativos listos para cliente. |
| 🎨 **Home Staging IA** | Amueblado virtual de estancias vacías. |
| 📊 **Analytics IA** | KPIs en tiempo real y lectura del pipeline. |
| ⚡ **Automatizaciones** | Reglas por evento para nutrir leads sin intervención manual. |
| 🌙 **Dark mode enterprise** | Sistema de diseño unificado, contraste accesible. |

### Módulos principales

- **Propiedades** — listado con filtros avanzados, fotos, mapa inteligente y dossier PDF.
- **CRM de leads** — pipeline visual con arrastrar y soltar, scoring por IA, historial y visitas.
- **Agentes** — alta/baja, permisos por rol y métricas reales de rendimiento.
- **IA comercial** — asistente con memoria, agente de WhatsApp, campañas y generador de anuncios.
- **Estudio de contenido IA** — home staging, vídeo y mejora de imágenes.
- **Analytics & automatizaciones** — dashboards y reglas por evento.
- **Calculadoras financieras** — 5 calculadoras: hipoteca, gastos, rentabilidad, **capacidad de compra** (cualificación del comprador) y **rentabilidad avanzada** (ROI, cash flow, análisis de inversión), con exportación a PDF/CSV.
- **Backups & cumplimiento** — copias verificadas y herramientas RGPD / AI Act.

---

## 📸 Capturas

> Capturas reales de la aplicación con **datos de demostración** (sin información personal real).

### Panel y analítica

| Dashboard | Analytics IA |
|---|---|
| ![Dashboard](screenshots/dashboard.png) | ![Analytics IA](screenshots/analytics.png) |

| Pipeline CRM | Lead Scoring IA |
|---|---|
| ![Pipeline CRM](screenshots/pipeline.png) | ![Lead Scoring IA](screenshots/lead-scoring.png) |

### Propiedades y clientes

| Propiedades | Ficha de inmueble |
|---|---|
| ![Propiedades](screenshots/properties.png) | ![Ficha de inmueble](screenshots/property-detail.png) |

| Mapa interactivo | Clientes (CRM) |
|---|---|
| ![Mapa interactivo](screenshots/properties-map.png) | ![Clientes](screenshots/crm-clients.png) |

### Funcionalidades premium con IA

| Home Staging IA | Video Studio IA |
|---|---|
| ![Home Staging IA](screenshots/staging.png) | ![Video Studio IA](screenshots/video-studio.png) |

| Generador de anuncios IA | Automatizaciones |
|---|---|
| ![Generador de anuncios](screenshots/anuncios.png) | ![Automatizaciones](screenshots/automations.png) |

| WhatsApp Business | Calculadoras |
|---|---|
| ![WhatsApp Business](screenshots/whatsapp.png) | ![Calculadoras](screenshots/calculators.png) |

### Responsive

| Móvil — Dashboard | Tablet — Dashboard |
|---|---|
| ![Móvil](screenshots/mobile-dashboard.png) | ![Tablet](screenshots/tablet-dashboard.png) |

---

## 🧭 Casos de uso

- **Agencia boutique** — un equipo pequeño gestiona toda su cartera y cierra más rápido con priorización por IA.
- **Red con varias oficinas** — cada oficina opera aislada (multi-tenant) bajo una misma plataforma.
- **Equipo de captación** — el agente de WhatsApp cualifica leads entrantes fuera de horario.
- **Marketing inmobiliario** — anuncios y home staging generados en minutos, no en días.

---

## 🛠️ Tecnologías (alto nivel)

Web moderna + aplicación de escritorio, con un backend de servicios y modelos de IA de Anthropic Claude para las funciones inteligentes.

`Frontend web` · `App de escritorio` · `API de servicios` · `IA (Anthropic Claude)` · `Dark mode enterprise`

> El detalle de implementación, versiones, infraestructura y arquitectura interna se mantiene privado de forma intencionada.

## 🧱 Arquitectura (simplificada)

```
Usuario
  ↓
Frontend (web / escritorio)
  ↓
API de servicios
  ↓
Base de datos
```

Ver [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md) y [docs/FEATURES.md](docs/FEATURES.md).

---

## 🗺️ Roadmap

- [ ] Integraciones con portales inmobiliarios (publicación multi-portal)
- [ ] App móvil nativa
- [ ] Firma electrónica de contratos
- [ ] Marketplace de plantillas de automatización
- [ ] Panel de analítica predictiva ampliado

---

## 🔗 Demo

Recorrido visual del producto: **[Demo en vivo](https://svetoslav1999.github.io/inmobiliaria-demo/)**

---

## 📬 Contacto

¿Interesado en el producto o en una demostración? Abre un *issue* en este repositorio.

---

## 🔒 Código fuente

El código fuente de este proyecto es **privado**.

Este repositorio tiene como finalidad mostrar las capacidades y funcionalidades del producto **sin exponer la implementación interna**. Ver el [informe de seguridad del showcase](SHOWCASE_SECURITY_REPORT.md).

---

<div align="center">

© InmobilarIA · Todos los derechos reservados

</div>
