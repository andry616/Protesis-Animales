---
description: Cierre explícito de sesión. Checkpoint + HANDOFF reanudable del topic. Solo cuando se pide.
---

Cierra la sesión de forma reanudable. Úsalo SOLO cuando yo lo pida (lo normal es `/checkpoint`).

Pasos:

1. **Checkpoint completo** del topic activo (pasos de `/checkpoint`).
2. **Escribir `docs/topics/<topic>/HANDOFF.md`** con el punto EXACTO de reanudación de ESE topic:
   - Fecha y hora · topic y rama.
   - Último paso completado.
   - **Próximo paso concreto** (la primera acción al volver).
   - Dudas / decisiones abiertas.
   - Archivos en juego y su estado.
   - Comandos exactos para retomar.
3. **Actualizar el puntero global** `docs/HANDOFF.md`: solo anota cuál fue el último topic tocado y
   la fecha (no dupliques el detalle, que vive en el topic).
4. **Refrescar el mapa:** invoca al `organizador` para actualizar `docs/MAP.md` y `docs/STATUS.md`.
5. **Guardar puntero de sesión:** anota en el HANDOFF del topic que en la misma máquina se reanuda
   con `claude --resume`, y en otra máquina con `/retomar <topic>`.
6. **Push (si lo pido):** por defecto no empujas.
7. Confirma en 3 líneas que el punto quedó guardado y cómo retomarlo.
