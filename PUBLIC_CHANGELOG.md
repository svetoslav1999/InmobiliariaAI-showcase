# InmobilarIA — Historial de cambios público

> Este changelog describe mejoras del producto visibles para clientes y usuarios. No incluye detalles de implementación técnica interna.

---

## v1.0.0 — Junio 2026 · PostgreSQL, Alembic y madurez enterprise

### Base de datos enterprise
- **Migración a PostgreSQL 16** — la plataforma opera sobre PostgreSQL en producción: máxima fiabilidad, transacciones ACID y concurrencia real bajo carga.
- **Alembic migrations** — las migraciones de esquema son la fuente única de verdad. La base de datos siempre está en el estado correcto al arrancar; no existen divergencias entre entornos.
- **Suite de tests ampliada** — 159 tests en verde incluyendo validación de migraciones, compatibilidad PostgreSQL real y aislamiento multi-tenant bajo ambos motores.

### Experiencia de producto
- **Sidebar enterprise** — rediseño completo al estilo HubSpot/ClickUp: grupos con cabeceras, íconos + etiquetas, navegación más rápida y limpia.
- **Centro IA** — hub central con métricas clickables y acceso directo a todos los módulos de inteligencia artificial.
- **Feedback integrado** — widget de feedback de usuario disponible en toda la plataforma.

### Rendimiento y fiabilidad
- **Proxy sin timeout** — las llamadas a IA lentas (anuncios, home staging, vídeo) ya no se cortan. El servidor transmite la respuesta en streaming sin límite de tiempo.
- **Launcher inteligente** — detecta y reemplaza instancias desactualizadas para evitar el error silencioso de "servidor antiguo sirviendo código viejo".

---

## v1.0.1 — Junio 2026 · Generador de Anuncios 12 plataformas + UX premium

### Generador de Anuncios IA expandido
- **12 portales simultáneos** — se añaden Habitaclia (Cataluña y Levante), Pisos.com (nacional) y Kyero (EN, compradores internacionales). El prompt de IA genera contenido específico para cada plataforma: tono, formato, CTA y estrategia diferenciada.
- **Email Marketing (4 plantillas)** — captación de propietario, captación de comprador, seguimiento post-visita y reactivación de lead. Asunto y cuerpo copiables por separado.
- **WhatsApp Marketing (5 mensajes)** — primer contacto, seguimiento, recordatorio de visita, recuperación de lead y cierre. Con contador de caracteres por límite de plataforma.
- **Campaña Completa** — grid con las 12 plataformas en una sola vista; exportar todo al portapapeles con un clic.

### Navegación UX premium
- **Scroll horizontal de tabs** — la fila de plataformas ahora soporta cualquier número de tabs sin corte. Scroll suave con rueda del ratón, drag horizontal y botones de navegación con desvanecimiento lateral gradual.

### Rendimiento
- **Cliente IA singleton** — el cliente Anthropic se reutiliza entre llamadas, eliminando el coste de reconexión en cada generación.
- **Prefetch de marketing** — al completar los anuncios, el contenido de email y WhatsApp se pre-genera en segundo plano. Al cambiar de modo, el resultado ya está disponible.

### Galería
- **28 capturas reales** — todas las pantallas regeneradas en modo oscuro enterprise a 1440×900 @2x, incluyendo nuevo generador de anuncios, floorplan, widget y detalle de propiedad.

---

## v0.9.1 — Junio 2026 · Refresco de presentación

- **Galería de capturas renovada** — todas las imágenes regeneradas a partir del producto actual (28 capturas reales del panel, IA, CRM, marketing, analítica y responsive), reemplazando material antiguo.
- **Navegación lateral estabilizada** — pulido estructural del *sidebar* (jerarquía de tarjetas, cero solapamientos en 280–400 px) para una experiencia impecable en cualquier ancho.
- **Documentación alineada** — README, características, arquitectura y roadmap actualizados al estado real del producto.

---

## v0.9.0 — Junio 2026 · Landing premium pública (SaaS Web)

