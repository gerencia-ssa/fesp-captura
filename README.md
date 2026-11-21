# Máscara de captura · Plan de Acción para el Fortalecimiento de las FESP

SNSP · Coordinación Estatal Morelos. Página de captura para las Jurisdicciones Sanitarias, publicada con GitHub Pages. Los datos se guardan en la hoja de concentración de Google mediante Apps Script (servidor).

## Estructura

| Archivo | Uso |
| --- | --- |
| `index.html` | Máscara de captura (no se edita) |
| `config.js` | URL del servidor Apps Script (único archivo a editar) |
| `assets/` | Imágenes institucionales de ÁGORA: logo Salud · SNSP, greca y emblema 2026 |
| `.nojekyll` | Indica a GitHub Pages que publique los archivos tal cual |

## Publicación

1. Implemente `Code.gs` en Apps Script como **Aplicación web**: *Ejecutar como* **Yo**, *Quién tiene acceso* **Cualquier usuario**. Copie la URL `/exec`.
2. En `config.js` pegue esa URL en `API_URL`.
3. Las imágenes ya vienen en `assets/` (las mismas de ÁGORA).
4. En GitHub: *Settings → Pages → Source: Deploy from a branch → main / (root) → Save*.
5. La página queda en `https://<usuario>.github.io/<repositorio>/`. Esa liga va en ÁGORA (Estrategias paralelas).

## Pruebas

- `<URL /exec>?action=ping` debe responder `{"ok":true,…}`.
- Con `API_URL` sin configurar, la página abre en modo demostración (franja amarilla) y no guarda.
