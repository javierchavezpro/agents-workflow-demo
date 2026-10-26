---
name: registrar
description: Escribe una entrada de registro en el archivo que le toca, con la fecha del reloj de Javier. Úsala al terminar un tramo, en vez de elegir a mano entre los registros del repositorio.
---

> Reading copy generated on 2026-10-26 (demo 2026.10) from `skills/registrar/SKILL.md`: the instructions; its scripts are not included. The instructions are the original Spanish ones. Links to files outside this copy are shown as paths in code. See `PROVENANCE.md` at the root of this folder.

# Registrar un tramo

> **Dueño del método:** el **Super Agent Admin**, `../../System/Super Agent Admin/SUPER_AGENT_ADMIN.md`, que es donde vive el género registro. **La corre** el Ops Manager como las demás. Nace el 2026-09-20, por decisión de Javier.
> **Qué resuelve:** hay 33 destinos de registro en el repositorio. Elegir entre ellos en medio del trabajo no es una regla, es un impuesto, y por eso el registro se aplazaba al cierre. Cuando el cierre no llega, porque la conversación se queda sin contexto, el estado se pierde.

## Cómo se corre

```
cd ~/agents-workflow
python3 skills/registrar/scripts/registrar.py --oficio "Tech Lead" --firma "Claude Opus 5" "qué pasó"
```

| Opción | Para qué |
|---|---|
| `--oficio` | Quién escribe. Se puede abreviar si no hay dos que se parezcan |
| `--firma` | Identidad con versión y esfuerzo |
| `--estado en-curso` | El tramo no terminó. La entrada sale marcada `· **en curso**` |
| `--para "Oficio"` | La entrada va al buzón del destinatario en vez de a tu registro |
| `--a Manager\|Delegado\|Worker` | Solo en el buzón interno de tu propio oficio: a qué cargo le escribes. Ahí **De** y **Para** son cargos, no oficios; el **De** sale del cargo con que empieza tu firma, y sin los dos el script no escribe (corregido el 2026-09-28, lo reportó el Delegado del Ops Manager) |
| `--marca` | Estado de una entrada de buzón: `Nuevo`, `Informa`, `Visto`, `Atendido`. Por defecto **Nuevo** |
| `--ver` | Enseña qué escribiría y dónde, sin escribir |

## Qué decide el script y qué no

**Decide el destino**, que se deduce y no se juzga: con `--para` va por la distancia, como mandan los encabezados de los buzones: al buzón propio del oficio solo si quien escribe es de ese mismo oficio, a `ADMIN_INBOX.md` si el destinatario es el Super Agent Admin, al de la categoría si los dos oficios la comparten, y si no al general, `INBOX.md`. **Corregido el 2026-09-24:** antes iba primero al buzón propio del destinatario, que es interno, y así escribieron ahí desde fuera el Brand Designer y el propio Super Agent Admin; sin `--para` va al changelog del oficio, o a su worklog si lo tiene y el tramo va en curso.

**Pone la fecha preguntándole al reloj de Javier**, con `TZ=America/Mexico_City`. **Esa es la razón principal de que exista.** La regla 5 se rompió cuatro veces en dos semanas y siempre por lo mismo, heredar la fecha del contexto de la conversación en vez de consultarla. Aquí no se puede: el texto de la conversación no toca la fecha.

**Escribe el formato, la firma y la posición.** En un changelog o worklog entra justo debajo de `## Registro`, que es donde va lo más reciente; en un buzón, al final. Nadie inserta a mano, así que nadie renumera lo que otro cita.

**No decide qué se escribe.** El texto es tuyo y el script no lo toca.

**Y nunca deja una entrada de buzón sin marca de estado.** Si no declaras `--marca`, pone **Nuevo**. Una entrada sin marca no es abierta ni cerrada: es invisible, porque ningún tablero puede contarla, y el 2026-09-19 ese balde tenía 52 entradas. El script se estrenó cometiendo ese error en su primera corrida real y se corrigió en el mismo tramo.

