
# 🚀 Markdown Avanzado

Ya dominas lo básico, ahora pasemos al siguiente nivel.

## Encabezados con Estilo y Anchor Links

Si quieres que una sección sea fácilmente enlazada desde otro punto, GitHub crea anclas automáticas para cada encabezado. Por ejemplo, si tu encabezado es `## Bloques Colapsables`, podrás enlazarlo con [`bloques colapsables`](#bloques-colapsables).

## Citas y Notas

Puedes usar `>` para crear citas:

```markdown
> Esta es una cita.
> Puede abarcar múltiples líneas.
```

> Esta es una cita.
> Puede abarcar múltiples líneas.

Para destacar un punto importante, puedes combinarlo con emojis:

```markdown
> **💡 Nota Importante:** Recuerda mantener tu README sencillo y claro.
```

> **💡 Nota Importante:** Recuerda mantener tu README sencillo y claro.

## Bloques Colapsables

GitHub soporta bloques colapsables con `<details>` y `<summary>`:

```markdown
<details>
  <summary>Haz clic aquí para ver más</summary>
  
  Contenido oculto hasta que se hace clic.
</details>
```

<details>
  <summary>Haz clic aquí para ver más</summary>
  
  Contenido oculto hasta que se hace clic.
</details>

Esto es útil para no sobrecargar la vista principal del README con información secundaria.

## Referencias a Issues, Pull Requests y Commits

Dentro de GitHub, puedes hacer referencia a:
- Issues: `#123` enlazará al Issue #123
- Pull Requests: `#456` enlazará a la PR #456
- Commits: usando el hash `abcd1234` creará un enlace a ese commit.

Esto hace que la documentación sea más interactiva y contextual.

## Checklists

Crea listas de tareas:

```markdown
- [x] Tarea completa
- [ ] Tarea pendiente
```

¡Excelente para el seguimiento del progreso de un proyecto!

## Emojis y Caracteres Especiales

Haz tu contenido más atractivo con emojis: 😄, 🚀, 📚.  
Para usarlos, puedes copiar y pegar desde la lista de emojis o usar el atajo `:nombre_del_emoji:` en GitHub (por ejemplo, `:rocket:`).

## Combinar Markdown con HTML

Si Markdown no es suficiente, puedes usar HTML para detalles finos de formateo.  
Por ejemplo, `<br>` para saltos de línea adicionales o `<sup>` y `<sub>` para superíndices o subíndices.

```markdown
Esto es texto normal<br><br>
Y este texto está separado por dos saltos de línea.
```

---

Has avanzado bastante. Ya no solo sabes las bases, sino también trucos para hacer tu documentación más dinámica y fácil de navegar. En el próximo archivo, [`github_flavored_markdown.md`](github_flavored_markdown.md), exploraremos las extensiones específicas que GitHub ofrece para enriquecer aún más tu contenido.
