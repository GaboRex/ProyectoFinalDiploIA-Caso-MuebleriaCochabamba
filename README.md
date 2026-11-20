# Mueblería Cochabamba – Página web con agente IA

Proyecto final, Módulo 1 – Diplomado en Agentes de IA (UPB).

Página estática (un solo `index.html`):

- **Catálogo**: se carga en vivo desde la API de Google Apps Script (`?accion=catalogo`), que lee la hoja de Google Sheets. Sin costos de compra.
- **Filtros**: categoría, ancho máximo (cm) y presupuesto (Bs).
- **Formulario de cotización**: valida el correo (doble confirmación) y registra en la hoja `Solicitudes_Cotizacion` (`?accion=registrar`). No genera duplicados si se reintenta.
- **Chat**: agente "Arce" de Botpress como burbuja flotante.

## Despliegue en Vercel

1. Crear un repositorio en GitHub (p. ej. `muebleria-cochabamba`) y subir `index.html`, `vercel.json` y este `README.md`.
2. En vercel.com → **Add New… → Project** → importar el repositorio.
3. Framework Preset: **Other**. Sin comando de build. Output: raíz del proyecto.
4. **Deploy**. La página queda en `https://<nombre>.vercel.app`.

Cada `git push` vuelve a desplegar la página automáticamente.

## Configuración

En `index.html`, constante `API_URL`: la URL `/exec` de la Web App de Apps Script.
Si se publica una nueva implementación con otra URL, solo hay que cambiar esa línea.
