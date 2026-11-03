# Arquitectura

## 1. Visión general

Qué hace el sistema y cuáles son sus piezas principales. El diagrama está en
[DIAGRAMAS.md](DIAGRAMAS.md#arquitectura-general).

## 2. Tecnologías y por qué

| Pieza | Tecnología | Por qué |
| --- | --- | --- |
| | | |

## 3. Estructura de carpetas

```
src/        código de la aplicación
docs/       documentación y diagramas
scripts/    utilidades de CI y mantenimiento
.github/    CI, CodeQL, Scorecard, Dependabot y plantillas
```

## 4. Capas

Interfaz, lógica de dominio y acceso a datos separados; la interfaz no habla
directo con la base de datos.

## 5. Seguridad

Resumen y enlace a [SEGURIDAD_OWASP.md](SEGURIDAD_OWASP.md).

## 6. Integración y despliegue continuos

- **CI** (`.github/workflows/ci.yml`): secretos, pruebas, auditoría de dependencias y build en cada push y PR.
- **CodeQL** (`.github/workflows/codeql.yml`): análisis de seguridad del código en cada PR y cada semana.
- **Scorecard** (`.github/workflows/scorecard.yml`): puntaje de prácticas del repo en cada merge y cada semana.
