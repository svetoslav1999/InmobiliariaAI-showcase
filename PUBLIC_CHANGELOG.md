# InmobilarIA — Historial de cambios público

> Este changelog describe mejoras del producto visibles para clientes y usuarios. No incluye detalles de implementación técnica interna.

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