### Nueva experiencia pública
- **Landing de clase mundial** — nueva página de inicio con escena 3D en tiempo real (skyline + red inteligente de matching), fondo vivo reactivo al cursor, animaciones al scroll y un diseño premium inspirado en las mejores plataformas SaaS.
- **Recorrido del producto** — secciones que explican la IA en cada fase comercial (captación, lead scoring, matching, seguimiento, automatización y cierre), métricas animadas, línea de tiempo del proceso y testimonios.
- **Acceso a la plataforma** — botón directo «Entrar a la Plataforma» y solicitud de demo.

### Experiencia y rendimiento
- **Totalmente responsive** — perfecto en móvil, tablet, portátil y pantallas grandes.
- **Accesible** — navegación por teclado, foco visible y respeto de «reducir movimiento».
- **Optimizada** — efectos 3D que se desactivan en móvil para mantener la fluidez.

### Calidad
- **151 tests en verde**, 0 errores TypeScript, build de producción limpio.

---

## v0.8.0 — Junio 2026 · Seguridad y estabilidad

### Seguridad reforzada
- **Aislamiento de datos multi-tenant mejorado** — el sistema garantiza que los datos de cada agencia son completamente inaccesibles para otras agencias, incluso en escenarios de error.
- **Validación de webhooks WhatsApp** — todos los mensajes entrantes de Meta se verifican criptográficamente antes de procesarse.
- **Protección de sesiones del widget** — el chat embebido en webs externas genera identificadores de sesión criptográficamente seguros.
- **Rate limiting reforzado** — protección mejorada contra uso abusivo del chat AI y los webhooks.

### Calidad
- Suite de tests ampliada a **151 tests en verde** (backend + regresiones de seguridad).
- 0 errores TypeScript, 0 errores de linting Python.
- Build limpio de 49 rutas en producción.

### Documentación
- Arquitectura técnica documentada con diagramas detallados.
- Modelo de seguridad publicado internamente.
- Roadmap de producto estructurado en 4 fases.

---

## v0.7.0 — Mayo 2026 · Gestión de equipo y cumplimiento

### Nuevas funcionalidades
- **Módulo de Agentes** — gestión completa del equipo comercial: perfiles, métricas reales de rendimiento (propiedades vendidas, leads gestionados, visitas realizadas, volumen cerrado), roles y reasignación de cartera.
- **Selector de carpeta de backups** — elige dónde almacenar las copias de seguridad con diálogo de sistema operativo.
- **Suite de cumplimiento RGPD / AI Act** — banner de cookies con log de consentimiento, páginas legales (aviso legal, privacidad, cookies, mis datos), exportación y eliminación de datos personales.
- **Assets PWA** — favicon e iconos de app para instalación como aplicación web.

### Mejoras
- **Mapa inteligente** — propiedades en mapa instantáneo usando coordenadas almacenadas; geocodificación solo para nuevas propiedades.
- **PDF de contratos premium** — diseño corporativo navy con cabecera de marca, pie de página y fecha/lugar.
- **Calculadoras financieras** — tabla de amortización con exportación CSV, tooltips de alta visibilidad.
- **Dark mode enterprise** — paleta navy unificada con contraste WCAG AA en toda la aplicación.

---

## v0.6.0 — Junio 2026 · Control de uso IA

### Nuevas funcionalidades
- **AI Metering** — control de gasto en tokens de IA por usuario y modelo. Cuotas por plan (starter / pro / enterprise). Panel de uso en organización.
- **Auto-update (escritorio)** — la aplicación de escritorio se actualiza automáticamente desde GitHub Releases.

---

## v0.5.0 y anteriores — Mayo 2026 · Fundaciones del producto

- CRM con pipeline Kanban y scoring por IA
- Portal privado por cliente con propiedades seleccionadas
- Agente de WhatsApp 24/7
- Home Staging, Video Studio, Vision Search, Tasación Visual, Floorplan AI
- Widget embebido con captura de leads
- Importación desde Idealista
- Publicación multi-portal
- Analytics en tiempo real
- Automations con triggers y actions
- Aplicación de escritorio Electron (Windows)
- Migración a Next.js 16 + React 19
