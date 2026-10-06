# trackingapp

## Objetivo

App web para Safari en iPhone 13 que mide la velocidad de cualquier objeto en movimiento al apuntarlo con la cámara, con el móvil en la mano. Todo se ejecuta en local y con visión clásica: seguimiento del objeto, compensación del movimiento de la cámara con el giroscopio, estimación de distancia y filtro de Kalman.

Meta: minimizar el error de la velocidad medida contra una verdad conocida.

## Restricciones fijas

- iPhone 13 sin LiDAR. La distancia sale de fusionar tamaño conocido del objeto, geometría del suelo con la inclinación del móvil y otras fuentes que se demuestren útiles.
- Sin Mac y sin app nativa. Solo Safari (getUserMedia, DeviceMotionEvent), servido por HTTPS en GitHub Pages.
- Sin IA generativa, sin servicios externos ni APIs de pago.
- Si el giroscopio no es fiable en Safari, compensación visual: puntos clave del fondo y homografía.

## Fases

1. Captura y análisis offline en Python (OpenCV, NumPy, SciPy) sobre grabaciones reales.
2. Port a JavaScript para ejecución en vivo.

## Reglas de calidad

- Nada sin métricas: error absoluto, error relativo (%) y dispersión. Cada mejora se compara con la versión anterior sobre las mismas grabaciones.
- Lo que dependa de Safari/iPhone (fps efectivos, frecuencia del giroscopio, estabilización, reloj compartido vídeo-sensores) se mide, no se supone. Las suposiciones se declaran.
- No inventar datos ni capacidades de API.
- Código completo y funcional, sin placeholders, reproducible con dependencias fijadas.
- Prioridad de fuentes de error: distancia, movimiento de cámara, sincronización, seguimiento.
- Vídeos cortos; Git LFS si hace falta.

## Organización del repo

- `CLAUDE.md`: este archivo.
- `docs/PLAN.md`: estado y siguientes pasos.
- `docs/REGISTRO.md`: decisiones y experimentos, con fecha y números.
- `docs/PROTOCOLO_PRUEBAS.md`: protocolo de verdad conocida (se creará en la tarea B).
- `capture/`: página de captura para Safari.
- `analysis/`: análisis en Python.
- `data/`: grabaciones y logs.

Commits pequeños.

## Comunicación

Español informal y directo: qué se ha hecho, qué número ha salido, qué toca.
