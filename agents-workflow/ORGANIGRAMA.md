> Reading copy generated on 2026-10-26 (demo 2026.10) from `ORGANIGRAMA.md`: open seams omitted. The instructions are the original Spanish ones. Links to files outside this copy are shown as paths in code. See `PROVENANCE.md` at the root of this folder.

# Organigrama: las áreas, los oficios y sus fronteras

> **Qué es.** El mapa administrativo del sistema: qué áreas existen, por qué existe cada una, de qué responde cada oficio y **dónde termina uno y empieza el siguiente**. Se lee cuando hay un dilema de jurisdicción — dos oficios creen que algo es suyo, o ninguno lo cree — y también cuando alguien nuevo quiere entender la forma del sistema sin leer veinte guías.
> **Es la fuente de las fronteras, y eso tiene consecuencia:** si una guía de oficio dice algo distinto de lo que dice aquí, **manda este documento** y esa guía está desfasada; se corrige. Por eso este archivo no describe procedimiento: qué hace un oficio por dentro, con qué método y en qué orden vive en su guía, y ahí manda la guía.
> **Quién lo edita: solo el Super Agent Admin.** Ningún otro oficio escribe aquí, ni siquiera para corregir su propia fila. Si una frontera te queda mal, te falta, o cambió por un acuerdo, **se pide en `ADMIN_INBOX.md`** y el administrador la escribe. La razón es que una frontera tiene dos lados: quien la vive de un lado no puede moverla solo.
> **Lo que no está aquí:** quién está sentado en cada oficio hoy — eso es la tabla de managers de `INDEX.md`, que cambia solo — y cómo se lee el sistema o cómo se da de alta un oficio, que son `AGENTS.md` y `System/Super Agent Admin/ROLE_CREATION.md`.
> **Actualizado en la fuente: 2026-10-19.**

## Cómo está partido el sistema

**Las áreas agrupan por tema, nunca por proyecto.** Es la regla que decide dónde entra un oficio nuevo, y la que impide que el sistema se convierta en una carpeta por cliente. Un oficio **dentro** de un área sí puede responder por un solo producto — el Software Architect lo hace — porque la regla habla del área, no del oficio.

Nueve áreas, y no todas son del mismo tipo:

| Área | De qué responde | Por qué existe aparte |
|---|---|---|
| **Javier** | Cómo se trabaja con él, su voz y su perfil | No es un área de oficios: es la fuente sobre la persona. La administra el sistema, pero lo que dice es suyo |
| **System** | Definir el sistema y operarlo | Dos oficios con una frontera de una línea: uno decide qué es el sistema, el otro lo hace correr |
| **Product** | La forma de todo proyecto | Cada proyecto no necesita dueño propio: moriría con el proyecto. Hacía falta uno para todos |
| **Design** | Qué se ve, cómo se comporta y cómo se construye visualmente | El área más poblada, porque la especialidad de diseño se repite igual en todos los proyectos |
| **Writing** | Cómo suena lo que se escribe y qué dice | La voz es transversal: aparece en producto, en documentación y en lo que se publica |
| **Presentation** | Cómo se presenta y se consulta lo que ya está escrito | Separa la entrega visible de la autoría de contenido, investigación y diseño |
| **Dev** | Cómo se construye, se prueba y se conecta lo construido | Aquí las decisiones no se transfieren entre productos, y por eso el Software Architect tiene una silla por producto |
| **Marketing** | A qué mercado se le habla y con qué mensaje | Nació el 2026-09-04: el sistema podía construir un producto y no tenía quién respondiera por quién lo compra |
| **Business** | El nivel empresarial: qué entidades existen y qué le pertenece a cada una | Nació el 2026-09-07: los proyectos vivían en una lista plana y la pertenencia solo existía en la cabeza de Javier |
| **Obsidian** | Nombrada por Javier, todavía sin oficio | Está en el mapa porque él la nombró, no porque tenga contenido |
| **Proyectos creativos** | La estructura y la memoria operativa de los proyectos creativos personales | **Es la única que no vive en este repositorio.** Su casa es `../Projects/Agents/`, porque la memoria operativa de lo creativo se mueve con sus proyectos y no con el sistema |

**Lo que todavía no tiene área, y está escrito para que nadie lo tome por vecindad:** monetización, modelos de negocio y estrategias de crecimiento. Javier las separó el 2026-09-04 para un área propia que aún no existe. **Mientras no exista, son suyas** — no de marketing, que decide mercado y mensaje, ni del Systems Analyst, que decide flujos de datos.

## Los niveles, y qué puede cada uno

**Un oficio es una fila; una silla es un asiento dentro de ella.** Casi todos los oficios tienen un solo asiento, el del Manager, y por eso las dos palabras se confunden. El **Software Architect** tiene una silla por producto, todas bajo un mismo oficio, un mismo método y unos mismos buzones, y quien ocupa cada una es el manager de su producto. El **Domain Advisor** tiene una silla por proyecto; su especialidad y lo compartido entre sillas se describen en su fila de Product. El sistema **cuenta oficios y no asientos**, salvo cuando declara sillas a propósito.

### Cargo frente a estado

**Cargo** es el título (Manager, Delegado, Worker…). **Estado** es si esa conversación está **activa** o **dormida**. Un Manager dormido sigue siendo el Manager: no pierde el cargo porque el modelo frontera no esté disponible. «Activo / dormido» se anota en `INDEX.md`; **no** forma parte del nombre del cargo.

### La administración, en más de un ecosistema

