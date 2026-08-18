# Regla: GitHub

- **Nunca trabajes directo en `main`.** Una rama por topic (`feature/`, `fix/`, `research/`,
  `refactor/`, `docs/`).
- **Integración por Pull Request.** Usa `.github/PULL_REQUEST_TEMPLATE.md`: objetivo, cambios,
  cómo se verificó, riesgos, docs/decisiones relacionadas.
- **`main` protegido:** PR obligatorio, checks de CI en verde, sin force-push ni borrado. (Se
  configura una vez, con permisos de owner/admin del repo.)
- **CI:** `.github/workflows/ci.yml` corre validaciones en cada PR. Ajusta los pasos al tipo de
  proyecto (tests, lint, build).
- **Commits claros:** `feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `wip(<topic>):`.
- **Secretos fuera de git:** `.env.example` versionado; los valores reales, en gestor de contraseñas
  o `.env` local (en `.gitignore`). Nunca subas claves.
- **Un repo por proyecto.** El buzón entre proyectos viaja por commit/PR al `.buzon/inbox/` del repo
  destino (ver agente `buzon` y `registry/proyectos.json`).
