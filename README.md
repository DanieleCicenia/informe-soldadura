# Informe de inspección de soldadura (página para el código QR)

Página fija del prototipo de inspección de uniones soldadas (ESPOCH, Facultad de Mecánica).

El equipo muestra un código QR al generar el informe. **El informe viaja dentro del propio
enlace** (la parte después de `#`, que el navegador nunca envía al servidor): esta página lo
lee en el teléfono y lo dibuja. En la rama `main` solo están la plantilla (`index.html`), el logo
y la tabla de frases que usa la compresión (`diccionarios/`).

**PDF completo con fotos (temporal y cifrado):** el equipo sube el PDF cifrado con AES-128-GCM a
la rama `datos`. La clave solo viaja en el QR, así que lo que queda aquí es ilegible. La rama se
reemplaza entera (un solo commit, sin historia) cada vez que se genera otro informe, y
`.github/workflows/limpiar.yml` la borra si tiene más de 24 h.

Un archivo de `diccionarios/` ya publicado no debe modificarse: los QR emitidos con él dejarían
de abrirse. Si cambian los textos, se agrega uno nuevo (`d2.txt`, ...).
