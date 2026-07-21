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

## Skill 2 — Notas de Reunión

### 1. ¿Qué hace esta skill?
Toma apuntes en bruto de una reunión o clase y los estructura en tres bloques —Decisiones, Tareas y Preguntas abiertas— guardando el resultado en un Google Doc.

### 2. ¿Qué input necesita el agente?
- **Lo que le doy:** apuntes desordenados en lenguaje natural (lo que anoté durante la reunión/clase), y opcionalmente un título o tema.
- **Formato:** texto libre, sin estructura previa.
- **Lo que ya sabe por los 5 archivos de configuración:**
  - `USER.md`: mis proyectos actuales → puede etiquetar de qué contexto es la reunión.
  - `TOOLS.md`: Google Docs es el destino por defecto; nombre `[Tipo] - [Tema] - [Fecha]`; fechas DD/MM/AAAA; contenido en español.
  - `SOUL.md`: tono directo y sin relleno.

### 3. ¿Cómo es un buen output?
- **Formato:** un Google Doc con tres secciones claras —Decisiones, Tareas (con responsable si se menciona), Preguntas abiertas—, encabezado con tema y fecha (DD/MM/AAAA).
- **Destino:** Google Doc nuevo en la raíz de Mi unidad, nombrado `Notas - [Tema] - [Fecha]`.
- **Cómo sé que funcionó:** abro el Doc y veo mis apuntes convertidos en decisiones, tareas y preguntas bien separadas, en español, con la voz de Al Capone.

## Nota de diseño
Ambas skills se apoyan **solo en Google Docs**, una herramienta ya conectada vía Composio. No requieren ninguna API, OAuth ni servicio externo nuevo. La Skill 1 (Diario de Aprendizaje) y la Skill 2 (Notas de Reunión) producen output verificable en Google Docs, cumpliendo el requisito de al menos una salida verificada en un servicio conectado.
