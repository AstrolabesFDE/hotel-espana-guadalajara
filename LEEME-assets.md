# Hotel España — kit de imágenes

13 PNG independientes generados con la herramienta integrada image_gen. Todos tienen canal alfa con transparencia real, comprobada. Se han revisado visualmente los 13 recursos.

## Organización

- `assets/fachadas/`: fachada-cerrada.png, fachada-abierta.png, fachada-luz.png.
- `assets/personajes/`: personaje-caballero.png, personaje-senora.png, personaje-botones.png, personaje-pareja.png, personaje-nino.png.
- `assets/elementos/`: nube-1.png, nube-2.png, sol.png, luna.png, farola.png.
- `referencias/`: cuatro ilustraciones originales, conservando sus nombres.
- `capturas/`: capturas de pantalla e imágenes auxiliares existentes.
- `img/`: imágenes WebP existentes que utiliza index.html, sin cambiar sus rutas.
- `index.html` y `dibujo.html`: conservados en la raíz.

## Integración y limitaciones

Las fachadas tienen exactamente 1086 × 1448 píxeles (3:4). La abierta se ha generado editando la cerrada y la iluminada editando la abierta. Hay pequeñas variaciones generativas fuera de las ventanas: no se garantiza coincidencia píxel a píxel. Antes de animar ventanas mediante máscaras se requiere registro y retoque; para una transición inicial puede usarse un fundido entre imágenes completas.

El manifiesto incluye dimensiones y el rectángulo visible aproximado `contentBounds` (alfa >= 64). Algunos PNG tienen píxeles residuales de alfa muy bajo en los márgenes. No se ha recortado ni remuestreado ningún original generado.

Los personajes conservan la escala visual de ilustración, pero su tamaño final debe fijarse en CSS. Para cumplir la escala solicitada, usar como altura visible adulta un tercio de la altura de la planta baja; el niño aproximadamente 55–60% de la altura adulta. En la fachada a tamaño nativo, la planta baja mide unos 300 px: adulto visible unos 100 px y niño unos 55–60 px. Ajustar el tamaño según contentBounds y anclar los pies a la acera. La pareja mide 1086 × 1449 px; no asumir que todos los lienzos son idénticos.

La señora y el globo conservan el rojo solicitado expresamente para esos personajes.

## Prompts utilizados (especificación)

Estilo común: grabado vintage con líneas finas azul marino, rayado cruzado delicado, grano de papel dentro de los objetos, ambiente elegante de cuento europeo; PNG transparente, sin fondo ni texto adicional.

1. Fachada cerrada: editar la referencia nocturna, conservar arquitectura, salmón y crema, cerrar todas las contraventanas y puertas, luz diurna neutra, eliminar cielo y edificios vecinos, conservar calle y acera vacías y rótulos del hotel.
2. Fachada abierta: editar la cerrada; abrir todas las contraventanas y puertas de balcón, interiores oscuros y cortinas crema, conservar encuadre y arquitectura.
3. Fachada iluminada: editar la abierta; iluminar todas las ventanas con luz dorada y abrir la entrada iluminada, conservar el exterior.
4. Caballero: cuerpo entero de perfil andando a la derecha, abrigo largo marrón, fedora y periódico sin texto legible.
5. Señora: cuerpo entero de perfil andando a la izquierda, abrigo rojo, sombrero pequeño y maleta vintage con ruedas; usar caballero como referencia de estilo y escala.
6. Botones: cuerpo entero de perfil andando a la derecha, uniforme azul marino, botones dorados, gorro pillbox y dos maletas; misma referencia.
7. Pareja: pareja mayor del brazo andando a la izquierda, ropa crema y azul marino; misma referencia.
8. Niño: abrigo azul marino y globo rojo, de perfil andando a la derecha, menor altura corporal que los adultos; misma referencia.
9. Nube 1: una nube grande abombada crema con rayado azul marino, aislada.
10. Nube 2: una nube larga y fina con extremos afilados, crema y azul marino, aislada.
11. Sol: disco cálido crema dorado con grabado y líneas radiantes, sin rostro, aislado.
12. Luna: luna llena crema con cráteres grabados azul marino, sin rostro, aislada.
13. Farola: farol clásico español de hierro con soporte mural curvo, vista frontal, encendido con brillo cálido, sin pared.
