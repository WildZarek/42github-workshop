# 🌐 Taller de Git y GitHub

¡Bienvenid@s a este Workshop sobre Git y GitHub! Aquí encontrarás recursos, guías y ejercicios prácticos para aprender a usar Git y GitHub de manera efectiva. El objetivo es ayudarte a estructurar repositorios profesionales, documentar de forma clara, dominar flujos de trabajo con ramas, comprender las plantillas de Issues/PRs, y aprovechar al máximo las herramientas que GitHub ofrece.

[![Licencia](https://img.shields.io/badge/Licencia-MIT-green.svg)](LICENSE.md)
[![Contribuir](https://img.shields.io/badge/Contribuir-Bienvenido-blue.svg)](CONTRIBUTING.md)

---

## 📜 Tabla de Contenidos

- [👋 Introducción](#-introducción)
- [📁 Estructura del Repositorio](#-estructura-del-repositorio)
- [🛠 Preparación del Entorno](#-preparación-del-entorno)
- [🚀 Tutoriales Prácticos](#-tutoriales-prácticos)
- [📚 Recursos Adicionales](#-recursos-adicionales)
- [🌱 Ramas: Feature y Hotfix](#-ramas-feature-y-hotfix)
- [⚙️ Ejemplos de Flujos de Trabajo (CI)](#️-ejemplos-de-flujos-de-trabajo-ci)
- [🤝 Contribuir & Código de Conducta](#-contribuir--código-de-conducta)

---

## 👋 Introducción

Este taller está enfocado en estudiantes y desarrolladores que deseen afianzar sus conocimientos en:

- Crear y gestionar repositorios en GitHub.
- Trabajar con ramas (feature, hotfix).
- Utilizar plantillas de Issues y Pull Requests.
- Aplicar buenas prácticas de Markdown (básico, avanzado y GFM).
- Integrar flujos de CI con GitHub Actions.
- Seguir lineamientos de contribución y mantener un entorno colaborativo sano.

---

## 📁 Estructura del Repositorio

La estructura principal es:

```
.
github-workshop/
├── .github/
│   ├── workflows/
│   │   └── ci.yml
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   ├── PULL_REQUEST_TEMPLATE.md
│   └── CODEOWNERS
├── docs/
│   ├── basic_markdown.md
│   ├── advanced_markdown.md
│   └── github_flavored_markdown.md
├── tutoriales/
│   ├── carpeta_punt_github.md
│   └── project_files.md
├── resources/
│   ├── git_cheat_sheet.pdf
│   ├── github_tips_links.md
│   └── README.md
├── branches/
│   ├── feature-branch-example.md
│   └── hotfix-branch-example.md
├── workflow-examples/
│   └── ci_workflow_demo.md
├── submodules/
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── LICENSE.md
└── README.md
```

**Puntos Clave:**

- **`.github/`**: Contiene flujos de CI, plantillas de Issues/PR y `CODEOWNERS`.
- **`docs/`**: Guías de Markdown (básico, avanzado, GFM).
- **`tutoriales/`**: Explicaciones prácticas sobre `.github` y archivos clave del proyecto.
- **`resources/`**: Recursos adicionales (PDF, enlaces útiles).
- **`branches/`**: Ejemplos y explicación de estrategias de ramas (feature y hotfix).
- **`workflow-examples/`**: Ejemplo de configuración CI con GitHub Actions.
- **`submodules/`**: Espacio para submódulos Git, si se integran.
- Archivos raíz: `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `LICENSE.md` y `README.md`.

---

## 🛠 Preparación del Entorno

Antes de comenzar:

- Instala [Git](https://git-scm.com/downloads).
- Crea o ingresa a tu cuenta de [GitHub](https://github.com/).
- Opcional: Un editor de texto moderno (VS Code, etc.).

Para clonar el repositorio (si tiene submódulos):

```bash
git clone --recurse-submodules https://github.com/tu-usuario/github-workshop.git
```

Si ya clonaste sin `--recurse-submodules`, simplemente:

```bash
cd github-workshop
git submodule update --init --recursive
```

---

## 🚀 Tutoriales Prácticos

En [`tutoriales/`](tutoriales/) encontrarás guías sobre:

- Cómo funciona la carpeta `.github` y sus archivos (`carpeta_punt_github.md`).
- Explicación de archivos clave del proyecto: `LICENSE.md`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `README.md` (`project_files.md`).

Estos tutoriales te ayudarán a entender la motivación y el uso de cada archivo.

---

## 📚 Recursos Adicionales

La carpeta [`resources/`](resources/) proporciona:

- [`git_cheat_sheet.pdf`](resources/git_cheat_sheet.pdf): Hoja de referencia rápida de comandos Git.
- [`github_tips_links.md`](resources/github_tips_links.md): Enlaces útiles para aprender más sobre GitHub.
- [`README.md`](resources/README.md): Descripción general de los recursos.

Usa estos materiales para profundizar en el manejo de Git y GitHub.

---

## 🌱 Ramas: Feature y Hotfix

En [`branches/`](branches/) encontrarás:

- [`feature-branch-example.md`](branches/feature_branch_example.md): Explica el flujo de trabajo con ramas de funcionalidad.
- [`hotfix-branch-example.md`](branches/hotfix_branch_example.md): Describe cómo manejar ramas para correcciones urgentes.

Estas estrategias de branching ayudan a mantener el código organizado, estable y fácil de evolucionar.
---

## ⚙️ Ejemplos de Flujos de Trabajo (CI)

En [`workflow-examples/ci_workflow_demo.md`](workflow-examples/ci_workflow_demo.md) se muestra cómo configurar y entender un flujo de CI con GitHub Actions. Esto te permitirá automatizar pruebas y otras tareas para mejorar la calidad del proyecto.

> [!IMPORTANT]  
> Esta parte del taller está destinada para usuarios más avanzados y con experiencia en GitHub. Si no es tu caso prueba a completar el resto del taller antes de venir aquí.

---

## 🤝 Contribuir & Código de Conducta

- **[CONTRIBUTING.md](CONTRIBUTING.md)**: Explica cómo contribuir al proyecto (reportar bugs, enviar PRs, sugerir mejoras).
- **[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)**: Establece las normas para asegurar un entorno inclusivo y respetuoso.

Te recomendamos leer estos documentos antes de colaborar.
