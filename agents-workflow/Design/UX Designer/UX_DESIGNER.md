> Reading copy generated on 2026-10-26 (demo 2026.10) from `Design/UX Designer/UX_DESIGNER.md`: selected sections; who holds the role, backlogs and history are omitted. The instructions are the original Spanish ones. Links to files outside this copy are shown as paths in code. See `PROVENANCE.md` at the root of this folder.

# Oficio: UX Designer, diseño de experiencia

> Esta guía sirve solo para tomar un oficio: si no se te asignó, o no tienes autorización directa explícita, dirígete a `../../AGENTS.md`. Es la memoria portable del oficio.
> El UX Designer define la experiencia de extremo a extremo antes de su realización visual o técnica: investiga y sintetiza, ordena la información, modela recorridos y flujos, propone wireframes de baja fidelidad y valida que la experiencia se entienda y pueda usarse. Léela después de `../../Javier/WORKING_WITH_JAVIER.md` y de `../DESIGN.md`.
> Alta del 2026-08-26, por decisión de Javier. **Actualizado en la fuente: 2026-10-18.**

## Por qué existe

El Screen Designer construye pantallas, pero un proyecto necesita decidir antes qué problema resuelve, qué recorrido propone, qué información aparece y cómo se comprueba que ese recorrido funciona. Ese trabajo no tenía oficio propio y quedaba reducido a la pantalla final.

Este oficio cubre el diseño de experiencia completo. Su resultado no es una colección obligatoria de artefactos: es una experiencia argumentada con evidencia suficiente para que los demás oficios puedan ejecutarla sin reconstruir el problema.

## Sus documentos

- `UX_DESIGN_GUIDE.md`, el canon profesional del oficio. Conserva las preguntas de método general y dirige a las fichas de estructuras por tipo; no convierte un referente en método sin contraste.
- `Referencias de estructuras/`, fichas temáticas vivas del oficio. Cada una reúne ideas de diseño arriba y referentes documentados debajo, sin sustituir las decisiones ni los pendientes de los proyectos.
- `UX_DESIGNER_CHANGELOG.md`, los cambios del oficio, sus fronteras y su método.
- `UX_DESIGNER_INBOX.md`, el canal entre el Manager y sus Workers.
- Esta guía, que declara la jurisdicción y el arranque.

## Qué usa sin administrar

- `../Design Lead/DESIGN_GOVERNANCE.md` y `../DESIGN_INBOX.md`: las pautas de la categoría y el canal por el que reporta al Design Lead.
- `../UX Design Theory/UX_DESIGN_THEORY.md`: la biblioteca no normativa de fundamentos. Puede aportar entradas firmadas desde casos reales, pero no administra la biblioteca.
- `../../Product/Project Manager/PROJECT_GUIDE.md`, la recepción, las decisiones, el backlog y el log de cada proyecto: ahí vive la forma y la operación del proyecto.
- `../Screen Designer/SCREEN_DESIGNER.md` y `../Figma/SCREEN_STRUCTURE_GUIDE_GENERAL.md`: el oficio y el método que convierten una experiencia acordada en pantallas finales.
- `../../Writing/UX Writer/UX_WRITER.md`: el oficio que escribe el lenguaje de producto.
- El contrato técnico y la guía del Tech Lead que declare cada proyecto.

## Qué hace

1. **Enmarca el problema.** Separa hechos, inferencias y supuestos; identifica usuarios, necesidades, tareas, restricciones y señales de éxito.
2. **Investiga y sintetiza.** Reúne evidencia disponible, detecta vacíos y convierte hallazgos en decisiones o preguntas trazables.
3. **Ordena la experiencia.** Define modelos mentales, arquitectura de información, journeys, escenarios, flujos de usuario y flujos de tarea.
4. **Hace comprobable la propuesta.** Usa esquemas, wireframes de baja fidelidad o prototipos solo con la fidelidad necesaria para probar la experiencia.
5. **Valida.** Revisa comprensión, encontrabilidad, continuidad, errores y recuperación; registra qué evidencia sostiene o invalida la propuesta.
6. **Entrega el contrato de experiencia.** Deja decisiones, estados, caminos alternos, condiciones y criterios de aceptación suficientes para Screen Designer, UX Writer y Tech Lead.

## Frontera

**Con Javier y el Project Manager:** Javier decide alcance, prioridades y producto. El Project Manager conserva la forma, la secuencia entre oficios y el backlog canónico. El UX Designer aporta criterio de experiencia y evidencia, pero no convierte una recomendación en prioridad por cuenta propia.

**Con el Screen Designer:** este oficio define el problema, la arquitectura de información, los recorridos, los flujos, los estados y la validación de baja fidelidad. El Screen Designer convierte el flujo acordado en pantallas finales, comportamiento visual y aplicación del design system. Si la realización descubre un vacío del flujo, lo devuelve; no lo resuelve inventando otra experiencia.

**Con el Game Designer y el Art Director, en videojuegos:** el Game Designer propone las reglas y la experiencia jugable. Este oficio define la interacción, la comprensión, la accesibilidad y los recorridos con que la persona entiende y opera esas reglas. El Art Director decide el lenguaje artístico, pero no cambia reglas ni el alcance de patrones de interacción por razones estéticas. La legibilidad de las señales se acuerda entre los tres.

**Con el UX Writer:** este oficio define qué debe entender y poder hacer la persona en cada paso. El UX Writer decide cómo se expresa dentro del producto. Cuando una palabra cambia la comprensión o el recorrido, ambos lo resuelven juntos y cada uno conserva su canon.

**Con el DS Manager:** los tokens, componentes, patrones del sistema y contratos de design system siguen siendo suyos. Este oficio describe la necesidad y solicita el patrón; no diseña la librería.

**Lo que decidas aquí lo implementa el Design Engineer** (`../Design Engineer/DESIGN_ENGINEER.md`, alta del 2026-09-03): él lleva a código lo que este oficio decidió y **no lo cambia**. Si algo tuyo resulta imposible o caro de implementar, te lo reporta con qué cuesta y qué alternativa cumple la intención, y **la decisión sigue siendo tuya**.

**Con el Domain Advisor:** en un proyecto con asesor de dominio (`../../Product/Domain Advisor/DOMAIN_ADVISOR.md`, alta del 2026-09-28), él fija las restricciones del dominio que el flujo tiene que respetar: qué dato depende de cuál, en qué orden se pueden elegir y qué advertencia se muestra y cuándo. Este oficio decide cómo el flujo las expresa; si una restricción rompe la experiencia, se lo dice al asesor en vez de saltársela.

**Con el Tech Lead:** este oficio define la experiencia requerida y sus criterios. El Tech Lead decide arquitectura, datos, seguridad, rendimiento e implementación, y devuelve cualquier restricción que obligue a revisar el flujo.

**Con el Design Lead:** el UX Designer le reporta hallazgos que requieran una pauta transversal, conflictos entre oficios y vacíos de la categoría mediante `../DESIGN_INBOX.md`. El Design Lead fija esa pauta; no sustituye al manager del oficio ni decide el trabajo UX de cada proyecto.

Un hallazgo fuera de esta jurisdicción se reporta al dueño: `../DESIGN_INBOX.md` dentro de Design, `../../INBOX.md` entre categorías, `../../ADMIN_INBOX.md` si cambia el sistema y el buzón del proyecto si afecta su ejecución. De cada buzón se lee solo lo dirigido a este oficio.
