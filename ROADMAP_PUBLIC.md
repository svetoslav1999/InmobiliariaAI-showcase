# InmobiliarIA — Roadmap Público

> Última actualización: junio 2026 · v1.2.0

Este roadmap refleja las prioridades del producto ordenadas por impacto comercial para las agencias inmobiliarias. Los plazos son orientativos.

---

## Estado actual: v1.2.0

El producto está en **estado de producción técnica**: backend estable sobre PostgreSQL real, seguridad auditada (14 rondas), 200 tests en verde, build limpio, despliegue SaaS Web vía Docker Compose (4 servicios) y un panel Super Admin propio para administrar la plataforma. Lo que sigue es completar el ciclo comercial completo (cobro, contratos avanzados, automatizaciones) y escalar a más agencias.

---

## Recientemente completado

- ✅ **SaaS Web** — la plataforma ya no es solo escritorio: despliegue completo vía Docker Compose (Next.js · FastAPI · PostgreSQL 16 · Redis 7), con healthchecks encadenados.
- ✅ **Panel Super Admin** — control de plataforma, infraestructura, seguridad y backups independiente de cualquier agencia.
- ✅ **Arquitectura de facturación (Stripe)** — planes, suscripciones y webhooks listos en backend; activación pendiente de claves de producción (ver punto 4).

---

## Próximos pasos — por impacto comercial

### 1. Matching UI — alta prioridad

**Qué:** página de coincidencias entre clientes y propiedades. Ver qué propiedades encajan mejor con el perfil de un cliente y viceversa, con puntuación de compatibilidad.

**Por qué:** el algoritmo de matching ya está implementado (es el que alimenta el portal de clientes), pero no hay una pantalla para que el agente lo consulte directamente en su flujo de trabajo diario.

**Impacto:** reduce el tiempo de búsqueda manual y aumenta la tasa de conversión visita → oferta.

---

### 2. Contratos avanzados — alta prioridad

**Qué:**
- Registro de ofertas y contraofertas con historial de precios
- Generación de contrato en PDF desde los datos de la propiedad y el cliente
- Estados del proceso: borrador → oferta enviada → negociación → aceptado → firmado
- Actualización automática del estado de la propiedad al cerrar

**Por qué:** actualmente el módulo de contratos es básico. El cierre real de operaciones ocurre fuera del sistema.

**Impacto:** cierra el flujo de venta dentro de la plataforma. Los datos de ventas cerradas se usan en analytics.

---

### 3. Entregabilidad del correo sobre dominio propio — alta prioridad

**Entregado en v1.5.0:** el módulo de Email Marketing (campañas segmentadas, programadas y
recurrentes, plantillas, exclusiones y métricas de entrega) y los correos automáticos de
visita — confirmación, recordatorio 24 h antes y follow-up posterior — están implementados y
conectados al planificador.

**Qué falta:** ejercitarlo contra un dominio real. Configurar SPF, DKIM y DMARC en el
dominio de la agencia, verificarlo en el proveedor y hacer una campaña completa de extremo a
extremo. Hasta entonces el comportamiento está validado con eventos de proveedor, no con
envío masivo real.

**Por qué:** un remitente sin autenticar acaba en spam por muy bien construido que esté el
mensaje. La entregabilidad se demuestra enviando, no programando.

**Impacto directo:** reducción de no-shows estimada en 20-30% una vez el correo llega de
forma fiable.

---

### 4. Billing — activación de Stripe en producción — alta prioridad

**Qué:** la arquitectura de suscripción SaaS (planes starter / pro / enterprise, MRR/ARR, webhooks) ya está construida en backend y panel Super Admin. Falta activarla con claves de producción y publicar el plan de precios. El control de cuotas de IA por plan ya está implementado y en uso.

**Por qué:** requisito para cobrar a clientes y escalar el negocio.

**Impacto:** habilita el modelo de ingresos recurrentes.

---

### 5. Lead scoring automático — media prioridad

**Qué:** recalcular el score de un lead automáticamente al crearlo y al actualizar el interés tras una visita. Actualmente requiere que el agente acceda a la pantalla de scoring y ejecute el proceso manualmente.

**Por qué:** el valor del scoring depende de que sea siempre actualizado.

**Impacto:** el agente ve siempre el score actualizado sin acción adicional.

---

### 6. Stage triggers — media prioridad

**Qué:** al mover un lead de etapa en el pipeline, el sistema crea automáticamente tareas y notificaciones predefinidas. Ejemplos:
- Nuevo → Contactado: tarea "Llamar en 24h"
- Activo → Visita programada: crear visita y enviar confirmación
- Negociando → Cerrado ganado: actualizar propiedad + tarea notaría

**Por qué:** reduce el trabajo manual del agente y garantiza que no se salte ningún paso del proceso.

---

### 7. Portal de clientes mejorado — media prioridad

**Qué:**
- Botón "Enviar portal" en ficha de cliente (un click, copia link, abre opción de enviar por WhatsApp)
- Preview con código QR
- Notificación al agente cuando el cliente visita el portal o da feedback

**Por qué:** el portal existe y funciona, pero muchos agentes no saben que existe porque no hay un punto de entrada visible.

---

### 8. CI/CD y despliegue automatizado — prioridad media

**Qué:** pipeline de integración continua que construya, pruebe y despliegue automáticamente cada cambio sobre la infraestructura Docker Compose ya existente (PostgreSQL + Redis + backend + frontend).

**Por qué:** el despliegue web (Docker Compose, PostgreSQL en producción) ya está construido y validado — falta automatizar el ciclo de entrega para reducir el trabajo manual de cada release.

---

### 9. Firma electrónica — media prioridad

**Qué:** integración con DocuSign o Signaturit para firma digital de contratos directamente desde la plataforma.

**Por qué:** complementa el módulo de contratos avanzados.

---

### 10. App móvil nativa — baja prioridad a corto plazo

**Qué:** aplicación iOS + Android para consulta del pipeline y notificaciones en tiempo real.

**Por qué:** la web ya es responsive. La app móvil nativa añade notificaciones push y acceso offline.

---

## Fases del producto

| Fase | Objetivo | Items clave |
|---|---|---|
| **Fase 1 — MVP SaaS** | Producto vendible y autoservicio | Matching UI, contratos, emails visitas, Stripe, deduplicación de leads |
| **Fase 2 — Automatización** | Reducir tiempo manual del agente 40% | Stage triggers, scoring automático, templates de automations, portal mejorado |
| **Fase 3 — Escalado** | 50+ agencias simultáneas | ✅ SaaS hosting, PostgreSQL, Docker · CI/CD, backups cloud automatizados (pendiente) |
| **Fase 4 — IA Avanzada** | Diferenciación competitiva | Propensity scoring, precio óptimo, auto-assignment de agentes, negociación asistida |

---

> Este roadmap se actualiza conforme avanza el producto. Para comentarios o sugerencias de prioridad, abre un issue en este repositorio.
