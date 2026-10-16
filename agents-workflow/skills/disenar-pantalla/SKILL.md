---
name: disenar-pantalla
description: "Crea o rehace pantallas de producto en Figma con el design system. Úsala para diseñar, montar o maquetar una vista; para solo auditar una existente usa revisar-pantalla."
---

> Derived reading copy, 15 October 2026. Source: `skills/disenar-pantalla/SKILL.md`. Closing example/test history omitted. External canons and tool integrations are intentionally incomplete. This copy is for reviewing the workflow and is not an installed or self-contained skill.


# Diseñar una pantalla

> **Skill de tarea.** Sirve para que cualquier agente haga el trabajo sin tomar el oficio. No copia ningún método: te dice qué leer y en qué orden, y el método sigue viviendo en su canon. **Tampoco lo resume:** donde la regla está en un canon, la receta la cita, porque un resumen se queda viejo en cuanto el canon cambia. Lo mostró el Screen Designer el 2026-09-25, cuando dos decisiones del día dejaron atrás dos frases de esta receta. Todas las rutas son desde la raíz del repositorio.
> **Dueño del método de pantallas:** el Screen Designer. Esta receta la mantiene el Super Agent Admin mientras dure el piloto. Nace el 2026-09-24 por decisión de Javier. **Estado: piloto, con la primera prueba aprobada por Javier el 2026-09-25.**
> **Actualizado: 2026-10-14.**

## Qué es una pantalla aquí

Una pantalla es un frame de producto que resuelve **una tarea del usuario en una plataforma concreta**, construido con piezas del design system del proyecto y nombrado para que otro la encuentre y la continúe. No es una ilustración ni una exploración libre: si no usa el sistema, no está terminada.

## Lo que esta receta no hace

- **No decide la experiencia.** El recorrido, los estados y los criterios de aceptación vienen del UX Designer o de Javier. Qué hacer si falta una decisión o no hay flujo lo dicen «La regla de escalación» de `Design/Screen Designer/SCREEN_DESIGNER.md` y el §10 de `Design/Figma/SCREEN_STRUCTURE_GUIDE_GENERAL.md`, donde está la *propuesta de flujo*.
- **No cambia piezas de la librería.** Si falta un componente, un token o una regla, haz lo que dice «Primero la librería» en `Design/Design Systems/SCREEN_DESIGN_RULES.md`: ahí está qué puedes crear en el archivo del proyecto, cómo se marca y a quién se pide.
- **No crea, renombra ni reordena páginas del archivo** sin autorización: las páginas son del File Architect.
- **No toma el oficio ni escribe en buzones.** Lo que sea de otro dueño va a la sección «Propuestas al sistema» de tu entrega, y Javier decide qué pasa con cada propuesta.
- **Lo que pide criterio lo decide Javier.** La receta cubre la parte mecánica: construir bien, con el sistema, y nombrar y comprobar como el método pide.

## Lo que te tienen que dar antes de empezar

Seguir pasos no basta: nadie diseña bien sin saber para qué es la pantalla. Lo comprobó la primera prueba. El encargo trae tres cosas, y si falta alguna, **pregúntala antes de dibujar**:

- **Qué se diseña y para qué:** la pantalla y la tarea del usuario que resuelve. **Comprueba si existe una Historia de Usuario (HU) en el proyecto:** busca en `HU/` (`Projects/<Proyecto>/HU/`) o en los enlaces de su `INDEX.md`. Si Javier no la mencionó explícitamente, búscala antes de dibujar. Si existe, la HU es la fuente de verdad funcional: úsala para alinear criterios de aceptación, estados y validaciones. Si no existe, decláralo al empezar y continúa sobre el flujo de UX o la propuesta de flujo.
- **El recorrido:** de dónde viene el usuario, a dónde va y qué decide en el camino. Si no existe un flujo escrito, dilo al empezar y sigue lo que dice el §10 de `SCREEN_STRUCTURE_GUIDE_GENERAL.md` sobre la *propuesta de flujo*.
- **Lo que ya existe:** el archivo, la página y las pantallas o piezas que ya se hicieron para ese tema.
- **La base:** si continúas sobre lo que hizo Javier, trabajas en una copia de referencia o empiezas desde cero. Las demás preguntas de presentación (anotaciones, notificaciones, numeración) están en `Design/Figma/PRESENTATION_GUIDE.md` §1.

## Cómo se complementa con las otras recetas

