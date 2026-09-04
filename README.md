# Política de privacidad de IRIS

Página pública con la política de privacidad de la aplicación móvil IRIS
(`com.sofratesa.iris`). Existe porque Google Play exige una política publicada
en una dirección web accesible sin iniciar sesión, y esa dirección se declara
tanto en la consola de Play como dentro de la aplicación.

Es un solo archivo, `index.html`, sin dependencias más allá de la tipografía
Inter Tight que carga de Google Fonts. La paleta y la tipografía son las de
`iris_flutter/lib/core/design/editorial_tokens.dart`, para que el documento se
lea como parte de la aplicación.

## Estado: BORRADOR

El documento **no es definitivo**. Lo resaltado en ámbar son decisiones que
corresponden a la dirección o al área legal de Sofratesa:

- Razón social y domicilio del responsable del tratamiento.
- Correo de contacto para asuntos de datos personales.
- Plazos de conservación de los tickets, de las imágenes adjuntas y de los
  registros técnicos.
- Base legal del tratamiento.
- Plazo de respuesta a las solicitudes de acceso, rectificación o eliminación.

Mientras siga siendo un borrador, `index.html` lleva una etiqueta
`<meta name="robots" content="noindex">`. **Quítala al publicar la versión
final**, junto con el aviso de borrador y el apartado 13 («Qué falta por
decidir»), que es para uso interno.

## Cómo publicarlo

Con el repositorio ya creado y el contenido subido:

1. En GitHub, entra en **Settings → Pages**.
2. En *Source* elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`.
3. Guarda. En un minuto la página queda en la URL que muestra esa misma
   pantalla.

Ten en cuenta que **GitHub Pages sirve el contenido públicamente** aunque el
repositorio fuese privado (para servir Pages desde un repositorio privado hace
falta un plan de pago). Cualquiera con la dirección puede leer la página.

## Dónde se declara la dirección

Cuando la URL sea definitiva hay que ponerla en dos sitios:

1. **Play Console** → Política y programas → Contenido de la app → política de
   privacidad.
2. **La aplicación**, en la pantalla de ajustes, si se añade el enlace.

Si la política se traslada más adelante a la web corporativa, hay que
actualizar los dos.
