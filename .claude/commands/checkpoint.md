---
description: Guardado seguro del topic activo (WIP commit + estado + chequeo de colisiones). NO cierra la sesión.
---

Haz un **checkpoint** del topic (línea de trabajo) activo. NO cierra la sesión; solo guarda para no
perder nada y se sigue trabajando.

Pasos:

1. **Ubicar el topic activo:** rama actual (`git branch --show-current`) y su carpeta
   `docs/topics/<topic>/`. Si no está claro cuál es, pregúntame antes de seguir.
2. **Actualizar el estado del topic:** edita `docs/topics/<topic>/STATUS.md` con lo hecho, lo que
   está a medias y el próximo paso concreto. Escribe SOLO en la carpeta de ese topic.
3. **Revisar colisiones:** invoca al agente `guardian`. Si reporta COLISIÓN, muéstramela y detente
   antes de commitear.
4. **Verificar el diff:** `git status` y `git diff`. Confirma que no hay secretos ni temporales.
5. **Commit del WIP en la rama del topic** (nunca `main`): `wip(<topic>): <resumen corto>`.
6. **No hagas push** salvo que lo pida explícitamente. Reporta en 2-3 líneas: topic, qué se guardó y
   el próximo paso.

Argumento opcional ($ARGUMENTS): nota corta para el mensaje del checkpoint.
