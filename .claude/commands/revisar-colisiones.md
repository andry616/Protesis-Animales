---
description: Invoca al guardian para detectar si dos topics están pisando los mismos archivos o docs.
---

Revisa si las líneas de trabajo (topics) activas se están pisando.

Invoca al agente `guardian` y pásale el foco actual. Debe:

1. Leer `registry/claims.json` y las ramas/worktrees activos.
2. Cruzar los archivos reclamados por cada topic y el `git diff` actual.
3. Reportar, ordenado por gravedad: **COLISIÓN** (dos topics al mismo archivo), **FUGA DE CAPA** (un
   topic escribió en un doc global), **RECLAMO SIN REGISTRAR** (cambios que ningún topic declaró), u
   **OK**.
4. Para cada hallazgo, proponer la resolución mínima. No reescribir ni descartar el trabajo de nadie.

Muéstrame el reporte y espera mi decisión antes de mover nada.
