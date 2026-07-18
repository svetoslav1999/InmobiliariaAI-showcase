<div align="center">

<img src="assets/icon.png" alt="InmobiliarIA" width="120" />

# 🏠 InmobiliarIA

### El sistema operativo inteligente para inmobiliarias modernas

**CRM inmobiliario premium con IA integrada — captación, gestión, automatización y cierre en una sola plataforma SaaS multi-tenant.**

[![Tests](https://img.shields.io/badge/tests-313%20backend%20%2B%2043%20frontend-brightgreen)](#estado-del-proyecto)
[![Multi-tenant](https://img.shields.io/badge/multi--tenant-nivel%20ORM-blue)](#seguridad)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Alembic-336791?logo=postgresql&logoColor=white)](#arquitectura)
[![Redis](https://img.shields.io/badge/Redis-7--alpine-DC382D?logo=redis&logoColor=white)](#arquitectura)
[![Docker](https://img.shields.io/badge/Docker-Compose%204%20servicios-2496ED?logo=docker&logoColor=white)](#arquitectura)
[![Security](https://img.shields.io/badge/seguridad-89%2F100-orange)](#seguridad)
[![Version](https://img.shields.io/badge/version-v1.5.0-purple)](#estado-del-proyecto)
[![Email](https://img.shields.io/badge/email-Resend%20%C2%B7%20SendGrid%20%C2%B7%20SMTP-0F172A)](#email-marketing)
[![Next.js](https://img.shields.io/badge/Next.js-16-black)](#tecnologías)
[![FastAPI](https://img.shields.io/badge/FastAPI-Python%203.12-009688)](#tecnologías)
[![Claude](https://img.shields.io/badge/IA-Claude%20(Anthropic)-d97757)](#ai-center--11-módulos-de-inteligencia-artificial)

`IA` · `Multi-tenant` · `SaaS Web` · `Panel Super Admin` · `Dark mode enterprise` · `42 routers · 240+ endpoints`

</div>

---

> ⚠️ **Repositorio de presentación (showcase).** Muestra las **capacidades y la experiencia** del producto.
> **No** contiene código fuente, lógica de negocio ni configuración de despliegue. El código es privado.

---

<div align="center">

### ✨ Landing premium — SaaS Web

![InmobiliarIA — landing](screenshots/landing-hero.png)

*Nueva landing "Light Enterprise" — clara, elegante y centrada en el producto (inspiración Apple · Stripe · Linear · Notion · Vercel).*

| Funcionalidades | IA en cada etapa | Preguntas frecuentes |
|---|---|---|
| ![Landing — características](screenshots/landing-features.png) | ![Landing — IA](screenshots/landing-modules.png) | ![Landing — FAQ](screenshots/landing-faq.png) |

</div>

---

## Tabla de contenidos

- [¿Qué es InmobiliarIA?](#qué-es-inmobiliaria)
- [El problema que resuelve](#el-problema-que-resuelve)
- [Características](#características)
- [AI Center — 11 módulos de IA](#ai-center--11-módulos-de-inteligencia-artificial)
- [Email Marketing](#email-marketing)
- [Panel Super Admin — Control Center](#panel-super-admin--control-center)
- [Galería de capturas](#galería-de-capturas)
- [Tecnologías](#tecnologías)
- [Arquitectura](#arquitectura)
- [Seguridad](#seguridad)
- [Estado del proyecto](#estado-del-proyecto)
- [Casos de uso](#casos-de-uso)
- [Roadmap](#roadmap)
- [FAQ](#faq)
- [Demo](#demo)
- [Contacto](#contacto)

---

## ¿Qué es InmobiliarIA?

**InmobiliarIA** es una plataforma inmobiliaria SaaS premium que convierte la operativa diaria de una agencia en un flujo inteligente y automatizado. No es un CRM más: es un **sistema operativo inmobiliario** que integra inteligencia artificial en cada etapa del negocio, desde la captación del lead hasta la firma del contrato.

Construida como producto **multi-tenant sobre PostgreSQL**, cada agencia opera en un espacio totalmente aislado —datos, usuarios, branding y configuración propios— con migraciones de esquema gestionadas por Alembic para garantizar consistencia en producción.

---

## El problema que resuelve

Las agencias inmobiliarias pierden operaciones por fricción operativa: leads sin seguir, tareas manuales repetitivas, contenido lento de producir y datos dispersos en hojas de cálculo y chats. InmobiliarIA centraliza captación, CRM, contenido y cierre en una sola plataforma, y delega en IA el trabajo repetitivo para que el equipo comercial dedique su tiempo a vender.

**Beneficios clave:**
- **Más cierres, menos fricción** — pipeline visual con priorización por IA
- **Captación 24/7** — agente de WhatsApp que responde y cualifica solo
- **Contenido en minutos** — anuncios, home staging y vídeo generados con IA
- **Decisiones con datos** — analítica en tiempo real del embudo comercial
- **Listo para equipos** — roles, permisos y métricas de rendimiento por agente

---

## Características

| Módulo | Descripción |
|---|---|
| **CRM Inmobiliario** | Pipeline Kanban de 8 etapas (nuevo lead → cerrado ganado/perdido). Drag-and-drop, historial de actividad, notas, documentos y comunicaciones por lead. |
| **Gestión de Propiedades** | Cartera ilimitada con ficha completa, galería, mapa interactivo con clustering, filtros avanzados, comparador hasta 4 inmuebles y dossier PDF corporativo. |
| **Tour Virtual 360°** | Visor panorámico WebGL en cada propiedad. Salas procedurales sin fotos 360°, hotspots de navegación, fallback limpio sin GPU. |
| **Gestión de Clientes** | Perfiles de compradores, vendedores, arrendatarios e inversores. Historial de visitas, documentos, resumen IA y scoring de interés. |
| **Matching IA** | Compatibilidad cliente-propiedad por presupuesto, preferencias, zona y características. Portal privado por cliente ordenado por relevancia. |
| **Portal de Clientes** | Enlace privado por token con propiedades seleccionadas. El cliente marca "me interesa / no me interesa" y comenta por inmueble. |
| **WhatsApp Business** | Agente IA 24/7 que responde, cualifica y captura contacto. Envío directo, campañas y plantillas por organización. |
| **Visitas y Contratos** | Agenda profesional de visitas (lista/día/semana/mes) y generación de contratos legales (encargo, arras, compraventa, arrendamiento) en PDF premium. |
| **Analytics IA** | KPIs en tiempo real, funnel de ventas, evolución mensual de leads, rendimiento por agente e insights generados por IA. |
| **Automatizaciones** | Reglas por evento (triggers + actions) para nutrir leads sin intervención manual, con plantillas predefinidas. |
| **Calculadoras financieras** | Hipoteca, gastos de compra, rentabilidad, **capacidad de compra** y **rentabilidad avanzada** (ROI, cash flow, análisis de inversión), exportables a PDF/CSV. |
| **Email Marketing** | Campañas segmentadas, programadas y recurrentes, con plantillas, redacción IA, exclusiones y métricas de entrega — ver sección dedicada [más abajo](#email-marketing). |
| **Facturación** | Facturas, presupuestos y pagos de la agencia a sus clientes: numeración por serie y ejercicio, IVA desglosado por línea, panel financiero con KPIs reales y export PDF/Excel. Preparado para VeriFactu y SII, sin activar. |
| **Multi-tenant SaaS** | Aislamiento total entre agencias a nivel de ORM — sin lógica adicional por pantalla. |
| **Panel Super Admin** | Centro de control de la plataforma completa, independiente de cualquier agencia — ver sección dedicada [más abajo](#panel-super-admin--control-center). |

---

## AI Center — 11 módulos de inteligencia artificial

| Módulo | Función |
|---|---|
| 🤖 Asistente IA | Chat comercial con herramientas (buscar propiedades, agendar visitas, crear tareas) |
| 📊 Lead Scoring | Score 0-100 por lead, historial y panel de top leads |
| 📝 Anuncios IA | **12 portales AI** (Idealista, Fotocasa, Instagram, Facebook, TikTok, Inversores, AirBnB, Lujo, Familias, Habitaclia, Pisos.com, Kyero EN) + copy de email (4 plantillas) + WhatsApp Marketing (5 mensajes) + Campaña Completa. Genera el texto para copiar; el envío de campañas vive en el módulo [Email Marketing](#email-marketing) |
| 🏠 Home Staging | Transformación visual de estancias vacías para foto profesional |
| 🎬 Video Studio | Composición automática de imágenes + música → vídeo MP4 |
| 🔍 Búsqueda Visual | Buscar propiedades similares por imagen |
| 💰 Tasación Visual | Foto + ciudad → valoración estimada de mercado |
| 📐 Planos IA | Análisis de planos: habitaciones, m², sugerencias de layout |
| 🧠 AI Memory | Contexto persistente del cliente en todas las conversaciones |
| ⚡ Automations | Workflows disparados por eventos con acciones IA |
| 📈 AI Metering | Control de gasto en tokens por usuario y modelo |

---

## Email Marketing

Campañas de email a la cartera de clientes, con segmentación, automatización y métricas
reales de entrega.

| Resumen y métricas | Campañas |
|---|---|
| ![Email Marketing](screenshots/email-marketing.png) | ![Campañas](screenshots/email-campaigns.png) |

| Nueva campaña y segmentación | Plantillas |
|---|---|
| ![Nueva campaña](screenshots/email-campaign-new.png) | ![Plantillas](screenshots/email-templates.png) |

**Qué incluye:**
- **Segmentación** sobre datos reales del CRM: etiquetas, etapa del pipeline, puntuación
  del lead, ciudad, agente asignado, tipo de cliente y días sin actividad.
- **Programación y recurrencia** — envío inmediato, en una fecha concreta, o repetido a
  diario, semanalmente o cada mes. Una campaña interrumpida se reanuda sin volver a
  escribir a quien ya recibió el correo.
- **Plantillas** reutilizables con variables (cliente, agente, inmueble, precio, empresa,
  fecha) y redacción asistida por IA: asunto, cuerpo, reescritura, resumen, mejora de la
  tasa de apertura y llamada a la acción.
- **Métricas de entrega** — enviados, entregados, aperturas, clics, rebotes y bajas, con
  CTR y tasa de apertura, exportables a CSV, Excel y PDF.
- **Bajas y exclusiones** — baja en un clic con las cabeceras que Gmail y Yahoo exigen a un
  remitente masivo. La lista de exclusiones se respeta en todos los envíos, incluidos los
  automáticos, y los rebotes del proveedor entran solos.
- **Automatizaciones** — el envío se puede disparar por eventos del CRM (nuevo lead,
  presupuesto enviado, inmueble vendido, cumpleaños, cliente inactivo).

> **Requiere una cuenta de envío propia** (Resend, SendGrid o SMTP). Sin configurarla se
> puede crear, segmentar y previsualizar, pero el envío queda deshabilitado y la interfaz
> lo dice — como se ve en la captura. El sistema nunca da por enviado un correo que no
> salió, ni muestra un 0 donde en realidad no hay dato: si falta la URL pública que
> construye los enlaces de seguimiento, las aperturas y los clics aparecen como
> "No disponible".

---

## Panel Super Admin — Control Center

Plataforma de administración independiente de cualquier agencia: un Super Admin gestiona el SaaS completo (todas las organizaciones, usuarios, consumo de IA, infraestructura y seguridad) desde un panel propio, separado del CRM de cada cliente.

| Dashboard de plataforma | Infraestructura en vivo |
|---|---|
| ![Super Admin Dashboard](screenshots/admin-dashboard.png) | ![Infraestructura](screenshots/admin-infra.png) |

| Seguridad y circuit breakers | Backups |
|---|---|
| ![Seguridad](screenshots/admin-security.png) | ![Backups](screenshots/admin-backups.png) |

**Qué incluye:**
- **Organizaciones y usuarios** — vista cross-tenant de todas las agencias, planes y cuentas, sin salir del panel.
- **Consumo de IA** — coste y tokens reales por proveedor (Claude/Gemini), por organización y por usuario, con previsión de gasto mensual.
- **Infraestructura en vivo** — métricas reales de host, Redis y PostgreSQL (latencia, memoria, conexiones, tablas) cuando el despliegue las expone; nunca datos inventados — si un servicio no está disponible, el panel lo dice explícitamente y explica por qué.
- **Seguridad** — accesos, intentos fallidos, IPs sospechosas y estado de los circuit breakers de IA por proveedor, en tiempo real.
- **Backups** — crear, verificar, descargar y restaurar copias de seguridad desde la interfaz.
- **Auditoría, logs, alertas y mantenimiento** — trazabilidad completa de la actividad de plataforma.
- **Suscripciones (Stripe)** — **pendiente de activación**: la arquitectura está lista en backend y panel (planes, MRR/ARR, webhooks con firma verificada) y se enciende al configurar las claves, sin cambios de código, pero no se ha procesado ningún cobro real. No confundir con el módulo de **Facturación**, que sí está operativo y factura de la agencia a sus clientes.

> Por diseño, el panel administra la **aplicación**, no el host: la monitorización de servidor (CPU/RAM de la VPS) se delega en herramientas externas (Grafana, Prometheus, Uptime Kuma), no en acceso directo al daemon de Docker — evita dar al backend privilegios de facto sobre la máquina.

---

## Galería de capturas

> Capturas **reales** de la aplicación en su estado actual (julio 2026) con **datos de demostración** (sin información personal real). Resolución 1440×900 @2x.

### Panel, analítica y pipeline

| Dashboard interactivo | Analytics IA |
|---|---|
| ![Dashboard](screenshots/dashboard.png) | ![Analytics IA](screenshots/analytics.png) |

| Pipeline CRM | Lead Scoring IA |
|---|---|
| ![Pipeline CRM](screenshots/pipeline.png) | ![Lead Scoring IA](screenshots/lead-scoring.png) |

### Gestión operacional

| Agenda de visitas | Tareas kanban |
|---|---|
| ![Visitas](screenshots/visits.png) | ![Tareas](screenshots/tasks.png) |

| Agentes — métricas y fichas | Conversaciones |
|---|---|
| ![Agentes](screenshots/agents.png) | ![Conversaciones](screenshots/conversations.png) |

### Propiedades y clientes

| Propiedades | Nueva propiedad — formulario premium |
|---|---|
| ![Propiedades](screenshots/properties.png) | ![Nueva propiedad](screenshots/properties-new.png) |

| Propiedad — detalle completo | Mapa interactivo |
|---|---|
| ![Propiedad detalle](screenshots/property-detail.png) | ![Mapa interactivo](screenshots/map.png) |

| Clientes (CRM) | Organización |
|---|---|
| ![Clientes](screenshots/crm.png) | ![Organización](screenshots/organization.png) |

### IA y contenido

| AI Center | Asistente IA |
|---|---|
| ![AI Center](screenshots/ia-workspace.png) | ![Asistente IA](screenshots/assistant.png) |

| Generador de Anuncios IA (12 plataformas) | Floorplan IA |
|---|---|
| ![Generador de anuncios](screenshots/ads-generator.png) | ![Floorplan IA](screenshots/floorplan.png) |

| Email Marketing IA | WhatsApp Marketing IA |
|---|---|
| ![Email Marketing](screenshots/email-marketing.png) | ![WhatsApp Marketing](screenshots/whatsapp-marketing.png) |

| Home Staging IA | Tasación visual IA |
|---|---|
| ![Home Staging IA](screenshots/home-staging.png) | ![Tasación visual](screenshots/valuation.png) |

| Video Studio IA | Búsqueda visual IA |
|---|---|
| ![Video Studio](screenshots/video-studio.png) | ![Búsqueda visual](screenshots/visual-search.png) |

### Automatización, marketing y cierre

| Automatizaciones | WhatsApp Business |
|---|---|
| ![Automatizaciones](screenshots/automation.png) | ![WhatsApp Business](screenshots/whatsapp.png) |

| Email Marketing | Campañas de email |
|---|---|
| ![Email Marketing](screenshots/email-marketing.png) | ![Campañas](screenshots/email-campaigns.png) |

| Facturación — panel financiero | Facturas |
|---|---|
| ![Panel financiero](screenshots/billing-financial-panel.png) | ![Facturas](screenshots/billing-invoices.png) |

| Contratos PDF | Calculadoras financieras |
|---|---|
| ![Contratos](screenshots/contracts.png) | ![Calculadoras](screenshots/calculators.png) |

### Configuración

| Configuración | Widget embebido |
|---|---|
| ![Configuración](screenshots/settings.png) | ![Widget](screenshots/widget.png) |

### Panel Super Admin

| Organizaciones | Usuarios |
|---|---|
| ![Super Admin — Organizaciones](screenshots/admin-organizations.png) | ![Super Admin — Usuarios](screenshots/admin-users.png) |

| Consumo de IA | Auditoría |
|---|---|
| ![Super Admin — Consumo IA](screenshots/admin-ai.png) | ![Super Admin — Auditoría](screenshots/admin-audit.png) |

| Logs de plataforma |
|---|
| ![Super Admin — Logs](screenshots/admin-logs.png) |

---

## Tecnologías

Una pila moderna, async y type-safe de extremo a extremo. *(El detalle de versiones e infraestructura interna se mantiene privado.)*

**Frontend** — Next.js 16 (App Router · RSC · Turbopack) · React 19 · TypeScript (strict) · Tailwind CSS · Framer Motion · React-Three-Fiber / Three.js (3D, tour 360°) · Leaflet (mapas) · Recharts (analítica).

**Backend** — FastAPI (74 routers · 240+ endpoints, incluyendo el panel Super Admin independiente) · Python 3.12 · SQLAlchemy 2 async con hook de aislamiento multi-tenant · Alembic · Pydantic v2 · JWT + bcrypt · APScheduler (recordatorios, campañas programadas y automatizaciones).

**IA** — Claude de Anthropic (Haiku / Sonnet / Opus) con *metering* de tokens por usuario y modelo; visión para staging, tasación y búsqueda visual. **Circuit breaker económico**: presupuestos configurables por organización/usuario/proveedor/modelo con contadores Redis atómicos.

**Datos e infra** — SQLite en desarrollo · PostgreSQL en producción · Redis 7 (rate-limiting distribuido, cache IA, budget counters) · Docker Compose con healthchecks · generación de PDF · FFmpeg embebido para Video Studio.

**Email** — Resend, SendGrid o SMTP mediante un adaptador con selección automática. Sin credenciales el módulo no envía y lo declara en pantalla; los webhooks de rebote se aceptan solo con la firma del proveedor verificada (Svix HMAC-SHA256 en Resend, ECDSA P-256 en SendGrid).

---

## Arquitectura

```
        Agentes / Clientes / Portal público
                      │
        ┌─────────────▼─────────────┐
        │   Frontend Web (Next.js 16)│  App Router · RSC · dark mode
        └─────────────┬─────────────┘
                      │  HTTPS
        ┌─────────────▼─────────────┐
        │  API de Servicios (FastAPI)│  42 routers · middleware de seguridad
        │  Tenant hook (ORM)         │  WHERE organization_id = X automático
        │  require_ai_quota (dep.)   │  Budget check antes de cada llamada IA
        └──────┬────────────┬────────┘
               │            │
   ┌───────────▼──┐  ┌──────▼──────────────────────┐
   │ PostgreSQL   │  │  Redis 7                    │
   │ (datos +     │  │  rate-limit · cache IA      │
   │  ai_usage    │  │  budget counters · locks    │
   │  ledger)     │  │  circuit breaker provider   │
   └──────────────┘  └──────┬──────────────────────┘
                             │
                    ┌────────▼────────────┐
                    │ Servicios IA        │
                    │ Claude (Anthropic)  │
                    │ Gemini · Stability  │
                    │ Budget: 8 dims USD  │
                    └─────────────────────┘

        ┌──────────────────────────────────┐
        │  Panel Super Admin (/admin/*)     │  Independiente de cualquier
        │  Guard propio · cross-tenant      │  organización · fail-closed
        │  is_active AND is_superadmin      │  por defecto
        └──────────────────────────────────┘
```

Detalle ampliado en [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md).

---

## Seguridad

Modelo de seguridad de nivel enterprise, auditado en 14 rondas (junio 2026).

- **Aislamiento multi-tenant** automático a nivel de ORM — imposible filtrar datos entre agencias, incluso ante errores en los handlers.
- **Autenticación** JWT + refresh tokens, contraseñas bcrypt, contraseña de admin de producción autogenerada, roles (admin / agente / visualización).
- **Rate limiting distribuido** via Redis sliding-window (sorted set) por IP y usuario: login (5/min), chat IA (20/min), widget (20/min), webhooks (10/min). Correcto bajo N workers.
- **Circuit breaker económico IA**: presupuestos USD configurables en 8 dimensiones (global/org/usuario · diario/mensual · proveedor · modelo). Contadores Redis atómicos → enforcement < 1 ms sin latencia DB.
- **Cache de respuestas IA**: peticiones deterministas idénticas no llegan al proveedor — deduplica single-flight via Redis lock. TTL configurable (default: 24h).
- **Circuit breaker de proveedor**: N fallos consecutivos abre el circuito → fast-fail sin gastar créditos hasta que el proveedor se recupera.
- **Retry inteligente**: backoff exponencial en errores 429/529/timeout de Anthropic.
- **Webhooks** de WhatsApp verificados con HMAC-SHA256 en comparación de tiempo constante.
- **Panel Super Admin aislado**: guard dedicado (no reutiliza la autenticación de tenant) — requiere `is_active` Y `is_superadmin`; 401 sin sesión, 403 si no es Super Admin. El aislamiento multi-tenant permanece desactivado por defecto incluso para el Super Admin: cada lectura cross-tenant lo declara explícitamente, así que un descuido falla cerrado en vez de filtrar datos.
- **Tests de seguridad**: 200 tests en suite (backend), 0 fallos — incluye validación de migraciones contra PostgreSQL real, no solo SQLite.

Informe público: [SHOWCASE_SECURITY_REPORT.md](SHOWCASE_SECURITY_REPORT.md).

---

## Estado del proyecto

| Métrica | Estado |
|---|---|
| Tests backend | **313 passing** ✅ |
| Tests frontend | **43 passing** ✅ |
| TypeScript errors | **0** ✅ |
| Multi-tenant | **Sí, nivel ORM** ✅ |
| Base de datos producción | **PostgreSQL 16** ✅ |
| Migraciones | **Alembic — fuente única de verdad, validada contra PostgreSQL real** ✅ |
| Seguridad | **14 rondas auditada** ✅ |
| API | **74 routers · 240+ endpoints** ✅ |
| Panel Super Admin | **Independiente, cross-tenant, fail-closed** ✅ |
| Build producción | **verde** ✅ |
| Envío de email | **Implementado** — requiere cuenta propia de Resend/SendGrid/SMTP |
| Suscripciones Stripe | **Pendiente de activación** — arquitectura lista, sin cobros reales |
| Versión actual | **v1.5.0** |
| Distribución | SaaS Web · Docker Compose (4 servicios orquestados) |

---

## Casos de uso

- **Agencia boutique** — un equipo pequeño gestiona toda su cartera y cierra más rápido con priorización por IA.
- **Red con varias oficinas** — cada oficina opera aislada (multi-tenant) bajo una misma plataforma.
- **Equipo de captación** — el agente de WhatsApp cualifica leads entrantes fuera de horario.
- **Marketing inmobiliario** — anuncios y home staging generados en minutos, no en días.
- **Inversores** — calculadoras de capacidad de compra y rentabilidad avanzada (ROI, cash flow) para decidir con datos.

---

## Roadmap

Roadmap completo y priorizado: [ROADMAP_PUBLIC.md](ROADMAP_PUBLIC.md).

**Entregado recientemente (v1.5.0 — julio 2026)**
- [x] **Email Marketing** — campañas segmentadas, programadas y recurrentes; plantillas con variables; redacción asistida por IA; bajas y exclusiones respetadas en todos los envíos; métricas reales de entrega exportables. Requiere cuenta propia de Resend, SendGrid o SMTP
- [x] **Rebotes y quejas incorporados automáticamente** a la lista de exclusiones, aceptando solo eventos con la firma del proveedor verificada
- [x] **Facturación** — facturas, presupuestos y pagos con numeración por serie y ejercicio, IVA desglosado por línea, panel financiero y export PDF/Excel
- [x] **Interfaz unificada** — todas las pantallas comparten cabecera y componentes, eliminando las diferencias que se habían acumulado entre módulos
- [x] **313 tests backend + 43 frontend en verde**

**Entregado en v1.2.2 (julio 2026)**
- [x] **Fiabilidad del informe de costes de IA en euros** restaurada y verificada — importes reales o "no disponible", nunca inventados; totales que cuadran con el consumo real
- [x] **Analytics más rápido** (los datos aparecen de inmediato) y **optimización de base de datos** (índices depurados)
- [x] **Mayor estabilidad visual** en el panel de infraestructura
- [x] **Endurecimiento de seguridad verificado en vivo** (v1.2.1) — aislamiento entre organizaciones, anti-escalada de privilegios, anti-abuso y subida de imágenes segura
- [x] **Auditoría de pre-producción con evidencias** — recorrido visual completo (580 combinaciones), rendimiento PostgreSQL real, IA en vivo (Claude + Gemini) y regresión completa en verde
- [x] **234 tests backend + 43 frontend en verde**

**Entregado en v1.2.0 (junio 2026)**
- [x] **Panel Super Admin — Control Center** — administración de la plataforma completa independiente de cualquier agencia: organizaciones, usuarios, consumo de IA, infraestructura en vivo, seguridad, backups, auditoría y mantenimiento
- [x] **Arquitectura de facturación (Stripe)** — planes, suscripciones, MRR/ARR y webhooks listos en backend y panel; queda dormida y se activa sola al configurar las claves, sin tocar código
- [x] **Migración 0003 validada contra PostgreSQL real** vía Docker Compose (no solo SQLite) — encontrados y corregidos 2 bugs de compatibilidad antes de llegar a producción
- [x] **200 tests en verde** (+10 desde v1.1.0)

**Entregado anteriormente (v1.1.0)**
- [x] **Docker Compose completo** — 4 servicios orquestados (Next.js · FastAPI · PostgreSQL 16 · Redis 7), healthchecks encadenados, log rotation, parámetros PG optimizados
- [x] **Redis 7 integrado** — rate limiting distribuido por ventana deslizante, circuit breaker IA, caché de respuestas, budget counters de gasto por proveedor
- [x] **Security headers en frontend** (X-Frame-Options, CSP, Referrer-Policy, Permissions-Policy) — antes solo en backend
- [x] **Página 404 personalizada** — diseño coherente con la marca, links a Dashboard y Home
- [x] **Landing rediseñada "Light Enterprise"** — diseño claro y premium (Apple/Stripe/Linear/Notion/Vercel): hero potente, botones premium, pipeline de IA, capturas reales, comparativa y FAQ
- [x] **Migración a PostgreSQL 16** — base de datos enterprise con Alembic migrations
- [x] Sidebar enterprise flat + auditoría funcional completa
- [x] Streaming proxy sin timeout para llamadas IA lentas
- [x] Tour virtual 360° con visor WebGL y salas procedurales
- [x] AI Metering: control de gasto de tokens por usuario y modelo
- [x] Hardening de seguridad multi-tenant (14 rondas de auditoría)

**Próximos pasos**
- [ ] Matching UI (coincidencias cliente-propiedad)
- [ ] Contratos avanzados (ofertas, firma digital)
- [ ] Verificación de entregabilidad sobre un dominio propio (SPF/DKIM/DMARC) y campaña real de extremo a extremo
- [ ] Activación de Stripe en producción (claves live + plan de precios público)
- [ ] App móvil nativa
- [ ] API pública para integraciones de terceros

---

## FAQ

**¿Puedo ver el código fuente?**
No. Este es un repositorio de presentación; el código es privado. Aquí se muestran capacidades, experiencia y capturas reales.

**¿Las capturas son reales o mockups?**
Reales. Se generan ejecutando la aplicación con datos de demostración (sin datos personales) mediante un script de captura automatizado.

**¿Es realmente multi-tenant?**
Sí. El aislamiento se aplica a nivel de ORM: cada query lleva automáticamente `WHERE organization_id = X`. No depende de filtros manuales en cada pantalla.

**¿Qué IA utiliza?**
Claude de Anthropic (Haiku / Sonnet / Opus según la tarea), con control de gasto de tokens por usuario y modelo.

**¿Cómo se distribuye?**
SaaS Web sobre Docker. PostgreSQL en producción.

**¿Cómo solicito una demo?**
Abre un *issue* o escribe a [sveti99fm@gmail.com](mailto:sveti99fm@gmail.com). Recorrido visual en la [demo en vivo](https://svetoslav1999.github.io/inmobiliaria-demo/).

---

## Demo

Recorrido visual del producto: **[Demo en vivo](https://svetoslav1999.github.io/inmobiliaria-demo/)**

---

## Contacto

¿Interesado en el producto o en una demostración? Abre un *issue* en este repositorio o escribe a [sveti99fm@gmail.com](mailto:sveti99fm@gmail.com).

---

## Licencia

Producto propietario. El código fuente es **privado** y no se distribuye. Este repositorio (textos, capturas y documentación de presentación) © InmobiliarIA 2026 — todos los derechos reservados.

---

<div align="center">

© InmobiliarIA 2026 · Hecho con FastAPI, Next.js y Claude

</div>
