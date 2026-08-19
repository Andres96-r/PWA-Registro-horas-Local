# Fichaje · Control de horas (PWA)

App local-first para iPhone (13 en adelante). Funciona **offline** y guarda todo en el celular (IndexedDB).

## Cómo publicarla (elegí una)
Necesita servirse por **HTTPS** para instalarse como PWA. Opciones que ya conocés:

- **Firebase Hosting**: `firebase init hosting` (public = esta carpeta) → `firebase deploy`.
- **Netlify / Vercel**: arrastrás la carpeta y listo.
- **GitHub Pages**: subís la carpeta a un repo y activás Pages.
- **Probar rápido en la compu**: `python3 -m http.server 8080` y entrás desde `http://localhost:8080`.

## Instalar en el iPhone
1. Abrí la URL en **Safari** (no Chrome; en iOS solo Safari instala PWAs).
2. Botón **Compartir** → **Agregar a inicio**.
3. Abrila desde el ícono (queda a pantalla completa, sin barra del navegador).

## Archivos
- `index.html` — toda la app (UI + lógica + almacenamiento + export). Autocontenido.
- `manifest.webmanifest` — datos de instalación.
- `sw.js` — service worker (cache offline).
- `icon-*.png`, `apple-touch-icon.png` — íconos.
- `fonts/` — Cormorant Garamond + Jost (locales, para andar offline).

## No perder info
- **Ajustes → Descargar respaldo (.json)**: copia completa. Guardala en Archivos/Drive.
- **Ajustes → Restaurar respaldo**: recupera todo en un celular nuevo.
- La app pide "almacenamiento persistente" al iOS y avisa si tenés datos sin respaldar.