Lee la fuente de la receta que el encargo necesite, aunque no aparezca en el catálogo de skills de tu entorno. Las cuatro conservan los mismos cánones y no se ejecutan siempre juntas.

| Necesidad dentro del encargo | Receta y alcance |
|---|---|
| Diagnosticar una pantalla antes de rehacerla o contrastar el resultado construido | `skills/revisar-pantalla/SKILL.md`. Usa la evidencia pertinente al alcance y los estados afectados; aprovecha un diagnóstico previo si sigue correspondiendo al archivo actual. Una revisión adicional no exige repetir una auditoría completa ni producir un segundo informe con los mismos datos. |
| Entender la composición y los nombres de un componente existente | `skills/revisar-composicion-componente/SKILL.md`. Separa la lectura de cualquier renombre: la autorización para diseñar una pantalla no autoriza editar los componentes de la librería. |
| Crear o ampliar una pieza del design system | `skills/construir-componente/SKILL.md`. Entrega la necesidad al DS Manager según el §13 del método de pantallas; identidad, residencia y API se resuelven en ese encargo. Los componentes locales `[draft]` siguen la regla «Primero la librería» y no equivalen al alta en el DS. |

Estas conexiones no cambian el encargo inicial: una consulta sobre un componente puede terminar en hallazgo, y una auditoría puede terminar en diagnóstico. La construcción o corrección se ejecuta solo dentro del alcance autorizado para ella.

## Pasos

