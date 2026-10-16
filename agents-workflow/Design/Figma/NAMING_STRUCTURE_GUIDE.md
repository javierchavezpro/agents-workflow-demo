> Reading copy, 15 October 2026. Source: `Design/Figma/NAMING_STRUCTURE_GUIDE.md`. Selected sections only; live backlogs, occupants and history omitted. Original Spanish instructions retained. Referenced canons outside this selection are dependencies, not bundled files; see PROVENANCE.md. This is documentation, not an operational checkout.

# Nomenclatura y estructura de frames: guía de generación (agentes)

## 6. Componentes

- Canon: **`Familia / Nombre`** con espacios (`Card / KPI Summary`). El slash agrupa la familia en el panel de assets; también lleva espacios (`Chart / Bar`, no `Chart/Bar`).
- **El slash nunca es puntuación.** Figma agrupa por cada `/` que encuentre, con espacios o sin ellos: los espacios son legibilidad nuestra y él los ignora al armar la familia. De ahí salen dos cosas. Cada slash abre un nivel, así que cuántos lleva un nombre es una decisión de agrupamiento y no de estilo (`Chart / Bar / Vertical` declara una subfamilia Bar). Y un slash dentro de un nombre parte el nombre: `Recruitment Status - On Pause/Multiple Processes` no se leía como un nombre con barra, creaba una familia `Recruitment Status - On Pause` con un miembro `Multiple Processes`. Cuando la barra es puntuación, se usa coma o `y`.
- Piezas internas: prefijo **`[block] `** con espacio tras el corchete; viven junto a su set padre (regla del contrato de cada DS; en Embit, `../Design Systems/Embit/Contract/EMBIT_DS_CONTRACT.md` §2).
- **Title Case en el nombre del componente** (decisión Javier, 2026-08-11): `Radio Button`, no `Radio button`. Las palabras menores van en minúscula (`[block] Menu List with Status`). Vale para cada segmento del slash y para el nombre tras el prefijo.
- Variantes = propiedades (`Variant`, `Color Style`, `Size`, `State`); sin slash en valores de variante. **Los valores también son nombre**, así que se nombran por intención y nunca se dejan los que Figma autogenera (`Variant2`, `Type4`, `Location4`): un valor autogenerado suele estar tapando un eje mal armado.
- **Los booleanos se nombran por lo que encienden, y `Show` queda para lo que no llega al producto** (decisión Javier, 2026-09-27). Si el booleano muestra algo que forma parte del producto, su nombre es el sustantivo de eso, en Title Case: `Label`, `Leading Icon`, `Badge`, `Actions`. Si muestra una ayuda de revisión que nunca se entrega, lleva `Show` delante: `Show Touch Area`. Así el prefijo informa por sí solo: quien lee `Show` sabe que ese interruptor no cambia lo que ve el usuario. No van `Has`, abreviaturas (`Left Fig`) ni símbolos (`⊗`). **Si el sustantivo ya lo ocupa otra propiedad del mismo componente**, y pasa porque Figma no deja dos propiedades con el mismo nombre, el booleano se queda con el sustantivo y lo que llena ese elemento lleva apellido: el slot ya se llama `Leading Slot`, así que su booleano es `Leading`; el texto de un chart pasa a `Value Text` para que su booleano sea `Value`.
- El calificador fino con guion (`Button Icon - Pin Map`) sigue válido cuando no se quiere abrir categoría en el panel. La migración de nombres existentes con ` - ` o `_` va por barrido planificado, no al paso.
- Los sufijos tipo `_Old` no marcan fósiles: los fósiles van a `📦 Archive`.
- **`[placeholder]` y `[draft]` no son lo mismo** (decisión Javier, 2026-08-11). `[placeholder]` es contenido de relleno, el estado de reposo de algo que sí existe: el slot vacío que espera al consumidor, la imagen que ocupa el lugar mientras no hay una real. No es deuda y no muere. `[draft]` marca la pieza provisional de un componente que todavía no existe, con su petición en el backlog, y muere cuando el componente se construye. Los dos son marcadores legítimos y un DS está lleno de los primeros; lo que no puede pasar es que compartan prefijo, porque entonces un barrido del backlog manda construir componentes que nunca faltaron.
- Dónde vive un componente (el DS base o su derivado): lo decide el contrato del DS; en Embit, `../Design Systems/Embit/Contract/EMBIT_DS_CONTRACT.md` §10.

## 6b. Frames de documentación en archivos de DS

Los frames que documentan el sistema dentro del archivo (portadas, muestrarios, plantillas de anatomía, playgrounds) son **capa de presentación**: existen para informar a otros sobre los componentes y su uso, no son pantallas de trabajo. Por eso pueden romper la norma estándar cuando la presentación lo pida (decisión Javier, 2026-08-05); en particular su idioma sigue a su audiencia, y conviven legítimamente `Page - Shape & Elevation` y `Muestrario - Radios y trazos`.

Su familia se declara con guion espaciado, no con slash, para que el frame no cree carpetas al exportarse:

- `Page - <nombre de la página>`: el frame principal de contenido de una página de documentación o foundation.
- `Muestrario - <tema>`: specimen que demuestra tokens o estilos bindeando el valor, nunca rotulándolo.
- `Doc - <componente>`: documentación de un componente. **Las anatomías viven aquí** (`Doc - <componente> - Anatomía`); si algún día se juntan en página propia, la familia se re-evalúa ahí (decisión Javier, 2026-08-05).
- `Test Playground - <componente>`: frame de pruebas junto a su set.
- `Note Card`: nota al margen, nombre simple.

Las piezas de documentación que se instancian en cualquier archivo (leyenda, registro de versiones de página, ficha, nota con indicador, playground) las define `PRESENTATION_GUIDE.md` §5 con nombres provisionales; este canon los ratifica cuando nazcan.

## 9. Auto-verificación al entregar

Además de las metas que declare el DS del proyecto en turno (`../Design Systems/SCREEN_DESIGN_RULES.md`, «Verificación medible al terminar»; en Embit, `../Design Systems/Embit/Governance/EMBIT_DESIGN_GUIDES.md` §8: textos con estilo, retícula, tokens), reporta:

- [ ] 0 nombres por defecto (frames, groups, textos).
- [ ] Capa de producto en español o idioma del cliente, capa de construcción en inglés; excepciones dichas explícitamente.
- [ ] Pantallas en canon de jerarquía y ejes; el viewport es sufijo y los pares responsive solo difieren en ese valor.
- [ ] Shell según tecnología destino, con la elección anotada.
- [ ] Textos por rol, o keys i18n si el proyecto los tiene.
- [ ] Secciones con estado declarado (color de la simbología).
- [ ] Groups solo en contenido exclusivo de animación.

---

*Establecido por Javier (2026-08-04 y 2026-08-24, conversaciones de auditoría y redefinición de nomenclatura). Cambios a esta guía: decisión de Javier.*

