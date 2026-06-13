# InmobilarIA — Roadmap Público

> Última actualización: junio 2026 · v0.8.0

Este roadmap refleja las prioridades del producto ordenadas por impacto comercial para las agencias inmobiliarias. Los plazos son orientativos.

---

## Estado actual: v0.8.0

El producto está en **estado de producción técnica**: backend estable, seguridad auditada (14 rondas), 151 tests en verde y un build limpio. Lo que sigue es completar el ciclo comercial completo y escalar como SaaS.

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

### 3. Emails automáticos de visitas — alta prioridad

**Qué:**
- Confirmación de visita (24 horas antes)
- Recordatorio por WhatsApp (2 horas antes, si el contacto tiene WhatsApp)
- Follow-up automático (2 horas después de la visita)

**Por qué:** la infraestructura de email (Resend) y los campos de control (`confirmation_sent`, `reminder_sent`, `followup_sent`) ya están implementados. Solo falta activar el scheduler.

**Impacto directo:** reducción de no-shows estimada en 20-30%.

---

### 4. Billing — Stripe — alta prioridad

**Qué:** suscripción SaaS con planes starter / pro / enterprise. El control de cuotas de IA ya está implementado en backend.

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

### 8. SaaS Hosting — prioridad alta para escalar

**Qué:** infraestructura web para que las agencias accedan a InmobilarIA sin instalar nada. PostgreSQL en producción, Docker, nginx, CI/CD.

**Por qué:** actualmente solo existe distribución como aplicación de escritorio (Windows). El modo web reduce la fricción de adopción.

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
| **Fase 3 — Escalado** | 50+ agencias simultáneas | SaaS hosting, PostgreSQL, Docker, CI/CD, backups cloud |
| **Fase 4 — IA Avanzada** | Diferenciación competitiva | Propensity scoring, precio óptimo, auto-assignment de agentes, negociación asistida |

---

> Este roadmap se actualiza conforme avanza el producto. Para comentarios o sugerencias de prioridad, abre un issue en este repositorio.
