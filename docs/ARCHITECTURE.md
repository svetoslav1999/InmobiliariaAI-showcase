# Arquitectura (vista simplificada)

> Esta es una **vista conceptual de alto nivel**. No representa la infraestructura real,
> ni los servicios, esquemas o detalles internos del producto.

```
        ┌─────────────┐
        │   Usuario   │
        └──────┬──────┘
               │
        ┌──────▼───────────────┐
        │  Frontend             │
        │  (web + escritorio)   │
        └──────┬───────────────┘
               │
        ┌──────▼──────┐
        │  API de      │
        │  servicios   │
        └──────┬──────┘
               │
        ┌──────▼──────┐
        │  Base de     │
        │  datos       │
        └─────────────┘
```

## Principios de producto

- **Multi-tenant**: cada agencia opera en un espacio aislado.
- **IA como servicio interno**: las funciones inteligentes se procesan en el servidor; las claves nunca llegan al navegador.
- **Experiencia unificada**: misma interfaz en web y escritorio, con dark mode enterprise.

## Lo que NO se documenta aquí (intencionadamente)

- Esquema de base de datos y tablas
- Endpoints y contratos de API
- Servicios internos, colas o trabajos en segundo plano
- Proveedores, configuración de despliegue e infraestructura
- Prompts de IA y flujos internos

> Mostrar el valor del producto sin mostrar cómo está construido.
