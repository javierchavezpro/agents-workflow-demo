> Reading copy generated on 2026-10-26 (demo 2026.10) from `FILE_NAMING.md`: complete. The instructions are the original Spanish ones. Links to files outside this copy are shown as paths in code. See `PROVENANCE.md` at the root of this folder.

# Cómo se nombran los archivos y las carpetas

> **El canon de los nombres en disco.** Aquí se decide cómo se llama un `.md`, una carpeta o un género nuevo del sistema. Lo administra el **Super Agent Admin**, y vive en la raíz y no dentro de su carpeta porque lo consume cualquiera que cree un archivo, igual que `GLOSSARY.md` vive aquí siendo del Voice Architect.
> **Nace el 2026-08-17**, por decisión de Javier al resolver que nombrar en disco no es jurisdicción del Naming Architect. No es una regla nueva: es la que ya se aplicaba repartida entre `AGENTS.md` y `System/Super Agent Admin/ROLE_CREATION.md`, reunida en un solo lugar para que el género siguiente no vuelva a decidir idioma, caja y fecha desde cero.
> Si vas a escribir aquí, usa las reglas de `Writing/VOICE_CONTRACT_DOCS.md`. **Actualizado en la fuente: 2026-10-17.**

## La frontera, que es lo primero

Nombrar no es una jurisdicción sino tres, y se separan por dónde vive la cosa nombrada.

| Qué nombras | De quién es | Su canon |
|---|---|---|
| Archivos y carpetas del repositorio | **Super Agent Admin** | este archivo |
| Lo que se genera dentro de Figma: páginas, frames, capas, componentes, animaciones | **Naming Architect** | `Design/Figma/NAMING_STRUCTURE_GUIDE.md` |
| Commits, ramas y repositorios | **Tech Lead**, pauta 3, y la operación diaria el **Git Manager** | `Dev/Tech Lead/TECH_GOVERNANCE.md` |

La prueba para separarlas: si el nombre se escribe en el disco, es de aquí; si se escribe dentro de una herramienta, es de quien administra esa herramienta. Los nombres de componentes y tokens de un design system son otra cosa todavía, y los fija el contrato de ese DS.

## Las dos capas, que es de donde sale todo lo demás

**Inglés para lo que consume el sistema, español para lo que lee una persona.** El principio es del §1 del canon de Figma, del Naming Architect, y se cita en vez de copiarse: allá gobierna las capas de un archivo y aquí las del disco, pero es la misma idea.

**La infraestructura va en inglés y en `UPPER_SNAKE_CASE`**, porque se cita por ruta desde cualquier parte del sistema y el nombre tiene que ser estable y escaneable: `AGENTS.md`, `DS_MANAGER_CHANGELOG.md`, `AUDIT_REPORT_GUIDE.md`.

**El documento que una persona busca por su tema va en español, con espacios, en minúsculas salvo la primera palabra:** `Selectores en fila 2026-08-14.md`, `Elecciones que ramifican.md`. Ese nombre es la portada, no el título; el título completo vive en el H1 y puede ser tan largo como haga falta.

**Las carpetas de categoría y de oficio van en título con espacios**, como se dicen en voz alta: `Design/`, `Dev/Tech Lead/`, `Design/DS Manager/`.

**El caso es la regla; el idioma lo hereda el género.** `UPPER_SNAKE_CASE` no se negocia, porque de ahí salen la estabilidad y el escaneo. El inglés es el **valor por defecto de un género nuevo**, no una ley sobre los que ya existen: **cuando un género ya tiene nombre, lo conserva aunque esté en español**, porque la consistencia dentro de un género vale más que la uniformidad del idioma. El caso vivo es `PENDIENTES`, en nueve archivos incluido el tablero de Javier; renombrarlos costaría nueve mudanzas con sus punteros para no resolver nada. Declarado el 2026-08-17, cuando el Project Manager señaló que la regla y la práctica se contradecían.

**Un documento nace con su nombre definitivo, aunque sea su primera versión.** Una guía en borrador ya se llama `..._GUIDE.md` y lo dice en su cabecera; `PROPOSAL` es solo del género propuesta, el que pide una decisión y se retira cuando se decide. La diferencia entre los dos está en «Propuesta», en `GENRES.md`. Escrito el 2026-10-17, cuando dos guías nacieron con nombre de propuesta (C-ADMIN-015).

