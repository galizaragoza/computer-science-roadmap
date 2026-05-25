# README
La intención de este proyecto es convertirse en una guía de referencia para personas interesadas o recién llegadas al mundo de la informática. La premisa principal del roadmap es la siguiente:

> En informática, la abstracción es el proceso de eliminar la gestión manual de ciertos procesos para simplificar una tarea. Cuando se habla de capas de abstraccion, lo que se está haciendo es clasificar la tecnología en distintos 'grupos' en función de su nivel de abstracción. Este roadmap se basa en la premisa de que es mucho más fácil subir capas que bajarlas. Aunque entender, y sobre todo saber manejar, conceptos de bajo nivel pueda suponer un reto más grande al principio, cuanto más se profundiza en informática más aumenta el valor de ese conocimiento. Comprender bien cimientos que sostienen la capa superior hace mucho más fácil entender la tecnología, y desarrolla un criterio más completo. En definitiva, es mejor construir desde los cimientos que levantar tejados en el aire e intentar cimentarlos después.

La idea es hacer un grafo estilo árbol invertido, iniciando en una raíz común, la arquitectura básica de ordenadores, a partir de ahí, la idea es crear ramas y bifurcaciones, definiendo rutas para distintas especializaciones. Cada nodo tendrá a su vez una justificación breve de su posición en el grafo y una lista de contenido, que se irá ampliando.

## Instrucciones
En este punto del proyecto, se está creando el esquema de referencia con el que luego se construirá la web. Hasta el momento, se está haciendo un grafo en un archivo `.canvas`, por lo que es necesario tener Obsidian instalado para contribuir (se aceptan sugerencias de otros métodos para elaborar el esquema de referencia).

Una vez instalado obsidian, basta con clonar este repositorio y abrirlo desde Obsidian para visualizar el canvas y aportar.

La estructura del proyecto es la siguiente
- README --> Este archivo
- roadmap.canvas  --> El esquema de referencia
- /categorías --> En este directorio están los nodos, con sus descripciones y contenido, el orden es irrelevante en este directorio ya que se define en el archivo `roadmap.canvas`

## Normas
Para aceptar una aportación, hay que adherirse a una serie de normas:

1. Las aportaciones deberían estar alineadas con la premisa básica del proyecto, y la estructura del grafo (árbol invertido: menos abstracto/díficil arriba hacia más abstracto/difícil abajo)
	- Destacar que es posible y deseable posicionar nodos menos abstractos pero más difíciles más abajo, por ejemplo: Arquitectura de ordenadores 1(poco abstracto) --> Python 1(Abstracto) --> Arquitectura de ordenadores 2 (poco abstracto pero nivel avanzado)
![[roadmap_estructura.svg|Ejemplo de esquema|1224x1161]]
2. La información tiene que ser fiable y verificable
3. Al hacer una aportación al directorio /categorías, ha de ubicarse también en el roadmap
4. Al ubicar nodos en el roadmap, hay que referenciar el archivo, no crear un "post-it"
