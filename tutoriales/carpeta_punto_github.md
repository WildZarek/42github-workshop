# Teoría y Práctica: Estructura de la Carpeta `.github/`

La carpeta `.github/` dentro de un repositorio de GitHub es un espacio reservado para configuraciones y plantillas que mejoran la calidad del proyecto, la experiencia de los colaboradores y la integración con las herramientas de GitHub. A continuación, revisaremos cada carpeta y archivo que hemos creado dentro de `.github/` explicando la función de cada uno.

## Objetivos de Aprendizaje

- Comprender el propósito de la carpeta `.github/` en un repositorio.
- Aprender cómo las plantillas de *Issues* y *Pull Requests* pueden mejorar la comunicación y calidad del proyecto.
- Entender cómo los flujos de trabajo (Workflows) de GitHub Actions automatizan tareas y mejoran la integración continua (CI).
- Conocer la utilidad del archivo `CODEOWNERS` para asignar responsabilidad a áreas específicas del repositorio.

---

## Estructura de la Carpeta `.github/`

```
.github/
├── workflows/
│   └── ci.yml
├── ISSUE_TEMPLATE/
│   ├── bug_report.md
│   └── config.yml
├── PULL_REQUEST_TEMPLATE.md
└── CODEOWNERS
```

---

### 1. Workflows: `ci.yml`

**Ruta:** `.github/workflows/ci.yml`

**Función:**  
`ci.yml` es un ejemplo de configuración para GitHub Actions. Estos flujos de trabajo se ejecutan automáticamente en respuesta a eventos del repositorio, como hacer *push*, crear un *pull request* o lanzar un *tag*. Con un flujo de CI (Integración Continua), puedes:

- **Ejecutar pruebas automáticamente:** Cada vez que se suben cambios, las pruebas se ejecutan garantizando que no se rompa funcionalidad existente.
- **Construir el proyecto:** Verificar que el código compile correctamente.
- **Generar informes:** Mostrar resultados de pruebas, cobertura, etc.

**En la práctica:**  
Una vez configurado `ci.yml`, cada *commit* en la rama `main` o cada nueva *pull request* disparará el flujo de trabajo. Si las pruebas pasan, sabrás que tu código es estable. Si fallan, tendrás retroalimentación inmediata para corregir antes de fusionar cambios.

---

### 2. Plantilla de Issues: `bug_report.md`

**Ruta:** `.github/ISSUE_TEMPLATE/bug_report.md`

**Función:**  
Este archivo define una plantilla preestablecida para la creación de *Issues* de tipo "Reporte de Bug". Cuando un usuario cree un nuevo *Issue* y seleccione esta plantilla, verá un formulario con secciones predefinidas:

- Descripción clara del problema.
- Pasos para reproducirlo.
- Comportamiento esperado.
- Capturas de pantalla (opcional).
- Información adicional.

**Beneficio:**  
Al estandarizar cómo se reportan errores, obtienes información más clara y útil, lo que facilita su resolución y ahorra tiempo a los mantenedores.

---

### 3. Plantilla de Pull Requests: `PULL_REQUEST_TEMPLATE.md`

**Ruta:** `.github/PULL_REQUEST_TEMPLATE.md`

**Función:**  
Esta plantilla proporciona una estructura estándar para las *pull requests*. Cuando un colaborador abre una *pull request*, la plantilla aparecerá automáticamente en el cuadro de descripción. La plantilla incluye secciones para:

- Descripción de los cambios.
- Tipo de cambio (bug fix, nueva característica, etc.).
- Cómo se probaron estos cambios.
- Checklist para asegurar calidad y completitud.

**Beneficio:**  
Mantener un formato uniforme en las *pull requests* facilita la revisión, la comunicación y la transparencia en el equipo.

**Notas adicionales:**

> [!TIP]
> Este paso es opcional, pero aconsejable si utilizamos nuestras propias plantillas.

Si queremos que sea obligatorio utilizar cualquiera de nuestras plantillas, evitando que se puedan enviar peticiones sin plantilla,
debemos crear un archivo `.github/ISSUE_TEMPLATE/config.yml` con el siguiente contenido:

```yaml
blank_issues_enabled: false
```

---

### 4. Archivo `CODEOWNERS`

**Ruta:** `.github/CODEOWNERS`

**Función:**  
`CODEOWNERS` permite asignar automáticamente revisores a partes específicas del repositorio. Por ejemplo, si un usuario es experto en la documentación (`docs/`), se le puede asignar como responsable. Cada vez que se realicen cambios en `docs/`, ese usuario será notificado para revisar y aprobar.

**Beneficio:**  
- Asegura que cada cambio sea revisado por la persona más apropiada.
- Distribuye la carga de trabajo de revisión.
- Garantiza que las áreas críticas del código sean supervisadas por expertos.

---

## Importancia de cada archivo

1. **Estandarización y Calidad:**  
   Las plantillas (*Issues* y *Pull Requests*) evitan la ambigüedad en la comunicación. Al estandarizar la información, se reduce el tiempo invertido en aclarar dudas y se facilita el entendimiento del estado del proyecto.

2. **Automatización con CI:**  
   Un flujo de trabajo de CI (como `ci.yml`) asegura que cada cambio se pruebe y valide automáticamente. Esto contribuye a la entrega continua de un software más estable y confiable.

