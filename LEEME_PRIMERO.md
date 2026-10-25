# SICLER Rural — tarjetas QR para GitHub Pages

Sitio configurado: https://academico2025.github.io/sicler-lectura/

## Publicación
1. Descomprime este ZIP.
2. En GitHub, abre el repositorio `academico2025/sicler-lectura`.
3. Sube **todo el contenido de la carpeta** a la raíz del repositorio, incluidas `tarjetas.html` y la carpeta `qr/`.
4. Confirma con Commit changes.
5. Comprueba `https://academico2025.github.io/sicler-lectura/tarjetas.html` y toca una tarjeta.
6. Imprime `TARJETAS_QR_SICLER_GITHUB.pdf` (incluido junto al ZIP) o imprime `tarjetas.html`.

Los diez códigos QR enlazan al dominio publicado. No funcionan sin acceso a GitHub Pages. Para una intranet offline se necesitan otros QR con direcciones del servidor local.

## Cómo funcionan
La cámara normal del celular reconoce el **QR** y abre la dirección de esa aventura. No reconoce una ilustración sola. El contenido sigue siendo una escena animada en el navegador, no una figura 3D anclada al entorno real.

Cada QR usa una de tres aventuras y conserva el código SA-04 del niño como parámetro de enlace. La web utiliza el parámetro `card` para seleccionar la aventura.
