# Políticas de privacidad · Sofratesa

Páginas públicas con las políticas de privacidad de las aplicaciones de
Sofratesa. Existen porque Google Play y App Store exigen una política publicada
en una dirección web accesible sin iniciar sesión, y esa dirección se declara
en la ficha de cada aplicación.

## Cómo está organizado

Un repositorio, una carpeta por aplicación. Un dominio de GitHub Pages solo
puede apuntar a **un** sitio, así que todas las políticas viven aquí y se
distinguen por la ruta:

```
/                → índice con todas las políticas
/iris/           → IRIS (com.sofratesa.iris), mesa de ayuda de TI
```

Para añadir otra aplicación —Tiamat, por ejemplo— se crea `tiamat/index.html`
y se añade su entrada al índice de la portada. Queda publicada en `/tiamat/`
sin tocar nada más.

Cada política es un único archivo HTML sin dependencias, salvo la tipografía
Inter Tight que carga de Google Fonts. La paleta y la tipografía son las del
sistema editorial de la propia aplicación
(`iris_flutter/lib/core/design/editorial_tokens.dart`), para que el documento
se lea como parte de ella.

## Estado: BORRADOR

Ninguno de los documentos es definitivo. Lo resaltado en ámbar son decisiones
que corresponden a la dirección o al área legal de Sofratesa:

- Razón social y domicilio del responsable del tratamiento.
- Correo de contacto para asuntos de datos personales.
- Plazos de conservación de los datos.
- Base legal del tratamiento.
- Plazo de respuesta a las solicitudes de acceso, rectificación o eliminación.

Mientras sigan siendo borradores, las páginas llevan
`<meta name="robots" content="noindex">`. **Quitarlo al publicar la versión
final**, junto con el aviso de borrador y el apartado «Qué falta por decidir»,
que es para uso interno.

## Dominio

Hoy se sirve en `sofratesa.github.io/privacidad/`.

Para pasarlo a `privacidad.sofratesa.com` hace falta un registro DNS en
SiteGround, que es quien gestiona el dominio:

| Tipo | Nombre | Valor |
|---|---|---|
| CNAME | `privacidad` | `sofratesa.github.io.` |

Cuando ese registro resuelva, se configura el dominio en *Settings → Pages* del
repositorio y GitHub emite el certificado HTTPS automáticamente. El dominio ya
está verificado en la organización (registro TXT
`_github-pages-challenge-sofratesa`).

## Dónde se declara cada dirección

Cuando una política sea definitiva, su URL va en dos sitios:

1. **Play Console** → Política y programas → Contenido de la app → política de
   privacidad.
2. **La propia aplicación**, si se añade el enlace en ajustes.
