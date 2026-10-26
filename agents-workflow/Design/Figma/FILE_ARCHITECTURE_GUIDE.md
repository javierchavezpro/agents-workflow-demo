> Reading copy generated on 2026-10-26 (demo 2026.10) from `Design/Figma/FILE_ARCHITECTURE_GUIDE.md`: selected sections; who holds the role, backlogs and history are omitted. The instructions are the original Spanish ones. Links to files outside this copy are shown as paths in code. See `PROVENANCE.md` at the root of this folder.

# Arquitectura del archivo: el canon

> Esta guía da **estructura y presentación** a los archivos de Figma del ecosistema: el mapa de páginas, las páginas de documentación, los muestrarios y las plantillas de anatomía. Trabaja el nivel macro del archivo, el que hace que se navegue, se entienda y se consulte.
> Se lee junto a `../../Javier/WORKING_WITH_JAVIER.md` (flujo y alcance), `../Design Systems/FILE_ARCHITECTURE.md` (las decisiones que todo archivo debe responder, y los cuatro invariantes que no se negocian) y el contrato del DS en turno, donde viven las respuestas del caso (vivo: `../Design Systems/Embit/Contract/EMBIT_DS_CONTRACT.md` §10b).
> **Esta guía no repite invariantes ni reglas del patrón: los consume.** Si una regla general aparece aquí duplicada, sobra aquí.
> **Lo administra el oficio File Architect** (`../File Architect/FILE_ARCHITECT.md`).
> **Frontera del oficio:** los NOMBRES de páginas y frames de documentación son del canon Naming (`NAMING_STRUCTURE_GUIDE.md` §6b), que este oficio consume y no define; y el contenido de diseño de las pantallas no es suyo, sino de los oficios de pantallas y reglas de aplicación.
> El oficio se llama **Arquitectura del archivo** (decisión de Javier, 2026-08-04). Redacción con IA (Fable). **Actualizado en la fuente: 2026-10-23.**

## 3. Método de trabajo

1. Por **lotes acordados** con Javier: cada lote se propone, se aprueba, y se cierra con verificación y su línea de worklog.
2. Al editar material de Javier se aplica la pauta 4 de `../../System/Super Agent Admin/SYSTEM_GOVERNANCE.md`, que distingue su texto literal de lo demás que él estableció.
3. Los **muestrarios bindean el valor, no lo rotulan**: así se mueven solos cuando el token cambia (regla de redacción del patrón).
4. Toda página nueva **declara sus modos** cuando el DS lo exige (en Embit: marca, tema, breakpoint tipográfico y de layout).
5. Renombres y mudanzas presentan su mapa **actual → propuesto** antes de ejecutarse.

## 4. Insumos de nomenclatura

El oficio consume el canon Naming (`NAMING_STRUCTURE_GUIDE.md`, en esta carpeta): la gramática de nombres de página, la jerarquía y sus ejes, los textos por rol para plantillas, y el §6b de **familias de frames de documentación** (`Page -`, `Muestrario -`, `Doc -`, `Test Playground -`, `Note Card`).

**La línea con Naming, en una frase:** el mapa es de este oficio (qué familias de página existen, en qué orden y con qué fronteras) y la gramática es de Naming (cómo se escribe cada nombre y qué símbolo lleva). Cuando las dos se encuentran en la misma cadena de texto (un separador, el símbolo de una familia), este oficio decide **qué tipo de página es** y Naming decide **cómo se marca**. La decisión resultante se registra en el contrato del DS, que es su tercera pata.

## 7. Frontera con el DS Manager

Este oficio **documenta el estado que encontró; no lo altera antes de registrarlo.** Es la excepción de evidencia de la regla 11 de `../../Javier/WORKING_WITH_JAVIER.md`: no es una prohibición de reparar, sino la condición para que el inventario siga siendo evidencia.

Documentar obliga a medir, y medir destapa defectos: una altura que en realidad la fija el icono y no la talla, un cruce de ejes incompleto, un token que resuelve distinto de lo que promete. Cuando eso pasa, la regla es: **se documenta el comportamiento REAL, se reporta el hallazgo con su evidencia al backlog, y se sigue.** Arreglar el componente es del DS Manager; decidir si se arregla, de Javier.

El corolario importa más que la regla: **nunca se documenta la intención.** Si el componente se comporta distinto de lo que dice el contrato, la página de documentación describe el comportamiento, marca la diferencia y deja el hallazgo anotado. Una documentación que describe el estado deseado convierte un defecto en una mentira con formato de spec, y el siguiente que la lea diseñará contra ella.

El límite inverso también es del oficio: si para documentar hace falta **construir** algo (un componente de documentación, un espécimen, una plantilla), eso sí es suyo (§1), porque no es parte del sistema que se documenta.
