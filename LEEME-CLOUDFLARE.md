# SURCOSSTREAMING — Cloudflare Pages e IMAP

Lee **ACTUALIZAR-ASUNTOS.md** antes de actualizar una instalación existente. Allí encontrarás los archivos exactos y los datos que debes conservar.

Se conserva la configuración propia de este proyecto: diseño, usuarios si existen, administrador, asuntos, buzones, ventana de búsqueda, límites de mensajes y salida de cuerpos/enlaces. No reemplaces datos actuales por archivos iniciales del ZIP.

Build: `npm run build`. Salida: `dist`. Variables: `GITHUB_TOKEN`, `GITHUB_REPO`, `GITHUB_FILE_PATH`, `GITHUB_BRANCH` y `MAILBOX_ENCRYPTION_KEY`. Conserva exactamente la clave de cifrado de Cloudflare. El token debe tener Contents: Read and write para el repositorio de este proyecto.

Los cambios de asuntos se guardan en `lib/mail-rules.js` mediante GitHub y necesitan terminar el despliegue para aplicarse a las búsquedas. El editor administra `codeSubjects` y conserva `linkSubjects`.

La página sigue consultando directamente, sin login de usuarios. El administrador gestiona buzones y asuntos, sin tabla de usuarios ni permisos individuales. Se conservan sus credenciales existentes.

Pruebas: `npm test`. No se han usado credenciales reales ni modificado tu repositorio desde aquí. Comprueba tus consultas reales después de desplegar. No subas node_modules, dist ni secretos al repositorio.
