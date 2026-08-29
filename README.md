# Nombre del Proyecto

> Reemplaza este README con la descripción real del proyecto. Lo que sigue es la guía de uso de la plantilla — bórrala una vez adaptado.

## 📁 Estructura

```
.
├── frontend/     # Aplicación cliente (React/Vue/etc.)
├── backend/      # API / lógica de servidor
├── database/     # Migraciones y seeds
├── docs/         # Documentación técnica adicional (ADRs, diagramas, etc.)
└── .github/      # Plantillas de Issues, PR y workflows de CI
```

Es un **monorepo**: una sola Historia de Usuario puede tocar frontend, backend y database a la vez, dentro de un mismo Issue y un mismo Pull Request.

## 🚀 Cómo usar esta plantilla

1. Click en "Use this template" en GitHub para generar el repo real del proyecto.
2. Renombra este README con la info del proyecto (usa la plantilla de Notion "Product Brief" para completar el contexto).
3. Dentro de `frontend/` y `backend/`, inicializa cada stack (`npm init`, `npx create-vite`, etc.) según corresponda.
4. Actualiza `.github/ISSUE_TEMPLATE/config.yml` con la URL real del repo.
5. En `.github/workflows/ci-backend.yml`, deja activo el bloque de Node **o** Python según tu stack, y comenta el otro.
6. Crea el Project (tablero) de GitHub Projects para este repo — ver documentación en `docs/`.

## 📖 Flujo de trabajo

1. Toda funcionalidad nueva empieza como un Issue usando la plantilla "Historia de Usuario".
2. Se crea una rama: `feature/hu-<numero>-descripcion-corta`
3. Al abrir el Pull Request, se usa `Closes #<numero>` para vincularlo automáticamente al Issue.
4. El CI corre linter + pruebas automáticamente según qué carpeta se modificó.
5. Al mergear a `main`, el Issue se cierra solo.

## 🔧 Requisitos

- Node.js 20+ (o el runtime que uses en el backend)
- Variables de entorno: copia `.env.example` a `.env` en cada carpeta que lo requiera (nunca subas `.env` real)

## 🔐 Seguridad

- Dependabot está configurado (`.github/dependabot.yml`) para alertar dependencias vulnerables semanalmente.
- Nunca commitear credenciales, tokens o llaves — usa siempre variables de entorno.
