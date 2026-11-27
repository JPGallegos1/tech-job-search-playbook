# Tech Job Search Playbook

Un playbook reutilizable para armar tu propia **búsqueda laboral en tech asistida por bot** — con Grok Bot, Cursor, ChatGPT o el asistente que uses — sin datos personales reales y con filtros 100 % tuyos.

Esta guía no te vende un perfil prearmado. Te da el sistema: de dónde sacar avisos, cómo puntuarlos, cómo llevar el seguimiento sin duplicados, cómo espaciar envíos y qué queda siempre en borrador para que lo apruebes.

---

## ¿Cómo funciona el flujo?

1. **Fuentes** — Portales tech y remotos, redes (LinkedIn / X), portales locales y consultoras boutique. Preferí avisos con email de postulación publicado.
2. **Filtro 1–10** — Cada aviso se puntúa según roles, stack, modalidad, idioma, banda salarial y frescura. Un **buen encaje** es puntaje **≥ 7**.
3. **Tracker sin duplicados** — `tracker.csv` es la fuente de verdad: una fila por aviso (también los descartados), para no evaluar dos veces la misma empresa + rol.
4. **Cola espaciada / borradores** — Los buenos encajes con email van a `queue.json`. El envío toma como máximo **1 ítem por corrida**, con ≥ 12 minutos entre mails y solo en horario laboral. Respuestas y follow-ups salen **siempre** como borrador.
5. **5 rutinas + 1 opcional** — Búsqueda diaria, rastreo de LinkedIn, envío, respuestas/seguimiento y resumen semanal; más una opcional para vigilar 1–3 empresas objetivo. Se crean **en pausa** hasta que vos las actives.

El detalle completo está en [`guia-busqueda-laboral-tech.md`](./guia-busqueda-laboral-tech.md).

---

## Arrancar en 2 minutos

### Opción recomendada — Pasarle la guía al bot

1. Cloná este repo (o descargá `guia-busqueda-laboral-tech.md`).
2. Compartí ese archivo con tu bot y pedile que te configure el sistema.
3. El bot te entrevista **pregunta por pregunta**, genera `PLAN.md`, `tracker.csv`, `queue.json` y `sent.log`, y deja las rutinas creadas **en pausa**.
4. Revisá el resumen, corregí lo que haga falta y recién ahí autorizá activarlas.

### Opción manual — Completar el plan a mano

1. Copiá [`templates/PLAN.example.md`](./templates/PLAN.example.md) a `PLAN.md` (por ejemplo en una carpeta `job-search/`).
2. Completá los placeholders con tus filtros, CVs y reglas.
3. Copiá las plantillas de `templates/` a tus archivos de trabajo (`tracker.csv`, `queue.json`, `sent.log`) y dejá la cola vacía `[]` y el log vacío al inicio, o pedile al bot que los genere a partir de tu plan.
4. Pedile a tu bot que cree las rutinas de la sección 6 **en pausa** y esperá tu OK antes de enviar nada.

> **Privacidad:** este repo ignora a propósito tus archivos personales (`PLAN.md`, `tracker.csv`, `queue.json`, `sent.log`, CVs, etc.). No subas tu CV ni datos reales al remoto.

---

## Estructura del repo

| Ruta | Qué es |
| --- | --- |
| [`README.md`](./README.md) | Esta presentación |
| [`guia-busqueda-laboral-tech.md`](./guia-busqueda-laboral-tech.md) | Guía completa: onboarding del bot, filtros, fuentes, archivos, redacción y rutinas |
| [`templates/PLAN.example.md`](./templates/PLAN.example.md) | Plantilla de `PLAN.md` lista para completar |
| [`templates/tracker.example.csv`](./templates/tracker.example.csv) | Encabezado del tracker + filas de ejemplo ficticias |
| [`templates/queue.example.json`](./templates/queue.example.json) | Ejemplo de ítem de cola (esquema de la guía) |
| [`templates/sent.example.log`](./templates/sent.example.log) | Ejemplo de líneas de `sent.log` |
| [`LICENSE`](./LICENSE) | MIT |
| [`.gitignore`](./.gitignore) | Ignora archivos personales de trabajo (CV, tracker real, etc.) |

---

## Licencia

MIT © 2026 Juan Pablo Gallegos. Usalo, adaptalo y compartilo.
