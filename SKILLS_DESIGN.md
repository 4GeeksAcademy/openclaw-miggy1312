# SKILLS_DESIGN.md

Diseño de las skills personalizadas para el agente **Al Capone** 🎩.

---

## Skill 1 — Diario de Aprendizaje Diario

### 1. ¿Qué hace esta skill?
Toma lo que aprendí hoy (unos pocos puntos en bruto) y añade una entrada estructurada y con fecha a mi Google Doc "Diario de Aprendizaje", como registro personal de conocimiento.

### 2. ¿Qué input necesita el agente?
- **Lo que le doy:** una lista informal de lo aprendido hoy, en lenguaje natural (ej. "hoy vi cómo funcionan las skills de OpenClaw, repasé permisos de archivos en Linux con chmod, y entendí la diferencia entre output en español y nombres de variables en inglés").
- **Formato:** texto libre, sin estructura previa. Puede ser una frase o varios puntos.
- **Lo que ya sabe por los 5 archivos de configuración:**
  - `USER.md`: mi nombre (Miguelangel), que estudio AI Engineering en 4Geeks y empiezo FP de Desarrollo Web en septiembre → puede etiquetar las entradas por área.
  - `TOOLS.md`: Google Docs es el destino por defecto; formato de nombre `[Tipo] - [Tema] - [Fecha]`; fechas en DD/MM/AAAA; contenido en español.
  - `SOUL.md`: tono directo y con chispa; nada de relleno.

### 3. ¿Cómo es un buen output?
- **Formato:** una entrada nueva anexada al final del Google Doc, con:
  - Encabezado con la fecha (DD/MM/AAAA).
  - Los aprendizajes reformulados como puntos claros y concisos (no copia literal de mi texto crudo).
  - Opcional: una etiqueta de área (ej. `#AI-Engineering`, `#Linux`, `#Desarrollo-Web`).
- **Destino:** Google Doc "Diario de Aprendizaje" en la raíz de Mi unidad. Si no existe, lo crea.
- **Cómo sé que funcionó:** abro el Doc y veo la entrada de hoy bien formateada, en español, con la fecha correcta y mis puntos ordenados. El estilo se nota "de Al Capone": directo, sin paja.

---

## Skill 2 — Briefing Rápido por Telegram

### 1. ¿Qué hace esta skill?
Cuando la activo, me manda a Telegram un briefing breve y directo con el estado de mi día: qué toca, qué quedó pendiente y un recordatorio de foco — sin que yo tenga que abrir varias apps.

### 2. ¿Qué input necesita el agente?
- **Lo que le doy:** el disparador (ej. "dame mi briefing") y, opcionalmente, un par de puntos de contexto del día (compromisos, tarea principal).
- **Formato:** un mensaje corto o incluso solo el comando de activación.
- **Lo que ya sabe por los 5 archivos de configuración:**
  - `USER.md`: mis proyectos actuales (Milestone 4 de 4Geeks, web de mi hermana) → puede recordármelos como foco.
  - `TOOLS.md`: Telegram es el canal de avisos/briefings; zona horaria Europe/Madrid; contenido en español.
  - `SOUL.md`: tono directo, con carácter, mensajes cortos y al grano.

### 3. ¿Cómo es un buen output?
- **Formato:** un único mensaje de Telegram, corto (cabe en pantalla sin scroll), con:
  - Saludo en personaje ("Salve! 🎩").
  - 2–4 líneas: foco del día / pendientes / un empujón final.
  - Nada de párrafos largos ni relleno.
- **Destino:** mensaje de Telegram a mí mismo.
- **Cómo sé que funcionó:** recibo el mensaje en Telegram al activar la skill, en español, breve, y con la voz de Al Capone reconocible. La información refleja mis proyectos reales de `USER.md`.

---

## Nota de diseño
Ambas skills se apoyan **solo en herramientas ya conectadas vía Composio** (Google Docs y Telegram). No requieren ninguna API, OAuth ni servicio externo nuevo. La Skill 1 produce output verificable en Google Docs y la Skill 2 en Telegram — cumpliendo el requisito de al menos una salida verificada en un servicio conectado.
