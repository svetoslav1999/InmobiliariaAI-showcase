# InmobilarIA — Historial de cambios público

> Este changelog describe mejoras del producto visibles para clientes y usuarios. No incluye detalles de implementación técnica interna.

---

## v1.4.1 — Julio 2026 · Panel financiero premium

### Un panel financiero de nivel comercial
- **KPIs grandes y claros**: cobrado y facturado del mes con **comparación respecto al mes anterior** (tendencia ↑/↓) y **mini-gráficos de evolución**, más facturado anual, pendiente de cobro, IVA repercutido y base cobrada.
- **Varios gráficos con datos reales**: facturado vs. cobrado a 12 meses, estado de las facturas, embudo de presupuestos con tasa de conversión, métodos de pago y rankings de clientes, propiedades y agentes que más facturan.
- **Widgets útiles de un vistazo**: próximos vencimientos, últimos pagos, clientes con deuda, presupuestos pendientes, últimas facturas y **alertas automáticas**.
- **Estados vacíos honestos**: cuando aún no hay datos, el panel lo indica e invita a crear la primera factura, en lugar de mostrar cifras inventadas.

### Cuidado en el detalle
- Tarjetas con profundidad, microinteracciones y jerarquía visual más clara; tablas con esqueletos de carga, estados vacíos con acción directa y realce de importes vencidos.
- Coherencia visual total con el resto del producto, en tema claro y oscuro.

### Verificación con evidencias reales
- Suite completa en verde (256 pruebas de backend, 43 de frontend), tipado y linters limpios, compilación de producción correcta y **stack Docker completo (frontend, backend, PostgreSQL y Redis) sano**.
- Recorrido funcional automatizado con navegador real sobre toda la aplicación: **cero errores de consola, de red o pantallas en blanco**.

---

## v1.4.0 — Julio 2026 · Módulo de Facturación

### Facturas y presupuestos profesionales
- **Facturas completas**: creación, edición, duplicado, anulación, emisión con **numeración automática por serie y año**, IVA configurable por línea, descuentos, vencimientos y **PDF profesional** listo para enviar.
- **Presupuestos**: creación, envío, aceptación/rechazo y **conversión a factura en un clic**, con su propio PDF.
- **Pagos**: registro de cobros parciales o completos (transferencia, tarjeta, efectivo, domiciliación…); el estado de la factura se actualiza solo (pendiente, parcial, pagada, vencida).

### Panel financiero real
- Ingresos del mes y del año, pendiente de cobro, importes vencidos, IVA repercutido y facturación emitida, con **gráfico de evolución de cobros** a 12 meses. Solo datos reales; cuando no hay datos, se indica de forma honesta.

### Preparado para crecer
- **Configuración fiscal por agencia**: identidad fiscal, país, moneda, tipos de IVA y series propias — pensado para escalar como SaaS multi-país.
- **Exportación** a CSV y Excel.
- Integración con **Stripe** (muestra "no configurado" de forma honesta si falta la clave) y arquitectura **preparada para VeriFactu, factura electrónica y SII**, sin activar integraciones falsas.

### Seguridad y calidad
- **Permisos por rol** (administrador, agente, solo lectura) y **aislamiento estricto entre agencias** verificado: ninguna organización puede ver ni tocar facturas de otra.
- **Verificación con evidencias reales**: batería de pruebas ampliada (247 en verde), tipado y linters limpios, compilación de producción correcta y recorrido funcional automatizado del módulo con navegador real — **cero errores de consola, red o pantallas en blanco**, en tema claro y oscuro.

---

## v1.3.0 — Julio 2026 · CRM Avanzado (Fase 1)

### Historial 360º del cliente
- **Timeline unificado real.** La ficha de cada cliente reúne ahora *toda* la actividad en una única línea temporal: llamadas, WhatsApp (enviados y recibidos), mensajes de conversación, visitas, tareas y acciones de IA. Antes parte de esta actividad no quedaba registrada; ahora el historial está completo y se puede filtrar por categoría (Comunicación, Visitas, Tareas, IA).
- **Registro de llamadas.** Un botón en la ficha permite anotar cada llamada con su resultado (contactado, no contesta, buzón, comunica, no interesado, reagendar, número erróneo), duración y notas. La llamada actualiza automáticamente la fecha de último contacto y aparece en el timeline.

### Inteligencia comercial
- **Próxima acción recomendada por IA.** Con un clic, el sistema analiza el estado real del lead y recomienda la mejor acción comercial, con un indicador de urgencia (alta / media / baja) calculado a partir del último contacto, el seguimiento pendiente y la etapa del embudo. La acción se puede convertir en una tarea de seguimiento al instante.
- **Seguimiento automático.** Cuando vence la fecha de próximo contacto de un lead, se genera automáticamente una tarea de seguimiento asignada a su agente, sin duplicados.

### Calidad y verificación
- **Sin datos inventados y sin romper nada existente.** Todo se apoya en la arquitectura actual; el aislamiento entre agencias se mantiene verificado (intentar registrar actividad sobre un cliente de otra organización se rechaza).
- **Verificación con evidencias reales:** batería de pruebas ampliada (240 en verde), tipado y linters limpios, compilación de producción correcta, y recorrido funcional automatizado del CRM con navegador real — **cero errores de consola, red o pantallas en blanco**, en tema claro y oscuro.

