---
license: openrail
language: es
tags: [text-to-speech, onnx]
---
# Voz Hikvoo (Supertonic 3, versión ligera ~100 MB)

Derivado de [Supertone/supertonic-3](https://huggingface.co/Supertone/supertonic-3) (licencia OpenRAIL-M, ver LICENSE).
Cambio: los pesos se guardaron en 8 bits (int8 por canal + DequantizeLinear) para que pese ~100 MB en lugar de ~400 MB.
El cálculo sigue siendo en 32 bits. Se usa en el navegador con onnxruntime-web (WebGPU).

Los archivos .onnx vienen partidos en pedazos de 16 MB (.part0, .part1…) para que GitHub
los acepte subiéndolos desde la página web (límite 25 MB por archivo).
