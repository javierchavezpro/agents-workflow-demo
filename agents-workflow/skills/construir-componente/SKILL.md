---
name: construir-componente
description: "Crea o amplía un componente de un design system en Figma: identidad, anatomía, API, tokens, estados y pruebas. Úsala para construir masters; no para auditar pantallas ni publicar."
---

> Reading copy generated on 2026-10-26 (demo 2026.10) from `skills/construir-componente/SKILL.md`: complete. The instructions are the original Spanish ones. Links to files outside this copy are shown as paths in code. See `PROVENANCE.md` at the root of this folder.

# Construir o ampliar un componente del DS

> **Fuente canónica de la receta.** Dueño del método: DS Manager; Naming Architect y File Architect conservan sus cánones. Alta técnica y adaptadores: Super Agent Admin.
> **Alcance:** cualquier proyecto y design system identificados en el encargo; base y derivado solo cuando existan. **Actualizado en la fuente: 2026-10-09.**

## Cuándo usarla

Úsala cuando el encargo pide crear o ampliar una pieza del design system. La identidad funcional y el sistema de destino los decide el DS Manager. Si solo se pide leer composición y nombres, corresponde `skills/revisar-composicion-componente/SKILL.md`; una auditoría de pantalla usa `skills/revisar-pantalla/SKILL.md`.

## Ubicar las fuentes y operar Figma

Localiza la copia viva de `agents-workflow` por su recepción `AGENTS.md`; las rutas citadas en esta receta parten de esa raíz, también cuando ejecutes una copia instalada. Sigue la recepción del proyecto para encontrar su contrato y sus fuentes locales. Los cánones conservan las reglas; esta skill ordena su aplicación y no los reemplaza.

Entra a Figma por `Design/Design Lead/DESIGN_GOVERNANCE.md` §12 y consulta `Design/Figma/FIGMA_GOTCHAS.md` para la lectura y cualquier edición autorizada. Carga las skills técnicas que tu entorno requiera para la operación antes de usar sus herramientas. Si falta acceso al árbol, a una captura o a un modo, declara el límite de verificación.

Cánones que se consultan según el paso:

- `Design/Design Systems/DS_GUIDE.md`.
- `Design/Figma/NAMING_STRUCTURE_GUIDE.md`.
- `Design/Figma/FILE_ARCHITECTURE_GUIDE.md`.

## Receta

**Entrada:** necesidad y casos de uso, DS y archivo objetivo, relación con piezas existentes y decisiones del producto que la pieza debe representar. **Salida:** master comprobado en instancias, documentación local sincronizada y decisiones abiertas explícitas. La ejecución pertenece al DS Manager o a un ejecutor delegado dentro de un encargo definido; la skill no concede jurisdicción sobre Naming, File Architect ni publicación.

1. **Recibe y lee el caso.** Identifica necesidad, usuarios, DS, ejemplos y decisiones de producto disponibles; abre su recepción, contrato o fuente equivalente, índice y ficha de familia si existen, y `Design/Design Systems/DS_GUIDE.md` «Construir un componente, de principio a fin». Declara las fuentes ausentes; no las sustituyas con supuestos.
2. **Audita antes de crear.** Identifica el design system de destino y busca equivalentes en él; si tiene bases o derivados, examina también esa relación. El DS Manager decide a qué sistema pertenece la pieza y si la necesidad pide composición, variante, ampliación, bloque o componente nuevo, con su promesa funcional y sus límites.
3. **Fija ubicación y nombre público.** Dentro del archivo del sistema decidido, aplica el criterio de File Architect para página y convivencia; consulta al oficio si hay una decisión nueva. Naming contrasta familia y nombre con la identidad decidida antes de fijar o multiplicar el set.
4. **Especifica y prepara.** Declara anatomía, subcomponentes, contenido opcional, medidas, estados, accesibilidad e interfaz prevista. Si se amplía un master, conserva IDs, capturas e invariantes; si cambiará API o consumidores, aplica el preflight y la auditoría de migración del canon.
5. **Construye el esqueleto.** Crea contenedor y regiones con auto-layout e instancias de átomos existentes. Naming revisa los nombres internos por responsabilidad antes de clonar variantes.
6. **Resuelve medida e interfaz.** Aplica alto, ancho mínimo, crecimiento, talla y densidad del contrato. El DS Manager declara ejes, valores, booleanos, textos, swaps y slots; Naming contrasta los nombres antes de multiplicar la API y se comprueba que cada propiedad gobierne su capa.
7. **Liga tokens y modos.** Vincula tipografía, rellenos, trazos, color por rol, espaciado, radio y efectos o sombras según la cadena del contrato local. Comprueba los valores resueltos en los modos pertinentes; un bind presente no prueba que el rol ni el resultado visual sean correctos.
8. **Construye estados y variantes.** Clona desde una cara sana y compara cada clon con el origen para restaurar propiedades o enlaces perdidos. Comprueba foco, disabled, contenido largo y reacciones cuando el DS los prometa.
9. **Prueba en instancias.** Alterna API, slots, tallas, estados y modos; redimensiona instancias y compara árbol y captura tras la última escritura. Comprueba el aspecto resuelto de tipografía, rellenos, trazos, color y efectos o sombras en cada modo y estado pertinente, no solo sus bindings. Naming contrasta nombre público, capas por responsabilidad, ejes, valores, booleanos, textos, swaps y slots con `Design/Figma/NAMING_STRUCTURE_GUIDE.md` §§4–6; no certifica tokens, comportamiento ni publicación. Si el encargo pide documentación en Figma, aplica el criterio de presentación de File Architect aunque la página ya estuviera decidida; la documentación visual no nace automáticamente.
10. **Documenta y entrega.** El acomodo del set en su página, su margen interior y su playground siguen `Design/Figma/PRESENTATION_GUIDE.md` §7. Actualiza ficha y worklog; índice solo si cambió lo que indexa, contrato si nació una regla y línea de réplica si corresponde. Informa evidencia, límites, decisiones abiertas y estado de publicación. La skill no publica por sí sola.
