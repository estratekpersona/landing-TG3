# Plan de actualización — Landing TG3 (branch `updates-presentation-24jun`)

> Fuente: Keynote del Desayuno Ejecutivo (Pablo & Luis, Estratek) + infografía NotebookLM + transcript.
> Objetivo: alinear el copy y la estructura de la landing con la **presentación actualizada**, sin romper el sistema de diseño ni la captación de leads.

---

## 0. Estado técnico (lo que ya validé)

- **Sitio estático**: un solo `index.html` (44KB), Tailwind por CDN, tipografía **Righteous**, GitHub Pages en `www.tg3estratek.com`. Sin build step.
- **Colores reales de marca** (usar estos, NO los del README):
  - `brand-aqua` = `#39afbc` (celeste primario / CTAs)
  - `brand-dark` / `brand-deepblue` = `#1d2f49` (navy, fondo)
  - `brand-bluegray` `#a0aab5`, `brand-gray` `#e2e8f0`, `brand-light` `#f8fafc`
  - Magenta `#df1a69` sólo como acento sutil (per README).
- **Formulario → Google Sheets** (Apps Script vía `fetch`): NO tocar la lógica de envío.
- Branch `updates-presentation-24jun` limpia (= main). Todo cambio va aquí.

### Orden actual de secciones
1. Hero
2. Logos clientes ("Empresas líderes que confían en Estratek")
3. `#videos-educativos` — "Aprende con Estratek" (cápsulas de YouTube)
4. `#que-es-g3` — "El Corazón del Modelo / ¿Qué es la Tecnología G3?" (3 pilares)
5. `#paradojas` — "El Problema / El patrón en 350+ organizaciones"
6. `#modelo-madurez` — "Autodiagnóstico Directivo / Modelo de Madurez TG3" (N1–N4)
7. `#demo` — formulario de agendamiento
8. Footer

---

## 1. Diagnóstico del gap (deck vs. landing)

La landing está **conceptualmente alineada** pero le faltan las 3 piezas que son la columna vertebral del nuevo keynote, y tiene copy que se puede afilar con frases del deck.

| # | Concepto del deck | ¿Está en la landing? | Acción |
|---|---|---|---|
| A | Pablo & Luis · 16 años · +350 orgs | Parcial ("350+") | Reforzar credibilidad |
| B | El engaño de las herramientas | Sí (cápsulas) | OK, afinar |
| C | **Pirámide del Conocimiento** | ❌ **Falta** | **Sección nueva** |
| D | Desalineación Estrategia/Cultura/Clima | Sí (`#paradojas`) | Afilar con "ecuaciones" |
| E | Cita de Drucker | ❌ Falta | Añadir como remate |
| F | **3 pilares = Inteligencia Lógica/Social/Relacional** | ❌ Falta el naming | **Actualizar `#que-es-g3`** |
| G | **Definición de "Tecnología"** (conocimiento aplicado ordenado → resultado repetible) | ❌ Falta | Añadir |
| H | "¿Por qué falla la ejecución?" (ecuaciones) | ❌ Falta | Añadir a `#paradojas` |
| I/J | Organismo vivo · retroceso · Proyecto de Vida Organizacional | ❌ Falta | Enriquecer `#modelo-madurez` |

---

## 2. Cambios propuestos (por sección, con el porqué)

### TIER 1 — Núcleo del nuevo keynote (alto impacto)

**1.1 · Sección NUEVA: "La Pirámide del Conocimiento"** — insertar entre `#que-es-g3` y `#paradojas` (o justo después de los pilares).
- **Qué:** visual de 6 niveles, de base a cima: **Conceptos → Principios → Métodos → Herramientas → Comportamientos → Resultados Sostenidos.** Marcar "Comportamientos" como el *punto de inflexión* (donde el conocimiento se vuelve resultado).
- **Copy ancla:** *"Las herramientas no transforman organizaciones. Lo hacen las personas y sus comportamientos."*
- **Por qué:** es la tesis central del deck y el diferenciador de por qué comprar software no basta. Hoy no existe en la landing.