## No mantiene tabla de oficios

Los descubre del disco: recorre las categorías, toma cada carpeta de oficio y busca sus archivos por sufijo, `_CHANGELOG.md`, `_WORKLOG.md`, `_INBOX.md`. **Un oficio nuevo funciona el día que nace, sin tocar este archivo.** Una tabla de 33 filas habría envejecido con la primera alta, que es la regla 9.

## Cuando falla, falla ruidoso

Si no reconoce el oficio, lo dice y lista los que ve. Si el oficio no tiene changelog ni worklog, **se niega a escribir** y dice que su registro no tiene casa propia. No inventa destino: escribir en el sitio equivocado es peor que no escribir, porque nadie lo encuentra después.

## Un tramo en curso no estrena archivo

Entra en el mismo registro con su marca. Un changelog que solo admite lo terminado obliga a callar lo que quedó a medias, que es justo lo que esta regla venía a evitar. La marca `en curso` ya existía como categoría de pendiente desde el 2026-09-13; aquí se extiende a los registros.

## Cómo se sabría que no se cumple

Cada entrada que pasa por aquí lleva la fecha del reloj y el formato exacto. Se puede contar cuántas entradas del día lo cumplen y cuántas se escribieron a mano. **Una entrada de registro sin comando detrás es la señal**, la misma que pide la pauta 8 del canon del sistema.

## Conversaciones de buzón

Desde el 2026-10-04 todos los buzones entre oficios se escriben como conversaciones con `scripts/conversacion.py`: `abrir`, `responder`, `visto`, `hecho`, `pausar`, `reanudar`, `bandeja` y `ver`. Las reglas y las órdenes viven en `../../INBOX.md`, «Instrucciones». **`registrar.py --para` solo escribe ya en el buzón interno del propio oficio**, con `--a` para el cargo; hacia cualquier otro oficio se niega y enseña la orden de `conversacion.py` que toca. Lo que el script garantiza: el nombre es un oficio del padrón (el cargo va en la firma), un mensaje puede traer varias líneas, un pedido cierra cuando quien responde termina y hay Resultado, o cuando quien lo abrió lo da por resuelto con `hecho` y su Resultado (desde el 2026-10-10), y a quien solo ve le queda «por ver» en su bandeja.

**La bandeja dice cuándo te contestaron, y `ver --nuevos` enseña solo eso.** Si esperabas a otros y el último mensaje del hilo no es tuyo, la fila dice «hay mensaje nuevo de X» y sube arriba; antes una respuesta se veía igual que el silencio. `ver ID --nuevos --oficio O` muestra la cabecera y solo los mensajes posteriores a tu último mensaje, para no releer un hilo largo. Ninguna de las dos cosas guarda estado: salen del propio hilo. Entraron el 2026-10-05, de una propuesta del Delegado en Grok.

**Los buzones de la capa creativa también cuentan.** Desde el 2026-10-05 el script descubre los buzones de `../Projects/Agents/` con la misma regla que los tableros del Ops Manager: la ruta declarada, o una carpeta vecina con las dos marcas (`PROJECTS.md` y `CPSA/CPSA.md`). La bandeja los incluye y `--proyecto` abre en ellos, aunque el proyecto viva dentro de otro. Si el entorno no alcanza esa carpeta, la bandeja simplemente no los trae y `--proyecto` lo avisa.

**Para migrar lo que quedó abierto en el formato anterior** hay dos órdenes: `viejas RUTA_DEL_BUZON` lista las entradas que siguen en Nuevo con su número de línea, y `migrar --buzon RUTA --linea N --tipo pedido|aviso --oficio O --firma F` pasa una a conversación conservando quién la escribió y cuándo, y deja la línea vieja marcada con a dónde se fue. `--abrio`, `--para`, `--copia` y `--asunto` corrigen lo que la línea original no trae en limpio.
