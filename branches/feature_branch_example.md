# 🌱 Ejemplo de Rama de Funcionalidad (Feature Branch)

Este archivo explica cómo manejar ramas de funcionalidad independientes, un enfoque común en equipos que siguen Git Flow o simplemente quieren aislar el desarrollo de nuevas características.

## ¿Qué es una Feature Branch?

Una *Feature Branch* es una rama creada desde la rama principal (ejemplo: `main` o `develop`) para trabajar en una nueva funcionalidad sin afectar el código estable. Una vez que la funcionalidad está lista y probada, se fusiona nuevamente en la rama principal.

## Beneficios

- **Aislamiento:** Si algo sale mal, puedes descartar la rama sin afectar el resto del proyecto.
- **Colaboración:** Varios desarrolladores pueden trabajar en distintas funciones en paralelo.
- **Historial Limpio:** El historial de la rama principal se mantiene más organizado, pues las nuevas funciones llegan en forma de *pull requests* revisadas.

## Flujo Sugerido

1. **Crear la rama:**
   ```bash
   git checkout -b feature/nueva-funcionalidad main
   ```
   
2. **Desarrollar en la rama:**
   Agrega, modifica o elimina archivos según la nueva función que estés implementando.

3. **Probar y depurar:**
   Ejecuta tus pruebas locales. Asegúrate de que todo funciona correctamente.

4. **Hacer un Pull Request:**
   Desde GitHub, crea una PR hacia `main`. Tus compañeros revisarán los cambios y, si todo está bien, se fusionará la nueva funcionalidad.
