# SICLER AR — 10 lecturas, 10 imágenes para colorear

Proyecto estático para GitHub Pages, sin PHP ni dependencias remotas.

## Publicar
1. Copia `index.html`, `tarjetas.html`, `lecturas.json` y la carpeta `assets/` a la raíz del repositorio `academico2025/sicler-lectura`.
2. GitHub > Settings > Pages > Deploy from a branch > `main` > `/(root)`.
3. Accede a https://academico2025.github.io/sicler-lectura/ y pulsa **Activar cámara AR**.
4. En https://academico2025.github.io/sicler-lectura/tarjetas.html imprime las diez hojas A4 y colorea SOLO los dibujos. **No colorear los rectángulos de color ni su marco negro.**
5. Apunta la cámara integrada de la página al rectángulo de color.

## Límites técnicos (importante)
Esta implementación usa detección cromática de marcadores y SVG vectoriales con efecto de profundidad en la imagen de cámara. No es seguimiento tridimensional de superficies ni reconstruye los colores que pintó cada niño. El algoritmo identifica el color predominante, por lo que otros objetos intensamente coloreados pueden interferir. Funciona mejor con fondo neutro y buena luz; hay acceso alternativo tocando cada figura. Para AR 3D realmente anclada a cada dibujo y conservar su coloreado se necesita un motor de seguimiento de imágenes y modelos/texture mapping adicionales.

La cámara del teléfono NO abre la web al mirar el dibujo; primero debe abrirse la URL en Chrome/Safari y pulsar Activar cámara AR. Se requiere HTTPS, que GitHub Pages proporciona.