3. **Responsabilidades Claras:**  
   Con `CODEOWNERS` sabes exactamente quién es responsable de revisar qué partes del proyecto. Esto ahorra tiempo y evita confusiones a la hora de asignar revisiones.

---

A continuación presentamos una guía práctica para observar cada uno de estos archivos en acción en tu repositorio. La idea es que realices pequeñas tareas que desencadenen el uso de las plantillas, el flujo CI y la asignación de revisores.

---

## Guía Práctica: Ver Cada Archivo en Acción

### 1. Ver el Flujo CI (`ci.yml`) en Acción

**Objetivo:** Comprobar que el archivo `ci.yml` ejecute pruebas automáticamente.

**Pasos:**

1. **Realiza un cambio en el código:**  
   - Crea una rama nueva:  
     ```bash
     git checkout -b prueba-ci
     ```
   - Realiza algún cambio sencillo en un archivo (por ejemplo, en `README.md`).
   - Realiza un commit y haz push:
     ```bash
     git add README.md
     git commit -m "Prueba CI"
     git push -u origin prueba-ci
     ```
2. **Crea una Pull Request en GitHub:**  
   - Desde la interfaz web de GitHub, abre una *pull request* hacia `main`.
   - Al abrir la PR, el flujo `ci.yml` se ejecutará automáticamente.
   - Ve a la pestaña "Actions" o revisa el estado de la PR. Deberías ver un check pendiente y luego verde (si todo funciona correctamente) o rojo (si hay errores).
   
**Resultado esperado:** El flujo CI se ejecuta sin intervención, mostrando si los cambios pasan las pruebas o no.

---

### 2. Plantilla de Issues (`bug_report.md`)

**Objetivo:** Experimentar con la creación de un *Issue* utilizando la plantilla de reporte de bug.

**Pasos:**

1. **Crear un Issue desde GitHub:**  
   - Ve a la pestaña "Issues" del repositorio en GitHub.
   - Haz clic en "New issue".
   - Selecciona "Reporte de Bug" (esta es la plantilla definida en `bug_report.md`).
2. **Completa el formulario:**  
   - Verás campos predefinidos: descripción, pasos para reproducir, comportamiento esperado, etc.
   - Completa la información y envía el *Issue*.

**Resultado esperado:** El *Issue* se crea con un formato estandarizado, ayudando a los mantenedores a entender rápidamente el problema.

---

### 3. Plantilla de Pull Requests (`PULL_REQUEST_TEMPLATE.md`)

**Objetivo:** Ver la plantilla de PR en acción.

**Pasos:**

1. **Crea una rama y un cambio ligero:**  
   - Desde tu terminal:
     ```bash
     git checkout main
     git pull
     git checkout -b mejora-documentacion
     ```
   - Edita algún archivo (por ejemplo, `docs/markdown_basics.md`).
   - Haz commit y push:
     ```bash
     git add docs/markdown_basics.md
     git commit -m "Mejora documentación Markdown"
     git push -u origin mejora-documentacion
     ```
2. **Crea la Pull Request en GitHub:**  
   - Abre la PR desde la interfaz web.
   - Al abrirla, verás el contenido de `PULL_REQUEST_TEMPLATE.md` ya cargado en el cuadro de descripción de la PR.
3. **Completa la información:**  
   - Describe qué cambios hiciste, el tipo de cambio y cómo lo probaste.
   - Envía la PR.

**Resultado esperado:** La PR se crea con una estructura clara, facilitando la revisión y discusión.

---

### 4. `CODEOWNERS` en Acción

**Objetivo:** Ver cómo se asignan revisores automáticamente.

**Pasos:**

1. **Revisar el archivo `CODEOWNERS`:**  
   - Si tienes una línea como `docs/ @doc-owner`, significa que cualquier cambio en `docs/` asignará a `@doc-owner` como revisor.
   
2. **Realiza un cambio en la carpeta indicada:**  
   - Edita un archivo dentro de `docs/`:
     ```bash
     git checkout -b actualiza-docs
     ```
     Edita, por ejemplo, `docs/markdown_basics.md` y realiza commit y push.
3. **Crea una Pull Request:**  
   - Abre la PR en GitHub.
   - Observa que `@doc-owner` ha sido añadido automáticamente como revisor en la sección de revisión de la PR.

**Resultado esperado:** La persona o equipo asignado en `CODEOWNERS` aparece automáticamente como revisor, sin que tengas que hacerlo manualmente.

---

## Conclusión

Si has seguido la guía práctica habrás visto en acción:

- **`ci.yml` (Workflows)**: Ejecutando tareas de CI/CD automáticamente.
- **`bug_report.md`**: Proporcionando una plantilla clara al crear Issues.
- **`PULL_REQUEST_TEMPLATE.md`**: Estandarizando la información en las Pull Requests.
- **`CODEOWNERS`**: Asignando revisores automáticamente a ciertas partes del código.

La carpeta `.github/` no solo es un espacio para configuraciones "tras bambalinas", sino que es un recurso poderoso para estandarizar procesos, asignar responsabilidades y mejorar la calidad del trabajo en equipo. Al comprender y utilizar estos archivos, tu repositorio estará mejor organizado, será más fácil de mantener y la colaboración fluirá con mayor naturalidad.