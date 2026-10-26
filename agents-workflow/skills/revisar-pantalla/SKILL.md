---
name: revisar-pantalla
description: "Audita una pantalla de producto existente en Figma: estructura, estados, aspecto y candidatos a componente. Úsala para revisar, sin rediseñar; renombra capas propias solo si se autorizó."
---

> Reading copy generated on 2026-10-26 (demo 2026.10) from `skills/revisar-pantalla/SKILL.md`: complete. The instructions are the original Spanish ones. Links to files outside this copy are shown as paths in code. See `PROVENANCE.md` at the root of this folder.

# Revisar una pantalla existente

> **Fuente canónica de la receta.** Dueño del método: Screen Designer; UX, Naming Architect, File Architect y DS Manager conservan sus decisiones y cánones. Alta técnica y adaptadores: Super Agent Admin.
> **Alcance:** cualquier proyecto y design system identificados en el encargo; base y derivado solo cuando existan. **Actualizado en la fuente: 2026-10-09.**

## Cuándo usarla

Úsala ante una pantalla ya construida. Para crearla o rehacerla corresponde `skills/disenar-pantalla/SKILL.md`. Un componente existente se revisa con `skills/revisar-composicion-componente/SKILL.md`; construir o ampliar un master corresponde a `skills/construir-componente/SKILL.md`. Un hallazgo no activa automáticamente otra receta.

## Ubicar las fuentes y operar Figma

Localiza la copia viva de `agents-workflow` por su recepción `AGENTS.md`; las rutas citadas en esta receta parten de esa raíz, también cuando ejecutes una copia instalada. Sigue la recepción del proyecto para encontrar su contrato y sus fuentes locales. Los cánones conservan las reglas; esta skill ordena su aplicación y no los reemplaza.

Entra a Figma por `Design/Design Lead/DESIGN_GOVERNANCE.md` §12 y consulta `Design/Figma/FIGMA_GOTCHAS.md` para la lectura y cualquier edición autorizada. Carga las skills técnicas que tu entorno requiera para la operación antes de usar sus herramientas. Si falta acceso al árbol, a una captura o a un modo, declara el límite de verificación.

Cánones que se consultan según el paso:

- `Design/Figma/SCREEN_STRUCTURE_GUIDE_GENERAL.md`.
- `Design/Design Systems/SCREEN_DESIGN_RULES.md`.
- `Design/Figma/NAMING_STRUCTURE_GUIDE.md`.
- `Design/Figma/FILE_ARCHITECTURE_GUIDE.md`.
- `Design/Figma/PRESENTATION_GUIDE.md`, para simbología, secciones, espaciado y documentación del lienzo.
- `Design/Design Systems/DS_GUIDE.md`.
- `Design/Design Lead/DESIGN_PRINCIPLES.md`.
- `Design/Design Lead/DESIGN_ACCESSIBILITY.md`.

## Entrada y salida

**Entrada:** archivo, página y URL o ID del frame; tarea que la pantalla debe permitir; estados y viewports relacionados; proyecto y cadena de design systems; motivo concreto de la revisión; alcance de lectura; y autorización expresa si Javier también pide corregir nombres internos. Si falta la tarea o la fuente de expectativa, la auditoría puede describir el estado actual, pero no declarar que cumple una intención inventada.

**Salida:** evidencia previa por ID y capturas; mapa de responsabilidades y estructura; contraste funcional, visual y responsive contra fuentes declaradas; mapa `ID · actual → propuesto` para cada cambio recomendado; renombres de capas internas propias de la pantalla y comprobados solo si se autorizaron; candidatos a componente con sus usos; límites de verificación; y decisiones separadas por oficio. Un resultado vacío declara qué se buscó y qué quedó fuera.

## Receta

