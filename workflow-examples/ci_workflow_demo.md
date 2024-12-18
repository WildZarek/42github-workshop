# Ejemplo de Flujo de CI con GitHub Actions

> [!IMPORTANT]  
> Esta parte del taller está destinada para usuarios más avanzados y con experiencia en GitHub. Si no es tu caso prueba a completar el resto del taller antes de venir aquí.

Este documento muestra un ejemplo práctico de cómo configurar un flujo de Integración Continua (CI) utilizando GitHub Actions. Aquí entenderás cómo automatizar pruebas, verificaciones y despliegues simples al realizar cambios en tu repositorio.

## ¿Qué es CI?

La Integración Continua (CI) es la práctica de fusionar frecuentemente cambios en la rama principal, ejecutando pruebas y validaciones automáticamente para detectar errores temprano. Esto mejora la calidad y estabilidad del código.

## Ejemplo de Archivo `ci.yml`

A continuación, un ejemplo de flujo de trabajo (`.github/workflows/ci.yml`) que:

- Se ejecuta cuando se hace *push* o se crea un *pull request* hacia la rama `main`.
- Clona el repositorio.
- Instala dependencias (ejemplo con Node.js).
- Ejecuta pruebas unitarias.

```yaml
name: CI

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build_and_test:
    runs-on: ubuntu-latest

    steps:
      - name: Clonar el repositorio
        uses: actions/checkout@v2

      - name: Configurar Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '14'

      - name: Instalar dependencias
        run: npm install

      - name: Ejecutar pruebas
        run: npm test
```

### Explicación de los Pasos

1. **Evento `on`:**  
   - `push` y `pull_request`: El flujo se activa cuando se hacen commits a `main` o se abre/actualiza una PR hacia `main`.

2. **jobs > build_and_test:**  
   - **runs-on: ubuntu-latest:** Indica en qué tipo de entorno se ejecuta el flujo.
   - **Clonar el repositorio:** Usa la acción oficial `actions/checkout` para obtener el código.
   - **Configurar Node.js:** Usa `actions/setup-node` para establecer una versión de Node.
   - **Instalar dependencias:** Ejecuta `npm install` para preparar el entorno.
   - **Ejecutar pruebas:** Con `npm test` se corren las pruebas. Si alguna falla, el flujo marcará el resultado como fallido.

### Ventajas de Este Enfoque

- **Detección Temprana de Errores:** Cada cambio se prueba automáticamente, evitando que bugs se acumulen.
- **Flujo Automatizado:** No necesitas ejecutar manualmente las pruebas en cada commit.
- **Confianza en el Código:** Si el flujo CI está en verde, el equipo sabe que el código es estable.

### Mejoras Potenciales

- **Agregar linting o formateo automático:** Incluir un paso con `npm run lint` o una acción de formateo.
- **Testeo en Múltiples Versiones de Node:** Ajustar el workflow para probar el código en varias versiones de Node.js.
- **Integración con CD (Entrega Continua):** Después de aprobar cambios, extender el flujo para desplegar automáticamente (por ejemplo, a GitHub Pages).
