---
description: Crea un nuevo nodo en el roadmap. Genera el archivo .md en /categorias y añade el nodo y la arista en roadmap.canvas.
---

El usuario quiere añadir un nuevo nodo al roadmap. Sigue estos pasos en orden:

1. **Pide los datos necesarios si no los ha proporcionado:**
   - Nombre del nodo (título legible)
   - Nodo padre (de cuál desciende en el grafo)
   - Justificación breve de su posición (por qué va aquí, qué aporta)
   - Recursos iniciales (opcional; si no los tiene, usa el agente `generador-contenido`)

2. **Crea el archivo en `categorias/`:**
   - Nombre de archivo: kebab-case del título, sin tildes ni caracteres especiales
   - Formato:
     ```markdown
     # Título del nodo #Tag
     Justificación breve.
     
     [Recurso](url) #Tipo
     ```

3. **Actualiza `roadmap.canvas`:**
   - Lee el canvas actual para conocer las coordenadas existentes
   - Calcula `x` e `y` coherentes: mismo nivel que nodos hermanos, un escalón de ~520 unidades por debajo del padre en `y`
   - Genera un `id` único (8 caracteres hexadecimales aleatorios)
   - Añade el nodo con `"type":"file"` y la ruta vault-relativa correcta (prefijo `CS/Contenido/cs-roadmap/categorias/`)
   - Añade la arista desde el nodo padre al nuevo nodo

4. **Confirma** el resultado mostrando el archivo creado y el fragmento JSON añadido al canvas.

⚠️ Nunca crear el `.md` sin actualizar el canvas, ni viceversa. Los dos pasos son atómicos.