Los agentes corren en más de un producto (Claude/Cowork, Codex, Grok…). **La administración del sistema es un solo oficio, el Super Agent Admin, y se reparte como cualquier otro** (decisión de Javier del 2026-10-04, que retira el cargo «Admin de ecosistema» del 2026-09-11):

- **Su Manager es el Super Admin.** Define la estructura, las reglas comunes, las altas y este organigrama. **Lo que le da esa autoridad es el modelo y el esfuerzo con que corre**, el de frontera del momento, y eso no cambia con este reparto. Hoy vive en Claude.
- **Las conversaciones que llevan el oficio en otro ecosistema, hoy Codex y Grok, son sus Delegados.** Misma guía, mismo oficio: pueden ejecutar tramos de sistema, como un alta o el tejido de una frontera, y no cambian las reglas a espaldas del Manager. Firman `[Delegado · …]`.
- **El oficio tiene una silla orientada a los proyectos creativos, el CPSA.** Usa la guía del Super Agent Admin como método y la aplica a la estructura de `../Projects/`. No administra este repositorio, y el Manager no inventa jerarquías allá.

### Asistentes personales

**Un asistente personal no es un oficio: es una identidad registrada** (decisión de Javier del 2026-10-07; el primero es dot, en Codex). Trabaja para Javier y no para un tema: conecta sus peticiones con encargos a conversaciones, prepara contexto, y sigue bloqueos y resultados. Consulta a los oficios, y **no toma sillas, no decide por ningún titular y no escribe en guías ni cánones**; lo que encuentre se lo dice al dueño por buzón. No tiene guía, changelog ni buzón propio: su único registro es la tabla «Asistentes personales» de `INDEX.md`, y con eso el script de conversaciones lo reconoce como remitente y le da bandeja. Firma `[Asistente personal · nombre · ecosistema]`. Si un asistente llega a necesitar método propio, eso ya es un oficio y pasa por un alta.

### Cargos de oficio

| Cargo | EN | Qué decide | Qué no puede |
|---|---|---|---|
| **Lead** | Lead | Pautas por encima de los oficios de su área | No es jefe de nadie; no nombra managers ni entra al método interno de un oficio |
| **Manager** | Manager | Dueño del oficio: método, canon, frontera vista desde su lado. **Uno por oficio.** Sigue siéndolo aunque esté dormido | No toca el canon de otro oficio. Lo pide |
| **Delegado** | Deputy | Misma guía; opera en otro ecosistema o mientras el Manager duerme. Cubre el día a día. **Un oficio puede tener más de uno**, por ejemplo uno en Codex y otro en Grok; Manager solo hay uno. **Se anota en la fila de su oficio en `INDEX.md`, y en ningún otro lado:** no lleva entrada en `CHANGELOG.md` ni documentos propios (aclaración de Javier del 2026-10-04) | No muda el canon a espaldas del Manager (ni sin OK de Javier cuando aplique) |
| **Worker** | Worker | Un encargo: pantalla, archivo, PR, cloud agent, o el trabajo de un proyecto mientras Javier se lo tenga, fijo o temporal. **No se registra:** queda en lo que firma | No administra el oficio ni reescribe su identidad |
| **Silla** | Seat | Asiento declarado **dentro** de un oficio para un producto o proyecto, que existe aunque esté vacío porque tiene cosas propias: su fila en `INDEX.md`, sus decisiones, su ámbito. Los casos de Software Architect y Domain Advisor se describen en sus filas más abajo | No es metáfora general ni sinónimo de Delegado. Una conversación que trabaja un proyecto sin cosas propias no ocupa silla: es Worker |

**Silla o Worker: la prueba es si la conversación tiene cosas propias que sobreviven a ella.** El Software Architect sí: su fila, el `DECISIONS.md` de su producto, decisiones que nadie más toma; por eso su silla existe aunque esté vacía (ver Dev, más abajo). La conversación del Screen Designer que lleva [cliente 2] no: el log es del proyecto y el método es del Manager, así que si desaparece no se pierde nada. Es un **Worker**, fijo o temporal, y **no se registra en ningún lado**: queda en lo que firma, que es lo que sirve saber, qué agente y con qué cargo hizo qué. Registrar que existe obligaría a saber cuándo deja de existir, y eso solo se sabe si Javier lo avisa. Antes a esas conversaciones se les nombraba manager temporal o «ejecutor» del proyecto, y cuando se acababan el cargo quedaba a nombre de algo que ya no existía. Decisión de Javier del 2026-09-24, el mismo día que se probó darles silla.

**Cómo despertar (frases cortas):** «Eres el **Manager** de Tech Lead» · «Eres **Delegado** de Screen Designer en Grok; el Manager está en Claude / dormido» · «Eres **Worker** de Screen Designer en el tramo X» · «Eres **Worker** de Screen Designer en [cliente 2]».

**«Ejecutor» (legado):** en documentos viejos cubría a la vez Delegado y Worker. **Deja de usarse como cargo único.** Al escribir de nuevo, usa Delegado o Worker. No hace falta reescribir toda la historia.

### Cómo decirlo fuera del sistema

Si alguien de fuera pregunta, la equivalencia basta: **orchestrator** (Admin) · **role owner** (Manager) · **role instance** (Delegado / Deputy) · **task agent** (Worker). No esperes que un paper diga «Deputy of Screen Designer».

### Forma de trabajo (estudio con SOPs)

