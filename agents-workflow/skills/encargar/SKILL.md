---
name: encargar
description: Prompt completo y esfuerzo recomendado para encargar trabajo a un worker o a un delegado. Úsala cuando un plan reparta trabajo a otra conversación o Javier pida «el prompt para el worker».
---

> Reading copy generated on 2026-10-26 (demo 2026.10) from `skills/encargar/SKILL.md`: complete except its example. The instructions are the original Spanish ones. Links to files outside this copy are shown as paths in code. See `PROVENANCE.md` at the root of this folder.

# Encargar a un worker

> **Skill de tarea.** Es la forma que toma la regla 16 de `Javier/WORKING_WITH_JAVIER.md`: todo encargo a un worker se entrega con su prompt completo y su esfuerzo recomendado. La regla dice qué se exige; esta plantilla dice cómo se ve. No copia ningún canon: donde hay una regla, la cita. Todas las rutas son desde la raíz del repositorio.
> **Dueño:** el Super Agent Admin. Nace el 2026-09-28 por decisión de Javier, sobre la práctica que el DS Manager asentó el 2026-09-26 en `Design/DS Manager/DS_MANAGER.md` («Reglas de operación»). **Estado: en uso.**
> **Actualizado en la fuente: 2026-10-12.**

## Por qué existe

Javier lanza cada encargo en una conversación nueva y **borra las conversaciones de los workers** al terminar. El worker no sabe nada de lo que se habló antes, y Javier no debería tener que reconstruirlo. Por eso el prompt va **completo cada vez que se comparte**, aunque sea la segunda vuelta del mismo encargo: nunca «el mismo de antes» ni «lo que te pasé ayer».

## Las dos piezas de cada encargo

**1. La recomendación de esfuerzo, con su porqué.** Va arriba, antes del prompt, porque Javier la necesita para elegir modelo y esfuerzo al abrir la conversación. El porqué es una frase que dice **qué parte del trabajo pide cuidado**, no cuánto trabajo es: «es lectura sistemática, pero hay que distinguir medida ligada de número fijo» sirve; «es largo» no.

**2. El prompt ajustable**, en un bloque de código para que se copie tal cual. Lo que se puede cambiar va **entre corchetes**. Es autosuficiente: quien lo lea sin ningún contexto sabe qué hacer y dónde dejarlo.

## La plantilla

```
Eres un worker del [oficio que encarga] en el sistema de oficios de Javier (carpeta agents-workflow). Lee primero [lo mínimo: la guía o sección del canon que manda sobre este trabajo, con su ruta].

Encargo[, SOLO LECTURA si aplica]: [qué hacer, en una o dos frases, y para qué sirve].
[El detalle: lista corta de lo que hay que revisar, producir o cambiar. Si toca Figma: archivo con su fileKey y las páginas o nodos.]
[Si toca Figma — Base: continuar sobre [enlace a lo de Javier] / copia de referencia de [enlace] / desde cero. Lienzo según Design/Figma/PRESENTATION_GUIDE.md.]

Lo que ya existe: [lo que ya se hizo o decidió, con ruta, para que no lo rehaga ni lo contradiga].

No toques: [lo que queda fuera: otros archivos, otros modos, decisiones que son de otro].

Entrega en [ruta], [dónde dentro del archivo, por ejemplo «sección nueva "Resultado X" antes de "Decisiones abiertas"»], [en qué forma: tabla, lista, párrafo]. [Si deja rastro en un registro: cuál y con qué marca.]
Abre esa entrega antes de tu primer cambio y anota cada paso al terminarlo, no al final: [qué anotar; en Figma, qué nodos y qué variables] y qué quedó verificado. Tu entrega cierra siempre con una sección «Para continuar»: hecho y verificado · hecho sin verificar · sin empezar · la siguiente acción concreta · lo que espera a Javier.
Firma como dice la regla 7 de FAST_TRACK.md: cargo primero, [Worker · modelo y versión · esfuerzo].
```

Cada línea responde una pregunta que el worker haría si pudiera: qué leo, qué hago, qué ya está, qué no toco, dónde lo dejo, cómo lo retoma otro si me corto, cómo firmo. Si una línea no aplica, se borra; no se deja vacía. **La del relevo no se borra nunca, y tampoco la de la base en un encargo de Figma:** si viene vacía, el worker tiene que preguntar antes de tocar el archivo (`Design/Figma/PRESENTATION_GUIDE.md` §1, decisión de Javier del 2026-10-09).

## El relevo: todo encargo deja cómo continuarlo

Decisión de Javier del 2026-10-07, a pedido del DS Manager. En la prueba en la nube, un lote de color de Embit se cortó por presupuesto sin nada escrito, y para saber qué se había aplicado hubo que releer Figma entero. Vale para trabajo local y en la nube; en la nube pesa más, porque el corte por presupuesto o por cuota llega sin aviso.

- **La entrega se abre al empezar, no al terminar.** El worker crea su sección o su archivo de entrega antes del primer cambio y anota cada paso cuando lo termina. Lo que no se escribió antes del corte no existe para quien sigue.
- **«Para continuar» va siempre, aunque el trabajo termine.** Cinco líneas: hecho y verificado; hecho sin verificar; sin empezar; la siguiente acción concreta; lo que espera a Javier. Si todo terminó, las tres del medio dicen «nada» y eso también es información.
- **Quien coordina cierra con relevo.** Un delegado que se detiene, por presupuesto, cuota o permiso, dice en su reporte en qué paso quedó cada encargo abierto y trae **el prompt de continuación ya escrito**, completo, como cualquier otro prompt de esta plantilla.

## Lo que tienes que tener antes de escribirlo

Es lo mismo que te tienen que dar a ti antes de un trabajo (ver «Lo que te tienen que dar antes de empezar» en `skills/disenar-pantalla/SKILL.md`), ahora del otro lado: **qué y para qué**, **el recorrido o el orden** si hay uno, y **lo que ya existe**. Si a ti te falta alguna de las tres, al worker también le va a faltar: pregúntalo antes de escribir el prompt, no se lo dejes a él.

## Casos que cambian la forma

- **Un delegado cuya conversación sigue viva** (hoy, el de Javium): su prompt **reúne todo lo que tiene pendiente**, no solo el encargo nuevo, para que Javier le pegue una sola cosa.
- **Varios encargos en un plan:** cada uno en su propia sección, con su esfuerzo y su bloque. Si uno depende de otro, dilo en la línea de esfuerzo («se lanza cuando B1 esté entregado»).
- **Un encargo que se repite tras una corrección:** el prompt nuevo va entero con la corrección integrada, no como «igual que antes, pero…».

## Errores que se repiten

- **Describir el encargo sin prompt.** Fue lo que originó la regla: un plan que decía qué haría cada worker, sin nada que Javier pudiera pegar.
- **Dar contexto que solo existe en tu conversación:** «lo que hablamos», «el componente de antes». Nombra el archivo, el nodo, la ruta.
- **Dejar la entrega para el final.** Si el trabajo se corta, no queda nada, y el siguiente tiene que reconstruir lo hecho leyendo el resultado.
- **Olvidar dónde se entrega.** Un worker que no sabe dónde escribir escribe donde puede, o entrega en su chat, que Javier va a borrar.
- **Copiar reglas en el prompt.** Apunta a la guía; si la regla cambia, el prompt copiado queda viejo.
