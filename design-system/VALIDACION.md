# Validación del hub

14 de octubre de 2026. Esta primera sección corresponde a la entrega inicial del hub (`8af3793`). La ampliación de IRIS se detalla al final.

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

## Ampliación: privacidad de IRIS

- Política de IRIS reescrita tras revisar los flujos de datos de cliente, soporte, identidad, notificaciones, gateway y mantenimiento. Fuentes y límites: `IRIS-PRIVACIDAD-EVIDENCIA.md`.
- Diseño unificado con el hub; navegación, tipografía, colores y hoja de estilos compartidos. Índice con doce secciones y contacto confirmado.
- Verificadas las cinco páginas del sitio y 73 enlaces/recursos locales, incluidas anclas y rutas de GitHub Pages.
- Verificados contacto `support@sofratesa.com`, identificador `com.sofratesa.iris_app`, h1 único, español, IDs únicos y atributos alt.
- IRIS no lleva aviso de borrador ni `noindex`. Cronos conserva `noindex`; sus dos páginas coinciden exactamente con las del commit anterior.
- HTML y CSS analizados y formateados con Prettier; `git diff --check` sin errores.
- Los textos nuevos usan los pares de colores ya comprobados en el hub. El índice fijo se desactiva tanto en móvil como en ventanas bajas.
- Se mantiene el límite de comprobación visual: este entorno no permite arrancar el navegador ni abrir un servidor local. No se ejecutó una validación visual en navegador ni una prueba contra los servicios de producción.
