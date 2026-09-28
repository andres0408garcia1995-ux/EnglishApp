# Puente Inglés — cómo obtener el APK

## Qué hay en esta carpeta
- `www/index.html` → la app completa (contenido, lecciones, tutor). Aquí se hacen los cambios.
- `assets/` → icono y pantalla de inicio.
- `package.json` y `capacitor.config.json` → configuración de Android.
- `.github/workflows/build.yml` → la receta que usa GitHub para compilar el APK.

## Pasos
1. Crea una cuenta gratis en github.com.
2. Pulsa "+" → "New repository", ponle de nombre `puente-ingles`, déjalo en Public o Private y pulsa "Create repository".
3. Pulsa "uploading an existing file" y arrastra el contenido de esta carpeta (www, assets, package.json, capacitor.config.json, .gitignore, LEEME.md). Pulsa "Commit changes".
4. Crea la receta de compilación: "Add file" → "Create new file". Como nombre escribe exactamente `.github/workflows/build.yml` y pega dentro el contenido del archivo build.yml de esta carpeta. Pulsa "Commit changes".
5. Ve a la pestaña "Actions". Verás "Construir APK" en marcha (tarda unos 5 minutos). Cuando aparezca el círculo verde, entra y descarga "puente-ingles-apk" al final de la página.
6. Descomprime el zip descargado, pasa `puente-ingles.apk` al teléfono y ábrelo. Android pedirá permitir "instalar apps de origen desconocido": acéptalo para esa instalación.

## Para actualizar la app
Edita `www/index.html` en GitHub (o sube la versión nueva). Cada cambio vuelve a compilar el APK automáticamente. Instálalo encima del anterior: el progreso se conserva.

## Tutor con IA
Dentro del APK, el tutor pide una clave de API de Anthropic (console.anthropic.com). Es opcional: todo lo demás funciona sin ella y sin internet.
