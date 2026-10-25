# SICLER Rural · Guardianes de la lectura

Sitio web estático, adaptable a celulares, preparado para **GitHub Pages**. No requiere PHP, compilación, CDN ni dependencias externas.

## Publicar en GitHub Pages

1. Crea un repositorio público, por ejemplo `sicler-lectura`.
2. Sube **los archivos que están dentro de esta carpeta**, directamente a la raíz del repositorio. No subas la carpeta contenedora como un nivel adicional.
3. En GitHub, ve a **Settings → Pages → Build and deployment → Deploy from a branch**.
4. Selecciona `main` y `/(root)`, y guarda.
5. La dirección suele ser `https://TU-USUARIO.github.io/sicler-lectura/`. GitHub la mostrará en Settings → Pages.
6. Abre la web desde tu celular y concede el permiso de cámara si deseas utilizar el reconocimiento de marcadores.

## Imprimir tarjetas

Abre `https://TU-USUARIO.github.io/sicler-lectura/tarjetas.html`, pulsa **Imprimir tarjetas**, usa impresión a color y papel mate. Son diez reconocimientos, códigos `SA-04-001` a `SA-04-010`, sin nombres ni calificaciones. Cada color activa uno de los tres mundos.

## Cómo se usa

- Entra al sitio y toca una de las tres aventuras; esta es la modalidad más fiable.
- Opcional: **Explorar una tarjeta con mi cámara** y apunta el centro de la guía al cuadro **verde / azul / morado** de la tarjeta. Es un prototipo de reconocimiento por color, no un sistema de seguimiento espacial 3D. Evita luces de colores y fondos saturados.
- Lee el relato, responde una pregunta y gana una estrella. Si falla, recibe una pista y puede intentarlo otra vez.
- La voz se activa con el botón de la esquina superior; depende de las voces instaladas en el dispositivo.
- Las estrellas se guardan en el navegador del dispositivo; no se registran datos personales ni hay cuentas o rankings.

## Sin conexión

La primera visita requiere internet para abrir GitHub Pages. Cuando el navegador guarda los recursos mediante el service worker, las visitas posteriores pueden funcionar offline **en ese mismo dispositivo**, sujeto a las políticas de almacenamiento del navegador. La cámara desde GitHub Pages normalmente funciona porque usa HTTPS. Si se borra el caché, será necesaria otra visita online.

## Límites

- La experiencia es una **superposición educativa activada por color**, no RA 3D anclada espacialmente.
- La precisión varía según luz/cámara; siempre existe el acceso manual.
- La impresión usa marcadores de color en lugar de códigos QR.
- Solo archivos estáticos. No se envían resultados a SICLER Rural ni a un servidor.
- Recomendado Chrome/Edge recientes en Android o Safari actualizado en iPhone.

## Ajustes

Para cambiar relatos o preguntas edita `app.js`, objeto `worlds`. Para colores, estilos y movimientos edita `style.css`. Para cambiar las tarjetas, edita la constante `ws` en `tarjetas.html`.


## Corrección de cámara (versión 2)

En la versión 2, la detección analiza la proporción de píxeles de color en la región central, ignorando en buena medida el dibujo que hay sobre el marcador. Tras reconocer verde, azul o morado, muestra una animación **superpuesta sobre la vista de cámara** y un botón para entrar al reto. No utiliza seguimiento de objetos tridimensionales ni reconoce la identidad del estudiante.

**Para actualizar GitHub:** reemplaza todos los archivos, haz *Commit changes*, espera a que finalice la publicación de Pages y **recarga la página**. Si ves todavía la versión anterior, cierra la pestaña y borra los datos del sitio; el Service Worker antiguo puede conservar archivos hasta la siguiente carga.

**Para probar:** imprime una tarjeta en color (blanco y negro no funciona), selecciona «Explorar una tarjeta con mi cámara», permite el acceso, acerca el cuadro de color hasta ocupar una zona considerable de la guía y mantén la posición un segundo. No basta con abrir la aplicación de cámara normal del teléfono; se utiliza la cámara dentro de la web. GitHub Pages suministra HTTPS. Para probar localmente desde un celular con HTTP por la red, el navegador normalmente bloqueará la cámara.
