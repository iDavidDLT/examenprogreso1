# Hosting Shop

Página de recursos para anfitriones construida con HTML y SCSS. Se adapta a distintos tamaños de pantalla y muestra un efecto al pasar el puntero sobre las imágenes de Essentials. Las imágenes de Template Library permanecen estáticas.

## Abrir el proyecto

1. Abre **Visual Studio Code**, el editor de icono azul.
2. Selecciona **Archivo > Abrir carpeta** y abre `C:\Users\ASUS\hosting-shop`.
3. Abre `index.html` en el navegador. Si usas la extensión Live Server, haz clic derecho en `index.html` y elige **Open with Live Server**.

El CSS compilado ya está incluido en `css/main.css`, así que puedes visualizar la página sin ejecutar comandos.

## Trabajar con SCSS y Live Sass Compiler

1. Instala o habilita la extensión **Live Sass Compiler** en Visual Studio Code.
   Si VS Code abre la carpeta en modo restringido, debes confiar en esta carpeta desde el aviso del editor para habilitar la extensión.
2. Abre `scss/main.scss` y pulsa **Watch Sass** en la barra inferior, o ejecuta **Live Sass: Watch Sass** desde la paleta (`Ctrl+Shift+P`).
3. Edita y guarda el archivo de la sección que quieras modificar dentro de `scss/`. La configuración indica a la extensión que compile `scss/main.scss` y guarde el resultado en `css/main.css`. Comprueba que el archivo CSS se actualice después de guardar: la compilación automática aún no se ha podido verificar en esta instalación.
4. Para detener la compilación automática pulsa **Stop Watching Sass**.

Modifica los archivos SCSS y no `css/main.css`, ya que el compilador sobrescribe el CSS generado. La ubicación de salida y el formato están configurados en `.vscode/settings.json`.

## Estructura del proyecto

- `index.html`: estructura y contenido de la página; carga `css/main.css`.
- `scss/main.scss`: reúne los archivos parciales de estilos con `@use`.
- `scss/_variables.scss`: colores compartidos.
- `scss/_base.scss`: estilos generales y contenedor.
- `scss/_header.scss`: encabezado, navegación y carrito visual.
- `scss/_essentials.scss`: buscador visual, galería y efecto de Essentials.
- `scss/_template-library.scss`: tarjetas de Template Library.
- `scss/_footer.scss`: pie de página.
- `scss/_responsive.scss`: reglas para diferentes tamaños de pantalla y movimiento reducido.
- `css/main.css`: CSS compilado que lee el navegador.
- `assets/`: imágenes del diseño.

Los parciales comienzan con `_` porque Sass los incorpora desde `main.scss` en lugar de generar un CSS independiente para cada uno. Se usan Flexbox, CSS Grid y media queries para la distribución. El buscador, el carrito, el menú y las políticas son elementos visuales; las imágenes de Essentials muestran su efecto al pasar el cursor o enfocarlas con el teclado.
