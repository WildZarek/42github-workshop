# ⚡ Hoja de Referencia Rápida de Git

Esta hoja de referencia resume los comandos Git más usados en tu día a día. 

## Tabla de Contenidos

- [Configuración Inicial](#configuración-inicial)
- [Flujo Básico (Día a Día)](#flujo-básico-día-a-día)
- [Navegación en el Historial y Versiones](#navegación-en-el-historial-y-versiones)
- [Ramas (Branching)](#ramas-branching)
- [Remotos](#remotos)
- [Etiquetas (Tags) y Lanzamientos (Releases)](#etiquetas-tags-y-lanzamientos-releases)
- [Guardar Cambios Temporales](#guardar-cambios-temporales)
- [Deshacer Cambios (Reset, Restore, Revert)](#deshacer-cambios-reset-restore-revert)
- [Comandos Avanzados](#comandos-avanzados)
- [Ejemplos Prácticos Rápidos](#ejemplos-prácticos-rápidos)


## Configuración Inicial

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@example.com"
git config --global core.editor "nombre_de_editor"      # Configurar el editor por defecto
git config --list                                       # Ver todas las configuraciones
```

---

## Flujo Básico (Día a Día)

```bash
git clone <url_del_repositorio>     # Clonar un repositorio
git status                          # Ver estado de cambios
git add <archivo>                   # Añadir un archivo al área de Staging
git add .                           # Añadir todos los cambios en el directorio actual
git commit -m "Mensaje"             # Confirmar cambios al repositorio local
git commit --amend                  # Modificar el último commit (mensaje o contenido)
git push                            # Enviar cambios al repositorio remoto
git pull                            # Descargar e integrar cambios desde el remoto
```

**Consejo:** Usa `git status` con frecuencia para saber en qué estado están tus archivos.

---

## Navegación en el Historial y Versiones

```bash
git log                             # Ver historial de commits (presiona q para salir)
git log --oneline --graph           # Ver historial resumido y con grafo
git show <commit>                   # Mostrar detalles de un commit en específico
git diff                            # Comparar cambios entre el área de trabajo y Staging
git diff HEAD^ HEAD                 # Comparar cambios entre el último commit y el anterior
```

---

## Ramas (Branching)

```bash
git branch                          # Listar ramas locales
git branch <nombre_rama>            # Crear nueva rama
git checkout <nombre_rama>          # Cambiar a la rama
git switch <nombre_rama>            # Otra forma de cambiar de rama (Git 2.23+)
git checkout -b <nueva_rama>        # Crear y cambiar a una nueva rama
git switch -c <nueva_rama>          # Crear y cambiar de rama (Git 2.23+)
git merge <nombre_rama>             # Fusionar rama en la rama actual
git branch -d <rama>                # Eliminar una rama ya fusionada
```

---

## Remotos

```bash
git remote -v                       # Ver remotos configurados
git remote add origin <url>         # Añadir un repositorio remoto
git fetch                           # Descargar cambios sin fusionar
git push -u origin <rama>           # Asocia la rama local con la remota y empuja cambios
git pull --rebase                   # Descargar cambios y rebasear (evitar merges automáticos)
```

---

## Etiquetas (Tags) y Lanzamientos (Releases)

```bash
git tag <etiqueta>                  # Añadir etiqueta ligera a un commit actual
git tag -a v1.0 -m "Versión 1.0"    # Crear etiqueta anotada con mensaje
git tag                             # Listar etiquetas
git push origin --tags              # Enviar todas las etiquetas al remoto
```

---

## Guardar Cambios Temporales

```bash
git stash                           # Guardar cambios actuales sin commitear
git stash list                      # Ver lista de stashes
git stash apply                     # Aplicar el stash más reciente
git stash pop                       # Aplicar y eliminar el stash más reciente
```

---

## Deshacer Cambios (Reset, Restore, Revert)

```bash
git restore <archivo>               # Deshacer cambios en el área de trabajo
git restore --staged <archivo>      # Sacar cambios del área de Staging
git reset <commit>                  # Mover la rama actual a un commit anterior (mantiene cambios)
git reset --hard <commit>           # Mover la rama y descartar cambios locales
git revert <commit>                 # Crear un commit inverso para deshacer un cambio anterior sin reescribir el historial
```

---

## Comandos Avanzados

```bash
git rebase <rama/base>              # Reaplicar commits sobre otro punto en el historial
git rebase -i <commit/base>         # Rebase interactivo, reordenar, combinar o eliminar commits
git cherry-pick <commit>            # Aplicar un commit específico en la rama actual
git blame <archivo>                 # Mostrar autoría línea a línea de un archivo
git reflog                          # Ver el registro de todos los movimientos de HEAD (muy útil para recuperar commits "perdidos")
git bisect                          # Búsqueda binaria en el historial para encontrar el commit que introdujo un bug
```

---

## Ejemplos Prácticos Rápidos

A continuación se muestran ejemplos sencillos del uso de los comandos. Estos ejemplos no cubren todas las opciones, pero sirven para ver cómo se usan en la práctica:

1. **Configurar tu usuario:**
   ```bash
   git config --global user.name "Maria Perez"
   git config --global user.email "maria@example.com"
   ```

2. **Clonar y revisar estado:**
   ```bash
   git clone https://github.com/usuario/proyecto.git
   cd proyecto
   git status
   ```

3. **Agregar y confirmar cambios:**
   ```bash
   echo "Nuevo contenido" >> archivo.txt
   git add archivo.txt
   git commit -m "Agrego archivo.txt con nuevo contenido"
   ```

4. **Enviar cambios al remoto:**
   ```bash
   git push
   ```

5. **Crear y cambiar a una nueva rama:**
   ```bash
   git checkout -b feature/nueva-funcion
   # Ahora estás en la rama "feature/nueva-funcion"
   ```

6. **Fusionar una rama:**
   ```bash
   git checkout main
   git merge feature/nueva-funcion
   ```

7. **Revertir un commit:**
   ```bash
   git revert <sha_del_commit>
   # Crea un nuevo commit que deshace los cambios anteriores.
   ```

8. **Stash y recuperación:**
   ```bash
   # Tienes cambios sin confirmar, pero debes cambiar de contexto rápidamente
   git stash
   # Más tarde...
   git stash pop
   ```

9. **Rebase interactivo:**
   ```bash
   git rebase -i HEAD~3
   # Rearranca los últimos 3 commits, permitiendo reordenar y combinar.
   ```

10. **Ver historial resumido:**
    ```bash
    git log --oneline --graph
    ```
