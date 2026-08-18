# Regla: código

- **Cambio mínimo suficiente.** Resuelve la tarea sin refactors estéticos no pedidos.
- **Escribe como el código que rodea.** Respeta convenciones, nombres e idioma del proyecto.
- **Un commit = un cambio coherente.** No mezcles tareas de topics distintos.
- **Verifica antes de cerrar:** corre pruebas/validaciones disponibles, revisa `git diff`, confirma
  que no entran secretos ni temporales.
- **No declares algo verificado sin correr la comprobación.**
- **Secretos fuera de Git.** Usa `.env.example` con valores ficticios; los reales van en `.gitignore`.
- **Ramas:** nunca trabajes directo en `main`; una rama por topic (`feature/`, `fix/`, `research/`,
  `refactor/`, `docs/`).

Ajusta o extiende estas reglas en el `CLAUDE.md` del proyecto solo si son estables y propias de él.