Este ecosistema no es un *swarm de prompts* (agentes con instrucciones cortas y memoria floja). Es un **estudio con SOPs**: cada oficio tiene guía, buzón y changelog; la fuente de verdad vive en `agents-workflow/`; el chat ejecuta el método. Más lento de nacer; aguanta pelea entre agentes y el tiempo. Que salgan errores de frontera es señal de que hay frontera escrita, no de rareza patológica.

**Quién ocupa cada asiento lo decide Javier, conversación por conversación.** Un lead no nombra managers; un manager no nombra Delegados ni Workers por su cuenta salvo que Javier lo haya autorizado.

## Las áreas por dentro

### System — definir y operar

| Oficio | De qué responde |
|---|---|
| **Super Agent Admin** (**Super Admin**) | Define: estructura, reglas comunes, **el esquema** de los índices, géneros de documento, **las altas de oficio, de lead y de área**, y los nombres en disco. **No da de alta proyectos.** Su Manager es la autoridad canónica del sistema; en otros ecosistemas lo llevan sus Delegados, y su silla para lo creativo es el CPSA |
| **Ops Manager** | Opera: corre las habilidades y las operaciones recurrentes, y reporta |

**La frontera, en una línea:** el Super Admin decide cómo es el sistema, y sus Delegados lo administran en su ecosistema con la misma guía, sin inventar método; Ops lo hace correr (habilidades) sin cambiarle el método a nadie. Si al operar aparece que falta un método, se pide.

### Product — el producto y la forma del proyecto

| Oficio | De qué responde |
|---|---|
| **Product Manager** | Qué se construye, el alcance y las etapas del producto **en propuesta**; Javier **ratifica**. Priorización de valor. No ejecuta el proyecto ni fija arquitectura de software |
| **Project Manager** | Que cada proyecto tenga sus piezas, su recepción y su orden, y coordinar a los oficios que actúan en él. **Da de alta los proyectos**: crea el paquete mínimo, escribe sus filas en `PROJECTS.md` y lo activa sin esperar a nadie |
| **Domain Advisor** | Qué es verdad en el dominio de un proyecto y cómo se modela: qué reglas, de qué fuente, con qué supuestos, en qué rango y qué se advierte fuera de él. **Una silla por proyecto, cada una con su especialidad** (la primera, Scientific Advisor en Cosmotelier; la segunda, Literary Advisor en Litteratium, abierta el 2026-10-13 y ocupada por un bot de Grok). Lleva su registro en el `DOMAIN_DECISIONS.md` del proyecto. Lo común entre sillas es de un **Manager general**, una conversación propia que no lleva ningún proyecto (decisión de Javier del 2026-10-26). Alta del 2026-09-28 |

**La frontera, en una línea:** Product Manager propone el *qué* del producto; Project Manager cuida la *forma* y la ejecución entre oficios. **Qué se construye ya no es solo de Javier en el día a día:** lo propone el Product Manager y Javier lo ratifica (alta 2026-09-11). El nombre Project Manager se conserva a propósito para no confundirlo con producto. **Domain Advisor y Product Manager:** ¿es plausible, o entra? El asesor dice qué es plausible y dónde termina lo que se sabe; el Product Manager decide si entra al alcance, y Javier ratifica.

### Design — lo que se ve

| Oficio | De qué responde |
|---|---|
| **Design Lead** | Las pautas por encima de los oficios de diseño, y los principios de diseño |
| **Game Designer** | Reglas y experiencia jugable, mecánicas y gameplay completos y coherencia del GDD; activo desde el 2026-10-18, titular en `INDEX.md` |
| **Game Economy Designer** | Recursos, progresión, costos, recompensas y ritmo dentro de la intención de Game Designer; dormido |
| **Art Director** | Lenguaje artístico del contenido y aceptación artística por proyecto, dentro de Design sin subordinación ni rango de Lead; dormido |
| **3D Artist** | Modelado, geometría, UV, texturas, originales y exportación; dormido |
| **Technical Artist** | Contratos de recursos, importación, materiales, rendimiento y especificación de shaders y herramientas, no código del producto; dormido |
| **Sound Designer** | Intención, función y especificación sonora de eventos y piezas; dormido |
| **DS Manager** | Los design systems: la guía de construcción, el contrato master y el inventario |
| **UX Designer** | La experiencia completa: investigación, arquitectura de información, recorridos, flujos, baja fidelidad y validación |
| **Screen Designer** | Las pantallas de producto aplicando el design system |
| **Brand Designer** | Concebir y construir una marca entera: la verificación del nombre que trae Javier, su filosofía visual, color, tipografía y sistema gráfico, y **producir sus piezas finales**, manuales de imagen y brand kits. Alta del 2026-09-23; las piezas finales, desde el 2026-09-24 por corrección de Javier |
| **Naming Architect** | Cómo se nombra lo que se genera dentro de Figma |
| **File Architect** | La estructura de un archivo de Figma: páginas, documentación interna, muestrarios y anatomías |
| **Motion Designer** | Cómo se mueve: duración, easing, jerarquía y motion reducido |
| **Media Editor** | Las piezas que no se generan en Figma — video, audio, imagen raster — y con qué archivo llegan a su destino |
| **Design Engineer** | Llevar a código lo que diseño decidió, con fidelidad, sin cambiarlo |

### Writing — lo que dice

| Oficio | De qué responde |
|---|---|
| **Voice Architect** | La voz: el canon, los contratos de cada medio y el registro de voces |
| **UX Writer** | El texto dentro de las pantallas |
| **Lore Writer** | El canon narrativo y su continuidad |

