# QR Studio

**Abrir la app:** https://isaacan123.github.io/qr-studio/

Generador de códigos QR personalizados: menú de enlaces con logo, 16 tipos de QR, diseño propio (formas, esquinas, colores, marcos, logo de fondo), contraseña y programación por fechas.
Funciona en celulares, tablets y laptops, y no necesita servidor ni instalar nada: todo corre en el navegador.

## Publicarlo en GitHub Pages (5 minutos)

1. **Crea el repositorio.** En GitHub ve a **New repository**, ponle de nombre `qr-studio`, márcalo como **Public** y crea el repositorio.
2. **Sube los archivos.** En el repositorio nuevo, entra a **Add file → Upload files** y arrastra **todo el contenido** de esta carpeta (incluida la carpeta `q`, la carpeta `img` y el archivo `.nojekyll`). Confirma con **Commit changes**.
   > Si tu sistema oculta el archivo `.nojekyll`, no pasa nada: todo funciona igual sin él.
3. **Activa Pages.** Entra a **Settings → Pages**. En **Source** elige **Deploy from a branch**, en **Branch** elige `main` y `/ (root)`, y presiona **Save**.
4. **Espera 1 o 2 minutos** y abre `https://TU-USUARIO.github.io/qr-studio/`.

La dirección para publicar tus QR (base_url) se configura sola como `https://TU-USUARIO.github.io/qr-studio/q`.
El QR de ejemplo **"Sustentabll · enlaces"** ya tiene su página en `q/sustentabll/`, así que puedes escanearlo desde el primer momento.

## Uso diario

1. Abre tu sitio y crea los QR en **+ Nuevo QR** (elige el tipo, el contenido y el diseño).
2. En **Mis QRs** presiona **Exportar todo (ZIP)** y descomprime el archivo.
3. En GitHub entra a **Add file → Upload files**, arrastra la carpeta **`q`** del ZIP y confirma con **Commit changes**.
4. Espera 1 o 2 minutos, escanea cada QR con tu celular y luego imprime (los PNG y SVG están en la carpeta `qrs` del ZIP).

Para cambiar un enlace después de imprimir: edita el QR, vuelve a exportar y vuelve a subir la carpeta `q`. **El QR impreso no cambia.**

## Instalarlo como app en el celular o la tablet

- **iPhone / iPad (Safari):** botón Compartir → **Agregar a inicio**.
- **Android (Chrome):** menú ⋮ → **Instalar app** o **Agregar a la pantalla principal**.

## Importante

- **Tus QR se guardan en el navegador donde los creas.** Para pasarlos a otra computadora o celular usa **Mis QRs → Descargar respaldo** y luego **Importar respaldo** en el otro equipo. El ZIP exportado también incluye `respaldo.json`.
- **No cambies el nombre del repositorio ni la dirección de una página** (`q/nombre`) después de imprimir el QR, o ese QR dejará de funcionar.
- **Contraseña:** el contenido de esas páginas se publica cifrado (AES-256) y solo se ve con la contraseña. GitHub Pages usa `https://`, que es necesario para que funcione.
- **Repositorio público:** en GitHub Pages gratis el repositorio es público, así que cualquiera puede ver los archivos que subes. Las páginas con contraseña siguen protegidas porque están cifradas.
- **Límite de escaneos y estadísticas:** necesitan un servidor; GitHub Pages solo sirve páginas estáticas, así que no están incluidos.
- **Tipos de QR sin página:** WiFi, Email, SMS y vCard directa llevan los datos dentro del código y funcionan sin publicar nada.

## Estructura

```
index.html            la aplicación QR Studio
manifest.webmanifest  para instalarla como app
img/                  iconos
q/                    páginas publicadas de tus QR (una carpeta por QR)
404.html              aviso cuando un QR aún no tiene página
.nojekyll             le indica a GitHub Pages que publique los archivos tal cual
```
