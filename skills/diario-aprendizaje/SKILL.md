---
name: diario-aprendizaje
description: Añade una entrada estructurada y fechada al Google Doc "Diario de Aprendizaje" con lo aprendido hoy.
---



# Skill: Diario de Aprendizaje

## Descripción
Toma lo que Miguelangel cuenta que aprendió hoy (texto en bruto) y lo convierte en una entrada limpia, fechada y estructurada que se añade al final de su Google Doc "Diario de Aprendizaje". Responde como Al Capone 🎩: directo, con chispa, en español y sin relleno.

## Cuándo Usar
Cuando el usuario diga que quiere registrar, apuntar o guardar lo que aprendió hoy, o pida añadir algo a su diario de aprendizaje.

## Prerrequisitos
- Conexión de Google Docs activa vía Composio.
- Google Doc llamado "Diario de Aprendizaje" en la raíz de Mi unidad (si no existe, se crea).

## Procedimiento
1. Recibir del usuario los aprendizajes del día en lenguaje natural (una frase o varios puntos).
2. Localizar el Google Doc "Diario de Aprendizaje" en la raíz de Mi unidad. Si no existe, crearlo con ese nombre.
3. Reformular los aprendizajes en puntos claros y concisos, sin copiar el texto crudo literal.
4. Etiquetar cada punto con su área cuando sea evidente (#AI-Engineering, #Linux, #Desarrollo-Web), usando el contexto de USER.md.
5. Añadir al final del documento una entrada nueva con este formato:
   ## FECHA DD / MM / AAAA
   - <aprendizaje 1> #etiqueta
   - <aprendizaje 2> #etiqueta
6. No borrar ni reescribir entradas anteriores; solo agregar.
7. Confirmar al usuario en una línea, en la voz de Al Capone, qué se añadió y a qué documento.

## Salida Esperada
El Google Doc "Diario de Aprendizaje" contiene una entrada nueva al final, fechada en DD/MM/AAAA, en español, con los aprendizajes en puntos claros y con etiqueta de área donde aplique. Las entradas anteriores permanecen intactas.

## Casos Especiales
- Si no se encuentra el Doc y hay duda sobre crear uno nuevo, parar y preguntar antes de actuar (regla de AGENTS.md).
- Si el usuario no aporta ningún aprendizaje, pedir al menos un punto antes de escribir.
- Nunca borrar contenido existente del documento.