### Presentation — cómo se entrega lo que ya existe

| Oficio | De qué responde |
|---|---|
| **Presentation Editor** | La presentación de sesiones y reportes, los derivados visuales solicitados de investigación y teoría, y el contrato editorial y visual de los tableros. Mantiene sus índices sin mover las fuentes |

**La frontera con Writing:** Writing decide qué dice y cómo suena; Presentation decide cómo se entrega y se ve una fuente ya aprobada. **Con Design:** Design decide dirección visual y gobernanza de componentes; Presentation no interviene documentos de componentes ni sandboxes. **Con Product:** Product decide dónde vive un documento de proyecto; Presentation sólo lo cataloga. **Con Ops:** Ops opera scripts, entorno y publicación; Presentation mantiene el contrato de salida y su revisión.

### Dev — lo que se construye

| Oficio | De qué responde |
|---|---|
| **Tech Lead** | Las pautas por encima de los oficios de dev, y todo lo transversal de la categoría |
| **Software Architect** | La arquitectura de **un** producto: la decide, coordina a los Workers que escriben el código, y revisa e integra lo que entregan. **No escribe código** desde el 2026-09-28. **Una silla por producto** |
| **Systems Analyst** | Lo que cruza el límite de un producto: qué plataformas se comunican, con qué contrato y bajo qué reglas |
| **QA** | Qué debe cumplir lo construido y cómo se prueba |
| **Git Manager** | Los repositorios: estado, respaldos y remotos |

**El Software Architect no tiene manager general.** Tiene una silla por producto, así que **un asunto transversal no tiene destinatario ahí: va al Tech Lead.** A una silla se le escribe solo de su producto, y el producto se nombra en el asunto.

**Una silla existe desde que existe su producto, esté ocupada o no.** Se declara en la tabla de managers de `INDEX.md` en cuanto el proyecto entra al mapa, para que se vea el hueco antes de que alguien lo llene; una silla vacía **no es un oficio sin manager** y no dispara aviso. Decisión de Javier del 2026-09-04.

### Business — de quién es cada cosa

| Oficio | De qué responde |
|---|---|
| **Career Manager** | Con qué se presenta Javier profesionalmente: qué dicen su CV, su portafolio, su página y sus perfiles públicos, y que digan lo mismo. Vive en `Javier/Career Manager/`. Alta del 2026-09-20 |
| **Portfolio Manager** | Qué entidades existen —estudios, plataformas, marcas—, qué es cada una y qué proyectos, IP y marcas le pertenecen. Su mapa es `Business/Portfolio Manager/PORTFOLIO_MAP.md` |

**La monetización no tiene dueño todavía, y vivir en esta categoría no la reparte.** Modelos de negocio, precios y crecimiento siguen siendo de Javier hasta que exista el segundo oficio de `Business/`. Está dicho en negativo a propósito: un oficio solo en una categoría tiende a comerse el tema entero por vecindad.

### Marketing — a quién se le habla

| Oficio | De qué responde |
|---|---|
| **Marketing Manager** | A qué mercado se le habla, con qué mensaje, por qué canal y con qué calendario; coordina campañas y material publicitario sin producirlo |

### Proyectos creativos — fuera de este repositorio

| Oficio | De qué responde |
|---|---|
| **CPSA** (Creative Projects Super Admin) | **Silla del Super Agent Admin orientada a lo creativo** desde el 2026-10-04: usa su guía como método. Responde por la estructura de los proyectos creativos personales: sus recepciones, índices, la separación entre memoria operativa y producción, y el mapa hacia Drive |

**Su casa es `../Projects/Agents/CPSA/`, no este repositorio.** El método transversal, los oficios y las reglas comunes siguen teniendo su fuente aquí; lo que él administra es la capa operativa de allá.

## Con qué manos cuenta cada oficio

**Un oficio no es solo una jurisdicción: es una jurisdicción más unas manos**, y hasta el 2026-09-13 este sistema solo declaraba la primera. El resultado es que casi todos los oficios tienen exactamente la misma herramienta, leer y escribir `.md`, y varios llevan semanas proponiendo trabajo que no pueden ejecutar sin que nadie lo dijera.

**Para qué sirve declararlo, y la segunda razón vale más que la primera:** para saber a quién se le puede pedir algo, y para que **un oficio sin manos lo sepa y lo diga** en vez de proponer y esperar.