**1.2 · Actualizar los 3 pilares en `#que-es-g3` con el naming de inteligencias**
- **Qué:** añadir el rótulo a cada pilar (mantener el copy actual, que ya calza):
  - Estrategia → **Inteligencia Lógica** — "hacia dónde vamos"; objetivos, procesos y KPIs.
  - Cultura → **Inteligencia Social** — "cómo decidimos actuar"; valores como hábitos.
  - Clima → **Inteligencia Relacional** — "cómo vivimos el proceso"; colaboración, sin silos.
- **Por qué:** es el vocabulario actualizado del keynote y la infografía. Da profundidad sin reescribir.

**1.3 · Añadir la definición de "Tecnología" en el intro de `#que-es-g3`**
- **Qué:** una línea destacada: *"Una tecnología no es un software: es conocimiento aplicado de forma ordenada para producir un resultado repetible."*
- **Por qué:** justifica el nombre "Tecnología G3" y desmarca del "software mágico".

### TIER 2 — Afilar lo que ya existe con copy del deck

**2.1 · `#paradojas` (El Problema): añadir las 3 ecuaciones de "por qué falla la ejecución"**
- **Qué:** bloque de remate con las tres frases:
  - **Estrategia sin cultura = dirección sin ejecución.**
  - **Resultados sin clima = éxito efímero.**
  - **Capacidad = éxito repetible.**
- **Por qué:** son punchlines memorables que cierran la sección con fuerza y conectan con "capacidad organizacional".

**2.2 · Cita de Drucker**
- **Qué:** *"La cultura se come a la estrategia de un bocado."* — Peter Drucker. Como quote destacado al final de `#que-es-g3` o inicio de `#paradojas`.
- **Por qué:** autoridad + memorabilidad; refuerza el pilar Cultura.

> ~~2.3 · Hero + credibilidad (16 años · +350 orgs)~~ — **DESCARTADO** por decisión de Chepe. El hero queda intacto. (El "350+ organizaciones" existente en `#paradojas` no se toca.)

### TIER 3 — Metáfora y cierre conceptual

**3.1 · `#modelo-madurez`: framing de "organismo vivo" + "Proyecto de Vida Organizacional"**
- **Qué:** mantener la escala N1–N4 (buena para diagnóstico granular), pero:
  - Añadir el marco: *"Las organizaciones son organismos vivos: nacen, maduran, evolucionan y también pueden retroceder."* (la madurez NO es lineal).
  - Renombrar el output del diagnóstico como **"Proyecto de Vida Organizacional"**: una ruta a la medida, no soluciones enlatadas (nada de aplicar Ninebox o feedback 360 sin la madurez para sostenerlos).
- **Por qué:** es el cierre del keynote y eleva el diagnóstico de "test" a "ruta estratégica personalizada".

---

## 3. Decisiones (resueltas)

1. **Sección Desayuno Ejecutivo:** ✅ **Se queda FUERA de la landing pública.** Los desayunos son exclusivos, cupo limitado, invite-only; el link de Luma se envía directo a clientes actuales/potenciales. El flyer queda huérfano en el repo (inofensivo; opcional moverlo a `/assets/archived/`).
2. **N1–N4 vs. 3 fases:** ✅ **Conservar N1–N4** + montar la narrativa de "organismo vivo" encima. (Default recomendado, aplicado en el prompt.)
3. **Pirámide:** ✅ **SVG/HTML nativo** (liviano, responsive). (Default recomendado, aplicado en el prompt.)

---

## 4. Prompt para Claude Code

> Pegar dentro del repo, en la branch `updates-presentation-24jun`. Decisiones ya resueltas y aplicadas — listo para correr tal cual.

