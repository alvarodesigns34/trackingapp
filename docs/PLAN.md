# Plan

Estado: Fase 0 hecha (documentación y estructura). Siguiente: tareas A, B y C.

## Fase 1: captura y análisis offline en Python

- [ ] Captura de grabaciones reales con log sincronizado (vídeo + giroscopio).
- [ ] Protocolo de pruebas con verdad conocida.
- [ ] Medir fps efectivos, jitter y sincronización vídeo-sensores.
- [ ] Seguimiento del objeto (OpenCV).
- [ ] Compensación del movimiento de cámara (giroscopio; si no vale, puntos clave del fondo y homografía).
- [ ] Estimación de distancia (tamaño conocido, geometría del suelo con inclinación, otras fuentes si se demuestran útiles).
- [ ] Filtro de Kalman sobre la velocidad.
- [ ] Métricas: error absoluto, error relativo (%) y dispersión, comparadas con la versión anterior.

## Fase 2: port a JavaScript

- [ ] Portar el pipeline validado en Fase 1 a JS para ejecución en vivo en Safari.
- [ ] Comprobar que los resultados en JS coinciden con los de Python sobre las mismas grabaciones.
- [ ] Publicar en GitHub Pages (HTTPS).

## Tareas PENDIENTES para la próxima sesión

- **A) PENDIENTE:** página de captura en Safari con log sincronizado de fotogramas y giroscopio.
- **B) PENDIENTE:** protocolo de pruebas de verdad conocida (`docs/PROTOCOLO_PRUEBAS.md`).
- **C) PENDIENTE:** análisis base en Python de fps, jitter y sincronización.
