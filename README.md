# Dashboard Auditorías LAR — sitio web

## Estructura
- `index.html` — código del dashboard (lógica, estilos). NO contiene datos.
- `data/manifest.json` — índice de edificios y su orden de visualización.
- `data/<edificio>.json` — datos de cada edificio (uno por archivo).
- `data/lar_logo.txt` — logo LAR en base64.

## Agregar un edificio nuevo
1. Generar su `data/nuevo_edificio.json` (misma estructura que los existentes).
2. Agregarlo en `data/manifest.json`: añadir una entrada en `buildings` y su nombre en `order`.
3. Listo. No se toca `index.html`.

## Probar localmente
No funciona abriéndolo con doble clic (file://) por seguridad del navegador.
Levantar un servidor local:
    python3 -m http.server 8000
y abrir http://localhost:8000

## Publicar
Subir la carpeta completa a cualquier hosting estático (Cloudflare Pages, Netlify, GitHub Pages).
