# Hotel España — web animada

Web de una sola página para el Hotel España (Guadalajara). Se abre con `index.html`; no necesita compilación ni dependencias.

## Estructura

- `index.html`: HTML, CSS y JavaScript.
- `img/`: fachadas (cerrada, abierta, iluminada), personajes, nubes, sol, luna y farola en PNG transparente.

## Escena

- PC: información a la izquierda y fachada completa (3:4, sin recortes ni zoom) fija a la derecha.
- Móvil: la escena ocupa toda la pantalla como fondo fijo y los textos van en velos crema translúcidos.
- El scroll recorre mañana, atardecer y noche: las contraventanas se abren de una en una, las ventanas se encienden y los paseantes caminan por la acera y entran o salen del hotel.
- `index.html?debug` muestra las máscaras de las ventanas. Se ajustan en `WINDOW_RECTS`; el tamaño de los paseantes, en `SCENE.adultHeight`.

## Pendiente antes de publicar como web oficial

- Sustituir `{{teléfono}}`, `{{email}}`, `{{año}}` y `{{precio}}`.
- Confirmar la dirección (Calle Teniente Figueroa, 3) y la posición del mapa.
- Conectar el formulario a un backend real (buscar `CONEXIÓN REAL` en el código). Ahora es una demostración y no envía datos.
