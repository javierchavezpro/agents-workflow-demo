> Reading copy generated on 2026-10-26 (demo 2026.10) from `AGENTS.md`: the entry point; two operational sections omitted. The instructions are the original Spanish ones. Links to files outside this copy are shown as paths in code. See `PROVENANCE.md` at the root of this folder.

# Agents, recepción del nivel transversal

> Esta recepción es la puerta del sistema y solo redirige: el detalle vive en los `.md` específicos, y cada puerta de abajo dice hasta dónde llega tu lectura. Lee solo lo que tu tarea pida. Se edita, no se reemplaza.
> El sistema vive en `agents-workflow/`, la raíz de todo lo que sigue.
> **Dónde trabajas, al 2026-08-27: siempre sobre la copia local que vive en la computadora de Javier, nunca contra GitHub.** Cómo la alcanzas depende de dónde corras: en Cowork llegas por el puente con su computadora, y si está apagada no hay sistema; en Codex ya estás dentro de la carpeta. En los dos casos el archivo que lees y escribes es el mismo y es esa copia local: **es la única fuente viva, y lo que no esté escrito ahí no existe para el sistema.** **El repositorio en GitHub es respaldo:** guarda el historial, y **sincronizar con el remoto es del Git Manager** — no clones, no traigas ni publiques ahí por tu cuenta. Trabajar contra el remoto se intentó y se descartó el 2026-08-10: obligaba a darle una credencial a cada conversación, que es peor problema que el que venía a resolver. Que tu copia local esté versionada no cambia nada de lo anterior: **el estado del git lo reporta sola la habilidad `skills/daily-backup/`, y cualquier otra operación de git pasa por ese oficio**, corras donde corras. **Quien vuelva a mover esto edita esta línea**, que es la que dice en qué mundo estás trabajando.
> **Antes de trabajar, comprueba que estás en el repositorio y no en una copia parcial. Son diez segundos y evita un día entero de conclusiones falsas.** Tienen que existir **a la vez** `AGENTS.md`, `INBOX.md` y `PROJECTS.md`, y el repositorio pasa de **200 archivos `.md`**. Si ves este archivo pero no los otros dos, **no estás en el repositorio**: estás en una copia subida a tu contenedor, que lleva su nombre y su estructura y es una fracción suya. Pasó el 2026-09-02: una conversación concluyó que no existía ningún buzón en todo el sistema, con los tres en el disco y 208 `.md` a su lado. **Un archivo que no ves no es un archivo que no existe**, y la diferencia no se deduce, se comprueba. Si la comprobación falla, **no trabajes con lo que haya**: dilo, porque cualquier cosa que escribas encima nace de un mapa incompleto.
> **Y comprueba qué eres antes de escribir: manager de tu oficio, o una conversación que trabaja en él.** La tabla de `INDEX.md` dice quién ocupa hoy la silla de cada oficio, con su modelo; compárate con ella. **Si coincides, la silla es tuya y respondes por los documentos generales del oficio. Si no coincides, no la tomes por tu cuenta:** trabajas en lo que Javier te encargó y se lo dices. Y si la silla está vacía porque su manager no está, sentarte no le quita nada a nadie —lo dice `INDEX.md`— pero **se declara escribiendo tu propia fila**, que es lo que esa tabla pide desde que existe. Nadie tiene hoy instrucción de hacer esta comparación, y por eso el 2026-09-02 dos conversaciones ejecutoras se creyeron managers el mismo día. **Cuesta una lectura y evita que el registro atribuya a un titular lo que hizo otro.**
> **Hay dos cosas llamadas «Dev»; nunca digas «Dev» a secas.** `Dev/` es la categoría de desarrollo de este repositorio; `~/Dev/` es la **raíz externa de desarrollo**, donde vive el código de Javier, y no es del sistema de agentes. Los proyectos creativos personales viven en la carpeta hermana `../Projects/Agents/`. Toda referencia entre documentos es relativa, y una carpeta se mapea cuando Javier la nombra, no cuando aparece en el disco. El detalle está en `FILE_NAMING.md`, «Las raíces del sistema y cómo se citan».
> **Si tocas una habilidad:** la fuente es `skills/<nombre>/SKILL.md`. Claude ejecuta una copia instalada en la cuenta de Javier y Codex un adaptador bajo `.agents/skills/`, que no copia el método: manda leer la fuente. Quien edita la fuente avisa en el mismo tramo para reinstalarla, y si hay adaptador verifica los dos. Cómo se instala, cómo se comprueba y los límites de Claude, en `System/Ops Manager/OPS_ENVIRONMENT.md`.
> **Cuándo hay que avisarle al Git Manager.** Es el oficio que opera el repositorio y no está de guardia, así que se le convoca: **le abres una conversación con el script de buzones** cuando vayas a crear o renombrar una carpeta del mapa · meter al repositorio un archivo pesado o binario · tocar `skills/` · arrancar un repositorio nuevo · escribir algo que parezca una llave, una contraseña o un token. **Cinco y no más, a propósito:** una lista larga no la sigue nadie. Fuera de esos casos no hace falta avisar, y el estado del git lo reporta la habilidad `skills/daily-backup/` sola, desde cualquier conversación.
> **Y lo que una herramienta genera en volumen no entra al repositorio.** Al repositorio entra lo que alguien escribe y se lee como texto; los volcados de datos y las capturas van al Drive de Javier, en `Drive/Projects/agents-workflow/<Proyecto>/Datos` o `Capturas`, o en `_General/` si no son de ningún proyecto, y el documento del proyecto los cita por su ruta. Decisión de Javier del 2026-10-07; el porqué y el procedimiento están en `Dev/Git Manager/GIT_MANAGER.md`, «Qué entra al repositorio y qué va a Drive». Un archivo escrito que pese mucho sigue siendo uno de los cinco casos de arriba.
> **La organización es por categorías que agrupan conocimiento por tema, nunca por proyecto.** Cuáles hay y por qué lo dice `INDEX.md`, «Las categorías de la carpeta Agents»; dónde termina cada oficio, `ORGANIGRAMA.md`. Un oficio nuevo lo da de alta el Super Agent Admin, y cómo se nombra lo que creas está en `FILE_NAMING.md`. **Actualizado en la fuente: 2026-10-07.**

