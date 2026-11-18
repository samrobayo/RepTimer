# Gym Rep Timer — PWA

App web instalable: funciona sin internet y se agrega a la pantalla de inicio como una app.

## Contenido
- `index.html` — la app completa
- `manifest.webmanifest` — nombre, colores e íconos de la app
- `sw.js` — service worker (permite usarla sin conexión)
- `icons/` — íconos para Android, iPhone y escritorio

## Cómo publicarla (gratis)
Necesita HTTPS; cualquiera de estos lo da automáticamente.

**Netlify Drop (lo más rápido, sin cuenta técnica)**
1. Entra a https://app.netlify.com/drop
2. Arrastra la carpeta `rep-timer-pwa` completa (descomprimida).
3. Te da un link `https://algo.netlify.app`. Puedes cambiarle el nombre en Site settings.

**GitHub Pages**
1. Crea un repositorio y sube estos archivos a la raíz.
2. Settings → Pages → Branch: `main` / root → Save.

**Vercel**: `npx vercel` dentro de la carpeta, o arrastra la carpeta en vercel.com/new.

## Cómo instalarla en el teléfono
- **Android (Chrome):** abre el link → botón "Install app" en la portada, o menú ⋮ → "Instalar app".
- **iPhone (Safari):** abre el link → Compartir → "Agregar a pantalla de inicio".

## Al publicar una nueva versión
Cambia `rep-timer-v1` por `rep-timer-v2` (y así sucesivamente) en la primera línea de `sw.js`,
para que los teléfonos que ya la instalaron descarguen la actualización.

## Limitaciones de una PWA
- Con la pantalla bloqueada, el navegador puede pausar el reloj y los pitidos. La app pide mantener
  la pantalla encendida mientras corre.
- En iPhone, el sonido sale solo si el interruptor de silencio está apagado.
