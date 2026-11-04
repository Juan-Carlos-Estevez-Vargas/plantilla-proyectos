# Diagramas

Diagramas en [Mermaid](https://mermaid.js.org/); GitHub los dibuja solo. Cada
cambio en la app actualiza aquí el diagrama afectado o agrega uno nuevo.

- [Arquitectura general](#arquitectura-general)
- [Modelo de datos](#modelo-de-datos)
- [Inicio de sesión y permisos](#inicio-de-sesión-y-permisos)
- [Integración y despliegue](#integración-y-despliegue)
- [Idiomas](#idiomas)

## Arquitectura general

```mermaid
flowchart LR
  U["Usuario"] --> FE["Frontend"]
  FE --> API["API / backend"]
  API --> DB[("Base de datos")]
```

## Modelo de datos

```mermaid
erDiagram
  USUARIO ||--o{ REGISTRO : crea
  USUARIO {
    uuid id
    text correo
  }
  REGISTRO {
    uuid id
    uuid usuario_id
    timestamptz creado
  }
```

## Inicio de sesión y permisos

```mermaid
sequenceDiagram
  actor U as Usuario
  participant FE as Frontend
  participant API as Backend
  U->>FE: correo y contraseña
  FE->>API: iniciar sesión
  API-->>FE: sesión (cookie HttpOnly / token)
  FE->>API: petición con la sesión
  API->>API: valida permisos
  API-->>FE: datos permitidos
```

## Integración y despliegue

```mermaid
flowchart LR
  B["Rama"] --> PR["Pull request"]
  PR --> CI["CI: secretos · pruebas · auditoría · build"]
  PR --> CQ["CodeQL"]
  CI -- "verde" --> M["Squash merge"]
  M --> D["Despliegue"]
  M --> SC["Scorecard"]
  D --> R["Tag vX.Y.Z + release"]
```

## Idiomas

```mermaid
flowchart TD
  A["Abrir la app"] --> B{"¿Hay idioma guardado?"}
  B -- "sí" --> L["Ese idioma"]
  B -- "no" --> C["navigator.languages<br/>matchLocale()"]
  C -- "disponible" --> L
  C -- "ninguno" --> BASE["Idioma base"]
  L --> D["Descarga su diccionario<br/>(si no es el base)"]
  D --> R["Pinta la app"]
  BASE --> R
  R --> H["&lt;html lang&gt;, SEO y fechas con Intl"]
  S["Selector 🌐"] -- "setLocale()" --> G["Guarda la elección"] --> D
```
