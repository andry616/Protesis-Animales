# Regla: arquitectura

- **`docs/ARCHITECTURE.md` es la referencia estructural vigente.** Consúltalo antes de cambiar
  estructura, integración o límites del sistema.
- **`docs/DECISIONS.md` manda sobre la memoria.** Si el pedido actual contradice una decisión
  vigente, señálalo antes de sustituir la arquitectura en silencio. Si se cambia, se registra una
  nueva DEC y se marca la anterior como "sustituida".
- **No cambies arquitectura por preferencia estética.** Solo cuando la tarea lo exige.
- **Los límites entre componentes se respetan.** Un cambio que cruza límites se documenta.
- **Investigación → decisión → desarrollo.** Un hallazgo de un topic `research` se convierte en una
  DEC antes de graduar a un topic de desarrollo. Así el árbol de trabajo queda intercomunicado.
