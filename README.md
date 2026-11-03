# Gonzalo Valentino Agronegocios: landing

Página estática (un solo `index.html`, sin dependencias). Se publica con GitHub Pages en https://gvagro.com.ar (el archivo `CNAME` define el dominio).

## Archivos
- `index.html`: toda la página (estilos, catálogo y formulario).
- `assets/`: video e imágenes de los banners y la foto de Gonzalo.
- `favicon.svg`, `robots.txt`, `sitemap.xml`, `CNAME`.

## Cómo se editan las cosas
- **Productos del muestrario y del desplegable del formulario:** la lista `P` dentro del script de `index.html`. Un solo lugar alimenta los dos. Las tarjetas son solo de muestra (no se pueden tocar); para sumar información por producto se amplía cada entrada de `P` y el dibujo de la tarjeta en la función `render`.
- **Destino del formulario:** el atributo `action` del `<form id="form">`. Apunta a un Google Apps Script que guarda la consulta en la planilla "Consultas GV" y envía el aviso por email. Si se vuelve a implementar el script y cambia la URL, se actualiza ahí.
- **WhatsApp:** el número está en la constante `WA` del script (formato internacional, sin signos).
- **Banda de empresas de la trayectoria:** lista `<ul class="marquee-pista">` en la sección Trayectoria. Cada empresa está dos veces (la segunda copia lleva `aria-hidden`) para que el movimiento sea continuo: si se agrega o quita una empresa, hacerlo en las dos copias. Si se quieren logos, reemplazar el texto de cada `<li>` por una imagen con su `alt`.
- **Pie de página:** email, teléfono y LinkedIn en el bloque `<ul class="pie-contacto">` al final de `index.html`.
- **Botón flotante de WhatsApp:** el enlace `<a class="wa-float">` al final de `index.html`. El número va en la dirección `wa.me/549…` y el mensaje inicial en el parámetro `text` (con %20 por los espacios).
- **Textos de los banners:** bloque `<div class="slides">` en `index.html`.
- **Video e imágenes de los banners:** archivos de `assets/` (mantener los mismos nombres o actualizar las rutas).

## Pendientes antes de campañas pagas
- Política de privacidad (con razón social, CUIT y domicilio) y enlace desde el formulario.
- Medición: pegar Google Tag / Meta Pixel donde dice `COMPLETAR` en el `<head>`.