1. **Reglas de trabajo.** Lee `Javier/WORKING_WITH_JAVIER.md`, según la puerta de tareas de proyecto de `AGENTS.md`.
2. **Contexto del proyecto y HU.** Sigue `Design/Figma/SCREEN_STRUCTURE_GUIDE_GENERAL.md` §1. Busca la recepción del proyecto, su `AGENTS.md`, su capa local y si existe una HU en `HU/` (`Projects/<Proyecto>/HU/`) o enlazada en su `INDEX.md`. Si existe, léela antes de dibujar para contrastar qué comportamiento y criterios de aceptación se esperan; si no existe, dilo al inicio y trabaja sobre el flujo de UX o la propuesta de flujo.
3. **La cadena de design systems.** Un proyecto puede usar **más de un sistema**, y tienes que saber cuáles antes de dibujar. El `AGENTS.md` del proyecto dice cuál usa. Si ese sistema es un **derivado**, tiene una base: HealthPod, por ejemplo, deriva de Embit, así que una pantalla de HealthPod se alimenta de los dos. Lee primero el `INDEX.md` del derivado en `Design/Design Systems/<DS>/` y su registro de componentes, que dicen qué es propio y qué hereda de la base. Después lee el de la base. **Por cada pieza:** si el derivado tiene la suya, se usa esa; si no, la de la base. Si no sabes de cuál es una pieza, pregúntalo y no mezcles. Qué es un derivado lo explica `Design/Design Systems/DS_CONTRACT_MASTER.md` §10.
4. **Entrar a Figma.** El orden está en `Design/Design Lead/DESIGN_GOVERNANCE.md` §12: primero MCP, luego lo que ofrezca tu entorno, y a clics solo con autorización de Javier. Si tu entorno tiene la skill `figma-use`, cárgala antes de escribir en Figma.
5. **Auditar antes de tocar.** Sigue `SCREEN_STRUCTURE_GUIDE_GENERAL.md` §2 y el apartado «Primero la librería» de `SCREEN_DESIGN_RULES.md`. Mira qué existe ya en el archivo y en la librería antes de construir nada. Si rehaces una pantalla, conserva su estado previo y usa el diagnóstico vigente o la lectura pertinente de `skills/revisar-pantalla/SKILL.md`; declara qué parte y estados cubriste.
6. **Función, jerarquía y preparación.** Sigue `SCREEN_STRUCTURE_GUIDE_GENERAL.md` §3 y §4, y para el lienzo (simbología, formato de secciones, espaciado y piezas de documentación) `Design/Figma/PRESENTATION_GUIDE.md`. Para elegir contenedores (Panel o Card, región, superposición), usa `Design/Design Lead/DESIGN_PRINCIPLES.md`. Antes de la primera escritura cumple la puerta del §16 del método de pantallas y deja su tabla por región en la respuesta o en el log; ahí viven sus campos y condiciones. Contrástala con lo construido al validar y entregar.
7. **Construir con el sistema.** Sigue `SCREEN_DESIGN_RULES.md` de principio a fin: retícula, tipografía y color solo por sistema, y todo bindeado. Usa `SCREEN_STRUCTURE_GUIDE_GENERAL.md` §5 y §6 para componentes y layout, y el contrato de cada sistema de la cadena para saber qué promete cada pieza, el de la base y lo que el derivado declare distinto. **Mientras construyes, ten abierto el checklist de cierre de `Design/Figma/FIGMA_GOTCHAS.md`:** es una puerta de construcción, no un repaso al final.
8. **Textos, UX Writing y voz.** Los textos no se improvisan ni se dejan en lorems genéricos. Revisa el contrato de voz del producto o medio (`Writing/VOICE_CONTRACT_PRODUCT.md` si aplica) y las pautas de UX Writing: claridad en botones, títulos de sección, estados vacíos y mensajes de error o confirmación. Si la HU define nombres literales de pestañas o estados (según `Product/Product Manager/HU_WRITING_GUIDE.md`), respétalos textualmente en la interfaz.
9. **Nombres.** Sigue `Design/Figma/NAMING_STRUCTURE_GUIDE.md` §3, §4 y §5, y pasa su auto-verificación del §9. Si la pantalla va a una página que no existe, léete `Design/Figma/FILE_ARCHITECTURE_GUIDE.md` y proponla en vez de crearla.
10. **Estados, responsive y accesibilidad.** Sigue `SCREEN_STRUCTURE_GUIDE_GENERAL.md` §7 y §10, y la parte «Uno» de `Design/Design Lead/DESIGN_ACCESSIBILITY.md`, que es lo que se comprueba en la propia pieza. Para el prototipo, el §10 contiene «Prototipo suficiente antes de componentizar» y «Cómo se cablea en Figma»: distingue lo representado, lo conectado y lo que recorriste. **Si no cableas o no reproduces las interacciones, dilo en la entrega.**
11. **Comprobar.** Pasa el checklist de cierre de `FIGMA_GOTCHAS.md` completo, la validación de `SCREEN_STRUCTURE_GUIDE_GENERAL.md` §12 y la «Verificación medible al terminar» de `SCREEN_DESIGN_RULES.md`. Si hubo HU, comprueba que cada uno de sus criterios de aceptación esté cumplido y representado en la pantalla o en sus variantes de estado. Para ordenar la evidencia del resultado puedes usar `skills/revisar-pantalla/SKILL.md`: su contraste es lectura; las correcciones se hacen bajo el encargo de diseño y después se vuelve a verificar lo afectado. Declara los estados, modos y viewports comprobados y sus límites. **Relee después de la última escritura y mira la captura:** lo que no releíste no está hecho.
12. **Entregar.** Informa la lista vigente de `SCREEN_STRUCTURE_GUIDE_GENERAL.md` §13, incluida la tabla del §16 contrastada con lo construido, más una tabla de **regla aplicada en cada paso**: por cada paso, qué hiciste y de qué archivo salió la regla. Esa tabla es lo que permite revisar tu trabajo sin rehacerlo. Si el proyecto tiene log, registra ahí tu tramo; si no, la entrega es el registro. Termina con **«Propuestas al sistema»**, donde van las piezas que faltan en el DS, las páginas que propones, las contradicciones que encontraste y las dudas de experiencia. Si diseñaste sin HU y la pantalla introdujo reglas funcionales o de negocio nuevas, sugiere aquí levantar la HU correspondiente con el Product Manager. Para candidatos a componente y sustitución de piezas resueltas, sigue «Consolidar después de que el prototipo se aprueba» del mismo §13. Para registrar las piezas ausentes en el `PENDIENTES` del DS local y dirigirlas a su dueño, sigue «La regla de escalación» de `Design/Screen Designer/SCREEN_DESIGNER.md`. Las demás propuestas que tengan dueño se escriben además en la lista de pendientes que indique el `AGENTS.md` del proyecto, dirigidas a ese dueño. Así no depende de que alguien las copie del chat.

## Errores que ya costaron

Estos errores están explicados en `FIGMA_GOTCHAS.md`; aquí solo se nombran para que los busques:

- Frames con alto o ancho fijo que recortan a sus hijos.
- Barras y botones de la librería puestos encima del layout en vez de en su hueco.
- Títulos de sección con negrita suelta en lugar de un estilo de texto.
- Copy inventado donde el flujo ya tenía el suyo.
- Una gráfica de relleno entregada como si fuera real.
- Dar por buena una pantalla sin releerla después de la última escritura.


