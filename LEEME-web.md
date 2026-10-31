# Hotel España — web animada

Abrir `index.html` directamente en un navegador. No requiere instalar paquetes, framework, compilación ni servidor. Las fuentes de Google requieren conexión; hay fuentes de sistema como alternativa.

## Archivos

- `index.html`: toda la estructura, CSS y JavaScript.
- `img/`: los 13 PNG usados por la escena, además de los WebP anteriores conservados.
- `assets/`: kit original organizado y manifiesto de imágenes.
- `archivo/index-antes-animacion-20261031.html`: copia del HTML previo.

## Ajustes de la escena

Abrir `index.html?debug` para ver las 20 zonas (15 ventanas superiores, 4 de planta baja y la entrada). Modificar `WINDOW_RECTS` al inicio del script: x, y, w, h son porcentajes del lienzo completo. Las variantes generadas tienen pequeñas diferencias arquitectónicas, por lo que las máscaras son ajustables y no garantizan un registro perfecto de píxeles.

`SCENE_CONFIG` controla la entrada, la altura de la acera, el tamaño adulto, la semilla aleatoria y la duración de los fundidos. `CHARACTERS` contiene orientación, dimensiones y altura corporal de cada personaje. `WHITE_BACKGROUND_ASSETS` permite activar multiply si algún recurso se sustituye por una imagen con fondo blanco.

En escritorio la fachada se ajusta al ancho y alto disponibles con margen para el zoom: se muestra la ilustración completa. En móvil la escena ocupa el fondo fijo de la pantalla con opacidad del 24%, detrás de todas las secciones; el edificio también se muestra completo. Las tarjetas y el formulario tienen fondo crema al 88% para mantener la legibilidad. Los desplazamientos utilizan un único bucle requestAnimationFrame. Las lecturas de geometría se agrupan al cargar, cambiar tamaño o fuentes. Movimiento reducido elimina paseantes, zoom, desplazamiento de nubes y parpadeo.

## Reservas y contenido

El formulario valida fechas y muestra un mensaje local. No envía información ni confirma reservas. Sustituir {{año}}, {{precio}}, {{dirección}}, {{teléfono}} y {{email}} por información real antes de publicar. El contenido sobre habitaciones y servicios es provisional.

## Comprobaciones

Verificados: sintaxis JavaScript, existencia de los 13 PNG y referencias del HTML, lógica de 20 máscaras, 9 posiciones de scroll, movimiento de personajes, desaparición después de p=0.93, validación de fechas y confirmación local. La lógica se ha ejecutado con geometrías simuladas de 1440×900, 1280×800 y 390×844, con movimiento normal y reducido.

La revisión visual en navegador no se completó: la herramienta de navegador denegó el acceso a la vista previa local. Las simulaciones no sustituyen capturas reales de esos tamaños.
