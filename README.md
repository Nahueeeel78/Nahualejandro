# Inventario TI Escuela

App instalable (PWA) para gestionar el inventario, notas y recordatorios del área de computación e informática de la escuela. Funciona sin conexión y guarda todo en el propio celular.

## Qué incluye
- **Inventario**: notebooks, cargadores, netbooks (Plan Sarmiento), cables de red, adaptadores WiFi USB y más. Cada equipo tiene marca, número, ubicación, estado (Bueno / En reparación / De baja), nota y foto.
- **Notas**: para anotar fallas, reparaciones o pedidos de repuestos, con foto como testigo.
- **Recordatorios**: pendientes con fecha límite opcional.
- **Copia de seguridad**: exportar/importar toda la información como archivo JSON (botón arriba a la derecha). Como los datos se guardan solo en este celular, conviene exportar una copia de vez en cuando.
- Ícono y pantalla de carga con tu propio logo.

## Cómo probarla ahora mismo (sin subir nada)
1. Abrí la carpeta `app` y hacé doble clic en `index.html`, o
2. Subí la carpeta completa a [Netlify Drop](https://app.netlify.com/drop) arrastrándola — te da un link al instante.

## Cómo subirla a GitHub Pages (gratis, con tu propio link)
1. Creá un repositorio nuevo en GitHub (por ejemplo `inventario-ti`).
2. Subí **todo el contenido de la carpeta `app`** (no la carpeta en sí, sino lo que está adentro: `index.html`, `manifest.json`, `sw.js`, la carpeta `icons`) a la raíz del repositorio.
3. Andá a **Settings → Pages** del repositorio.
4. En "Source" elegí la rama `main` y la carpeta `/ (root)`. Guardá.
5. En un minuto vas a tener tu app en una dirección como `https://tu-usuario.github.io/inventario-ti/`.

## Cómo instalarla en el celular
1. Abrí el link de la app en Chrome (Android).
2. Tocá el menú (⋮) → **"Agregar a pantalla de inicio"** o **"Instalar app"**.
3. Va a quedar con tu ícono, como cualquier otra app, y va a abrir a pantalla completa.

## Notas técnicas
- Los datos (inventario, notas, recordatorios) se guardan en el almacenamiento local del navegador (`localStorage`), no en ningún servidor. Si cambiás de celular o borrás datos del navegador, hay que restaurar desde el backup JSON.
- Las fotos se comprimen automáticamente antes de guardarse para no ocupar demasiado espacio.
- El Service Worker (`sw.js`) permite que la app cargue y funcione aunque no tengas señal.