**La forma es de este canon; la palabra nueva se ratifica con el Voice Architect.** Cuando un nombre estrena vocabulario que el sistema todavía no usa —`HISTORIAL` donde antes solo había `WORKLOG`, por ejemplo— la elección de esa palabra es voz, no estructura, y se le ratifica a él, que es lo que Javier repartió el 2026-08-10. Lo que no se le pregunta es el caso, el género, la posición de la fecha ni el apellido: eso es forma y se decide aquí. **Escrito el 2026-08-18**, porque hasta ese día su guía decía que los nombres de archivo del sistema eran suyos y esta decía que eran del administrador; dos documentos declarándose dueños del mismo dato es la regla 9 rota, y lo reportó un oficio antes que nosotros.

**Un renombre pasa por encima del documento que lo describe.** El encargo, el pendiente y la entrada de buzón que explican un renombre están escritos con los nombres viejos, así que el barrido los reescribe y quedan diciendo «renombrar `X` a `X`». Pasó el 2026-08-18 con la mudanza de esta categoría. **No se repara el texto: se cierra el pendiente**, porque en cuanto el renombre corre el encargo dejó de tener sentido; lo que se conserva es lo que pasó, y eso vive en el changelog y en el worklog.

**Una traducción no es una pieza nueva: lleva subextensión de idioma.** La regla del género de reporte dice que las piezas de un documento comparten raíz exacta y solo cambian de extensión, porque cualquier palabra añadida las separaría al ordenar. Una copia en otro idioma no cabe ahí —no es otra pieza, es la misma en otra lengua— y por eso va como `<asunto> AAAA-MM-DD.en.html`, con el código de idioma antes de la extensión. Quedan contiguas, el idioma es inequívoco, y el asunto no gana una palabra que no le corresponde. **Solo se marca lo que no es el idioma de origen:** el archivo sin marca es el original, sea cual sea su lengua. Declarado el 2026-08-18, al nacer las sesiones de trabajo, que llevan copia en inglés cuando la sesión fue en español. Avisado al Naming Architect por cortesía, porque el criterio del que salió la forma original fue suyo: la decisión no pasa por él, que su canon es el de Figma.

**El token de un proyecto se declara en su recepción.** Un proyecto prefija sus piezas con un token corto, `CLIENTE1_LOG.md` o `CLIENTE2_PENDIENTES.md`, y ese token se fija en el `AGENTS.md` de ese proyecto, que es donde viven sus decisiones locales. **Se declara porque colisiona:** `C1_` ya identifica a [cliente 1] DS dentro de Embit DS, así que el proyecto [cliente 1] no puede usarlo, y sin declaración cada quien elige el suyo. Si un archivo anterior conserva un token que ya no es el del proyecto, **la excepción se declara junto al token** en vez de renombrarlo: renombrar cuesta rutas y la excepción cuesta una línea.

La frontera entre las dos capas se ve dentro de una misma carpeta: `AUDIT_REPORT_GUIDE.md` es infraestructura y sus reportes no, porque la guía dice cómo se trabaja y el reporte es el trabajo.

## El apellido lleva el ámbito, no la carpeta

Un documento que se cita por ruta desde fuera de su carpeta lleva su ámbito en el nombre: `DESIGN_INBOX.md` dice qué es aunque la categoría se reorganice, y `DS_MANAGER_CHANGELOG.md` también. **La carpeta donde vive es comodidad, no significado**, y por eso un renombre de carpeta no debería obligar a renombrar lo de dentro.

`INBOX.md` es la única excepción: es el buzón de todos y por eso no necesita apellido.

## Cuándo el nombre lleva fecha

**Al final, y solo cuando el género garantiza colisión por asunto.** Un reporte de auditoría del mismo asunto se repite con los años y cada uno es un archivo nuevo, así que la fecha desempata; un changelog o una guía existen una sola vez y fecharlos sería ruido. Al final y no al principio porque lo que se busca es el asunto: la fecha ordena dentro de un mismo tema, no por encima de todos.

Cuando la lleva, es la misma fecha que declara el documento por dentro. Dos fechas distintas para el mismo archivo son dos dueños del mismo dato.

## Cuándo el nombre NO lleva palabra de género

**Cuando la carpeta ya la dice.** Nada de `REPORTE_` dentro de `Reports/`. La distinción es cómo se cita el documento: un buzón o un changelog cargan su género porque se citan por ruta desde cualquier parte del sistema; una pieza que se cita por su título y desde la capa vecina no lo necesita.

## Los nombres que crea un alta

Los fija este canon y `System/Super Agent Admin/ROLE_CREATION.md` los aplica; si alguna vez divergen, manda lo de aquí.

