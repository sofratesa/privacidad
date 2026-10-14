# IRIS · Evidencia de la política de privacidad

Revisión del 14 de octubre de 2026. Alcance limitado a IRIS por instrucción del usuario.

## Qué se revisó

Revisión por flujos de datos de cliente Flutter, servicio de soporte IRIS, gateway, identidad Janus, notificaciones Hermes y módulos de inventario/mantenimiento Hefesto que consume IRIS. Se contrastaron campos persistidos, transportes, permisos, copias de información, integraciones y operaciones de baja. No es una lectura exhaustiva de cada línea ni una prueba de la configuración en producción.

El MCP Graphify exigido por las reglas del ecosistema no estaba disponible en la sesión. Se consultó primero su grafo local `graphify-out/graph.json` y después las fuentes actuales: el grafo era anterior a cambios relevantes y referenciaba, por ejemplo, un clasificador Gemini que ya fue sustituido por TypeSafe.

## Copias locales

| Repositorio | HEAD | Cambios locales |
| --- | --- | --- |
| `iris_flutter` | `0e1b50d` | 34 entradas de estado |
| `iris` | `f6c3c0d` | 5 entradas de estado |
| `iris-api-gateway` | `5f52489` | 0 entradas de estado |
| `janus-iam-service` | `db15685` | 69 entradas de estado |
| `hermes-notification-service` | `b9f0872` | 0 entradas de estado |
| `hefesto_backend` | `4eee097` | 12 entradas de estado |

La revisión utiliza los archivos actuales, incluidos cambios locales sin publicar. Los hashes de la tabla siguiente identifican las fuentes consultadas; los SHA de HEAD por sí solos no describen todos esos archivos.

## Evidencias

| Hecho | Fuente y línea | SHA-256 (prefijo) |
| --- | --- | --- |
| Identificador Android actual | `iris_flutter/android/app/build.gradle.kts:45` | `489be86dcee31aba` |
| Permisos y retirada de lectura general de medios | `iris_flutter/android/app/src/main/AndroidManifest.xml:31` | `d22b45bff50ef1b0` |
| Permiso de cámara y Face ID en iOS | `iris_flutter/ios/Runner/Info.plist:17` | `c33ca95a07df5adb` |
| Dependencias del cliente y ausencia de SDK publicitario | `iris_flutter/pubspec.yaml:60` | `8288568e419162e0` |
| Campos de perfil leídos por IRIS | `iris_flutter/lib/features/auth/infrastructure/models/user_model.dart:40` | `4ca66ab8e21d41bb` |
| Documento de identidad en la administración de cuentas | `iris_flutter/lib/features/admin/users/presentation/widgets/detalle_de_usuario_dialog.dart:126` | `87a44fe8ded83e51` |
| Cuenta, identificación, permisos y seguridad de identidad | `janus-iam-service/src/features/users/domain/entities/user.entity.ts:25` | `04e25e9ba235ba06` |
| Tokens y petición de revocación al cerrar sesión | `iris_flutter/lib/features/auth/infrastructure/repositories/auth_repository_impl.dart:107` | `2f1e8d1806335b74` |
| Desbloqueo mediante el sistema, sin plantillas biométricas | `iris_flutter/lib/features/auth/infrastructure/biometria/desbloqueo_biometrico_local_auth.dart:34` | `fe2648910eafb5e9` |
| Datos locales para volver a abrir una sesión guardada | `iris_flutter/lib/features/auth/infrastructure/sesion/sesion_para_huella_segura.dart:11` | `35c4e39ff13c87ac` |
| Contenido del ticket, tiempos y desactivación | `iris/src/features/tickets/domain/entities/ticket.entity.ts:9` | `be81a532bf9c567a` |
| Permisos y alcance real de lectura del ticket | `iris/src/features/tickets/application/services/ticket-access.service.ts:29` | `78811bab447a7e3b` |
| Mensajes, lectura, edición y extractos de respuestas | `iris/src/features/ticket-notes/domain/entities/ticket-note.entity.ts:69` | `57402455443116e2` |
| Calificación y comentario ligados al usuario y ticket | `iris/src/features/satisfaccion/domain/entities/encuesta-satisfaccion.entity.ts:19` | `8c78045b57098765` |
| Envíos sin firma siguen conservando sede y departamento | `iris/src/features/sugerencias/application/use-cases/enviar-sugerencia.use-case.ts:59` | `4a917bf397aa0da1` |
| Copia de solicitante e hilo al compartir una solución | `iris/src/features/conocimiento/application/use-cases/compartir-solucion.use-case.ts:140` | `e0cfd2120056dc3d` |
| Acceso a la base de conocimiento por permiso específico | `iris/src/features/conocimiento/interface/controllers/conocimiento.controller.ts:50` | `40179d9f10692f95` |
| Datos personales en exportación del soporte | `iris/src/features/exports/application/services/support-anual-sheet.builder.ts:43` | `82ec7cbddcabfd10` |
| Selección real de almacenamiento, dependiente de instalación | `iris/src/features/ticket-attachments/infrastructure/adapters/file-storage.provider.ts:8` | `ef84ddf36422c58c` |
| Objetos nuevos con acceso autenticado en Cloudinary | `iris/src/features/ticket-attachments/infrastructure/adapters/cloudinary.adapter.ts:76` | `a645ab1cb5155928` |
| Borrado del archivo y baja lógica del adjunto | `iris/src/features/ticket-attachments/application/use-cases/delete-attachment.use-case.ts:34` | `a1b0994b540a031d` |
| Excepción de adjuntos antiguos con URL pública | `iris/src/features/ticket-attachments/application/use-cases/resolve-attachment-url.use-case.ts:44` | `2d21ef9957db9697` |
| La optimización no elimina metadatos en todos los caminos | `iris/src/features/ticket-attachments/infrastructure/adapters/sharp-image-optimizer.adapter.ts:60` | `454f0610b3eedbc2` |
| Alta, baja y preferencias de push Android | `iris_flutter/lib/core/notificaciones/avisos_push.dart:169` | `e075a863a2f6b269` |
| Inicialización de Firebase al entrar al espacio de trabajo | `iris_flutter/lib/features/tickets/presentation/widgets/shared/workspace_shell.dart:121` | `74d688c4341633b3` |
| Datos almacenados del dispositivo de notificaciones | `hermes-notification-service/src/features/notifications/infrastructure/database/mongoose/push-token.schema.ts:19` | `49ea47cde09343f6` |
| Título, cuerpo y datos de apertura enviados a FCM | `hermes-notification-service/src/features/notifications/infrastructure/adapters/fcm-push.adapter.ts:109` | `0dfdf57599faff29` |
| Destinatarios, asunto y contenido enviados por SMTP | `hermes-notification-service/src/features/notifications/infrastructure/adapters/email.adapter.ts:51` | `1167babb505675b4` |
| IP y agente de usuario de la sesión | `janus-iam-service/src/features/users/infrastructure/database/typeorm/refresh-token.typeorm-entity.ts:52` | `9d973d620c42ead0` |
| Cookies de autenticación web y control CSRF | `janus-iam-service/src/shared/http/auth-cookies.ts:46` | `cd653cf3b3eb5057` |
| La baja de cuenta conserva el usuario y revoca sesiones | `janus-iam-service/src/features/users/application/use-cases/deactivate-user.use-case.ts:68` | `2b4c22d7da05f438` |
| Registro de auditoría y ocultación de campos sensibles | `iris/src/features/audit/domain/services/redactar-datos-sensibles.ts:23` | `1879e4cd998a4eb3` |
| Método, ruta, estado y duración de solicitudes en el gateway | `iris-api-gateway/src/middleware/request-logging.middleware.ts:20` | `b4c2ba612df25495` |
| Responsable de equipo y sus asignaciones históricas | `hefesto_backend/src/features/equipos/domain/entities/asignacion-equipo.entity.ts:12` | `e608554a9d2e47b1` |
| Carga de actas en el cliente | `iris_flutter/lib/features/mantenimientos/infrastructure/datasources/importacion_actas_remote_data_source.dart:41` | `1092fb34af250c2d` |
| Texto, capturas y datos extraídos de actas; propuestas a confirmar | `hefesto_backend/src/features/mantenimientos/application/use-cases/procesar-acta-importada.use-case.ts:170` | `b89f02b2710449aa` |
| TypeSafe recibe texto, equipos y datos de candidatos cuando se habilita | `hefesto_backend/src/features/mantenimientos/infrastructure/ai/jev-juez-actas.ts:32` | `bfd1a2d16a36f3e2` |