## Las tres puertas

Esta sección te ubica: son tres rutas de lectura y solo una es la tuya. Abrir lo que no te toca gasta tokens y te contamina el trabajo con reglas ajenas.

**1. Tu tarea es de un proyecto.** Lee `Javier/WORKING_WITH_JAVIER.md` y sigue a `PROJECTS.md`, que reúne los proyectos y dice qué oficio se toma en cada uno. Hasta esa parada no hace falta saber qué oficios existen.

Una tarea es de proyecto cuando Javier nombra el proyecto, o cuando pide algo que solo existe dentro de uno: una pantalla, un archivo de Figma, un design system, un changelog, un componente. En caso de duda, la pregunta va antes que la lectura: casi todo el trabajo vivo aquí es de proyectos, y una pregunta corta cuesta menos que leer de más.

**2. Tu tarea no es de un proyecto.** Si es simple, o todavía no tienes una, tu arranque es `FAST_TRACK.md`: el mínimo para trabajar con Javier, en un resumen que no es fuente, y su última sección te regresa aquí cuando la tarea crezca. Para lo demás, lee `Javier/WORKING_WITH_JAVIER.md`, que son las reglas de trabajo con él y aplican a cualquier cosa, y detente ahí. `INDEX.md` solo entra si la tarea es entender cómo funciona el sistema. Después, de la tabla de abajo, la fila de tu caso y nada más.

**3. Tomas el rol de administrador.** Lee `System/Super Agent Admin/SUPER_AGENT_ADMIN.md` y lo que ese archivo mande. Es el único rol que lee de todo, porque su trabajo es la consistencia entre las partes. Fuera de ese rol, ni ese archivo ni su buzón sirven.

## A dónde ir según tu tarea