---

## v1.2.2 — Julio 2026 · Fiabilidad del panel de costes, rendimiento y pulido visual

### Fiabilidad del informe de costes de IA
- **Conversión de costes a euros restaurada y más robusta.** El panel financiero del Super Admin siempre muestra importes reales o, cuando la referencia de cambio no está disponible, lo indica de forma explícita — nunca aparecen euros inventados. Los totales cuadran exactamente con el consumo real registrado.

### Rendimiento
- **Analytics carga notablemente más rápido.** Las métricas y gráficos aparecen de inmediato; los insights generados por IA se cargan de forma independiente, sin bloquear el resto del panel.
- **Base de datos optimizada.** Se depuraron índices redundantes, reduciendo el coste de escritura sin afectar a las consultas.

### Experiencia de usuario
- **Mayor estabilidad visual** en el panel de infraestructura: se eliminan los saltos de maquetación mientras se cargan las métricas en vivo.

### Calidad y verificación
- **Auditoría de pre-producción con evidencias reales:** recorrido visual automatizado de toda la aplicación (580 combinaciones de página, resolución y tema — sin defectos de maquetación), análisis real de rendimiento de PostgreSQL, verificación en vivo de la generación de IA (Claude y Gemini) y batería de pruebas completa en verde.

---

## v1.2.1 — Julio 2026 · Endurecimiento de seguridad y verificación en vivo

### Seguridad reforzada (auditoría de penetración)
- **Aislamiento entre organizaciones verificado en vivo.** Se levantó el stack completo y se intentó, de forma real, acceder a los datos de una agencia desde otra (identificadores manipulados, lectura, edición y borrado directos). Todos los intentos fueron rechazados: cada organización solo ve y opera sobre sus propios datos.
- **Protección contra escalada de privilegios.** Se corrigió y se blindó el cambio de rol de cuentas: solo un administrador de la organización puede modificar roles o el estado de una cuenta; ningún usuario puede aumentarse permisos a sí mismo.
- **Protección anti-abuso robustecida.** Los límites de peticiones (inicio de sesión, IA, formularios) resisten intentos de evasión mediante cabeceras manipuladas, protegiendo frente a fuerza bruta y consumo económico no autorizado.
- **Subida de imágenes segura.** Validación por firma real del archivo (no solo por extensión), análisis de contenido y nombres de fichero aleatorios, evitando la subida de archivos maliciosos.

### Calidad y verificación
- **Verificación con evidencias reales:** batería de pruebas ampliada, recorrido automatizado de 22 secciones de la aplicación con navegador real (sin errores), y stack completo (PostgreSQL + Redis + backend + frontend) desplegado con Docker y en estado saludable.

---

## v1.2.0 — Junio 2026 · Panel Super Admin y validación PostgreSQL real

### Panel Super Admin — Control Center
- **Nuevo panel de administración de plataforma**, completamente independiente de cualquier agencia: el operador del SaaS gestiona organizaciones, usuarios, consumo de IA, infraestructura, seguridad, backups y auditoría desde una interfaz propia.
- **Infraestructura en vivo** — métricas reales de Redis y PostgreSQL (latencia, memoria, conexiones) cuando el despliegue las expone. Si un servicio no está configurado o no es accesible, el panel lo indica de forma explícita — nunca se muestran datos inventados.
- **Seguridad en tiempo real** — accesos, intentos fallidos, IPs sospechosas y estado de los circuit breakers de IA por proveedor.
- **Arquitectura de facturación (Stripe)** lista en backend y panel; se activa automáticamente al configurar las claves de producción, sin requerir cambios de código.

### Calidad y fiabilidad
- **Migración de base de datos validada contra PostgreSQL real** (no solo el entorno de desarrollo SQLite) desplegando el stack completo con Docker Compose. Se encontraron y corrigieron 2 incompatibilidades antes de que llegaran a un entorno de producción.
- **200 tests en verde** (+10 desde la versión anterior).

---

## v1.1.0 — Junio 2026 · Nueva landing y pulido

### Landing rediseñada "Light Enterprise"
- **Nuevo diseño claro y premium** inspirado en Apple, Stripe, Linear, Notion y Vercel — se retira el estilo anterior (mapa neural) por una página de producto elegante, con mucho espacio en blanco y tipografía cuidada.
- **Más contenido y mejor explicado**: hero potente con mockup real del producto, barra de estadísticas, problema→solución, funcionalidades, pipeline de IA paso a paso, capturas reales, comparativa con el método tradicional y una sección de preguntas frecuentes.
- **Botones premium** y animaciones sutiles; totalmente responsive (escritorio, tablet y móvil).

### Calidad
- **Auditoría funcional completa** de la aplicación (todas las pantallas verificadas) y aislamiento entre agencias confirmado.
- **Capturas actualizadas** en toda la documentación, reflejando el estado actual del producto.

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
