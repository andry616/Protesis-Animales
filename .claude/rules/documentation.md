# Regla: documentación

## Pregunta guía
> Si mañana otra sesión abre este repo sin conocer el chat, ¿tiene con qué continuar bien?

## Se documenta cuando
- Cambia una decisión de arquitectura → `docs/DECISIONS.md` (ADR).
- Entra una dependencia importante o cambia un protocolo/formato/interfaz.
- Aparece una restricción no evidente.
- Cambia cómo se ejecuta, prueba o despliega el sistema.

## No se documenta
- Lo trivial y autoexplicativo · razonamientos temporales · cada conversación con Claude.

## Dónde va cada cosa
| Contenido | Archivo | Quién lo escribe |
|---|---|---|
| Estado global corto | `docs/STATUS.md` | agente `organizador` |
| Jerarquía y madurez (proyecto→subproyecto→topic→subtopic) | `docs/MAP.md` | agente `organizador` |
| Estado detallado de un topic | `docs/topics/<topic>/STATUS.md` | ese topic |
| Punto de reanudación de un topic | `docs/topics/<topic>/HANDOFF.md` | `/cierre-sesion` |
| Puntero al último topic tocado | `docs/HANDOFF.md` | `/cierre-sesion` |
| Decisiones importantes | `docs/DECISIONS.md` | quien decide |
| Arquitectura | `docs/ARCHITECTURE.md` | quien la cambia |
| Cómo se suma otra PC/persona | `docs/ONBOARDING.md` | quien lo cambia |

La documentación reduce el coste de reconstruir contexto; no es burocracia.
