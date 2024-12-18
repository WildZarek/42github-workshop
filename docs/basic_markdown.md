# 🌱 Fundamentos de Markdown

Markdown es un lenguaje de marcado ligero diseñado para ser fácil de leer y escribir. Se utiliza ampliamente en GitHub, documentación, blogs técnicos y muchos otros contextos. **¿Por qué es tan popular?** Porque te permite escribir texto estructurado con muy poca sintaxis, centrando tu atención en el contenido y no en el formato.

## ¿Qué es Markdown?

Imagina un lenguaje que puedes escribir en un archivo de texto plano, pero que al renderizarlo (por ejemplo, en GitHub) se convierte en un documento con **estilos**, **encabezados**, **listas**, **enlaces** y **imágenes**. Eso es Markdown.

- **Ventaja 1:** Es sumamente fácil de aprender.  
- **Ventaja 2:** Es compatible con la mayoría de las plataformas de desarrollo.  
- **Ventaja 3:** Puedes ver directamente el resultado final en GitHub, sin instalar nada adicional.

> **💡 Tip:** Si ves cualquier `README.md` en GitHub, lo estás viendo en Markdown. Para ver el código fuente, solo ve al archivo en el repositorio y haz clic en el botón "Raw" o "Code" (a menudo representado por el icono `<>`). Así verás exactamente cómo se escribe.

## Ejemplo de Encabezados

En Markdown, los encabezados se crean usando el símbolo `#`:

```markdown
# Encabezado de nivel 1
## Encabezado de nivel 2
### Encabezado de nivel 3
```

Lo que ves arriba se convierte en títulos con distintos tamaños, permitiendo organizar tu contenido.

## Listas

- Listas desordenadas: Usan `-`, `*` o `+`.
```markdown
- Manzana
- Pera
- Uva
```

- Listas ordenadas: Usan números.
```markdown
1. Primer elemento
2. Segundo elemento
3. Tercer elemento
```

## Énfasis en el Texto

- **Negritas:** Se usa `**texto**` para resaltar en negritas.
- *Cursivas:* Se usa `*texto*` o `_texto_` para cursivas.
- ~~Tachado:~~ Se usa `~~texto~~` para tachar.

## Enlaces

```markdown
[Texto del Enlace](http://ejemplo.com)
```

Al renderizar, el texto se convierte en un enlace clicable. Ideal para referencias externas o internas dentro de tu proyecto.

## Imágenes

```markdown
![Texto Alternativo](url_de_la_imagen)
```

El texto alternativo describe la imagen para accesibilidad y en caso de que no cargue la imagen.

> **Ejemplo:**
> ```markdown
> ![Logo de GitHub](https://github.githubassets.com/images/modules/logos_page/GitHub-Logo.png)
> ```

## Bloques de Código

Para mostrar código en tu documentación:

<pre><code>```language
Aquí tu código
```
</code></pre>

Cambia *language* por `bash`, `js`, `python`, etc., para resaltar la sintaxis.

## Tablas

También puedes crear tablas fácilmente:

```markdown
| Encabezado 1 | Encabezado 2 |
|--------------|--------------|
| Fila 1 Col 1 | Fila 1 Col 2 |
| Fila 2 Col 1 | Fila 2 Col 2 |
```

¡Y listo! Una tabla clara para organizar datos.

---

**¡Felicidades!** Ahora conoces los fundamentos de Markdown.  
En el siguiente documento, `markdown_advanced.md`, profundizaremos en características más avanzadas.
