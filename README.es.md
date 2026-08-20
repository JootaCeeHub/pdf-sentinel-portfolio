# PDF Sentinel

Aplicación frontend base pensada para evolucionar hacia una herramienta de monitoreo y análisis de PDFs, actualmente estructurada con un stack moderno de React + Vite + shadcn/ui.

## Overview
PDF Sentinel se encuentra actualmente en una fase temprana de preparación. El repositorio incluye una base frontend completa (enrutamiento, sistema UI, estilos, linting y tooling de build), pero aún no implementa funcionalidades de negocio relacionadas con PDFs.

En este momento, el proyecto funciona como una base web lista para extender, con:
- ruta principal,
- ruta 404,
- componentes UI reutilizables,
- hooks utilitarios,
- y cadena de herramientas lista para desarrollo.

### Propósito previsto (según el nombre del repositorio)
Por el nombre del repositorio, la dirección esperada parece ser un sistema tipo "sentinel" para flujos con PDFs (por ejemplo: vigilar, procesar, clasificar o inspeccionar contenido PDF). Sin embargo, esta funcionalidad de dominio **todavía no está presente** en el código.

## Features
### Implementado actualmente
- SPA en React inicializada con Vite.
- Manejo de rutas con `react-router-dom` (`/` y `*` como catch-all).
- Base UI compartida con componentes shadcn/ui.
- Estilos globales y design tokens vía Tailwind CSS y variables CSS.
- Cliente de consultas preparado con `@tanstack/react-query`.
- Proveedores de toasts y tooltips preconfigurados.
- Configuración de TypeScript + ESLint para control de calidad en desarrollo.

### Aún no implementado
- Carga, parsing, indexación, validación, monitoreo o alertas de PDFs.
- Integración backend/API para procesamiento de archivos.
- Autenticación, persistencia o gestión de roles.

## Tech Stack
- **Lenguaje:** TypeScript
- **Frontend:** React 18
- **Build tool:** Vite 5
- **Routing:** React Router DOM
- **Base de capa de datos:** TanStack React Query
- **Sistema UI:** shadcn/ui + Radix UI primitives
- **Estilos:** Tailwind CSS + PostCSS + tailwindcss-animate
- **Linting:** ESLint 9 + TypeScript ESLint

## Architecture
El proyecto sigue una arquitectura SPA cliente estándar:

- `src/main.tsx` inicializa la aplicación.
- `src/App.tsx` integra proveedores globales y rutas.
- `src/pages/*` contiene componentes de páginas por ruta.
- `src/components/ui/*` contiene primitivas UI reutilizables tipo framework.
- `src/hooks/*` y `src/lib/*` centralizan lógica/utilidades compartidas.

Actualmente es una **arquitectura solo frontend**, sin runtime de servidor ni adaptador de API en el repositorio.

## Installation
### Requisitos previos
- Node.js 18+ (recomendado)
- npm 9+

### Pasos
```bash
git clone <tu-url-del-repositorio>
cd pdf-sentinel
npm install
```

## Usage
### Ejecutar en desarrollo
```bash
npm run dev
```
El servidor de desarrollo corre en el puerto `8080` por defecto.

### Compilar para producción
```bash
npm run build
```

### Previsualizar build de producción
```bash
npm run preview
```

### Ejecutar lint
```bash
npm run lint
```

## Project Structure
```text
pdf-sentinel/
├─ public/                  # Assets estáticos (favicon, robots, placeholders)
├─ src/
│  ├─ components/
│  │  ├─ ui/                # Librería de componentes reutilizables shadcn/ui
│  │  └─ NavLink.tsx        # Wrapper de compatibilidad para Router NavLink
│  ├─ hooks/                # Hooks personalizados de React
│  ├─ lib/                  # Funciones utilitarias compartidas
│  ├─ pages/                # Páginas por ruta (Index, NotFound)
│  ├─ App.tsx               # Proveedores + rutas de la app
│  ├─ main.tsx              # Punto de entrada React
│  └─ index.css             # Tailwind global + design tokens
├─ components.json          # Configuración de shadcn/ui
├─ tailwind.config.ts       # Configuración de tema y plugins Tailwind
├─ vite.config.ts           # Configuración Vite + alias + servidor dev
├─ eslint.config.js         # Configuración ESLint
└─ package.json             # Scripts y manifiesto de dependencias
```

## Development
### Flujo sugerido
1. Crear una rama de feature.
2. Implementar módulos de funcionalidad en `src/pages`, `src/components` y `src/lib`.
3. Ejecutar lint antes de hacer commit:
   ```bash
   npm run lint
   ```
4. Compilar para verificar build de producción:
   ```bash
   npm run build
   ```

### Notas para contribuir
- Mantener la lógica de negocio separada de primitivas de UI.
- Favorecer tipado fuerte a medida que madure el proyecto.
- Incorporar tests conforme entren funcionalidades de dominio PDF.

## Roadmap
Posibles líneas de evolución para PDF Sentinel:
- Agregar pipeline de carga y almacenamiento de PDFs.
- Integrar extracción de texto/OCR de PDFs.
- Introducir reglas de validación/calidad documental.
- Añadir jobs de monitoreo y canales de notificación.
- Implementar autenticación y control de acceso por workspace.
- Añadir servicio API/backend para procesamiento persistente.
- Incorporar pruebas automatizadas (unitarias + integración + e2e).

## License
Esto es personal y privado, creado y desarrollado por **JootaCee**.

## Author
Esto es personal y privado, creado y desarrollado por **JootaCee**.