| Oficio | Con qué cuenta hoy, además de leer y escribir `.md` | Lo que su propio canon ya declara que va a pedir |
|---|---|---|
| **Screen Designer** | Figma por MCP: crear y editar pantallas, instanciar componentes | — |
| **DS Manager** | Figma por MCP sobre los archivos de design system | — |
| **File Architect** | Figma por MCP sobre la estructura del archivo | — |
| **Design Engineer** | Escribir código en el repositorio del producto que le toque | — |
| **Software Architect** | El repositorio de su producto, **para revisar y unir a main lo que entregan sus Workers; no escribe código** (decisión de Javier del 2026-09-28). El código lo escriben los Workers | — |
| **Git Manager** | Los comandos de git, **que corren en la terminal de Javier y nunca en la del agente** | — |
| **Ops Manager** | Correr las habilidades de `skills/` y publicar tableros | — |
| **Presentation Editor** | Publicar páginas con enlace | — |
| **Super Agent Admin** | Escribir en cualquier `.md` del sistema, publicar tableros | — |
| **QA** | **Lee código, resultados de pruebas y artefactos; corre comandos que solo leen, como comparar huellas o bytes; y opera la aplicación por su interfaz, con documentos sintéticos y en copias que no son la entrega.** No escribe ni cambia código del producto, no modifica la entrega aceptada, no abre documentos personales de Javier y no opera git. Fuente: `Dev/QA/QA_METHOD.md`, «Con qué manos comprueba QA» (decisión de Javier del 2026-10-17) | **Escribir y correr su propia batería de regresión**, cuando un producto tenga su segunda entrega y la ejecución propia de QA sobre los mismos casos se repita de una versión a otra |
| **Tech Lead** | **`.md`, y desde el 2026-09-20 leer una biblioteca de Eagle por MCP**, solo lectura, a través del plugin personal de Codex. La escritura sigue deshabilitada para bibliotecas reales. Su memoria operativa está en `System/Eagle/` | **Escribir en Eagle**, el día que Javier lo autorice: hoy solo se ha ejercido mecánicamente en una biblioteca ficticia |
| **UX Designer** | Figma por MCP para wireframes y prototipos de baja fidelidad; ya los produjo así para el portafolio | — |
| **Career Manager** | Figma por MCP, en lectura, sobre el CV vigente: es su fuente laboral primaria, declarada en `Javier/Career Manager/CAREER_GUIDE.md` | — |
| **Brand Designer** | **`.md` y las piezas visuales de una identidad**: Figma e Illustrator por MCP para construirla (guía y fallos conocidos de Illustrator en `Design/Illustrator/`), e imágenes generadas para concepto, manuales y piezas finales | **Generar imágenes**: hoy el sistema no tiene habilidad para eso y se resuelve en la conversación |
| **Naming Architect** | Figma por MCP, en lectura y escritura, **solo sobre nombres**: frames, capas, secciones, componentes y propiedades de variante. No crea ni reanida nodos, que es del Screen Designer, ni publica la librería, que es acción de Javier. Lo pidió él el 2026-09-25: renombra en Figma desde agosto | — |
| **Motion Designer** | **Figma por MCP, en lectura y escritura, sobre animación:** keyframes, timelines y easing, más la composición de escena que esa animación necesita (agrupar, clonar, reposicionar y recolorear sus nodos). No crea pantallas ni componentes del sistema, que son del Screen Designer y del DS Manager. Lo ejerce desde agosto: diez secuencias animadas en un archivo de producto (C-DESIGN-003). **Depende de una bandera de la cuenta de Javier:** si Motion no está habilitada, la primera llamada dice que la propiedad no existe y reintentar no lo arregla. **Y produce motion por código fuera de Figma:** escribe y corre la pieza como programa (`.html` con función de tiempo) y su renderizador en Python con Chromium y `ffmpeg`, y escribe los archivos que entrega; no escribe en el repositorio de ningún producto. Ejercido desde el 2026-10-18, con el isotipo animado de Javier (C-ADMIN-028); quién entrega el archivo final, frente al Media Editor, sigue sin acordarse | — |
| **Media Editor** | **`.md`, `ffmpeg` y scripts de proceso por cuadro** para producir la pieza: recorte, canal alfa, compresión y póster. **Escribe los archivos entregados en el repositorio del producto y en el Drive del proyecto**, que es donde vive lo pesado. No genera el material de origen: llega del Brand Designer, del Motion Designer o de un generador. Lo ejerce desde su primer trabajo, el video de portada de un producto (C-ADMIN-024) | **Audio**, que su alcance incluye y todavía no tiene un caso |
| **Todos los demás** | **Solo `.md`.** Marketing Manager, Portfolio Manager, Systems Analyst, Project Manager, Product Manager, Domain Advisor (más la consulta de fuentes en la web), UX Writer, Voice Architect, Lore Writer, Design Lead | — |
| **Game Designer** | Solo `.md` | Prototipos en motor: reparto con desarrollo y herramientas por declarar; no escritura de código por el alta. `Design/Game Designer/GAME_DESIGN_GUIDE.md` |
| **Game Economy Designer** | Solo `.md` | Ejecución de cálculos y simulaciones, con herramientas y comprobación todavía por declarar. `Design/Game Economy Designer/GAME_ECONOMY_GUIDE.md` |
| **Art Director** | Solo `.md` | Revisión visual en herramientas de producción, con acceso por declarar; no producción de recursos por el alta. `Design/Art Director/ART_DIRECTION_GUIDE.md` |
| **3D Artist** | Solo `.md` | Modelado, UV, texturas y exportación en Blender u otra herramienta, todavía sin acceso ni capacidad comprobados. `Design/3D Artist/3D_ART_GUIDE.md` |
| **Technical Artist** | Solo `.md` | Operación del motor, importación y pruebas de materiales y rendimiento, por comprobar. No incluye escribir código. `Design/Technical Artist/TECHNICAL_ART_GUIDE.md` |
| **Sound Designer** | Solo `.md` | Producción, grabación y edición de audio, con herramientas por declarar; no música ni programación por el alta. `Design/Sound Designer/SOUND_DESIGN_GUIDE.md` |

**La segunda columna existe porque la primera envejece en silencio.** Una tabla que solo dice el presente se lee como un límite permanente, y el día que el alcance de alguien crece, su fila y su canon dicen cosas distintas sin que nadie se entere. **Solo se llena con lo que el canon de ese oficio ya declara**, nunca con lo que parece probable. Entró el 2026-09-14, cuando QA leyó su fila y reportó exactamente ese desfase el día siguiente de que la tabla naciera.

