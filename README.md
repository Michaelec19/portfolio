# Portafolio — Michael Espinal Cardona

Sitio estático: HTML + CSS + JS + Bootstrap 5 (sin build, sin instalación).

## Estructura

```
index.html          ← estructura de todas las secciones
css/style.css        ← tema visual sobre Bootstrap (colores, tipografía, motivo pixel)
js/data.js            ← todo el contenido (perfil, stack, experiencia, proyectos, estudios)
js/main.js            ← arma el DOM a partir de data.js
assets/
  favicon.svg
  img/
    profile.jpg               ← foto de portada (provisional)
    projects/lanhua.jpg       ← vista previa del proyecto (provisional)
    logos/generation.png      ← logo de la institución (provisional)
    logos/sena.png
    logos/jala.png
```

Convención interna: variables, funciones, ids y clases usan el prefijo `me`
(`meProfile`, `me-hero`, `#meStackGrid`...). Es solo una firma en el código,
no aparece como texto visible para quien visita el sitio.

## Cómo verlo

No necesita instalación. Dos formas:

1. **Directo**: doble clic en `index.html` y se abre en el navegador.
2. **Con servidor local** (recomendado, evita problemas de rutas):
   ```bash
   npx serve .
   ```
   o, si tienes Python:
   ```bash
   python3 -m http.server 8000
   ```
   y abres `http://localhost:8000`.

Necesitas conexión a internet al verlo: Bootstrap, los íconos y las fuentes
se cargan desde CDN.

## Reemplazar las imágenes provisionales

Todas están marcadas con su texto ("FOTO", "VISTA", "LOGO..."). Para poner
las reales, **reemplaza el archivo manteniendo el mismo nombre y ruta**:

- `assets/img/profile.jpg` → tu foto
- `assets/img/projects/lanhua.jpg` → captura del proyecto
- `assets/img/logos/generation.png`, `sena.png`, `jala.png` → logos de cada institución

No hace falta tocar el HTML ni el JS.

## Otros ajustes pendientes

- En `js/data.js`: reemplaza `linkedin` y `cvUrl` con tus enlaces reales.
- Los logos del stack (Java, Spring, Docker, etc.) vienen de devicon vía CDN;
  si quieres cambiarlos, edita el campo `icon.src` de cada item en `meStack`.
