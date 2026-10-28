# NexoX

Blog en español con Astro, Decap CMS y despliegue estático en Netlify.

## Desarrollo

Requiere Node.js 22. Ejecutar `npm install` y `npm run dev`. Para generar el sitio: `npm run build`.

## Netlify

Importar el repositorio `WaPeR/NexoX` en Netlify y seleccionar la rama `main`. El archivo netlify.toml configura la construcción y la carpeta dist. Las modificaciones en main activarán despliegues una vez conectado el repositorio.

## Panel editorial

Ruta: `/admin/`. El panel guarda artículos en src/content/reviews e imágenes en public/images/uploads. Los borradores no se publican en el sitio. Para publicar, desactivar Borrador y guardar/publicar desde Decap.

IMPORTANTE: el inicio de sesión de Decap no está listo solo con estos archivos. Hay que configurar OAuth de GitHub para el sitio en Netlify (o un proveedor OAuth compatible con Decap) y autorizar el acceso al repositorio. No pegar contraseñas, tokens ni secretos en el repositorio. Si se usa un proveedor externo, ajustar base_url y auth_endpoint del backend según su documentación.

La apariencia del panel de edición no reproduce necesariamente el diseño público: no hay previsualización personalizada configurada.

## Estado inicial

Incluye una entrada de bienvenida, no una review real. La construcción y el acceso al panel deben verificarse en el primer despliegue. No se ha configurado dominio propio, analítica, comentarios ni publicidad. Las dependencias usan rangos de versión; conviene guardar el package-lock.json generado al validar la instalación.
