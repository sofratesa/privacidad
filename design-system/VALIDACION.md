# Validación del hub

14 de octubre de 2026.

- Analizadas y formateadas las cuatro páginas HTML nuevas/modificadas del hub, CSS y SVG con Prettier existente en el espacio de trabajo; no se instalaron dependencias en el sitio.
- Verificadas cinco páginas en español, un h1 por página, IDs únicos y atributos alt.
- Verificados 50 enlaces y recursos locales, incluidas anclas y rutas bajo el prefijo de GitHub Pages `/privacidad/`.
- SVG analizados como XML.
- Confirmado `noindex` en los dos borradores de privacidad.
- Comparado el documento de IRIS con la versión original: solo se añade el enlace de regreso al hub.
- Contraste calculado: texto principal 15.57:1, texto secundario al menos 5.89:1, textos sobre superficies de tarjetas al menos 5.36:1. Azul claro en el título grande: 3.92:1.
- CSS contempla móvil, escritorio, reducción de movimiento, foco visible e impresión. La adaptación visual aún requiere comprobación en navegador.

## Límites de verificación

El entorno restringe sockets y red. El servidor de previsualización no pudo abrir el puerto local; Chromium tampoco pudo arrancar por una restricción del sandbox. No hay capturas ni una comprobación visual ejecutada en navegador. Los enlaces externos y la carga de Google Fonts no se pudieron verificar desde este entorno.

La copia de partida corresponde a `master` del repositorio local `privacidad-iris`, commit `5890580`. No se pudo verificar que coincida con el HEAD remoto; cualquier publicación debe actualizarse sobre el estado remoto y resolver diferencias sin forzar cambios.
