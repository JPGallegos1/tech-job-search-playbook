# Guía de búsqueda laboral en tecnología

Metodología reutilizable para organizar una búsqueda laboral en el sector tech con ayuda de un bot o asistente personal. Sirve para cualquier rol (desarrollo, diseño, datos, producto, QA, etc.), en cualquier país o zona horaria.

Esta guía no trae el perfil de nadie prearmado. Trae el sistema: cómo filtrar avisos, de dónde sacarlos, cómo llevar el seguimiento, cómo redactar, qué se puede automatizar y qué siempre queda en borrador para que lo apruebes.

---

## 1. Cómo usar esta guía (Onboarding para tu bot)

Tenés dos caminos. Los dos terminan en lo mismo: un `PLAN.md` con tus filtros, los archivos de seguimiento vacíos y las rutinas creadas **en pausa**, hasta que vos confirmes que pueden arrancar.

### Opción A — Completar el bloque a mano

1. Copiá esta guía a tu espacio de trabajo.
2. Completá la [sección 2](#2-bloque-de-perfil-y-filtros-plantilla-editable) con tus datos, CVs y filtros.
3. Pedile a tu bot que, a partir de este archivo ya completado, genere tu `PLAN.md`, `tracker.csv`, `queue.json` y `sent.log`, y que deje creadas las rutinas de la [sección 6](#6-las-5-rutinas-listas-para-configurar--1-opcional) **pausadas**.
4. Revisá el resultado y recién ahí autorizá activarlas, y si querés que los primeros envíos salgan solos o siempre como borrador.

### Opción B — Subirle este archivo a tu bot (recomendado)

Compartí este `.md` tal cual está (aunque el bloque de filtros esté vacío) y pedile que te configure el sistema. El bot debería entrevistarte pregunta por pregunta, no de un saque.

### Instrucciones para el bot (seguir al pie de la letra)

Si estás leyendo esta guía porque la persona te la compartió para armar su búsqueda laboral, hacé lo siguiente. No inventes datos. No actives envíos ni rutinas hasta que la persona lo confirme con sus propias palabras.

1. **Explicá el plan en una frase.** Vas a entrevistarla para armar su perfil y filtros, generar los archivos base y dejar las rutinas creadas en pausa.
2. **Entrevistá pregunta por pregunta** (una o dos por turno, en este orden, salteando lo que ya haya respondido):
   1. Nombre completo, ciudad o país, zona horaria y email desde el que se van a enviar las postulaciones.
   2. Links a incluir en emails o mensajes (LinkedIn, GitHub, portfolio, web) y links que **no** hay que mencionar (por ejemplo, un sitio todavía vacío).
   3. Roles y seniority que busca, y los que hay que descartar.
   4. Stack, disciplina o área (y stacks o rubros a excluir).
   5. Modalidad y ubicación: remoto (¿abierto a qué regiones?), híbrido (¿máximo de días de oficina por semana? ¿en qué ciudad?), presencial, y si contempla relocalización (¿solo si el aviso la incluye?).
   6. Idiomas y nivel real de cada uno (nativo, B1, B2, C1, etc.).
   7. Banda salarial objetivo y un piso por debajo del cual descartar avisos que ya publican sueldo. Aclará la [regla de pretensión](#245-banda-salarial-objetivo).
   8. CVs disponibles (ruta o archivo de cada uno) y cuándo adjuntar cada uno (especialidad, idioma, tipo de rol).
   9. Respuestas estándar: disponibilidad para empezar, modalidad de contratación que acepta (relación de dependencia, freelance, contrato), y cualquier hecho técnico o laboral que el bot **nunca** puede inventar ni exagerar.
   10. Empresas, consultoras o tipos de aviso que quiere excluir.
   11. Horario laboral y días hábiles para envíos (por defecto, lunes a viernes en el horario laboral de su zona).
   12. Permiso de envío: ¿los primeros mails de postulación pueden salir solos cuando el encaje es alto y hay email publicado, o preferís que **todo** salga como borrador? Dejá en claro que respuestas a recruiters y follow-ups van **siempre** como borrador.
   13. Si quiere sincronizar con Notion (base de Postulaciones + Aprendizajes).
   14. Si quiere la rutina opcional de vigilar 1 a 3 empresas objetivo (y cuáles).
3. **Generá los archivos base** en una carpeta acordada (por ejemplo `job-search/`):
   - `PLAN.md`: el perfil y las reglas ya personalizados, siguiendo el esquema de la [sección 4.1](#41-planmd).
   - `tracker.csv`: solo la fila de encabezados, con las columnas de la [sección 4.2](#42-trackercsv).
   - `queue.json`: un array vacío `[]`.
   - `sent.log`: archivo vacío, listo para ir agregando una línea por envío.
   - Si pidió Notion, un `notion.json` con la correspondencia de propiedades (sin inventar IDs: se completan al conectar y crear las bases).
4. **Creá las 5 rutinas de la sección 6 en pausa** (y la opcional, si la pidió). No las actives.
5. **Mostrá un resumen** del perfil, los filtros, los archivos creados y las rutinas en pausa. Pedí correcciones.
6. **Esperá confirmación explícita** antes de: activar cualquier rutina, conectar Gmail u otro correo, o habilitar el envío automático de primeras postulaciones. Si no hay permiso explícito de envío automático, todas las postulaciones salen como borrador.
7. **No empieces a buscar ni a escribirle a empresas** durante el onboarding, salvo que la persona te lo pida en ese momento.

La persona puede cambiar filtros más adelante. Cuando lo haga, actualizá el `PLAN.md` y aplicá los criterios nuevos de ahí en más (no reescribas el historial del tracker).

---

## 2. Bloque de perfil y filtros (plantilla editable)

Completá los campos entre corchetes. Lo que no aplique, borralo o dejalo en «no aplica». Este bloque es la base de tu `PLAN.md`.

### 2.1 Datos básicos

- **Nombre completo:** [NOMBRE]
- **Ubicación:** [CIUDAD / PAÍS]
- **Zona horaria:** [ZONA HORARIA, p. ej. America/Argentina/Buenos_Aires]
- **Email de envío:** [EMAIL DESDE EL QUE SALEN LAS POSTULACIONES]
- **Otros buzones a revisar** (opcional, si alguna postulación usa otra casilla): [EMAIL SECUNDARIO O NINGUNO]
- **Links a incluir** (solo los que quieras que aparezcan en emails o mensajes):
  - LinkedIn: [URL O «no incluir»]
  - GitHub / portfolio / web: [URL O «no incluir»]
- **Links a omitir siempre:** [p. ej. un sitio personal todavía vacío]
- **Años de experiencia y resumen profesional** (hechos reales, sin inflar): [RESUMEN]
- **Idiomas y nivel real:** [p. ej. español nativo, inglés B1–B2]

### 2.2 CVs y cuándo adjuntar cada uno

El bot **nunca modifica** los CVs. Solo elige cuál adjuntar, según estas reglas. Si un aviso no encaja con ninguna regla, pregunta antes de mandar.

| Archivo | Usarlo cuando el aviso sea… |
| --- | --- |
| [ruta/CV-especialidad-A.pdf] | [p. ej. frontend, React, mobile] |
| [ruta/CV-especialidad-B.pdf] | [p. ej. full-stack, backend, producto] |
| [ruta/CV-en-ingles.pdf] | [p. ej. avisos redactados en inglés] |

Si tenés una sola versión, dejá una sola fila. Si más adelante sumás un CV, agregalo acá y decí cuándo usarlo.

### 2.3 Respuestas estándar

Usar solo lo que esté confirmado acá. Si un formulario pregunta algo que no está, no inventar: dejar ese aviso para la persona.

- **Disponibilidad para empezar:** [p. ej. dentro de las 2 semanas de una oferta]
- **Modalidad de contratación que acepta:** [relación de dependencia / freelance / contrato / todas]
- **Pretensión neta o bruta, si un formulario la pide por separado:** [VALOR O «usar la banda del punto 2.5»]
- **Cómo llegaste al aviso** (si el formulario lo pregunta): responder con la verdad, según la fuente real del tracker (Get on Board, LinkedIn, email directo, etc.).
- **Hechos técnicos o laborales que el bot puede mencionar** (y nada más): [p. ej. tecnologías que sí usaste, y las que no hay que afirmar]
- **Otras respuestas fijas:** [lo que quieras dejar zanjado de antemano]

### 2.4 Criterios de encaje (puntaje 1–10)

Cada aviso se puntúa del 1 al 10. Un **buen encaje** (candidato a envío o a la lista manual del día) es **puntaje ≥ 7** y, para salida automática por email, además una **dirección real de postulación** publicada en el aviso o en la página de carreras de la empresa. Nunca adivinar ni construir un email. Nunca postular dos veces a la misma empresa + rol (chequear `tracker.csv` y los enviados del correo).

#### 2.4.1 Roles y seniority

- **Busca:** [p. ej. Frontend, Full-Stack, Product Engineer, Mid / Senior / Lead]
- **Descartar:** [p. ej. junior only, roles no relacionados con tu disciplina, stacks que no son los tuyos]

#### 2.4.2 Stack o área

- **Afinidad alta:** [tecnologías, herramientas o disciplina]
- **Aceptable:** [lo que sumaría puntos, sin ser excluyente]
- **Fuera de juego:** [p. ej. un stack que no querés o un rubro que no te interesa]

#### 2.4.3 Modalidad y ubicación

Marcá lo que aceptás (puede ser más de uno):

- [ ] Remoto abierto a [tu país / región / worldwide]
- [ ] Híbrido en [ciudad], con un tope de **[N] días** de oficina por semana (descartar si piden más)
- [ ] Presencial en [ciudad]
- [ ] Presencial o híbrido en el exterior **solo si el aviso incluye relocalización**
- [ ] Freelance / contrato

Descartar, salvo que indiques lo contrario: on-site en ciudades que no te sirven, híbrido por encima del tope de días, relocalización sin apoyo, y remoto «solo con work authorization» de un país donde no tenés permiso de trabajo.

#### 2.4.4 Nivel de idioma real (regla estricta)

El nivel declarado en el perfil es el real. **Si un aviso pide un nivel más alto, se descarta**, aunque el resto encaje. Ejemplos: si tu inglés es B1–B2, se descartan avisos que pidan fluent, native, C1, C2, «excellent/advanced English» o atención a clientes solo en ese idioma.

Si el aviso **no aclara el nivel**:

- Conservarlo solo cuando está redactado en tu idioma nativo, o cuando es de una empresa de tu país o región.
- Descartar avisos en otro idioma (por ejemplo, en inglés de empresas de EE.UU. o Europa) que no declaren el nivel: en la práctica suelen esperar un nivel alto.

Nunca afirmar un nivel de idioma que no esté en este bloque.

#### 2.4.5 Banda salarial objetivo

- **Banda objetivo:** [p. ej. USD o moneda local, monto mensual, negociable o no]
- **No descartar** un aviso solo porque no publica sueldo.
- **Sí descartar** si el rango publicado está claramente por debajo de [PISO, un margen razonable bajo tu banda].

**Regla clave de pretensión:** cuando el aviso ya publica un sueldo explícito, **no menciones tu banda** en ningún lado: ni en el email, ni en la carta, ni en el mensaje para pegar, ni en campos de pretensión del formulario (dejarlos en blanco o aceptar la cifra publicada). La banda solo se escribe cuando el aviso **no** publica sueldo.

#### 2.4.6 Frescura del aviso

Priorizar avisos publicados en los **últimos ~21 días**. Los más viejos se pueden anotar con puntaje más bajo o saltarse, salvo que la persona pida lo contrario o que la empresa siga activamente la búsqueda.

#### 2.4.7 Empresas o consultoras excluidas

Lista explícita (nombre de empresa, consultora o tipo de aviso). El bot no postula ni las sugiere:

- [EMPRESA O CONSULTORA 1]
- [EMPRESA O CONSULTORA 2]

#### 2.4.8 Cómo puntuar (orientación)

Usá el 1–10 con criterio consistente:

- **9–10:** rol, stack, modalidad e idioma calzan muy bien; el aviso está fresco; hay email o un canal claro.
- **7–8:** buen encaje con algún punto menor en contra (sueldo no publicado, un requisito secundario, frescura justa).
- **5–6:** dudoso; va a `low_fit` o se consulta, no se envía solo.
- **1–4:** no calza; `skipped` o `low_fit`, con el motivo en `notes`.

Un puntaje alto no alcanza si falta el email publicado: ese aviso va a la [lista manual del día (canal C)](#34-los-3-canales-de-postulación), no a la cola de envío automático.

---

## 3. Fuentes de búsqueda y canales

Preferí siempre avisos que publiquen un email de postulación. Todas las fuentes se recorren con los filtros de la sección 2 (incluido el de idioma).

### 3.1 Portales tech y remotos

Recorrer en cada búsqueda diaria:

- **Get on Board** (getonbrd.com) — especialmente útil en LATAM; si la persona tiene cuenta, las postulaciones por el propio portal se registran con estado `applied_gob`.
- **Hacker News**, hilo del mes: «Ask HN: Who is hiring?» (muchos posts traen email).
- **Y Combinator Work at a Startup**
- **We Work Remotely**
- **Remote OK**
- **Himalayas**
- **Working Nomads**

Se pueden sumar o sacar portales según el perfil (por ejemplo, tableros freelance como Workana o Malt, si la persona los quiere; si no, van a la lista de excluidas).

### 3.2 Redes

- **LinkedIn**
  - Búsqueda pública de avisos y posts de hiring (vía búsqueda web).
  - Lectura del feed o de avisos **con la sesión iniciada**, si hay acceso: **estrictamente solo lectura**. El bot no postula con Easy Apply, no manda DMs y no cambia nada de la cuenta. Esos avisos, si encajan, van a la lista manual (canal C) o a la cola de email si el post publica una dirección.
  - Ventana de frescura corta para el rastreo frecuente: avisos de las **últimas ~3 horas** (ver rutina de rastreo).
- **X (Twitter):** posts de hiring que combinen el rol o stack con un email publicado («hiring» + rol + «email» / «send CV» / «enviá tu CV»). Sin email publicado, van a la lista manual solo si el encaje es alto y hay un canal concreto (formulario o instrucción explícita).

### 3.3 Portales locales, directorios de startups y consultoras boutique

Esta lista es **editable según el país o la región**. Abajo hay un ejemplo para Argentina y LATAM; quien esté en otro lugar debería reemplazarla por sus equivalentes (portales locales, directorios de startups y agencias de recruiting tech).

**Ejemplo (Argentina / LATAM), para adaptar:**

- Portales generales: Computrabajo, Bumeran, Zonajobs (útiles sobre todo para híbrido o presencial en una ciudad concreta).
- Directorio y avisos de startups: [Startups Argentina](https://www.startupsargentina.com/) — sirve tanto para la búsqueda diaria como para armar outreach del canal B.
- Consultoras boutique de recruiting tech (revisar sus páginas de openings; la mayoría se postula por formulario, o sea canal C):
  - Werben HR — [werbenhr.com/openings](https://werbenhr.com/openings/)
  - 5411 Hub — [5411hub.com/jobs](https://5411hub.com/jobs/)
  - Dolphin Digital Recruiting — [dolphinrrhh.com/jobs](https://dolphinrrhh.com/jobs/)
  - HV Talent — [hvtalent.com/es/empleos](https://hvtalent.com/es/empleos/)
  - Carryer Tech — [sites.google.com/view/carryertech/our-openings](https://sites.google.com/view/carryertech/our-openings)
  - Puente Talent Partners — [puentetalent.com/jobs](https://puentetalent.com/jobs)

En otros países, reemplazá por el equivalente local (por ejemplo InfoJobs o Tecnoempleo en España, OCC Mundial en México, Computrabajo u otros portales del país, directorios de startups locales, y las consultoras boutique que la persona elija). Si una agencia no le interesa, va a la lista de excluidas.

### 3.4 Los 3 canales de postulación

Los tres se usan juntos. El bot no inventa un cuarto canal (por ejemplo, no escribe a un mail personal que no haya sido publicado para postulaciones).

#### Canal A — Postulación directa por email

Para avisos que publican una dirección de postulación (en el texto, en un post o en la página de carreras de la empresa). Esos entran a `queue.json` si el puntaje es ≥ 7, ordenados por prioridad (mejor encaje primero).

Variante de portal con cuenta propia (ejemplo: Get on Board): si la persona autorizó postular desde su cuenta en ese portal, el bot usa el flujo del aviso, adjunta el CV si el formulario lo permite y completa la carta con las mismas reglas de redacción. Si una pregunta del formulario pide un dato que no está en el perfil (otra moneda, documentos, una fecha de inicio distinta de la acordada), **no inventa**: saltea ese aviso y lo deja en la lista para la persona. Estas postulaciones se registran con `applied_gob` (o un estado equivalente si se suma otro portal).

#### Canal B — Contacto directo a startups que están contratando

Buscar startups y scale-ups (de la región de la persona, o remotas amigables con su ubicación) que estén **contratando de forma activa** el tipo de rol buscado: avisos recientes, página de carreras, novedad de ronda, o un post de hiring del equipo.

Solo se escribe a un email **publicado** de carreras o postulaciones, por ejemplo `jobs@`, `careers@`, `talento@`, `rrhh@`, o el que figure en la página de carreras. **Nunca adivinar direcciones** ni escribir a mails personales que no hayan sido publicados para ese fin.

Mismas reglas de redacción que el canal A, mencionando el rol abierto o que se vio que están armando el equipo. Fuente en el tracker: `startup_direct`. Tope orientativo: **hasta ~5 nuevas por día**, puntaje ≥ 7, **una por empresa**.

#### Canal C — Lista diaria manual

Todo buen encaje que solo se pueda postular por un formulario fuera de los portales autorizados, por Easy Apply, por un DM en LinkedIn o X, o por una propuesta en una plataforma freelance, va a la persona **cada mañana hábil** con:

- el link del aviso, y
- un **mensaje listo para pegar**, en el idioma del aviso, con las mismas reglas de redacción y de pretensión.

Estado: `manual`. Tope orientativo: **hasta ~8 por día**, las mejores primero. Cuando la persona diga que ya postuló, se hace una copia de seguridad del tracker y se marca esa fila como `applied_manual`, con la fecha de ese día, y se saca de la cola si estaba ahí.

---

## 4. Sistema de archivos (fuente de verdad)

El tracker es la fuente de verdad. Si un dato choca entre archivos, gana `tracker.csv`. Cada rutina lee el `PLAN.md` antes de actuar.

Carpeta sugerida: `job-search/`.

### 4.1 `PLAN.md`

Es la especificación operativa de **esta** persona. El bot lo lee en cada corrida y no lo contradice. Estructura recomendada (la misma de esta guía, ya personalizada):

```markdown
# Búsqueda laboral: especificación operativa

## Persona candidata
- Nombre, ubicación, zona horaria, email de envío, links a incluir y a omitir.
- Resumen profesional y niveles de idioma reales.

## CVs a adjuntar
- Una fila por CV, con la regla de cuándo usarlo.

## Criterios de encaje
- Roles, stack, modalidad, idioma, banda y piso salarial, frescura (~21 días),
  empresas excluidas, umbral de buen encaje (≥ 7) y la regla de no adivinar emails.

## Fuentes
- Portales, redes, portales locales y consultoras que aplican a esta persona.

## Archivos
- Rutas y esquemas de tracker.csv, queue.json y sent.log (como en esta guía).

## Reglas de redacción y de envío
- Idioma, largo, pretensión (y cuándo no mencionarla), permisos, horario,
  espaciado, etiqueta de correo, verificación del remitente y chequeo de rebote.

## Canales A, B y C
- Incluidas las variantes de portal con cuenta (p. ej. Get on Board) y los topes diarios.

## Respuestas estándar
- Disponibilidad, contratación, hechos que no se pueden inventar.

## Notion (opcional)
- Nombres de las bases y el mapa de estados; los IDs reales viven en notion.json.

## Pausas y holds
- Feriados, ventanas en las que no se busca ni se envía, y uso de not_before.
```

No hace falta copiar esta guía entera al `PLAN.md`: el plan es el perfil ya lleno más las reglas que esa persona confirmó.

### 4.2 `tracker.csv`

Una fila por aviso encontrado, sin excepciones (también los que se descartan). Columnas, en este orden:

```text
id,date_found,company,role,url,source,modality,location,relocation,startup,salary_info,contact_email,fit_score,cv,language,status,date_sent,gmail_thread_id,notes
```

| Columna | Qué va |
| --- | --- |
| `id` | Identificador estable y único (p. ej. `li-post-…`, `gob-empresa-rol`, `sd-empresa-rol`). |
| `date_found` | Fecha en que se encontró, `YYYY-MM-DD`. |
| `company` | Empresa (o recruiter + cliente, si la empresa no está revelada). |
| `role` | Título del rol, como en el aviso. |
| `url` | Link al aviso o al post. |
| `source` | Fuente: `Get on Board`, `LinkedIn post`, `Hacker News`, `startup_direct`, etc. |
| `modality` | `remote`, `hybrid`, `on-site`, `freelance`, etc. |
| `location` | Región o ciudad que declara el aviso. |
| `relocation` | `yes` / `no` (si el aviso incluye relocalización). |
| `startup` | Si es startup/scale-up, u otra nota corta de tipo de empresa. |
| `salary_info` | Rango publicado, o `not stated` / `no publicado`. |
| `contact_email` | Email publicado, o vacío si no hay. |
| `fit_score` | Entero 1–10. |
| `cv` | Clave del CV elegido (`fullstack`, `frontend`, `en`, etc.). |
| `language` | Idioma del aviso (`es`, `en`, …). |
| `status` | Uno de los estados de la tabla de abajo. |
| `date_sent` | Fecha de envío o de postulación, `YYYY-MM-DD`, o vacío. |
| `gmail_thread_id` | ID del hilo en el correo, si aplica. |
| `notes` | Motivo, frescura, follow-up, rebotes; se agregan con fecha, no se pisan. |

**Estados posibles:**

| Estado | Cuándo usarlo |
| --- | --- |
| `queued` | Buen encaje con email publicado, esperando envío. |
| `sent` | Primer mail de postulación enviado. |
| `replied` | Hubo respuesta (de la empresa o del recruiter). |
| `no_response` | Enviado y, tras el seguimiento, no hubo respuesta. |
| `rejected` | Rechazo explícito. |
| `interview` | Avanzó a entrevista o equivalente. |
| `no_email` | Buen encaje pero solo se postula por formulario (sin email). |
| `low_fit` | Encaje insuficiente; queda registrado para no volver a evaluarlo como nuevo. |
| `skipped` | Descartado por un filtro (idioma, modalidad, frescura, empresa excluida, etc.). |
| `manual` | Enviado a la persona para que postule (canal C). |
| `applied_manual` | La persona postuló por su cuenta; `date_sent` es ese día. |
| `applied_gob` | Postulado en Get on Board (o el portal equivalente autorizado). |
| `send_failed` | El envío falló o rebotó. |
| `discarded_by_user` | La persona descartó el aviso, un borrador o un widget. **No se reenvía nunca.** |

Antes de cambiar un estado a mano (sobre todo a `applied_manual`) o de editar el tracker de forma no trivial, hacer una copia de seguridad (por ejemplo `tracker.csv.bak-YYYYMMDD-motivo`).

Fila de ejemplo (datos ficticios):

```text
sd-acme-full-stack-engineer,2026-11-20,Acme,Full-Stack Engineer,https://ejemplo.com/jobs/full-stack,startup_direct,remote,LATAM,no,yes,no publicado,jobs@ejemplo.com,8,fullstack,es,queued,,,
```

### 4.3 `queue.json`

Array de postulaciones listas para enviar, en orden de prioridad (mejor encaje primero). El envío toma **como máximo un ítem por corrida**, respetando horario, espaciado y `not_before`.

Campos de cada ítem:

```json
[
  {
    "id": "sd-acme-full-stack-engineer",
    "to": "jobs@ejemplo.com",
    "subject": "Full-Stack Engineer - [NOMBRE COMPLETO]",
    "body": "Texto plano del email, 120–200 palabras, según las reglas de redacción.\n",
    "cv": "job-search/cvs/CV-FullStack.pdf",
    "company": "Acme",
    "role": "Full-Stack Engineer",
    "source": "startup_direct",
    "not_before": "2026-11-24T09:00:00-03:00",
    "resend": false
  }
]
```

- `id`, `to`, `subject`, `body`, `cv`, `company`, `role` son obligatorios.
- `source` es recomendable.
- `not_before` (opcional, datetime ISO con offset de la zona horaria de la persona): **no enviar antes de esa hora**; saltear el ítem, dejarlo en la cola y seguir con el siguiente que sí se pueda enviar. Las reglas normales de día hábil, horario y espaciado siguen valiendo después de esa marca.
- `resend: true` (opcional): reenvío aprobado de un mail que rebotó. La línea anterior en `sent.log` y el hilo del rebote **no** cuentan como postulación previa.

Al enviar con éxito: sacar el ítem de la cola, actualizar el tracker (`status=sent`, `date_sent`, `gmail_thread_id`) y agregar una línea en `sent.log`.

### 4.4 `sent.log`

Una línea por evento, campos separados por tabulación. Hay dos tipos de línea:

**Envío:**

```text
<timestamp ISO con offset>	<id>	<company>	<role>	<to>	thread=<gmail_thread_id>	from=<email remitente>
```

Ejemplo ficticio:

```text
2026-11-20T10:15:00-03:00	sd-acme-full-stack-engineer	Acme	Full-Stack Engineer	jobs@ejemplo.com	thread=abc123	from=tu@email.com
```

**Notas operativas** (pausas, reanudaciones, rebotes). Empiezan con `NOTE` en la segunda columna:

```text
2026-11-20T10:16:30-03:00	NOTE	sd-acme-full-stack-engineer bounced (address not found; remitente OK); se marca send_failed y se continúa
```

Al calcular la brecha de ≥ 12 minutos, **ignorar las líneas `NOTE`**. Solo cuentan los envíos reales.

### 4.5 Sincronización opcional con Notion

Si la persona lo pide, el workspace de Notion refleja el tracker, no al revés. Lo mínimo:

1. Una base **Postulaciones**, con propiedades como: Empresa, Rol, Estado, Canal, Fecha de postulación, Link, Contacto, Fit, CV, Modalidad, Motivo / aprendizaje, Notas.
2. Una base **Aprendizajes**, con: Aprendizaje, Tipo (`Funcionó` / `No funcionó` / `A probar`), Postulación relacionada, Fecha, Detalle.

Mapa sugerido de estados del tracker → Estado en Notion:

| Tracker | Notion |
| --- | --- |
| `queued` | En cola |
| `sent` | Enviada |
| `applied_gob` | Postulada en Get on Board (o el nombre del portal) |
| `applied_manual` | Enviada |
| `replied` | Respondió |
| `interview` | Entrevista |
| `rejected` | Rechazada |
| `send_failed` | Falló el envío |

No hace falta subir a Notion los avisos en `low_fit`, `skipped` o `no_email` (ni los `manual` que todavía no se postularon). Guardá IDs de páginas y el mapa tracker → página en un `notion.json`, para no duplicar filas.

**Aprendizajes:** solo cuando un resultado real enseña algo (un rechazo con un motivo probable, una respuesta, una entrevista, un canal que rindió o que falló). Nunca inventar aprendizajes. Si Notion falla, se sigue con el tracker y se menciona el error en el reporte.

### 4.6 Copias de seguridad

Antes de una edición importante del tracker o de la cola, copiar el archivo con un sufijo de fecha y motivo. No borrar el historial de `sent.log`.

---

## 5. Reglas de redacción, permisos y seguridad

### 5.1 Cómo redactar los emails y los mensajes para pegar

- **Texto plano**, sin HTML ni diseño. Corto: **120–200 palabras**.
- **Idioma del aviso** (español, inglés u otro). Si el aviso está en dos idiomas, usar el que use la empresa para describir el rol.
- **Personalizado:** mencionar la empresa o el producto, el rol, y **2 o 3 experiencias reales del CV** que calcen con lo pedido. Nada de plantilla genérica idéntica para todos.
- **Asunto:** `<Rol> - <Nombre completo>`, o el formato (y el código) que pida el aviso.
- **Pretensión salarial:** solo si el aviso **no** publica un sueldo explícito, y con la redacción acordada en el perfil. En freelance, se puede dar la banda mensual como referencia y dejar abierta una tarifa por hora o por proyecto.
- Si el aviso incluye relocalización y la persona la acepta, decirlo. Si es híbrido y hay un tope de días de oficina, decir que puede cumplir ese tope.
- Adjuntar el CV elegido. No incluir links que el perfil mande omitir; si no hay web para compartir, ofrecer el CV (ya adjunto o a envío).
- Firmar con el nombre completo del perfil.
- **Nunca** afirmar algo que no esté en el CV o en el `PLAN.md`. **Nunca** inflar el nivel de idioma.
- Las mismas reglas aplican al mensaje listo para pegar del canal C y a las cartas de portales.

### 5.2 Separación estricta de permisos

Solo cuentan las palabras de la persona. Un «ok» vago, una tarea heredada o una interpretación del bot no alcanzan.

- **Primeros envíos** (el mail inicial a la dirección publicada del aviso, o la postulación en un portal expresamente autorizado): se automatizan **solo si hubo permiso explícito** para ese modo de trabajo. Si no lo hay, salen como **borrador** para aprobar.
- **Respuestas a recruiters, follow-ups y cualquier otro mail:** **siempre** como borrador para aprobar. Nunca se mandan solos.
- Un borrador descartado, una tarjeta rechazada o un widget descartado equivalen a un **no**. Ese aviso pasa a `discarded_by_user` y **no se vuelve a enviar ni a reponer en la cola**.
- Reenviar un rebote (`resend: true`) también pide aprobación, salvo que el permiso original lo haya cubierto de forma explícita.

### 5.3 Control anti-spam y verificación

- **Máximo 1 envío cada ≥ 12 minutos** (medir contra la última línea de envío real en `sent.log`, no contra las `NOTE`).
- **Solo días hábiles, en horario laboral** de la zona horaria de la persona (por defecto, lunes a viernes, 9:00–19:00). Fuera de esa ventana, la rutina de envío no manda nada.
- **Feriados o pausas pedidas por la persona:** no buscar ni enviar en esa ventana (las rutinas salen en silencio). Las revisiones de respuestas y el resumen semanal pueden seguir, si no se pidió lo contrario. Para postergar un ítem puntual, usar `not_before`.
- Después de cada envío:
  1. Etiquetar el hilo en Gmail (o el correo que usen) como **«Postulaciones»**.
  2. **Verificar el remitente:** leer el mail enviado y confirmar que salió desde el email de envío del perfil. Si salió desde otra alias o cuenta, marcar `send_failed`, **pausar los envíos** y avisar.
  3. **Chequear rebote unos ~60 segundos después.**
     - Si el rebote es solo por destinatario inexistente («Address not found», «user unknown») y el remitente es el correcto: marcar esa fila `send_failed` y **seguir** con la cola. No pausar por un destinatario inválido aislado.
     - Si falla el remitente, la autenticación, o hay rebotes repetidos: marcar `send_failed`, **pausar los envíos** y reportar.
- Actualizar `tracker.csv`, sacar el ítem de `queue.json` y agregar la línea en `sent.log`.

### 5.4 Otras reglas que no se negocian

- No adivinar ni construir emails. No escribir a casillas personales que no hayan sido publicadas para postulaciones.
- No postular dos veces a la misma empresa + rol.
- No modificar los CVs.
- No inventar disponibilidad, sueldo, stack, seniority ni nivel de idioma.
- No molestar con mensajes de «no hubo novedades» cuando una rutina no encontró nada accionable (el resumen semanal sí puede decir que la semana estuvo tranquila).
- Si la persona dice que postuló, no reenviar: backup del tracker y estado `applied_manual` con la fecha de ese día.

---

## 6. Las 5 rutinas listas para configurar (+ 1 opcional)

Crearlas **en pausa** durante el onboarding. Activarlas solo cuando la persona lo confirme. Cada corrida lee el `PLAN.md` primero. Ajustá horas a la zona horaria del perfil.

### 6.1 Búsqueda laboral diaria

- **Cuándo:** lunes a viernes, a la mañana (por ejemplo 8:30 o 9:00).
- **Qué hace:** recorre las fuentes de la sección 3, puntúa cada aviso nuevo, lo escribe en `tracker.csv` (también los que descarta, para no repetir trabajo), carga en `queue.json` los de puntaje ≥ 7 con email publicado, arma la lista manual del canal C (hasta ~8, con link y mensaje listo para pegar) y suma hasta ~5 contactos nuevos del canal B, si hay.
- **Qué no hace:** no envía mails (eso es la rutina de envío). No vuelve a postular a un `id` o a una empresa + rol ya registrados.
- **Qué reporta:** un resumen corto de lo nuevo que sí encaja, la cola, la lista manual y cualquier duda. Si no hay nada accionable, no hace falta escribir: el silencio está bien.

### 6.2 Rastreo de LinkedIn cada 2 horas

- **Cuándo:** cada 2 horas, en una ventana diurna; se puede dejar lunes a viernes o también fin de semana, según prefiera la persona.
- **Qué hace:** busca avisos o posts nuevos de las **últimas ~3 horas** (búsqueda pública y, si hay sesión, lectura del feed en solo lectura). Aplica los mismos filtros. Los que encajan y traen email van a la cola; los que encajan sin email van a un listado corto para la persona, o quedan en `manual` / `no_email`.
- **Qué no hace:** no postula, no manda DMs, no usa Easy Apply, no escribe en LinkedIn.
- **Qué reporta:** solo si hay algo nuevo que valga la pena. Si no hay novedades, **no manda mensaje**.

### 6.3 Envío de postulaciones

- **Cuándo:** cada 15 minutos, lunes a viernes, en el horario laboral del perfil.
- **Qué hace:** toma como máximo **1 ítem** de `queue.json` (el de más prioridad que ya pueda salir: sin `not_before` pendiente, y con ≥ 12 minutos desde el último envío real). Envía desde el email del perfil si hay permiso explícito; si no, deja el borrador y se detiene en ese ítem hasta que lo aprueben. Después del envío: etiqueta «Postulaciones», verifica remitente, espera ~1 minuto y chequea rebote, actualiza tracker, cola y `sent.log`.
- **Qué no hace:** no manda respuestas ni follow-ups. No manda fuera de horario ni en feriados cargados como pausa. No manda un segundo mail en la misma corrida.
- **Qué reporta:** cada envío (o cada fallo), de forma breve. Si la cola está vacía, no hace falta escribir.

### 6.4 Respuestas y seguimiento

- **Cuándo:** cada 3 horas, lunes a viernes, en horario diurno.
- **Qué hace:**
  - Revisa la casilla de envío (y cualquier buzón extra del perfil) buscando respuestas a postulaciones.
  - Actualiza el tracker (`replied`, `rejected`, `interview`, etc.) y Notion, si está conectado.
  - Redacta **borradores** de respuesta, nunca envíos directos.
  - Propone follow-ups en borrador para postulaciones enviadas hace **7 días o más** sin respuesta (y que no hayan sido descartadas).
- **Qué no hace:** no manda esos mails. No insiste en un aviso `discarded_by_user`. No inventa un motivo de rechazo si la empresa no lo dijo.
- **Qué reporta:** respuestas nuevas, borradores listos para revisar y follow-ups propuestos. Si no hay nada, no hace falta escribir.

### 6.5 Resumen semanal de búsqueda

- **Cuándo:** viernes a la tarde (por ejemplo 17:00 o 18:00).
- **Qué hace:** arma un balance de la semana: cuántos avisos se vieron, cuántos se enviaron o se postularon a mano, respuestas, rechazos, entrevistas, rebotes, y **qué canales rindieron de verdad**. Propone un foco concreto para la semana siguiente (una fuente, un tipo de rol, un ajuste de filtro), apoyado en resultados reales.
- **Qué no hace:** no inventa aprendizajes ni recomienda cambios de filtro sin evidencia. No relista los 50 avisos descartados.
- **Qué reporta:** el resumen, siempre, aunque la semana haya estado corta: en ese caso, lo dice y apunta a qué conviene mirar la semana siguiente.

### 6.6 Opcional: Vigilar empresas objetivo

- **Cuándo:** 1 vez al día, en días hábiles (o la cadencia que pida la persona).
- **Para qué:** seguir las páginas de carreras de **1 a 3 empresas** concretas que le interesen, aunque no tengan un aviso nuevo en los portales generales.
- **Qué hace:** revisa esas páginas (y, si aplica, sus posts de hiring) y, si aparece un rol que encaja, lo carga al tracker y lo manda a la cola o a la lista manual, con las mismas reglas.
- **Qué no hace:** no escribe a un email adivinado. Si la página no publica canal de postulación, lo deja en la lista manual con el link.
- **Qué reporta:** solo cuando aparece algo nuevo que encaje, o si una página dejó de estar disponible.

---

## Antes de activar

Checklist corto para la persona, una vez que el bot terminó el onboarding:

- [ ] El `PLAN.md` refleja bien roles, modalidad, idioma, banda y exclusiones.
- [ ] Los CVs correctos están en la carpeta acordada y las reglas de adjunto cierran.
- [ ] `tracker.csv`, `queue.json` y `sent.log` existen (los dos últimos, vacíos al inicio).
- [ ] Las rutinas están creadas y **siguen en pausa** hasta tu OK.
- [ ] Quedó por escrito si los primeros envíos salen solos o siempre como borrador.
- [ ] El correo de envío está conectado (y Notion, si lo pediste) antes del primer envío real.

Con eso, el sistema está listo. Los filtros son tuyos; la metodología, las fuentes, los archivos y las rutinas son lo que esta guía busca que puedas copiar y adaptar.
