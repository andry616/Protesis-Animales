---
description: Abre un nuevo topic (línea de trabajo) con su carpeta, su rama y su registro de reclamos.
---

Abre un nuevo **topic** de forma aislada, para trabajar en paralelo sin pisar otras líneas.

El argumento ($ARGUMENTS) trae nombre y, opcionalmente, tipo. Ej: `catalogo feature` o
`modbus-timing research`. Si es parte de un subproyecto, indícalo (`sub/<nombre>`).

Pasos:

1. **Definir el topic:** nombre en kebab-case y tipo (`research` | `feature` | `fix` | `refactor` |
   `docs`). Si no me diste el tipo, pregúntamelo.
2. **Crear la rama** con el prefijo del tipo: `git switch -c feature/<nombre>` (o `research/...`). Si
   dos topics van a editar los mismos archivos en paralelo, propón un git worktree.
3. **Crear la carpeta del topic:** `docs/topics/<nombre>/STATUS.md` con objetivo, criterio de
   aceptación, madurez inicial y próximos pasos. Es propiedad exclusiva del topic.
4. **Registrar reclamos:** añade una entrada del topic en `registry/claims.json` con los
   archivos/carpetas que planea tocar (para que el `guardian` detecte colisiones).
5. **Actualizar el mapa:** invoca al `organizador` para añadir el topic a `docs/MAP.md` con su
   madurez, propósito y subproyecto (si aplica).
6. Confirma el topic creado, la rama y su carpeta.
