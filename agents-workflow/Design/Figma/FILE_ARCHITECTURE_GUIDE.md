> Reading copy, 15 October 2026. Source: `Design/Figma/FILE_ARCHITECTURE_GUIDE.md`. Selected sections only; live backlogs, occupants and history omitted. Original Spanish instructions retained. Referenced canons outside this selection are dependencies, not bundled files; see PROVENANCE.md. This is documentation, not an operational checkout.

# Arquitectura del archivo: el canon

> El oficio se llama **Arquitectura del archivo** (decisión de Javier, 2026-08-04). Redacción con IA (Fable). **Actualizado: 2026-10-09.**

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

