# CLAUDE.md
## Proyecto
Hoja de ruta de aprendizaje de informática. Estructurada como un árbol invertido: la raíz son los temas más fundamentales/menos abstractos, las hojas son los más especializados/abstractos. Es más fácil subir capas de abstracción que bajarlas. El canvas de Obsidian (`roadmap.canvas`) define el grafo. El contenido vive en `categorias/`.
## Estructura

- `roadmap.canvas` — definición del grafo (nodos + aristas en JSON). Dos tipos de nodo:
  - `"type":"file"` → referencia a un `.md` en `categorias/` (obligatorio para contenido)
  - `"type":"text"` → texto inline (solo para el bloque de tesis, no para nodos de contenido)
- `categorias/` — un `.md` por cada nodo del roadmap
- `assets/` — exportación SVG del roadmap

## Rutas en el canvas

Las referencias dentro de `roadmap.canvas` usan **rutas relativas al vault de Obsidian**, no al repositorio:

```
"file":"Camara/Contenido/cs-roadmap/categorias/nombre-nodo.md"
```

Ajustar el prefijo (`Camara/Contenido/cs-roadmap/`) si la raíz del vault es distinta. Preguntar al usuario antes de asumir la ruta correcta.

## Formato de archivo de nodo (`categorias/*.md`)

```markdown
# Nombre del nodo #Tag
Justificación breve de por qué este nodo va en esta posición del grafo.

[Recurso 1](url) #YouTube
Descripción breve de recurso
[Recurso 2](url) #Paper
Descripción breve de recurso
```

Tags de recurso: `#YouTube`, `#Paper`, `#Libro`, `#Curso`, `#Herramienta`, `#Artículo`.

**Tags de nodo** — mínimo 1 tag de especialidad (path final), resto indican skills cubiertos: `# Golang 1 #programacion #golang #concurrencia`

| Categoría | Tags disponibles |
|-----------|-----------------|
| **Especialidad (path)** | `#programacion` `#web-dev` `#game-dev` `#data-science` `#machine-learning` `#ia` `#ciberseguridad` `#redes` `#hardware` `#embedded` `#software-architecture` `#devops` `#ux-dev` `#sistemas-operativos` |
| **Lenguaje** | `#c` `#cpp` `#c-sharp` `#python` `#javascript` `#typescript` `#golang` `#rust` `#java` `#bash` `#sql` |
| **Concepto** | `#low-level` `#concurrencia` `#punteros` `#memoria` `#algoritmos` `#estructuras-de-datos` `#patrones-de-diseno` `#compiladores` `#estadistica` `#criptografia` `#rest-api` |
| **Tecnología** | `#html` `#css` `#nodejs` `#react` `#vue` `#numpy` `#pandas` `#deep-learning` `#redes-neuronales` `#tcp-ip` `#protocolos` `#http` `#hacking` `#pentesting` `#fpga` `#arduino` `#electronica` |

## Añadir un nodo nuevo (siempre dos pasos)

1. Crear `categorias/nombre-nodo.md` con el formato anterior.
2. En `roadmap.canvas`, añadir:
   - Nodo `"type":"file"` con la ruta vault-relativa correcta y coordenadas `x`/`y` coherentes con su posición en el árbol (valor `y` mayor = más abajo = más abstracto).
   - Arista desde el nodo padre al nuevo nodo.

Nunca hacer solo uno de los dos pasos.

## Reglas de contribución

1. Todo nodo en `categorias/` debe estar referenciado y conectado en `roadmap.canvas`.
2. No usar nodos `"type":"text"` para contenido.
3. Ordenación: menos abstracto/fundamental → arriba. Más abstracto/niveles superiores de nodos previos → abajo.
4. Recursos fiables, verificables, preferiblemente gratuitos.
5. Todo el contenido en castellano.

## Especialidades previstas

El tronco común desemboca en estas ramas: Programación (→ Web Dev, Game Dev, Software Architecture), Datos/IA (→ Data Science, ML/IA), Sistemas (→ Ciberseguridad, Redes), Hardware (→ Embedded/FPGA). Las ramas comparten inicio antes de bifurcarse.
