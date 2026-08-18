---
description: Cierra un topic terminado: lo mueve a docs/topics/_archivados y lo cierra en el mapa.
---

Archiva un **topic** que ya llegó a su fin (mergeado a `main` o descartado), para que el árbol no
acumule líneas muertas.

El argumento ($ARGUMENTS) es el nombre del topic.

Pasos:

1. **Verificar que está cerrado:** su trabajo se mergeó a `main` (o se decidió descartarlo). Si aún
   tiene cambios sin integrar, avísame y detente.
2. **Consolidar aprendizaje:** confirma que cualquier decisión importante del topic quedó en
   `docs/DECISIONS.md`. Si falta, regístrala antes de archivar.
3. **Mover la carpeta:** `docs/topics/<topic>/` → `docs/topics/_archivados/<topic>/` (con `git mv`).
   Conserva su `STATUS.md` y `HANDOFF.md` como historia.
4. **Limpiar reclamos:** quita la entrada del topic en `registry/claims.json`.
5. **Actualizar el mapa:** invoca al `organizador` para marcar el topic como `archivado` en
   `docs/MAP.md` (fila movida a una sección de cerrados, con su madurez final).
6. **Borrar la rama** local del topic si ya se mergeó (`git branch -d`), tras confirmar conmigo.
7. Confirma qué se archivó y el estado del mapa.
