# NOMBRE DEL PROYECTO

**Una frase que diga qué es y para quién.**

[![CI](https://github.com/Juan-Carlos-Estevez-Vargas/NOMBRE-DEL-REPO/actions/workflows/ci.yml/badge.svg)](https://github.com/Juan-Carlos-Estevez-Vargas/NOMBRE-DEL-REPO/actions/workflows/ci.yml)
[![CodeQL](https://github.com/Juan-Carlos-Estevez-Vargas/NOMBRE-DEL-REPO/actions/workflows/codeql.yml/badge.svg)](https://github.com/Juan-Carlos-Estevez-Vargas/NOMBRE-DEL-REPO/actions/workflows/codeql.yml)
[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/Juan-Carlos-Estevez-Vargas/NOMBRE-DEL-REPO/badge)](https://scorecard.dev/viewer/?uri=github.com/Juan-Carlos-Estevez-Vargas/NOMBRE-DEL-REPO)
[![Licencia: MIT](https://img.shields.io/badge/licencia-MIT-blue)](LICENSE)

> Repo creado desde la plantilla de proyectos. Antes del primer commit:
> reemplaza `NOMBRE-DEL-REPO` en todos los archivos, borra este aviso y sigue
> la lista de [Primeros pasos](#primeros-pasos-de-la-plantilla).

## Contenido

- [Descripción](#descripción)
- [Capturas](#capturas)
- [Tecnologías](#tecnologías)
- [Inicio rápido](#inicio-rápido)
- [Documentación](#documentación)
- [Contribuir](#contribuir)
- [Licencia](#licencia)

## Descripción

Qué problema resuelve, sus funciones principales y en qué estado está.

## Capturas

<!-- Imágenes en docs/capturas/ con texto alternativo descriptivo. -->

## Tecnologías

| Capa | Tecnología |
| --- | --- |
| Interfaz | |
| Backend | |
| Base de datos | |
| Pruebas | |
| Publicación | |

## Inicio rápido

```bash
# instalar dependencias
# copiar .env.example a .env y llenarlo
# correr en local
# correr las pruebas
```

## Documentación

| Documento | Contenido |
| --- | --- |
| [Arquitectura](docs/ARQUITECTURA.md) | Piezas del sistema y cómo se conectan |
| [Diagramas](docs/DIAGRAMAS.md) | Diagramas en Mermaid de la arquitectura y de cada flujo |
| [Despliegue](docs/DESPLIEGUE.md) | Cómo montarlo desde cero y qué variables necesita |
| [Seguridad](docs/SEGURIDAD_OWASP.md) | Estado de cada punto de seguridad |
| [Legal](docs/LEGAL.md) | Privacidad, datos personales y licencias |
| [Política de seguridad](SECURITY.md) | Cómo reportar una vulnerabilidad |

## Contribuir

Lee la [guía de contribución](CONTRIBUTING.md). Los commits siguen
[Conventional Commits](https://www.conventionalcommits.org/es/).

## Licencia

[MIT](LICENSE) © Juan Carlos Estevez Vargas

## Primeros pasos de la plantilla

- [ ] Reemplazar `NOMBRE-DEL-REPO` y `NOMBRE DEL PROYECTO` en todos los archivos
- [ ] Dejar en `.github/dependabot.yml` solo los ecosistemas que use el proyecto
- [ ] Ajustar los lenguajes de `.github/workflows/codeql.yml` (CodeQL y Scorecard solo corren en repos públicos; en uno privado se saltan solos)
- [ ] GitHub → Settings → General: permitir solo *squash merge* y borrar ramas al fusionar
- [ ] GitHub → Settings → Rules: proteger la rama principal (PR obligatorio, CI en verde, sin force push)
- [ ] GitHub → Settings → Code security: Secret scanning, Push protection, Dependabot alerts y Private vulnerability reporting
- [ ] Descripción, temas (topics) y enlace al sitio del repo
- [ ] Borrar esta sección
