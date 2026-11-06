# groundster-updates

Canal de distribución de las actualizaciones del kiosco Groundster.

- `ota/manifest.json` — qué versión debe correr la flota. Los equipos lo leen por
  `raw.githubusercontent.com`, sin credencial.
- Los APK van como *release assets* de este repositorio, no versionados.

Este repositorio **tiene que seguir siendo público**: los equipos no llevan ningún token, así que uno
privado les responde 404 y la flota deja de actualizarse.

No hay secretos aquí. Lo que protege a la flota es la llave de firma — Android rechaza un APK firmado
con otro certificado — más el `sha256` del manifiesto. Ver `docs/actualizaciones.md` §7 en el
repositorio del código.

Se publica con `tools/release.py` desde el repositorio del código.