1. **Delimita la pantalla y carga sus fuentes.** Lee las reglas de colaboración, recepción y decisiones del proyecto, contexto de uso, flujo o criterios de UX, capa local del método y contrato del DS. Identifica base y derivado solo si esa relación existe. Anota qué frame es el viewport canónico, cuáles son estados, variantes o referencias extendidas y qué pregunta debe responder la auditoría. Aplica `Design/Figma/SCREEN_STRUCTURE_GUIDE_GENERAL.md` §§1–2 y el orden de fuentes de `Javier/WORKING_WITH_JAVIER.md`; no conviertas una pantalla existente en autoridad por sí sola.
2. **Conserva el estado encontrado antes de corregir.** Captura render y árbol por ID del frame y los estados incluidos. Registra padres, orden, visibilidad, regiones, wrappers, instancias y componentes de origen, propiedades, modos, bindings, reacciones y destinos; conserva también medidas y comportamiento de scroll. Declara qué descendientes o consumidores no pudiste leer. Esta fotografía separa hallazgo previo de cualquier edición posterior.
3. **Reconstruye la responsabilidad de la pantalla.** Identifica qué tarea, información, decisión y acción corresponden a cada región; distingue región funcional, componente, elemento interno y agrupador instrumental con `Design/Figma/SCREEN_STRUCTURE_GUIDE_GENERAL.md` §§3–4 y `Design/Design Lead/DESIGN_PRINCIPLES.md`. Un `Frame N`, un wrapper o dos bloques parecidos son preguntas de anatomía: su nombre o aspecto no autorizan borrado, reanidado ni componentización.
4. **Contrasta estructura y adaptación.** Revisa auto-layout, dirección, padding, gaps, HUG/FILL/FIXED y razón de cada medida fija; crecimiento con contenido corto, largo y vacío; clipping, overlays, persistencia, propietario y límites del scroll. Compara cada viewport y estado que el alcance incluya: qué se apila, alterna o conserva, área de toque y lectura según ancho, distancia y tipo de entrada. El viewport canónico conserva sus límites; una referencia extendida no demuestra por sí sola que el scroll funcione. Cita `Design/Figma/SCREEN_STRUCTURE_GUIDE_GENERAL.md` §§6–7 y el contrato local, no un breakpoint supuesto.
5. **Contrasta el sistema y el aspecto resuelto.** Para cada región representativa, comprueba componentes disponibles y procedencia de sus instancias, tipografía por estilo o variable y su rol, fills, strokes, color por rol, espaciado, radio y efectos o sombras según `Design/Design Systems/SCREEN_DESIGN_RULES.md` y `Design/Design Lead/DESIGN_PRINCIPLES.md`. Registra excepciones y valores crudos visibles. Lee bindings y valores efectivos en los modos pertinentes; compara capturas renderizadas por modo y estado. Una cuenta de bindings al cien por ciento no prueba rol correcto, contraste ni apariencia. Distingue fallo de la instancia o del layout consumidor de fallo del master, que corresponde al DS Manager.
6. **Comprueba estados, interacción y accesibilidad observable.** Contrasta los estados existentes con el flujo o criterios de UX: default, hover, focus, active, disabled, loading, empty, error, apertura y retorno cuando apliquen. Relee las reacciones y sus destinos por origen; distingue control dibujado, conexión escrita y recorrido reproducido. Inspecciona foco, contraste, área de toque, truncado y lectura de contenido según `Design/Figma/SCREEN_STRUCTURE_GUIDE_GENERAL.md` §§10 y 12 y `Design/Design Lead/DESIGN_ACCESSIBILITY.md`. Un flujo ausente se declara; no se inventa ni se cablea durante la auditoría.
7. **Aplica Naming y File Architect a lo observado.** Una vez establecida la responsabilidad de cada nodo, construye el mapa `ID · actual → propuesto` con `Design/Figma/NAMING_STRUCTURE_GUIDE.md` §§3–5 y clasifica cada nombre: pantalla o sección, propuesta sin edición en esta pasada; capa interna propia de la pantalla con responsabilidad inequívoca, posible renombre autorizado; componente, propiedad, valor o slot, propuesta al DS Manager. Aplica el criterio de File Architect al mapa y la residencia entre páginas cuando afecten la lectura. El Screen Designer decide la agrupación funcional de flujos y secciones dentro de la página; Naming contrasta cómo se nombran. Consulta al oficio respectivo ante una decisión nueva o ambigüedad. La auditoría no crea ni mueve páginas ni reagrupa secciones; el nombre de una capa no decide si su contenedor debe existir.
8. **Evalúa candidatos a componente sin crearlos.** Busca primero equivalentes en la librería del proyecto y, si corresponde, en base y derivado. Para cada patrón observado registra responsabilidad, anatomía, configuraciones, estados, comportamiento y reglas de contenido, con usos reales por ID y sus diferencias. Un hallazgo de una sola pantalla se conserva como hipótesis con evidencia insuficiente; la repetición visual tampoco prueba que deba ingresar al DS. Indica si parece composición de piezas existentes, variante de una familia, `[draft]` local ya existente o posible pieza nueva. Contrasta los nombres propuestos de componentes y de su interfaz con `Design/Figma/NAMING_STRUCTURE_GUIDE.md` §6 sin renombrarlos. Entrega al DS Manager el mapa de usos, la anatomía observada y las preguntas de API; él decide si se convierte en componente, su interfaz y su sistema de destino. La auditoría no crea ni toca un master.
9. **Separa hallazgos de cambios autorizados.** Por defecto termina en informe. Si Javier autorizó renombres, aplica solo los de capas internas propias de la pantalla, inequívocas y fuera de instancias, masters y slots, en los mismos IDs y después de la fotografía previa. Nombres de pantalla, sección, componente, propiedades, valores y slots, además de tokens, anatomía, layout, reacciones y comportamiento, quedan como propuestas para sus dueños. Tras la última escritura relee IDs y padres, claves de componentes, asociaciones de variantes, vínculos de instancias, API, propiedades, modos, bindings, reacciones, medidas y capturas. Si cualquiera cambió fuera del nombre autorizado, informa la divergencia y no declara el renombre como neutro.
10. **Entrega un dictamen acotado.** Agrupa hechos comprobados, inferencias, propuestas y puntos no verificados. Para cada hallazgo indica ID, evidencia, fuente esperada, efecto para la tarea, cambio propuesto y dueño de la decisión. Señala el conjunto de estados, modos, viewports y descendientes medidos, y lo que quedó fuera; incluye antes y después solo si hubo edición. Los candidatos se remiten al DS Manager con su mapa de usos. Un rediseño, una corrección funcional, una migración o una skill de construcción se abren como encargos separados.

## Frontera de la receta

Esta revisión puede encontrar que una pantalla necesita una región distinta o que una pieza del DS falla. Eso es un diagnóstico, no autorización para rehacer la pantalla o modificar un master. El Screen Designer responde por la estructura y aplicación dentro de la pantalla; UX por recorrido y estados de experiencia; Naming por la forma de los nombres; File Architect por la arquitectura del archivo; DS Manager por componentes y tokens. La consulta entre oficios se hace cuando el hallazgo requiere una decisión nueva, no como espera obligatoria en cada auditoría.

Si se usa Figma, se entra según `Design/Design Lead/DESIGN_GOVERNANCE.md` §12 y se consulta `Design/Figma/FIGMA_GOTCHAS.md` para lecturas por herramienta y para toda edición autorizada. Si no se puede obtener árbol, captura o render de un modo, el informe dice «escrito, no verificado» respecto de esa parte; no sustituye la evidencia con una suposición.
