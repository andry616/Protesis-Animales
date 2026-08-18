---
description: Reconstruye el punto de trabajo de un topic desde git, sin depender del chat anterior.
---

Reconstruye el contexto para seguir exactamente donde se dejó. Funciona aunque el chat ya no exista
(otra máquina, contexto nuevo): la fuente de verdad es git, no la conversación.

Pasos:

1. **Ubicarse:** `git status`, `git branch --show-current`, `git log --oneline -5`.
2. **Elegir topic:** si el argumento nombra uno, úsalo. Si no, lee `docs/HANDOFF.md` (puntero global)
   para saber cuál fue el último topic tocado, o lista los topics activos de `docs/MAP.md` y pregúntame.
3. **Leer, en orden:** `docs/topics/<topic>/HANDOFF.md` → `docs/topics/<topic>/STATUS.md` →
   `docs/MAP.md` → `docs/DECISIONS.md` (si la tarea toca decisiones).
4. **Revisar el buzón:** mensajes sin atender en `.buzon/inbox/`.
5. **Resumir el punto de reanudación:** topic/rama, último paso, próximo paso concreto, dudas abiertas.
6. **Confirmar antes de actuar:** propón el próximo paso y espera mi confirmación antes de editar.

Argumento opcional ($ARGUMENTS): nombre del topic a retomar.
