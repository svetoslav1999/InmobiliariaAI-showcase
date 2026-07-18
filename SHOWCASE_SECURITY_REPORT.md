# 🔐 Informe de seguridad del showcase — InmobiliarIA

**Fecha:** 2026-06-02
**Repositorio de origen:** privado
**Repositorio público:** `InmobiliariaAI-showcase`
**Demo pública:** `inmobiliaria-demo` (GitHub Pages)

---

## Clasificación de riesgo de copia

| Nivel | **BAJO** ✅ |
|---|---|
| Justificación | El showcase y la demo exponen únicamente propuesta de valor, funcionalidades de alto nivel y capturas con datos de demostración. No se publica código, lógica, esquema de datos, endpoints ni configuración. Un desarrollador externo **no** puede reconstruir el producto a partir de este material. |

---

## Elementos eliminados respecto al repositorio privado

Se excluyó de forma deliberada todo lo que facilita la copia o la ingeniería inversa:

- ❌ **Código fuente** (frontend, backend, Electron, scripts).
- ❌ **Comandos de arranque** y guía de instalación (`uvicorn`, `npm run dev`, build-exe).
- ❌ **Credenciales de demo** (usuario/contraseña de login).
- ❌ **Instrucciones de `.env`** y nombres de variables de entorno.
- ❌ **Árbol de ficheros** y estructura de carpetas interna.
- ❌ **Detalle de la API**: nº y rutas de routers, `/api/v1`, contratos.
- ❌ **Esquema de base de datos** y modelos.
- ❌ **Arquitectura interna**: servicios, colas, trabajos en segundo plano.
- ❌ **Configuración de despliegue**: `docker-compose.yml`, ngrok, infraestructura.
- ❌ **Versiones exactas** de frameworks y dependencias.
- ❌ **Prompts de IA**, flujos y automatizaciones internas.
- ❌ Documentos internos de auditoría, changelog y compliance detallado.

## Elementos publicados (seguros)

- ✅ Propuesta de valor y beneficios.
- ✅ Funcionalidades descritas a alto nivel (qué hace, no cómo).
- ✅ Stack en términos genéricos (web + escritorio + IA), sin versiones.
- ✅ Arquitectura conceptual `Usuario → Frontend → API → Base de datos`.
- ✅ Capturas con **datos de demostración**.
- ✅ Logo y branding públicos.

---

## Riesgos detectados y mitigación

| Riesgo | Detección | Mitigación aplicada |
|---|---|---|
| PII real en capturas | Auditoría visual de las capturas seleccionadas | Solo se usan capturas con datos sembrados (nombres ficticios, correos `@example.com`, teléfonos de demo). Se descartaron capturas de configuración con datos de organización. |
| Fuga de stack explotable | Revisión del README de origen | Se redujo a stack genérico; sin versiones ni rutas. |
| Reconstrucción desde arquitectura | Revisión de docs | Diagrama reducido a 4 cajas; sin tablas/endpoints/servicios. |
| Secretos / claves / tokens | Revisión de ficheros copiados | No se copia ningún `.env`, clave ni token. La demo es 100% estática sin backend. |

---

## Nivel de exposición

- **Código:** nulo.
- **Lógica de negocio:** nula.
- **Superficie de ataque:** nula en la demo (sitio estático sin backend ni API).
- **Datos:** solo datos de demostración en capturas.

## Posibilidad de ingeniería inversa

**Muy baja.** El material publicado es descriptivo y visual. No hay artefactos ejecutables del producto real, ni contratos de API, ni esquema de datos que permitan replicar la implementación.

---

## Auditoría final

> *"¿Podría un desarrollador reconstruir este producto a partir de esta información?"*

**No.** Podría inspirarse en el concepto y la UI, pero tendría que diseñar e implementar desde cero toda la lógica, la IA, el modelo de datos y la arquitectura multi-tenant.

## Recomendaciones

- Mantener el repositorio de origen **privado**.
- Antes de añadir nuevas capturas, verificar que usan datos de demostración.
- No incluir vídeos de pantalla que muestren paneles de configuración con datos reales.
- Revisar este informe en cada actualización del showcase.
