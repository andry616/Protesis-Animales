# Regla: trabajo en paralelo sin colisiones

Regla central para que varias líneas de trabajo (topics) convivan sin pisarse.

## Principios
1. **Un topic = una carpeta de docs + una rama.** El detalle vive en `docs/topics/<topic>/` y solo
   ese topic escribe ahí (incluido su `HANDOFF.md`).
2. **Los docs globales son de solo-lectura para los topics.** `docs/STATUS.md` y `docs/MAP.md` los
   mantiene el `organizador`. Un topic nunca los edita a mano (evita conflictos de merge).
3. **Declara antes de tocar.** Todo archivo/carpeta de código que un topic modifique se registra en
   `registry/claims.json`.
4. **El `guardian` es el árbitro.** Antes de un checkpoint con varios topics activos, corre
   `/revisar-colisiones`. Si dos reclaman el mismo archivo, se resuelve ANTES: secuenciar, dividir o
   reasignar.
5. **Aislamiento físico cuando hace falta.** Si dos topics editan de verdad los mismos archivos en
   paralelo, se usan git worktrees, no solo ramas.

## Qué NO hacer
- Que dos topics escriban el mismo archivo sin pasar por el `guardian`.
- Editar `STATUS.md`/`MAP.md` desde un topic.
- Mezclar cambios de dos topics en un mismo commit.
