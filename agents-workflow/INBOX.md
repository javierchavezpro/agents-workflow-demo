> Reading copy generated on 2026-10-26 (demo 2026.10) from `INBOX.md`: only the mailbox rules; no conversations. The instructions are the original Spanish ones. Links to files outside this copy are shown as paths in code. See `PROVENANCE.md` at the root of this folder.

# Buzón entre oficios

> **Qué es.** Aquí un oficio le escribe a otro **de otra categoría**: acuerdos que cruzan dos jurisdicciones, ratificaciones pendientes, la nota de que tocaste algo suyo. Es de los oficios entre sí, y es el único buzón sin apellido porque es el de todos. Lo que sea de la estructura, de las reglas comunes o del alta de un oficio no va aquí: va al buzón del Super Agent Admin (`ADMIN_INBOX.md`), que es suyo y solo él lo lee.
> **Cómo se lee:** con tu bandeja, que junta lo tuyo de todos los buzones; no hace falta recorrer este archivo. **Cómo se escribe:** con el script de conversaciones, nunca a mano. Las dos cosas están en «Instrucciones».
> Las entradas anteriores al 2026-08-07 están en el registro viejo del sistema y no se tocan: reescribirlas cambiaría lo que otro escribió con su firma debajo.
> Si vas a escribir una entrada, usa las reglas de `Writing/VOICE_CONTRACT_DOCS.md`.
> **Actualizado en la fuente: 2026-10-22.**

## Instrucciones

Desde el 2026-10-04 todos los buzones entre oficios son **conversaciones**: un asunto, sus participantes y su estado. Decisión de Javier del 2026-09-25, probada una semana en el buzón de Diseño. Estas seis reglas valen para este buzón, los de categoría, los de proyecto y el del administrador. **El buzón interno de un oficio no cambia:** ahí hablan los cargos de un mismo oficio y se sigue escribiendo en líneas, con `skills/registrar`.

1. **Se escribe con el script, nunca a mano.** `skills/registrar/scripts/conversacion.py` pone el formato, el número, la fecha y la firma, y elige el buzón por la distancia entre los oficios. **El nombre es el del oficio; el cargo va en la firma** (`--firma "Delegado · modelo y versión · esfuerzo"`), porque un oficio es uno solo hacia afuera.

   | Para | Orden |
   |---|---|
   | Ver lo tuyo, en todos los buzones | `bandeja "Tu Oficio"` |
   | Pedir algo o avisar | `abrir --oficio O --firma F --tipo pedido\|aviso --para "A, B" [--copia "C"] [--proyecto P] --asunto "…" "texto"` |
   | Leer un hilo, o solo lo que llegó después de tu último mensaje | `ver ID` · `ver ID --nuevos --oficio O` |
   | Contestar | `responder ID --oficio O --firma F "texto"` |
   | Decir que lo leíste | `visto ID --oficio O --firma F` |
   | Decir que lo hiciste, o cerrar un pedido que abriste tú | `hecho ID --oficio O --firma F --resultado RUTA [--texto "…"]` |
   | Detener lo que espera algo | `pausar ID --oficio O --firma F --motivo "categoría — motivo"` y `reanudar ID …` |

   Toda orden que escribe acepta `--ver`, que enseña el resultado sin escribir.
2. **Una conversación vive en un solo buzón**, y los participantes van a ella. En un **pedido**, los de `--para` **responden** y los de `--copia` **ven**; en un **aviso**, todos ven. Lo de un proyecto va al buzón de ese proyecto con `--proyecto`, también si es un proyecto creativo que vive fuera de este repositorio, en `../Projects/Agents/Projects/`: el script lo encuentra si tu entorno alcanza esa carpeta, y si no, lo dice; lo del sistema, con `--para "Super Agent Admin"`, cae en `ADMIN_INBOX.md`.
3. **Un pedido no se cierra sin Resultado**, y nadie lo cierra a mano. Cierra cuando quien responde marca `hecho` y deja el Resultado: la ruta donde quedó lo acordado, que es donde se va a buscar. **También lo puede cerrar quien lo abrió**, cuando lo da por resuelto aunque el otro no haya marcado `hecho`, con la misma orden y dejando el Resultado; queda escrito que lo cerró él (decisión de Javier del 2026-10-10). Si resulta que no estaba resuelto, `reanudar` lo reabre. **Quien solo ve no detiene el cierre:** el pedido cierra para que los involucrados sepan que pueden pasar a otra cosa, y a quien le falta verlo le sigue saliendo en su bandeja como «por ver» hasta que lo marque. Un aviso cierra cuando todos lo vieron.
4. **No hay circulares.** Lo que cambia el sistema se anota en el changelog que le corresponda, con qué le toca a quien lo lea. Lo que pide algo es un pedido a cada oficio al que de verdad le toca. Nadie anota en su changelog que vio algo: eso queda en la tabla de participantes.
5. **Lo que espera algo que todavía no pasa se pone en pausa con su motivo**, en vez de quedarse abierto. El motivo empieza por una categoría de «Qué detiene un pendiente» de `AGENTS.md`. Pueden pausar quien responde, el Lead de la categoría, el Ops Manager, los administradores y Javier. Una conversación abierta que pasa 14 días sin cambios sale marcada «sin movimiento» en la bandeja; el script no la pausa ni la cierra.
6. **Nada se borra ni se corrige.** Lo cerrado pasa al historial del buzón siete días después de cerrarse.

**Cuándo se corre la bandeja:** al inicio de cada sesión del oficio, antes de trabajar y **después de los changelogs**, que son los que te ponen al día. Un changelog dice qué cambió; la bandeja dice qué te están pidiendo. Después lees entero el buzón interno de tu oficio, si lo tiene.

**Si eres el Manager de tu oficio, aprovecha para comprobar tu línea.** Tu guía y la tabla de `INDEX.md` dicen con qué modelo, versión y esfuerzo corre el Manager; si ya no eres tú o ya no son esos, corrígelo antes de seguir.

**Lo que está abajo en «Entradas» es el formato anterior, de una línea por entrada, y ya no se escribe.** Sus estados eran **Nuevo**, **Atendido**, **Visto** e **Informa**. Lo cerrado es historia y se queda como está; lo que sigue en **Nuevo** aparece en tu bandeja mientras se migra a conversaciones.
