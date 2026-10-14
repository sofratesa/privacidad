# SOFRATESA · Hub de aplicaciones

## Fuente y decisiones

Se aplicó UI/UX Pro Max 2.13.0, consulta `enterprise application directory minimal --design-system`. El resultado de directorio y diseño plano corresponde al catálogo. Sus recomendaciones de verde e Inter se sustituyen por la identidad aportada por el usuario.

- Manual: Presentación Manual de Identidad Visual - SOFRATESA (V1) ALP, páginas 3, 4 y 9–11.
- Colores corporativos: azul #001D61, azul claro #0181C9 y gris #D1D2D4. Fondos y bordes derivados para lectura.
- Nunito Sans para la comunicación web; el manual reserva Rileno Sans Medium a títulos de documentos. No se incluyen archivos de fuentes comerciales extraídos del PDF.
- Logotipo corporativo existente, sin redibujar. IRIS conserva su marca de arcos; Cronos utiliza el icono PNG de 512 × 512 aportado por el usuario, servido localmente como `assets/cronos.png`.
- Portada: introducción, catálogo de dos aplicaciones, estado de privacidad y firma corporativa. Sin buscador innecesario para dos entradas.
- Fichas públicas; uso de las aplicaciones con cuenta autorizada. No se anuncian descargas sin enlace confirmado.
- HTML y CSS estáticos. Enlaces relativos compatibles con el prefijo /privacidad/ de GitHub Pages.
- Foco visible, salto al contenido, navegación semántica, enlaces con nombre único, contraste, adaptación móvil y reducción de movimiento.

## Contenido

IRIS: texto de la política existente. Cronos: README, ADR-004, ADR-008, ADR-009, ADR-018, ADR-019 y reportes de septiembre de 2026 del repositorio Documentacion-proyectos.
La privacidad de Cronos publica el texto final aportado por el usuario, con fecha del 13 de octubre de 2026 y sin avisos de borrador.

## Privacidad de IRIS · 14 de octubre de 2026

IRIS usa ahora `assets/site.css`, la cabecera y el pie del hub, Nunito Sans, una introducción con ficha de contacto y un índice de doce secciones. En móvil el índice pasa al flujo normal; en ventanas bajas no queda fijo. El texto se reescribió a partir de la revisión por flujos de datos del cliente y sus servicios. El contacto confirmado es `contactos@sofratesa.com`. Las fuentes y límites están en `IRIS-PRIVACIDAD-EVIDENCIA.md`. Cronos conserva su estado y su contenido.

## Privacidad final de Cronos

La página `/cronos/` comparte cabecera, pie, tipografía, ficha de contacto, índice y clases de documento con IRIS. Se utiliza el icono PNG aportado por el usuario y se conservan el texto final y sus nueve apartados. La dirección, el correo y la fecha corresponden al texto recibido. Se retiraron `noindex` y los avisos de borrador del contenido, la ficha y el hub.
