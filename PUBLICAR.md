# Cómo publicar Atlas Quirúrgico en GitHub Pages

Al terminar tendrá un enlace como `https://SU-USUARIO.github.io/atlas-quirurgico/` que cualquier médico puede abrir e instalar en su celular. Es gratis.

## Archivos que se suben

Suba solo estos archivos de esta carpeta:

- `index.html`
- `sw.js`
- `manifest.webmanifest`
- `.nojekyll`
- la carpeta `icons` completa

No suba la carpeta `.claude` (son herramientas de prueba) ni `atlas-quirurgico.html` (es la versión anterior, ya incluida en `index.html`).

## Primera publicación (unos 10 minutos)

1. Entre a https://github.com e inicie sesión. Si no tiene cuenta, créela con **Sign up**.
2. Arriba a la derecha, toque **+** y luego **New repository**.
3. En **Repository name** escriba `atlas-quirurgico`, marque **Public** y toque **Create repository**.
4. En la página del repositorio, toque el enlace **uploading an existing file**.
5. Arrastre desde el Explorador de Windows los archivos y la carpeta `icons` listados arriba.
6. Baje y toque **Commit changes**.
7. Vaya a **Settings**, luego a **Pages** en el menú de la izquierda.
8. En **Build and deployment** elija **Source: Deploy from a branch**, **Branch: main**, carpeta **/ (root)**, y toque **Save**.
9. Espere uno o dos minutos y recargue la página de **Pages**. Arriba aparecerá el enlace de su sitio.

## Instalar en el celular

- **Android (Chrome):** abra el enlace y toque **Instalar app**, o abra el menú ⋮ y elija **Instalar aplicación**.
- **iPhone (Safari):** abra el enlace, toque **Compartir** y luego **Agregar a pantalla de inicio**.

La primera vez se necesita internet. Después la app funciona sin conexión.

## Publicar cambios

1. En `sw.js`, cambie la línea `const VERSION = 'v1';` por el número siguiente (`'v2'`, `'v3'`, …). Sin este cambio, los teléfonos seguirán mostrando la versión anterior.
2. En GitHub, entre al repositorio, toque **Add file**, luego **Upload files**, arrastre los archivos modificados y toque **Commit changes**.
3. Quienes ya tengan la app instalada verán el aviso **Hay una versión nueva del Atlas** con el botón **Actualizar**.

## Probar en esta computadora

Desde PowerShell, en esta carpeta:

```
powershell -ExecutionPolicy Bypass -File .claude\serve.ps1 -Root . -Port 8080
```

Luego abra http://localhost:8080 en Edge o Chrome.
