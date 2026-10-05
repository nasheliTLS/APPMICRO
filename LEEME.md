# Tabla Nutricional Perú – App Android

App sin internet con los 1,534 registros del Excel (buscador por código o nombre, grupos, ficha por porción, favoritos).

## Opción A: sin instalar nada (GitHub, ~5 min)
1. Crea una cuenta en github.com (gratis) y luego un repositorio nuevo (botón **New**).
2. En el repo: **Add file → Upload files** y arrastra TODO el contenido de esta carpeta (no la carpeta en sí). Pulsa **Commit changes**.
   - Si la carpeta `.github` no se subió (a veces se ocultan), ve a **Actions → set up a workflow yourself**, pega el contenido de `.github/workflows/build-apk.yml` y guarda.
3. Ve a la pestaña **Actions**: verás "Construir APK" ejecutándose (3-5 min).
4. Cuando tenga ✔ verde, entra a la ejecución y descarga **TablaNutricional-APK** (es un .zip con `app-debug.apk`).
5. Pasa el `.apk` al celular/tablet, ábrelo y acepta "instalar apps de origen desconocido".

## Opción B: Android Studio
1. Instala Android Studio (developer.android.com/studio).
2. **File → Open** y elige esta carpeta. Espera a que termine "Gradle sync".
3. **Build → Build App Bundle(s) / APK(s) → Build APK(s)**.
4. El APK queda en `app/build/outputs/apk/debug/app-debug.apk`.

(Visual Studio Code no sirve para generar el APK; Android Studio sí.)

## Actualizar los datos
Reemplaza `app/src/main/assets/index.html` por una versión nueva y vuelve a construir.