| Documento | Cómo se llama | Ejemplo |
|---|---|---|
| Carpeta de categoría | Título, con espacios | `Dev/` |
| Recibidor de la categoría | `<CATEGORÍA>.md` | `DEV.md` |
| Changelog de la categoría | `<CATEGORÍA>_CHANGELOG.md` | `DEV_CHANGELOG.md` |
| Buzón de la categoría | `<CATEGORÍA>_INBOX.md` | `DEV_INBOX.md` |
| Carpeta de oficio | Título, con espacios | `Dev/Git Manager/` |
| Guía del oficio | `<OFICIO>.md` | `GIT_MANAGER.md` |
| Changelog del oficio | `<OFICIO>_CHANGELOG.md` | `GIT_MANAGER_CHANGELOG.md` |
| Buzón del oficio | `<OFICIO>_INBOX.md` | `QA_INBOX.md` |
| Canon de un lead | `<TEMA>_GOVERNANCE.md` | `TECH_GOVERNANCE.md` |

**Un oficio de dos palabras se aprieta en el archivo y se separa en la carpeta:** `Dev/Git Manager/GIT_MANAGER.md`. La carpeta es para el ojo y el archivo para la cita.

## Cuando un género nuevo necesita convención

Se decide aquí, se escribe en la guía de ese género, y **este canon solo gana la regla si generaliza.** Lo específico vive con su género y lo cita; si sube todo aquí, este archivo se vuelve un catálogo y deja de ser un canon.

El ejemplo trabajado es `AUDIT_REPORT_GUIDE.md`, sección «Cómo se llaman los archivos»: la convención de los reportes de auditoría, fijada el 2026-08-17 por el Naming Architect antes de que la frontera se moviera. De ahí salieron los tres principios de arriba —las dos capas, la fecha y la palabra de género—, y por eso la sección se queda donde está y con su atribución.

## Las raíces del sistema y cómo se citan

*Vivía en el encabezado de `AGENTS.md` hasta el 2026-10-07, cuando se adelgazó la puerta de entrada; se mudó entero.*

**Y hay dos cosas llamadas «Dev». Nunca digas «Dev» a secas.** `Dev/`, dentro de este repositorio, es **la categoría de desarrollo del sistema de agentes**: el Tech Lead, QA y el Git Manager, y el trabajo de desarrollo de los propios agentes. La otra es **la raíz externa de desarrollo**, `~/Dev/`, carpeta hermana de este repositorio en el disco de Javier, donde viven sus proyectos de código —repositorios ejecutables, cursos, experimentos— y que **no es del sistema de agentes**: ninguna de sus carpetas entra al mapa por existir. Al escribir, la de aquí se cita como `Dev/` con su ruta relativa, y la de allá se nombra completa, **la raíz externa de desarrollo**, con su ruta absoluta, porque una ruta relativa que salga de este repositorio no significa lo mismo en Cowork que en Codex. Decisión de Javier del 2026-08-27, tomada antes de mapear nada para evitar la colisión que costó el renombre de [cliente 1]. Junto a las categorías está `Projects/`, donde viven los `.md` de los proyectos profesionales y de producto que ya opera este repositorio. **La memoria operativa de los proyectos creativos personales vive en la carpeta hermana `../Projects/Agents/`**, y su recepción está en `../Projects/AGENTS.md`; el método transversal, los oficios y las reglas comunes siguen teniendo su fuente aquí. Los archivos pesados de cualquier proyecto no entran al repositorio que guarda su memoria, y la recepción de ese proyecto dice dónde están. Toda referencia entre documentos es relativa y nunca una ruta de máquina, porque los repositorios se clonan en lugares distintos. Las carpetas que no aparezcan aquí ni en el recibidor creativo enlazado no son del sistema de agentes, estén donde estén: una carpeta se mapea cuando Javier la nombra, no cuando aparece en el disco. **`skills/` y `.agents/skills/` son infraestructura declarada:** la primera guarda los métodos canónicos y la segunda los adaptadores que Codex descubre. No son paradas de lectura del sistema; se abren cuando el trabajo invoca una habilidad o su mantenimiento.

## Renombrar tiene un costo, y hay que pagarlo entero

Un renombre rompe las rutas que apuntaban al nombre viejo, y en este sistema eso ya pasó dos veces. Quien renombra:

1. **Reescribe las rutas vivas** que apuntaban ahí, y las verifica contra el disco. Cuidado con las dos formas de romperlas: apuntar a algo que se movió, y ser el archivo que se movió y quedarse con rutas que ya no resuelven desde su nueva casa.
2. **No toca las entradas fechadas.** Una ruta rota dentro de una entrada firmada era cierta el día que se escribió y no es un error que arreglar.
3. **Corrige lo que el nombre viejo prometía.** Si el archivo dejó de anunciar lo que es, quien lo lee por el nombre se equivoca: pasó el 2026-08-12 con `AGENT_ADMIN_WORKLOG.md`.
4. **Le deja una línea al Git Manager** si la carpeta es del mapa, según los disparadores de `AGENTS.md`.

## Registro del archivo

