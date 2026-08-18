# Onboarding — clona y arranca

Cómo sumarse a Protesis-Animales desde otra PC o como otra persona. No dependes de ningún chat
anterior: todo se reconstruye desde git.

## 1. Clonar
```bash
gh repo clone <owner>/<repo>
cd <repo>
```

## 2. Identidad de git (una vez por máquina)
```bash
git config user.name "Tu Nombre"
git config user.email "tu@email"
```

## 3. Secretos
- No hay secretos en el repo. Copia `.env.example` a `.env` y rellena los valores reales (viven en
  tu gestor de contraseñas o te los pasa el owner por un canal seguro, nunca por git).

## 4. Arrancar
- Abre Claude Code en la carpeta y corre **`/inicio`**: hace el protocolo de entrada, te muestra en
  qué quedó el proyecto y te propone el próximo paso.
- Para una línea de trabajo nueva: `/nuevo-topic <nombre> <tipo>`.

## 5. Reglas mínimas
- Nunca trabajes en `main`; una rama por topic; integra por Pull Request.
- Guarda con `/checkpoint`; cierra reanudable con `/cierre-sesion`.
- Lee `CLAUDE.md` y `METHODOLOGY.md` para el detalle.
