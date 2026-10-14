# Aplicaciones SOFRATESA

Hub público de aplicaciones, servido en https://sofratesa.github.io/privacidad/ con GitHub Pages.

## Rutas

| Ruta | Contenido |
| --- | --- |
| `/` | Catálogo de aplicaciones IRIS y Cronos |
| `/aplicaciones/iris/` | Ficha de IRIS |
| `/aplicaciones/cronos/` | Ficha de Cronos |
| `/iris/` | Política de privacidad de IRIS basada en la revisión del código |
| `/cronos/` | Política de privacidad final de Cronos |

La ruta `/iris/` se conserva para los enlaces que ya la usan. Las fichas son públicas; el uso de cada aplicación requiere autorización de SOFRATESA. No se anuncian enlaces de descarga hasta confirmar las direcciones públicas.

## Diseño y ejecución

HTML y CSS, sin compilación ni dependencias JavaScript. La portada y las páginas nuevas usan Nunito Sans de Google Fonts, con tipografía del sistema como alternativa sin red. Los logotipos se sirven localmente. La política de IRIS utiliza la misma identidad y navegación del hub, con un índice de secciones.

La identidad se basa en el manual de SOFRATESA proporcionado: colores corporativos, logotipo y tipografía de comunicación. Las decisiones están en `design-system/SOFRATESA.md`; se aplicó la skill UI/UX Pro Max 2.13.0.

Para previsualizar desde la raíz del repositorio:

```sh
python3 -m http.server 8080 --bind 127.0.0.1
```

Abrir http://127.0.0.1:8080/. En GitHub Pages, publicar la raíz de la rama `master`, como en la configuración existente. Los enlaces relativos también funcionan bajo `/privacidad/`.

## Privacidad

IRIS tiene una política descriptiva basada en la revisión del cliente Flutter y sus servicios de soporte, identidad, notificaciones y mantenimiento. El contacto `contactos@sofratesa.com` fue confirmado por el responsable de la tarea. No se inventan razón social registrada, país de alojamiento, plazos de borrado ni garantías generales de privacidad de los adjuntos.

Las comprobaciones y límites de la revisión están en `design-system/IRIS-PRIVACIDAD-EVIDENCIA.md`. El texto describe lo implementado en las copias locales del código; no certifica configuración de producción, cumplimiento normativo o coincidencia con el binario distribuido. Se actualiza cuando cambian las funciones o el tratamiento de datos.

Cronos publica el texto final aportado por el usuario, con fecha de actualización del 13 de octubre de 2026. Se conservaron sus nueve apartados y su redacción; se retiraron los avisos de borrador y `noindex` de la página, y se actualizó su estado en la ficha y el hub. La copia del texto está en `design-system/CRONOS-POLITICA-FINAL.txt`. Esta actualización es de contenido y diseño; no incorpora una auditoría del código de Cronos.

## Añadir una aplicación

Crear su ficha en `aplicaciones/<nombre>/index.html`, su documento en `<nombre>/index.html` y su tarjeta en la portada. Reutilizar `assets/site.css`, mantener los enlaces relativos y dar un nombre accesible a cada enlace. Añadir acceso o descarga solo con una URL pública confirmada.
