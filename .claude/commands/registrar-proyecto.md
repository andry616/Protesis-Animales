---
description: Añade o actualiza una entrada en el directorio de proyectos (address book del buzón).
---

Registra un proyecto en el **directorio** `registry/proyectos.json`, para que el buzón sepa a dónde
enviar mensajes.

El argumento ($ARGUMENTS) trae el nombre del proyecto y su repo (`owner/repo`). Si falta algo,
pregúntamelo.

Pasos:

1. **Leer** `registry/proyectos.json`.
2. **Añadir o actualizar** la entrada del proyecto con: `nombre`, `repo` (`owner/repo`),
   `buzon_inbox` (ruta dentro del repo, por defecto `.buzon/inbox/`), y una descripción de una línea.
3. **Validar** que no haya nombres duplicados y que el repo tenga formato `owner/repo`.
4. Confirma la entrada registrada y el total de proyectos en el directorio.

Nota: este directorio es la "libreta de direcciones". Mantenlo igual en los proyectos que se
comunican entre sí (o apúntalos a una copia compartida) para que las direcciones coincidan.