**Esa última fila es el hallazgo, no el relleno.** Doce oficios sin manos al 2026-09-28, con el alta del Domain Advisor; eran catorce cuando la tabla nació, y los tres que salieron lo pidieron ellos por `ADMIN_INBOX.md`, que es como tiene que pasar. Algunos no las necesitan; otros sí y nadie lo había dicho. **El caso que lo demuestra es el UX Writer**, que tiene manager asignado desde hace semanas y su changelog está vacío: darle silla no le dio capacidad de hacer nada.

**Cómo cambia esta tabla:** un alta la escribe en el mismo tramo, y una herramienta nueva se pide por `ADMIN_INBOX.md`, como cualquier cosa de este archivo.

## Las fronteras

**Cada una es una pregunta que se contesta, no un reparto de temas.** Están escritas del lado en que se usan: si te toca decidir algo y no sabes si es tuyo, busca el par y contesta la pregunta.

### Dentro de Design

| Entre | La pregunta que decide |
|---|---|
| Design Lead y cualquier oficio de diseño | ¿La decisión afecta solo a un oficio, o a cómo trabajan varios? Solo a uno, es suya; a varios, es del lead |
| Design Lead y Art Director | ¿Pauta entre oficios, o dirección artística de un proyecto? La primera es del Design Lead; la segunda y su método, del Art Director, sin subordinación. Una categoría artística propia se reevalúa cuando un segundo proyecto tenga producción artística propia y necesite pautas para varios oficios |
| Game Designer y Game Economy Designer | ¿Intención jugable, o modelo cuantitativo de recursos y progresión? La intención es del Game Designer; costos, recompensas y ritmo dentro de ella, del Game Economy Designer |
| Art Director y Brand Designer | ¿Lenguaje artístico del contenido, o identidad de marca? Lo primero es del Art Director, que declara qué hereda; marca, verificación del nombre, filosofía visual, logotipo y sistema gráfico siguen con Brand Designer |
| Art Director, Game Designer y UX Designer | ¿Preferencia estética, regla de juego o comprensión de una señal? La dirección artística no cambia reglas ni alcance de patrones; la legibilidad se acuerda entre los tres. UX conserva interacción, comprensión, accesibilidad y recorridos; Screen Designer realiza la pantalla final |
| Art Director, 3D Artist y Technical Artist | ¿Aceptación artística, recurso tridimensional o requisitos de integración? La intención y aceptación artística son del Art Director; modelado, UV, texturas y originales, del 3D Artist; contratos técnicos, del Technical Artist con desarrollo |
| Sound Designer, Motion Designer y Media Editor | ¿Qué comunica y cómo suena, cómo se mueve, o con qué archivo llega? Lo sonoro es del Sound Designer; el movimiento, del Motion Designer; preparación técnica, formato, compresión y entrega, del Media Editor. Música, composición y programación de audio siguen sin dueño expreso |
| UX Designer y Screen Designer | ¿Es el problema y el recorrido, o la pantalla que lo resuelve? Lo primero es del UX, lo segundo del Screen |
| UX Designer y UX Writer | ¿Qué debe entender la persona, o cómo se le dice? Lo primero es del UX, lo segundo del Writer |
| Naming Architect y Screen Designer | ¿Qué nodos existen y cómo se anidan, o cómo se llaman? La estructura es del Screen, la gramática del nombre es de Naming |
| Motion Designer y Media Editor | ¿Cómo se mueve, o con qué archivo llega? El movimiento es del Motion **aunque la pieza final sea un video**; el formato, el códec y el alojamiento son del Media Editor |
| Design Engineer y cualquier oficio de diseño | El Engineer **implementa y no cambia**. Si una decisión es imposible o cara, reporta el costo y una alternativa; cambiarla por su cuenta es el fallo que este oficio existe para evitar |
| DS Manager y Design Engineer | El sistema en Figma es del DS Manager; el archivo fuente de tokens en el repositorio lo sostiene el Engineer, y responde por que los dos correspondan |

### Dentro de Dev

| Entre | La pregunta que decide |
|---|---|
| Tech Lead y Software Architect | ¿Vale para todos los productos, o solo para este? Lo transversal es del lead, lo de un producto es de su arquitecto |
| Software Architect y Systems Analyst | **¿El dato cruza el límite del producto?** Si no cruza, es del arquitecto; si cruza, es del analista. Decisión de Javier del 2026-09-04 |
| ¿Esto es de un producto o del oficio entero? | **Si es de un producto, va a su silla; si es del oficio — su guía, su canon, su frontera — va al Tech Lead.** El Software Architect tiene una silla por producto y **ninguna es dueña de lo compartido**, así que una entrada a «Software Architect» a secas no tiene destinatario. Decisión de Javier del 2026-09-14, al notar que alguien había empezado a firmar como delegado del canon compartido sin que esa figura existiera en el padrón. **No se crea esa silla:** el Tech Lead ya es el lead de la categoría y ya recibe lo transversal de dev |
| Systems Analyst y Software Architect, al implementar | El contrato se decide en el analista y **se implementa en el producto**. Si el contrato obliga a cambiar la arquitectura interna, el arquitecto lo dice en vez de aceptarlo callando |
| ¿Dónde vive el contrato que toca dos productos? | En `Dev/Integrations/`, uno por integración, del **Systems Analyst**. El `DECISIONS.md` de cada producto lo **enlaza** y no lo copia. Costura del 2026-09-04, cerrada el 2026-09-11 con la pauta 9 del Tech Lead |
| Cualquiera y QA | Quien construye pide la comprobación; **cómo se prueba y qué bloquea una entrega es de QA** |
| Cualquiera y Git Manager | El git es suyo, **ni siquiera `git status` por cuenta propia** |

