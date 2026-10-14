# Aplicaciones SOFRATESA

Hub público de aplicaciones, servido en https://sofratesa.github.io/privacidad/ con GitHub Pages.

## Rutas

| Ruta | Contenido |
| --- | --- |
| `/` | Catálogo de aplicaciones IRIS y Cronos |
| `/aplicaciones/iris/` | Ficha de IRIS |
| `/aplicaciones/cronos/` | Ficha de Cronos |
| `/iris/` | Política de IRIS existente, en borrador |
| `/cronos/` | Privacidad de Cronos, en borrador |

La ruta `/iris/` se conserva para los enlaces que ya la usan. Las fichas son públicas; el uso de cada aplicación requiere autorización de SOFRATESA. No se anuncian enlaces de descarga hasta confirmar las direcciones públicas.

## Diseño y ejecución

HTML y CSS, sin compilación ni dependencias JavaScript. La portada y las páginas nuevas usan Nunito Sans de Google Fonts, con tipografía del sistema como alternativa sin red. Los logotipos se sirven localmente. La política existente de IRIS conserva Inter Tight y su contenido.

La identidad se basa en el manual de SOFRATESA proporcionado: colores corporativos, logotipo y tipografía de comunicación. Las decisiones están en `design-system/SOFRATESA.md`; se aplicó la skill UI/UX Pro Max 2.13.0.

Para previsualizar desde la raíz del repositorio:

```sh
python3 -m http.server 8080 --bind 127.0.0.1
```

Abrir http://127.0.0.1:8080/. En GitHub Pages, publicar la raíz de la rama `master`, como en la configuración existente. Los enlaces relativos también funcionan bajo `/privacidad/`.

## Privacidad: borradores

Los documentos de privacidad no son políticas vigentes. IRIS conserva sus datos pendientes y Cronos tiene un borrador basado en su documentación técnica, con revisión técnica y legal pendiente. Ambos documentos llevan `noindex`.

Antes de aprobarlos se deben confirmar responsable y domicilio, contacto, inventario de datos, fundamento del tratamiento, proveedores y alojamiento, conservación y eliminación, gestión de solicitudes y fecha de vigencia. El formulario de Seguridad de los datos debe validarse con la versión real de cada app.

Al aprobar una política, actualizar su contenido y fecha, retirar el aviso de borrador y `noindex`, y actualizar el estado de la portada y su ficha. No retirar estos avisos solo por desplegar el diseño.

## Añadir una aplicación

Crear su ficha en `aplicaciones/<nombre>/index.html`, su documento en `<nombre>/index.html` y su tarjeta en la portada. Reutilizar `assets/site.css`, mantener los enlaces relativos y dar un nombre accesible a cada enlace. Añadir acceso o descarga solo con una URL pública confirmada.