## Decisiones del texto

- Identificador Android corregido a `com.sofratesa.iris_app`, según el archivo Gradle; el documento anterior usaba `com.sofratesa.iris`. La URL `/iris/` permanece estable.
- `support@sofratesa.com` fue aportado y confirmado por el usuario como canal de consultas sobre datos personales.
- SOFRATESA se identifica como operador de la aplicación. No se inventó una razón social registrada, domicilio legal o base jurídica aplicable a todos los países.
- Se describe la baja lógica de cuentas, tickets y mensajes. No se promete borrado inmediato, anónimo o automático a una fecha ficticia.
- Cloudinary y R2 se describen como alternativas configurables; no se afirma que todas estén activas. TypeSafe se explica como integración opcional.
- No se afirma que todas las imágenes sean privadas: el código conserva el camino de URL pública para adjuntos históricos.
- Se advierte que el buzón sin firma conserva sede/departamento y no garantiza anonimato absoluto.
- No se garantiza borrado de metadatos en todas las imágenes, ni eliminación de identificadores Firebase por apagar avisos.
- La política de Cronos y su ficha no se modificaron.

## Fuentes primarias externas

- [Google Play: datos de usuario y contenido de la política](https://support.google.com/googleplay/android-developer/answer/10144311?hl=es).
- [Firebase: privacidad y datos de Cloud Messaging](https://firebase.google.com/support/privacy).
- [FCM: inicialización y datos de instalación](https://firebase.google.com/docs/cloud-messaging/android/get-started).
- [TypeSafe: privacidad](https://typesafe.ai/legal/privacy-policy).
- [GitHub: privacidad](https://docs.github.com/es/site-policy/privacy-policies/github-general-privacy-statement).
- [Google Fonts: privacidad](https://developers.google.com/fonts/faq/privacy).

## Límites

No se inspeccionaron cuentas, actas o tickets reales ni se accedió a secretos, archivos de entorno o infraestructura. No se pudo conectar con el despliegue para confirmar proveedores activos, copias de seguridad, países de alojamiento, TLS o plazos corporativos. La política no certifica cumplimiento legal ni sustituye esas comprobaciones operativas; tampoco atribuye a la empresa garantías no acreditadas.

No se modificó el código de las aplicaciones. Las comprobaciones de entrega corresponden únicamente al sitio estático de privacidad; no se ejecutaron las baterías Flutter/NestJS de otros repositorios.