| Vas a… | Lee… |
|---|---|
| Trabajar con Javier en CUALQUIER cosa (reglas generales) | `Javier/WORKING_WITH_JAVIER.md` · SIEMPRE primero |
| Tarea simple, o todavía sin tarea (el arranque corto) | `FAST_TRACK.md` · resumen de las reglas, no fuente; te regresa aquí cuando la tarea crezca |
| Trabajar en un proyecto, o averiguar si tu tarea es de uno | `PROJECTS.md` · índice de proyectos y qué oficio se toma en cada uno |
| Trabajar en un proyecto creativo personal | `../Projects/AGENTS.md` · recepción externa; las reglas y los oficios siguen teniendo su fuente aquí |
| Desarrollar lore, consolidar canon narrativo o revisar continuidad | `Writing/Lore Writer/LORE_WRITER.md` |
| Saber qué piezas tiene un proyecto y dónde se registra cada cosa | `Product/Project Manager/PROJECT_GUIDE.md` · el canon de la capa de proyecto; lo lee cualquiera que trabaje en uno |
| Proponer alcance, etapas o priorización de un producto | `Product/Product Manager/PRODUCT_MANAGER.md` · canon (vacío al alta) `PRODUCT_SCOPE_GUIDE.md` |
| Coordinar a los oficios de un proyecto, o arreglar su forma | `Product/Project Manager/PROJECT_MANAGER.md` |
| Arrancar un proyecto o un subproyecto nuevo | `Product/Project Manager/PROJECT_GUIDE.md` · ficha única, paquete mínimo por tipo, activación y encargos |
| Producir o entregar una pieza de medio fuera de Figma (video, audio, imagen raster): formato, códec, alfa, compresión, alojamiento | `Design/Media Editor/MEDIA_EDITOR.md` |
| Guardar una **sesión de trabajo** («guarda esto como una sesión») | `Work Sessions/WORK_SESSIONS.md` · qué es, en qué carpeta va y qué lleva dentro; la guía de tipo de esa carpeta dice lo demás |
| Preparar una sesión para enseñarse, censurarla o traducirla | `Presentation/Presentation Editor/PRESENTATION_EDITOR.md` |
| Presentar un reporte, una investigación o un tablero; consultar sus índices | `Presentation/Presentation Editor/PRESENTATION_EDITOR.md` |
| Consultar o producir el overview visual de un proyecto | `Product/Project Manager/PROJECT_GUIDE.md` §Overview · género en `GENRES.md`; salidas vía Presentation Editor / Ops |
| Ya tienes oficio, porque Javier te lo dio o `PROJECTS.md` te lo asignó | Su guía, sus pendientes y su log, donde ese archivo te haya mandado; y de los buzones, tu bandeja |
| Escribir cualquier cosa en nombre de Javier (documentos, copy, portafolio, redes) | `Javier/JAVIER_VOICE.md` · la voz |
| Pedir o redactar **contenido** que suene a Javier (ideas, posts, ángulos; base fija sin memoria de chat) | `Javier/JAVIER_CONTENT_PROFILE.md` · perfil de contenido; la voz sigue en `JAVIER_VOICE.md` |
| Escribir o reescribir un `.md` de este sistema | `Writing/VOICE_CONTRACT_DOCS.md` · el contrato que fija las dos densidades y qué vocabulario se puede usar |
| Evaluar o adoptar una idea, un repositorio o una herramienta de fuera | `System/Super Agent Admin/FUENTES_EXTERNAS.md` · «Cómo se adopta un criterio de fuera» |
| Usar un término del sistema, o saber si puedes usarlo sin explicarlo | `GLOSSARY.md` · si está ahí se usa tal cual; si no está, entra al glosario o no se usa |
| Pedirle o avisarle algo a otro oficio, de tu categoría o de otra | Una conversación: `skills/registrar/scripts/conversacion.py abrir`, que elige el buzón por ti. Reglas en `INBOX.md`, «Instrucciones» |
| Hablar con el Manager de tu propio oficio, o con sus Delegados o Workers | El buzón interno de tu oficio, en líneas, con `skills/registrar --para` tu oficio y `--a` el cargo |
| Reportarle al administrador algo del SISTEMA (estructura, reglas comunes, alta de oficio) | Una conversación con `--para "Super Agent Admin"`: cae en `ADMIN_INBOX.md`, aunque lleve copias |
| Tomar el rol de Super Agent Admin (definir el sistema) | `System/Super Agent Admin/SUPER_AGENT_ADMIN.md` |
| Correr una habilidad o una operación recurrente | `System/Ops Manager/OPS_MANAGER.md` · el oficio que ejecuta lo que otros definen |
| Conectar, probar o documentar un servicio externo (conector o MCP), o descubrir por qué falla | `System/Ops Manager/SERVICES.md` · lo que averigües de una conexión se escribe ahí, no en tu memoria, que ninguna otra conversación puede leer |
| Registrar meta-trabajo transversal | `System/Super Agent Admin/SUPER_AGENT_ADMIN_WORKLOG.md` |
| Saber si algo es tuyo, o de quién es | `ORGANIGRAMA.md` · qué áreas hay, de qué responde cada oficio y **dónde termina uno y empieza el siguiente**. Es la fuente de las fronteras: si una guía dice otra cosa, manda ese archivo. **Solo lo edita el Super Agent Admin**; lo que le falte o esté mal se pide en `ADMIN_INBOX.md` |
| Dar de alta una categoría, un oficio o un lead | `System/Super Agent Admin/ROLE_CREATION.md` · el procedimiento completo, con qué se crea según el nivel |
| Enterarte de qué cambió en el sistema desde la última vez que entraste | `CHANGELOG.md` · lo más reciente arriba |
| Nombrar un archivo, una carpeta o un género nuevo | `FILE_NAMING.md` · el canon de los nombres en disco |
| Escribirle a todos los oficios a la vez | **Es un aviso: informa y no pide.** Nadie es su destinatario único, así que nadie puede cerrarlo y **no cuenta como espera** en ningún tablero; sale aparte en `ACTIVIDAD`. Se archiva por antigüedad como cualquier otra entrada. Decisión de Javier del 2026-09-02 |
| Instalar una habilidad, publicar un tablero, o entender por qué una copia envejece | `System/Ops Manager/OPS_ENVIRONMENT.md` · cómo se opera el entorno, no el sistema. Lo mantiene el Ops Manager |
| Abrir o cerrar un pendiente de tu oficio | **Solo tu lista.** Si tu lista vive en otro archivo, **decláralo** con `> Lista en: ``RUTA.md`` ` en la primera línea de tu sección de pendientes: el generador lee esa marca y no adivina de la prosa. Un pendiente cerrado **se borra**: su rastro queda en tu changelog. **No corras el generador ni publiques:** eso es del Ops Manager en una sola pasada, por la pauta 10 de `System/Super Agent Admin/SYSTEM_GOVERNANCE.md`. **Y todo pendiente declara qué lo detiene**, en la sección de abajo |
| Cambiar tu prompt de arranque | Tu guía, que es la fuente. Registra tu tramo y sigue: `ARRANQUE` lo regenera el Ops Manager en su pasada (pauta 10 de `System/Super Agent Admin/SYSTEM_GOVERNANCE.md`) |
| Cambiar un rol, buzón, backlog o skill | Registra tu tramo con `skills/registrar` y sigue. **No regeneres tableros ni le avises al Ops Manager:** su pasada compara cada fuente con su tablero (`decidir.py`) y encuentra sola lo que cambió. Pauta 10 de `System/Super Agent Admin/SYSTEM_GOVERNANCE.md`; el aviso se retiró el 2026-09-28 por decisión de Javier |
| Saber qué hay en `Javier/Dashboard/` | Sus tableros, que solo lee él. **Ninguno es fuente:** espejan lo que ya está escrito en cada oficio, así que no se citan como autoridad ni se leen para trabajar |
| Entender el sistema completo como humano | `INDEX.md` |

