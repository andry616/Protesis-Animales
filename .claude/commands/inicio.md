---
description: Arranque diario. Un solo comando: te ubica, te dice en qué quedaste y te propone seguir.
---

Este es el comando de **uso diario**. Lo corres al abrir el proyecto y hace todo el protocolo de
entrada por mí, sin que tenga que recordar nada. Sé breve y claro.

Pasos (hazlos en silencio y muéstrame solo el resumen final):

1. **Ubícate:** `git status`, `git branch --show-current`, `git log --oneline -5`.
2. **Lee el estado:** `docs/STATUS.md`, `docs/MAP.md`, y el puntero `docs/HANDOFF.md`.
3. **Revisa el buzón:** cuenta los mensajes sin atender en `.buzon/inbox/`.
4. **Detecta la situación** y actúa:
   - **Proyecto nuevo/vacío** (sin topics reales): dilo y ofrece abrir el primero con `/nuevo-topic`.
   - **Hay topics activos:** muéstrame la lista corta (topic · madurez · próximo paso, desde cada
     `docs/topics/<topic>/HANDOFF.md`).
5. **Preséntame el arranque** en un bloque corto:
   - Rama actual y último topic tocado.
   - **Próximo paso concreto** de ese topic (leído de su HANDOFF).
   - Mensajes de buzón pendientes (si hay).
   - Un menú de 3 opciones: **(a)** seguir con `<topic>`, **(b)** abrir topic nuevo (`/nuevo-topic`),
     **(c)** atender el buzón (`/buzon-check`).
6. **Espera mi elección.** No modifiques archivos hasta que yo elija.

Argumento opcional ($ARGUMENTS): si nombro un topic, salta directo a retomarlo (`/retomar <topic>`).