```
Contexto: Este repo es la landing page de "Tecnología G3" de Estratek. Es un sitio
estático de UN SOLO archivo `index.html` (Tailwind por CDN, tipografía Righteous,
GitHub Pages en www.tg3estratek.com). Estoy en la branch `updates-presentation-24jun`.
NO hay build step. NO toques la lógica del formulario (envío a Google Sheets vía
Apps Script/fetch) ni el sistema de logos de clientes.

Sistema de diseño a respetar (ya definido en el config de Tailwind del <head>):
- brand-aqua #39afbc (celeste primario, CTAs)
- brand-dark/brand-deepblue #1d2f49 (navy, fondo)
- brand-bluegray #a0aab5, brand-gray #e2e8f0, brand-light #f8fafc
- magenta #df1a69 sólo como acento sutil
- Headings con la fuente `font-righteous`. Reutilizá los patrones existentes
  (badges `bg-brand-aqua/10 text-brand-aqua rounded-full uppercase tracking-widest`,
  cards con `border border-white/5`, secciones `py-24 px-6 lg:px-8 max-w-7xl mx-auto`).

Objetivo: actualizar el copy y la estructura para alinearlos con el keynote más
reciente del Desayuno Ejecutivo. Hacé estos cambios, quirúrgicos y consistentes con
el diseño actual:

1) SECCIÓN NUEVA "La Pirámide del Conocimiento" (insertar entre #que-es-g3 y
   #paradojas). Visual de 6 niveles de base a cima:
   Conceptos → Principios → Métodos → Herramientas → Comportamientos → Resultados
   Sostenidos. Marcá "Comportamientos" como el punto de inflexión. Construilo como
   SVG/HTML nativo, responsive, con la paleta de marca (base en brand-aqua/navy,
   cima destacada). Copy ancla arriba de la sección:
   "Las herramientas no transforman organizaciones. Lo hacen las personas y sus
   comportamientos." Badge: "La Tesis". id="piramide".

2) EN #que-es-g3 (los 3 pilares Estrategia/Cultura/Clima): añadí a cada card el
   rótulo de inteligencia, SIN borrar el copy existente:
   - Estrategia → "Inteligencia Lógica"
   - Cultura → "Inteligencia Social"
   - Clima → "Inteligencia Relacional"
   Y agregá, en el intro de la sección, una línea destacada:
   "Una tecnología no es un software: es conocimiento aplicado de forma ordenada
   para producir un resultado repetible."

3) EN #que-es-g3 o inicio de #paradojas: agregá un quote destacado
   (estilo blockquote con brand-aqua): «La cultura se come a la estrategia de un
   bocado.» — Peter Drucker.

4) EN #paradojas (El Problema): al cierre, añadí un bloque de 3 "ecuaciones" tipo
   callout, cada una en su card:
   - "Estrategia sin cultura = dirección sin ejecución."
   - "Resultados sin clima = éxito efímero."
   - "Capacidad = éxito repetible."
   Con una bajada corta para cada una (1 línea).

5) EN #modelo-madurez: conservá los niveles N1–N4 tal cual, pero:
   - Añadí arriba el marco: "Las organizaciones son organismos vivos: nacen,
     maduran, evolucionan y también pueden retroceder."
   - Reframeá el resultado del diagnóstico como "Proyecto de Vida Organizacional":
     una ruta a la medida, no soluciones enlatadas. Ajustá el copy del CTA
     "Diagnosticar mi organización" para que hable de trazar ese proyecto.

Restricciones:
- NO toques el HERO (H1, subtítulo y CTAs quedan igual). NO agregues líneas de
  estadísticas de "años/organizaciones".
- NO re-agregues ninguna sección de "Desayuno Ejecutivo" (es invite-only, va fuera
  de la landing pública).
- Mantené TODO en un solo index.html. No agregues frameworks ni build.
- No rompas el formulario ni los anchors del nav. Si agregás la sección #piramide,
  actualizá cualquier navegación interna si corresponde.
- Español de Guatemala, tono directivo y claro. Nada de relleno.
- Al final, corré una revisión: que el sitio siga renderizando (podés levantar
  `python3 -m http.server`), que no haya scroll horizontal roto, y mostrame un
  diff resumido de lo que cambiaste.
```

---

## 5. Cómo revisar en local (tu máquina)

```bash
git checkout updates-presentation-24jun
python3 -m http.server 8000
# abrir http://localhost:8000
```