**La cadena completa:** este archivo, `PROJECTS.md`, la recepción del proyecto —dentro de este repositorio o en la capa creativa enlazada—, el oficio que te toque y el ámbito de trabajo. Cada parada da el contexto de la siguiente. Nadie salta pasos hacia adelante ni lee de más hacia los lados.

## Los géneros de documento

**El catálogo vive en `GENRES.md`:** qué es cada tipo de documento, quién lo escribe y quién lo lee. Ábrelo cuando vayas a crear un documento o cuando no sepas a qué registro va lo que hiciste; no es lectura de arranque. De ahí solo necesitas tres cosas al llegar:

- **Corre tu bandeja y resuelve lo que puedas**, una vez y antes del encargo: `python3 skills/registrar/scripts/conversacion.py bandeja "Tu Oficio"`. Los buzones entre oficios son conversaciones y se escriben con ese script; las reglas están en `INBOX.md`, «Instrucciones». Cierras lo tuyo, no lo dirigido a otro.
- **En un archivo de historia no se corrige ninguna entrada.** Changelogs, worklogs y buzones son entradas fechadas y firmadas: lo que dicen era cierto el día que se escribió.
- **Un pendiente cerrado se borra**, no se tacha: su rastro queda en el changelog de quien lo hizo.

## Cerrar el pendiente de otro oficio

