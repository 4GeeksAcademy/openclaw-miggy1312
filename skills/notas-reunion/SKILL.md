---
name: notas-reunion
description: Ordena y estructura apuntes o notas en bruto (de reuniones, clases o sesiones) en Decisiones, Tareas y Preguntas abiertas, y las guarda en un Google Doc.
---

# Skill: Notas de Reunión

## Descripción
Toma los apuntes desordenados que Miguelangel pega de una reunión o clase y los estructura en tres bloques —Decisiones, Tareas y Preguntas abiertas— guardándolos en un Google Doc nuevo. Responde como Al Capone 🎩: directo, con chispa, en español y sin relleno.

## Cuándo Usar
Cuando el usuario pegue apuntes de una reunión o clase y pida ordenarlos, resumirlos o guardarlos como notas.

## Prerrequisitos
- Conexión de Google Docs activa vía Composio.
- Apuntes en bruto aportados por el usuario.

## Procedimiento
1. Recibir los apuntes en bruto y, si se da, el tema/título de la reunión.
2. Analizar el texto y clasificar su contenido en tres categorías:
   - **Decisiones:** lo que se acordó o se dio por cerrado.
   - **Tareas:** acciones a realizar; incluir responsable si se menciona.
   - **Preguntas abiertas:** dudas o temas sin resolver.
3. Crear un Google Doc nuevo en la raíz de Mi unidad, nombrado: Notas - <Tema> - <DD/MM/AAAA>.
4. Escribir en el Doc un encabezado con el tema y la fecha, y las tres secciones con sus puntos.
5. Confirmar al usuario en una línea, en la voz de Al Capone, qué se creó y con qué nombre.

## Salida Esperada
Existe un Google Doc nuevo llamado "Notas - <Tema> - <Fecha>" en la raíz de Mi unidad, en español, con tres secciones claras (Decisiones, Tareas, Preguntas abiertas) que reflejan los apuntes aportados.

## Casos Especiales
- Si los apuntes no permiten llenar alguna sección, dejarla con "Ninguna" en vez de inventar contenido.
- Si el usuario no da tema, usar uno genérico con la fecha (ej. "Notas - Reunión - DD/MM/AAAA").
- No inventar decisiones ni tareas que no estén en los apuntes.
