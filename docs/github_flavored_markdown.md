
# 🎨 GitHub Flavored Markdown (GFM)

GitHub no solo soporta Markdown estándar, sino también su propia variante con características adicionales llamadas "GitHub Flavored Markdown (GFM)". Estas extensiones hacen tu documentación más interactiva y poderosa.

## Extensión de Citas para Alertas

Para destacar un punto importante, GFM que incluye diferentes tipos de notas/alertas:

```markdown
> [!NOTE]  
> Así se ve una alerta de tipo NOTE.

> [!TIP]
> Así se ve una alerta de tipo TIP.

> [!IMPORTANT]  
> Así se ve una alerta de tipo IMPORTANT.

> [!WARNING]  
> Así se ve una alerta de tipo WARNING.

> [!CAUTION]
> Así se ve una alerta de tipo CAUTION.
```

Ejemplo de como se ve cada una de ellas:

> [!NOTE]  
> Así se ve una alerta de tipo NOTE.

> [!TIP]
> Así se ve una alerta de tipo TIP.

> [!IMPORTANT]  
> Así se ve una alerta de tipo IMPORTANT.

> [!WARNING]  
> Así se ve una alerta de tipo WARNING.

> [!CAUTION]
> Así se ve una alerta de tipo CAUTION.

## Tablas Mejoradas

Aunque ya vimos tablas, GFM las hace más simples y con alineaciones:

```markdown
| Columna Izq. | Columna Centro | Columna Der. |
|:-------------|:--------------:|-------------:|
| Texto izq.   |   Texto cent.  |   Texto der. |
```

Las alineaciones se controlan con `:`, generando tablas más limpias.

## Listas de Tareas (Checklists) Interactivas

Las listas de tareas creadas en Issues y Pull Requests son clicables, permitiendo marcar tareas como completadas directamente desde la interfaz web de GitHub:

```markdown
- [ ] Pendiente
- [x] Hecho
```

En la vista de GitHub, puedes hacer clic para marcar las tareas.

## Soporte para @menciones

Menciona a usuarios: `@usuario` enviará notificaciones a la persona mencionada.  
Menciona equipos: `@tu-organizacion/equipo` para notificar a todo el equipo.

Esto facilita la comunicación y el flujo de trabajo en repositorios con múltiples colaboradores.

## Referencias Automáticas a Issues y Pull Requests

Como se mencionó, escribir `#1` creará un enlace al Issue o PR #1 dentro del mismo repositorio. Esto agiliza la navegación interna y la trazabilidad del trabajo.

## Markdown en Comentarios y Discussions

GFM no se limita a archivos `.md`. Todos los comentarios en Issues, Pull Requests y las discusiones de GitHub soportan Markdown. Esto significa que puedes mantener una comunicación estructurada y clara con tus colaboradores, usando todos los beneficios del formateo.

## Sugerencias de Código (Code Suggestions)

En las discusiones de PR, puedes sugerir cambios directos en el código usando bloques con sugerencias. Este es un plus enorme para las revisiones.

<pre>
```suggestion
// Aquí puedes sugerir un cambio específico en el código
```
</pre>

Esta funcionalidad no está disponible en archivos estáticos, pero es parte de la experiencia GFM en la interfaz de GitHub.