**Antes de cerrarlo, comprueba que el archivo que resolviste sea exactamente el que la línea nombra.** Si no coincide, **conserva la línea** y reporta el hallazgo en vez de borrarla. Y cuando sí lo cierres, **avísale al oficio dueño en su buzón**, para que quede rastro fuera de git.

Decisión de Javier del 2026-09-02, elevada a regla transversal desde un caso del Design Lead: un cierre equivocado borró un pendiente vivo al confundir **dos capas locales del Screen Designer con nombres parecidos**. El caso completo vive en `Design/DESIGN_INBOX.md`, entrada del 2026-09-01. **Lo que la regla protege no es el archivo, es la línea:** un pendiente borrado no deja hueco, y nadie echa de menos lo que ya no se ve.

## Qué detiene un pendiente

**Todo pendiente declara su categoría, y no se infiere al leerlo.** Decisión de Javier del 2026-08-19: dos líneas que cuestan diez segundos y una tarde no pueden verse igual, porque quien vuelva mañana no sabe por dónde empezar, y una tarea programada que actúa sobre una categoría supuesta hace trabajo que no le tocaba.

**La marca va al final de la línea del pendiente**, en su propia lista:

```
· detiene: requiere decisiones — el canon se llena con Javier
```

| Categoría | Qué significa |
|---|---|
| **requiere decisiones** | Necesita que Javier decida algo antes de poder avanzar |
| **requiere tokens** | El trabajo cabe, pero no en lo que queda de sesión |
| **fin de jornada laboral** | Apareció cuando ya no podía atenderse. **Es la única que caduca sola:** en la siguiente sesión deja de estar detenida, y si nada más la frena pasa a «ninguno». Un pendiente con esta marca que lleva semanas quieto está mal clasificado, no esperando |
| **espera a otro oficio** | Depende de la respuesta de otro oficio, no de una acción propia. Añadida el 2026-08-19 con el primer caso: QA esperando al Tech Lead |
| **espera fecha** | Solo depende del calendario: no falta ninguna decisión ni ningún otro oficio. **El motivo lleva la fecha en que despierta**, `· detiene: espera fecha — 2026-10-30`, para que se lea cuándo vuelve a estar libre. Decisión de Javier del 2026-10-14 (C-GENERAL-061), con sus primeros casos en Litteratium |
| **requiere una serie de acciones** | Nada lo bloquea salvo que es largo y hay que hacerlo por partes |
| **en curso** | **Ya empezó y no está terminado.** Es la única que describe trabajo en vuelo, y por eso su motivo carga dos datos y no uno: **qué falta y desde cuándo está parado** — `· detiene: en curso — rebindeo hecho hasta Semantic, falta Component; parado desde 2026-09-05`. Alta del 2026-09-13 |
| **ninguno** | Se puede hacer ya |

**Lo que estás haciendo también es un pendiente, y es el que más se pierde.** Se escribe **al empezar**, no al terminar. Las otras categorías describen lo que no ha arrancado, así que un lote a medias no cabía en ninguna y terminaba sin escribirse en ningún lado: el caso que lo destapó es el DS Manager el 2026-09-13, con el tablero diciendo «en cero» mientras tenía un rebindeo a medias, un mapeo encima y decisiones previas colgando. **Un lote que se interrumpe no es un fallo**, es lo normal cuando Javier cambia de proyecto; lo que sí es un fallo es que el sistema no supiera representarlo.

**Hay dos que suman en vez de sustituir**, y se escriben después de la categoría: **requiere contexto** y **requiere sistema encendido**. La lista crecerá con el uso: si tu caso no cabe en ninguna, no la fuerces — pídele a Javier que la nombre, como se hizo con «espera a otro oficio».

**Un pendiente sin marca sale como «sin declarar»** en el tablero. Eso es correcto y no un error del generador: es la señal de que a esa línea le falta su categoría.

**De dónde sale la razón al capturarla** —cuándo se deduce y cuándo se le pregunta a Javier— vive en `Javier/WORKING_WITH_JAVIER.md`, porque es sobre cómo trabaja él.

## Reglas de este nivel

Las reglas de colaboración viven en `Javier/WORKING_WITH_JAVIER.md`, que es su fuente única. Cada proyecto suma las suyas en su recepción y nunca las copia. Una regla no se duplica: se redirige.