### Entre áreas

| Entre | La pregunta que decide |
|---|---|
| Design y Writing | ¿Cómo se ve y dónde va, o qué dice? Lo primero es de Design, lo segundo de Writing |
| Design y Marketing | **Es de enfoque, no de tema.** ¿La decisión estratégica se toma desde el usuario y el producto, o desde el mercado y la comunicación? Lo primero es del Design Lead, lo segundo del Marketing Manager. **Ninguno es lead del otro** |
| Marketing y Design, al producir | Marketing dice qué pieza hace falta y para cuándo; **producirla es siempre de Design** |
| Marketing y Systems Analyst | Marketing dice qué métrica quiere mover y qué necesita saber; el analista resuelve qué tiene que fluir para poder saberlo |
| Brand Designer y Marketing Manager | **¿Cómo es la marca, o a quién le habla?** La concepción y la identidad visual son del Brand Designer, y la plataforma de marca las consume. **El nombre lo trae Javier**: el Brand Designer conduce su verificación y solo propone uno cuando Javier se lo encarga (`Design/Brand Designer/BRAND_DESIGN_GUIDE.md`, «Fuentes y reparto del trabajo»); el mercado, el mensaje, el canal y el calendario siguen siendo del Marketing Manager. **La palabra «filosofía» nunca va sola** (cerrado por Javier el 2026-10-05): la **filosofía visual** es del Brand Designer y vive en la identidad de marca; la **filosofía de mercado** es del Marketing Manager y vive en la plataforma de marca. Son dos documentos, uno junto al otro en el proyecto de la marca |
| Voice Architect y Marketing Manager | **¿Qué promete la marca, o cómo lo dice?** La frase de marca, la descripción corta y el relato los redacta el Voice Architect desde el 2026-10-18, decisión de Javier: escribe primero quien ya está en la marca, el Voice Architect redacta desde cero solo cuando nadie escribió y, si hay borrador ajeno, lo revisa en pares, sale y entra. El Marketing Manager valida que lo prometido cuadre con la plataforma de marca. El copy de producto y el de campaña se siguen encargando pieza por pieza |
| Brand Designer, Voice Architect y Marketing Manager | **¿Dónde vive la personalidad de la marca?** En la plataforma de marca, que es del Marketing Manager. El Brand Designer la deriva a expresión visual y el Voice Architect a expresión verbal, y la proponen juntos (decisión de Javier del 2026-10-18) |
| Brand Designer y DS Manager | **¿El activo, o su distribución?** Qué es el logo y cómo se usa fuera de producto es del Brand Designer; el componente que lo publica dentro de un design system es del DS Manager |
| Brand Designer y Media Editor | **¿La pieza de marca, o con qué archivo llega?** Concebir y producir la pieza visual de una marca es del Brand Designer; formato, compresión, alfa y alojamiento son del Media Editor, igual que con el Motion Designer. **Donde no hay pieza de identidad detrás, la imagen raster es entera del Media Editor:** el póster de un video, el recorte de un render, la optimización de una foto de cliente. Acordado entre los dos el 2026-10-18 (C-DESIGN-006) |
| Brand Designer y Naming Architect | **¿La marca, o lo que vive en el archivo?** La verificación del nombre de una marca, que trae Javier, es del Brand Designer; los nombres de páginas, capas y frames dentro de Figma siguen siendo del Naming Architect |
| Career Manager y Voice Architect | **¿Qué dice, o cómo suena?** La estructura y el contenido del material profesional son del Career Manager; la redacción literal y las capas de voz, incluida `Javier/JAVIER_CV_VOICE.md`, son del Voice Architect, que revisa al final. Reparto fijado por Javier el 2026-09-16 |
| Career Manager y Project Manager | **¿Qué dice la pieza, o cómo va el proyecto?** El Career Manager decide qué dice y si está sincronizada, y le pasa el encargo; el Project Manager lleva las etapas, el alcance y los oficios que trabajan `Projects/Javier Profesional/` |
| Career Manager y Marketing Manager | **¿La cuenta, o lo que el perfil dice?** El mismo LinkedIn son dos cosas: la cuenta, su estado y dónde se publica son del Marketing Manager; el texto del perfil profesional es del Career Manager |
| Portfolio Manager y Marketing Manager | **¿Es de quién es, o es qué se le dice?** Qué entidades existen y qué le pertenece a cada una es del Portfolio Manager; a quién le habla esa marca y con qué mensaje es del Marketing Manager |
| Portfolio Manager y Project Manager | **¿De quién es, o cómo está armado?** La pertenencia es del Portfolio Manager; la forma del proyecto es del Project Manager, que además mantiene sus filas en `PROJECTS.md` |
| Portfolio Manager y Lore Writer | **¿Que el universo exista y de quién sea, o qué pasa dentro de él?** Lo primero es del Portfolio Manager; el canon narrativo es del Lore Writer, y la estructura de los proyectos creativos, del CPSA |
| Domain Advisor y Software Architect | **¿Qué es verdad, o cómo se construye?** Qué reglas del dominio, de qué fuente, con qué supuestos y en qué rango es del asesor, y su inventario vive en el `DOMAIN_DECISIONS.md` del proyecto; cómo se implementa es del arquitecto, que reporta el costo en vez de cambiar la regla. Decisión de Javier del 2026-09-28 |
| Domain Advisor y UX Designer | **¿Qué restricción, o cómo se expresa?** Qué dato depende de cuál, en qué orden se elige y cuándo se advierte lo fija el asesor; cómo lo muestra el flujo, el UX Designer |
| Domain Advisor y QA | **¿Qué debe salir, o cómo se prueba?** Los casos de contraste y sus valores esperados los da el asesor; cómo se prueba y si el producto los cumple es de QA |
| Domain Advisor y Marketing Manager, en Litteratium | **¿Es cierto, o conviene?** El Marketing Manager propone cada pieza y su estrategia; los dos definen juntos el brief (escena, elementos, datos citados, simbolismos que evitar) y el asesor valida datos, atribuciones, traducciones y simbolismos antes de que pase al Brand Designer. No es paso obligado en cada publicación. Decisión de Javier del 2026-10-13 |
| Domain Advisor y Brand Designer, en Litteratium | **¿Qué dice, o cómo se ve?** El brief llega resuelto; el Brand Designer decide solo concepto visual, composición, técnica y apego al manual antes del generador. Sus dudas de contenido van directo al asesor; las de estrategia, al Marketing Manager. Decisión de Javier del 2026-10-13 |
| Design y Dev | Diseño decide qué se ve y cómo se comporta; dev lo implementa y **reporta el costo en vez de cambiarlo** |
| Game Designer, Product Manager, Software Architect y Project Manager | ¿Cómo se juega, qué entra y cuándo, cómo se implementa, o cómo se organiza el proyecto? Game Designer propone reglas y gameplay y custodia coherencia del GDD; Product Manager propone alcance, etapas y valor, que Javier ratifica; Software Architect decide implementación y devuelve evidencia y alternativas cuando algo es caro o inviable; Project Manager conserva forma y coordinación. Una silla por oficio de videojuego, no una por juego; decisiones locales en su GDD |
| Game Economy Designer, Domain Advisor y Javier | ¿Diseño de economía, conocimiento externo o decisión comercial? Recursos, progresión, costos y recompensas son del Game Economy Designer; Domain Advisor solo valida conocimiento externo cuando haga falta. Precios, objetivos comerciales y monetización siguen con Javier mientras no se declare otro dueño |
| Technical Artist, Software Architect y Tech Lead | ¿Especificación de arte técnico, implementación o pauta de código? Technical Artist especifica recursos, importación, materiales, rendimiento, shaders y herramientas. No escribe código del producto: lo implementan Workers del Software Architect con su revisión. Una futura capacidad de escribir shaders o herramientas se pide expresamente al Tech Lead; el alta no la concede. Aceptación artística del Art Director, técnica de desarrollo y comprobación independiente de QA |
| Cualquiera y Product | Que el proyecto tenga sus piezas, su orden y su registro es del Project Manager; el contenido de cada pieza es del oficio que la escribe |
| Cualquiera y System | Estructura, carpetas, nombres en disco, el **esquema** de los índices, y las altas **de oficio, de lead y de área** son del Super Agent Admin. **Un oficio que necesite mover estructura la pide, no la mueve** |
| Super Agent Admin y Project Manager | **¿Qué se da de alta?** Un **oficio, un lead o un área** lo da de alta el administrador; un **proyecto**, el Project Manager: crea el paquete, escribe sus filas y lo activa **sin esperar respuesta**, y lo informa por el changelog del sistema. Decisión de Javier del 2026-09-03 |
| Super Agent Admin y Project Manager, sobre `PROJECTS.md` | **¿Es una fila o es el esquema?** Las filas normales de proyectos y subproyectos las escribe y mantiene el Project Manager; **las columnas, la cadena de lectura y el método del recibidor** son del administrador. Un proyecto que necesite una forma que el sistema no tiene se le pide por `ADMIN_INBOX.md` |
| Super Agent Admin y CPSA, su silla de lo creativo | ¿Es el sistema, o es la capa operativa de lo creativo? El sistema general es del administrador; la estructura de `../Projects/` es del CPSA. **El CPSA no administra este repositorio y el administrador no inventa jerarquías creativas** |
| Lore Writer y CPSA | ¿Es canon narrativo, o es la forma en que se guarda? Lo primero es del Lore Writer; el CPSA **no escribe lore ni decide cronologías** |
| Cualquiera y Javier | Alcance, prioridades, producto y quién ocupa cada asiento son suyos, siempre |

### La regla que cierra todas

**Lo que encuentres fuera de tu jurisdicción no lo ejecutas y tampoco se lo cargas a Javier de mensajero: lo reportas al dueño.** Al buzón de tu área si es un vecino, al general si cruza áreas, al del administrador si es del sistema.

## Cómo se mantiene vivo

**Se edita cuando cambia una frontera, no cuando cambia una guía.** Un oficio que reescribe su método por dentro no toca este archivo; un acuerdo que mueve dónde termina uno y empieza otro, sí.

**El disparador es el alta y el acuerdo.** Dar de alta un oficio o un área obliga a escribir aquí su fila y sus fronteras en el mismo tramo — está en `System/Super Agent Admin/ROLE_CREATION.md`. Y cuando dos oficios cierran una costura, quien la cerró **lo reporta en `ADMIN_INBOX.md`**, porque él no escribe aquí.

**Si al leerlo encuentras una frontera que ya no es cierta**, ese es el peor estado posible de este archivo y no se deja pasar: se reporta en `ADMIN_INBOX.md` con las dos versiones, la de aquí y la que veas en la guía.
