# Búsqueda laboral: especificación operativa

> Copiá este archivo a `PLAN.md` (por ejemplo en `job-search/`) y reemplazá todos los placeholders `[…]`.
> No subas tu `PLAN.md` real al remoto: está en `.gitignore`.

## Persona candidata

- **Nombre completo:** [NOMBRE COMPLETO]
- **Ubicación:** [CIUDAD / PAÍS]
- **Zona horaria:** [p. ej. America/Argentina/Buenos_Aires]
- **Email de envío:** [EMAIL DESDE EL QUE SALEN LAS POSTULACIONES]
- **Otros buzones a revisar** (opcional): [EMAIL SECUNDARIO O «ninguno»]
- **Links a incluir:**
  - LinkedIn: [URL O «no incluir»]
  - GitHub / portfolio / web: [URL O «no incluir»]
- **Links a omitir siempre:** [p. ej. un sitio personal todavía vacío]
- **Años de experiencia y resumen profesional** (hechos reales, sin inflar): [RESUMEN]
- **Idiomas y nivel real:** [p. ej. español nativo, inglés B1–B2]

## CVs a adjuntar

El bot **nunca modifica** los CVs. Solo elige cuál adjuntar según estas reglas.

| Archivo | Usarlo cuando el aviso sea… |
| --- | --- |
| [ruta/CV-especialidad-A.pdf] | [p. ej. frontend, React, mobile] |
| [ruta/CV-especialidad-B.pdf] | [p. ej. full-stack, backend, producto] |
| [ruta/CV-en-ingles.pdf] | [p. ej. avisos redactados en inglés] |

## Criterios de encaje

- **Umbral de buen encaje:** puntaje ≥ 7.
- **Email:** nunca adivinar ni construir direcciones; solo usar emails publicados para postulaciones.
- **Roles y seniority — busca:** [p. ej. Frontend, Full-Stack, Mid / Senior]
- **Roles y seniority — descartar:** [p. ej. junior only, stacks que no son los tuyos]
- **Stack — afinidad alta:** [tecnologías / disciplina]
- **Stack — aceptable:** [lo que sumaría puntos]
- **Stack — fuera de juego:** [stacks o rubros a excluir]
- **Modalidad y ubicación:**
  - [ ] Remoto abierto a [país / región / worldwide]
  - [ ] Híbrido en [ciudad], tope de **[N] días** de oficina por semana
  - [ ] Presencial en [ciudad]
  - [ ] Presencial o híbrido en el exterior **solo si el aviso incluye relocalización**
  - [ ] Freelance / contrato
- **Idioma:** si el aviso pide un nivel más alto que el declarado, se descarta.
- **Banda salarial objetivo:** [moneda, monto, negociable o no]
- **Piso para descartar** (si el aviso publica sueldo): [PISO]
- **Regla de pretensión:** si el aviso ya publica sueldo, **no** mencionar la banda; solo escribirla cuando el aviso no publica sueldo.
- **Frescura:** priorizar avisos de los últimos ~21 días.
- **Empresas o consultoras excluidas:**
  - [EMPRESA O CONSULTORA 1]
  - [EMPRESA O CONSULTORA 2]

## Fuentes

- Portales tech / remotos: [Get on Board, HN Who is hiring, WWR, Remote OK, Himalayas, Working Nomads, …]
- Redes: LinkedIn (solo lectura), X (posts con email publicado).
- Portales locales / directorios / consultoras boutique: [adaptar a tu país o región]
- Variantes de portal con cuenta autorizada: [p. ej. Get on Board — sí/no]

## Archivos

Carpeta de trabajo sugerida: `job-search/`.

| Archivo | Rol |
| --- | --- |
| `tracker.csv` | Fuente de verdad. Columnas: `id,date_found,company,role,url,source,modality,location,relocation,startup,salary_info,contact_email,fit_score,cv,language,status,date_sent,gmail_thread_id,notes` |
| `queue.json` | Array de postulaciones listas; máximo 1 envío por corrida. |
| `sent.log` | Una línea por envío (y líneas `NOTE` operativas); brecha ≥ 12 min solo contra envíos reales. |
| `notion.json` (opcional) | Mapa de IDs tracker → página Notion. |

## Reglas de redacción y de envío

- Texto plano, 120–200 palabras, idioma del aviso, personalizado (empresa + rol + 2–3 experiencias reales).
- Asunto: `<Rol> - <Nombre completo>` (o el formato que pida el aviso).
- Adjuntar el CV elegido; no incluir links marcados para omitir.
- Firmar con el nombre completo del perfil.
- Nunca afirmar lo que no esté en el CV o en este plan; nunca inflar el nivel de idioma.
- **Permiso de primeros envíos:** [automático si encaje alto + email publicado / siempre borrador].
- Respuestas a recruiters y follow-ups: **siempre borrador**.
- Horario laboral: [p. ej. lun–vie 9:00–19:00] en la zona horaria del perfil.
- Espaciado: máximo 1 envío cada ≥ 12 minutos.
- Etiqueta de correo: «Postulaciones»; verificar remitente tras cada envío; chequear rebote ~60 s después.

## Canales A, B y C

- **A — Email / portal autorizado:** cola `queue.json` si puntaje ≥ 7 y hay email (o flujo de portal autorizado → `applied_gob`).
- **B — Startups directas:** solo email publicado de carreras; hasta ~5 nuevas/día; una por empresa; fuente `startup_direct`.
- **C — Lista manual:** formularios, Easy Apply, DMs; hasta ~8/día con link + mensaje listo para pegar; estado `manual` → `applied_manual` cuando la persona confirme.

## Respuestas estándar

- **Disponibilidad para empezar:** [p. ej. dentro de las 2 semanas de una oferta]
- **Modalidad de contratación:** [relación de dependencia / freelance / contrato / todas]
- **Pretensión si el formulario la pide por separado:** [VALOR O «usar la banda del perfil»]
- **Hechos técnicos o laborales que se pueden mencionar** (y nada más): [lista]
- **Otras respuestas fijas:** [lo que quieras dejar zanjado]

## Notion (opcional)

- Bases: **Postulaciones** y **Aprendizajes**.
- Mapa de estados tracker → Notion según la guía.
- IDs reales: solo en `notion.json` (sin inventar IDs).
- ¿Activar sincronización?: [sí / no]

## Pausas y holds

- Feriados o ventanas sin búsqueda ni envío: [fechas o «ninguna por ahora»]
- Uso de `not_before` en ítems de cola para postergar un envío puntual.
- Empresas objetivo a vigilar (rutina opcional 6.6): [1–3 nombres o «no»]
