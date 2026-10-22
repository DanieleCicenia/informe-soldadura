# Informe de inspección de soldadura (página para el código QR)

Página fija del prototipo de inspección de uniones soldadas (ESPOCH, Facultad de Mecánica).

El equipo muestra un código QR al generar el informe. **El informe viaja dentro del propio
enlace** (la parte después de `#`, que el navegador nunca envía al servidor): esta página lo
lee en el teléfono y lo dibuja. Aquí no se guarda ningún informe; solo están la plantilla
(`index.html`), el logo y la tabla de frases que usa la compresión (`diccionarios/`).

Un archivo de `diccionarios/` ya publicado no debe modificarse: los QR emitidos con él dejarían
de abrirse. Si cambian los textos, se agrega uno nuevo (`d2.txt`, ...).
