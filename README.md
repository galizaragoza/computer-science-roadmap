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

<svg xmlns="http://www.w3.org/2000/svg" width="900" height="920" viewBox="0 0 900 920">
  <defs>
    <marker id="arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="5" markerHeight="5" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#4a5568" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
    <marker id="arr-seq" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="5" markerHeight="5" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="#6b7a99" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
    <filter id="glow-teal">
      <feGaussianBlur stdDeviation="3" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <linearGradient id="bg-grad" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#0d1117"/>
      <stop offset="100%" stop-color="#111827"/>
    </linearGradient>
    <linearGradient id="root-grad" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#0d4f4a"/>
      <stop offset="100%" stop-color="#0a3d3a"/>
    </linearGradient>
    <linearGradient id="fund-grad" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#1e1b4b"/>
      <stop offset="100%" stop-color="#1a1836"/>
    </linearGradient>
    <linearGradient id="bridge-grad" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#3d1f00"/>
      <stop offset="100%" stop-color="#2d1800"/>
    </linearGradient>
    <linearGradient id="spec-grad" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#1a2535"/>
      <stop offset="100%" stop-color="#141e2e"/>
    </linearGradient>
    <linearGradient id="seq-grad" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#0f2618"/>
      <stop offset="100%" stop-color="#0a1f12"/>
    </linearGradient>
  </defs>

  <!-- Fondo -->
  <rect width="900" height="920" fill="url(#bg-grad)"/>

  <!-- Líneas de cuadrícula sutil -->
  <line x1="0" y1="460" x2="900" y2="460" stroke="#ffffff" stroke-width="0.3" stroke-opacity="0.04"/>
  <line x1="450" y1="0" x2="450" y2="920" stroke="#ffffff" stroke-width="0.3" stroke-opacity="0.04"/>

  <!-- ══ CABECERA ══ -->
  <text x="450" y="42" text-anchor="middle" font-family="'Georgia', 'Times New Roman', serif" font-size="11" fill="#5eead4" letter-spacing="4" font-weight="400">ROADMAP DE INFORMÁTICA</text>
  <text x="450" y="68" text-anchor="middle" font-family="'Georgia', 'Times New Roman', serif" font-size="22" fill="#e2e8f0" letter-spacing="0.5" font-weight="400">De los cimientos a la especialización</text>
  <line x1="200" y1="80" x2="700" y2="80" stroke="#5eead4" stroke-width="0.5" stroke-opacity="0.4"/>

  <!-- ══ ETIQUETA DE EJE ══ -->
  <text x="22" y="200" text-anchor="middle" font-family="'Georgia', serif" font-size="9" fill="#4a5568" letter-spacing="2" transform="rotate(-90,22,200)">MENOS ABSTRACTO</text>
  <text x="22" y="700" text-anchor="middle" font-family="'Georgia', serif" font-size="9" fill="#4a5568" letter-spacing="2" transform="rotate(-90,22,700)">MÁS ABSTRACTO</text>
  <line x1="36" y1="110" x2="36" y2="850" stroke="#4a5568" stroke-width="0.5" stroke-opacity="0.5"/>
  <polygon points="36,104 33,114 39,114" fill="#4a5568" fill-opacity="0.5"/>
  <polygon points="36,856 33,846 39,846" fill="#4a5568" fill-opacity="0.5"/>

  <!-- ══ CAPA 0: RAÍZ ══ -->
  <!-- Nodo raíz -->
  <rect x="270" y="105" width="360" height="64" rx="10" fill="url(#root-grad)" stroke="#2dd4bf" stroke-width="1.2" stroke-opacity="0.8"/>
  <rect x="270" y="105" width="360" height="3" rx="1.5" fill="#2dd4bf" fill-opacity="0.6"/>
  <text x="450" y="132" text-anchor="middle" font-family="'Georgia', serif" font-size="15" fill="#ccfbf1" font-weight="700" letter-spacing="0.3">Arquitectura de computadores</text>
  <text x="450" y="152" text-anchor="middle" font-family="'Georgia', serif" font-size="10" fill="#5eead4" letter-spacing="1">BASE COMÚN · NIVEL 1</text>

  <!-- etiqueta de capa -->
  <text x="880" y="138" text-anchor="end" font-family="'Georgia', serif" font-size="9" fill="#2dd4bf" letter-spacing="1.5" fill-opacity="0.7">CAPA 0</text>

  <!-- ══ CONECTORES 0→1 ══ -->
  <line x1="340" y1="169" x2="175" y2="228" stroke="#4a5568" stroke-width="1" marker-end="url(#arr)"/>
  <line x1="450" y1="169" x2="450" y2="228" stroke="#4a5568" stroke-width="1" marker-end="url(#arr)"/>
  <line x1="560" y1="169" x2="726" y2="228" stroke="#4a5568" stroke-width="1" marker-end="url(#arr)"/>

  <!-- ══ CAPA 1: FUNDAMENTOS ══ -->
  <text x="880" y="260" text-anchor="end" font-family="'Georgia', serif" font-size="9" fill="#a78bfa" letter-spacing="1.5" fill-opacity="0.7">CAPA 1</text>

  <!-- SO -->
  <rect x="65" y="228" width="220" height="62" rx="8" fill="url(#fund-grad)" stroke="#7c3aed" stroke-width="0.8" stroke-opacity="0.7"/>
  <rect x="65" y="228" width="220" height="2.5" rx="1.5" fill="#7c3aed" fill-opacity="0.5"/>
  <text x="175" y="252" text-anchor="middle" font-family="'Georgia', serif" font-size="13" fill="#c4b5fd" font-weight="700">Sistemas operativos</text>
  <text x="175" y="270" text-anchor="middle" font-family="'Georgia', serif" font-size="9.5" fill="#8b5cf6" letter-spacing="0.5">Memoria · procesos · I/O</text>

  <!-- Redes 1 -->
  <rect x="340" y="228" width="220" height="62" rx="8" fill="url(#fund-grad)" stroke="#7c3aed" stroke-width="0.8" stroke-opacity="0.7"/>
  <rect x="340" y="228" width="220" height="2.5" rx="1.5" fill="#7c3aed" fill-opacity="0.5"/>
  <text x="450" y="252" text-anchor="middle" font-family="'Georgia', serif" font-size="13" fill="#c4b5fd" font-weight="700">Redes 1</text>
  <text x="450" y="270" text-anchor="middle" font-family="'Georgia', serif" font-size="9.5" fill="#8b5cf6" letter-spacing="0.5">TCP/IP · modelo OSI</text>

  <!-- Algoritmos -->
  <rect x="615" y="228" width="220" height="62" rx="8" fill="url(#fund-grad)" stroke="#7c3aed" stroke-width="0.8" stroke-opacity="0.7"/>
  <rect x="615" y="228" width="220" height="2.5" rx="1.5" fill="#7c3aed" fill-opacity="0.5"/>
  <text x="725" y="252" text-anchor="middle" font-family="'Georgia', serif" font-size="13" fill="#c4b5fd" font-weight="700">Algoritmos y estructuras</text>
  <text x="725" y="270" text-anchor="middle" font-family="'Georgia', serif" font-size="9.5" fill="#8b5cf6" letter-spacing="0.5">Complejidad · búsqueda · grafos</text>

  <!-- ══ CONECTORES 1→2 ══ -->
  <line x1="175" y1="290" x2="350" y2="350" stroke="#4a5568" stroke-width="1" marker-end="url(#arr)"/>
  <line x1="450" y1="290" x2="450" y2="350" stroke="#4a5568" stroke-width="1" marker-end="url(#arr)"/>
  <line x1="725" y1="290" x2="548" y2="350" stroke="#4a5568" stroke-width="1" marker-end="url(#arr)"/>

  <!-- ══ CAPA 2: PRIMER LENGUAJE ══ -->
  <text x="880" y="385" text-anchor="end" font-family="'Georgia', serif" font-size="9" fill="#fb923c" letter-spacing="1.5" fill-opacity="0.7">CAPA 2</text>

  <rect x="245" y="350" width="410" height="64" rx="10" fill="url(#bridge-grad)" stroke="#f97316" stroke-width="1" stroke-opacity="0.8"/>
  <rect x="245" y="350" width="410" height="2.5" rx="1.5" fill="#f97316" fill-opacity="0.5"/>
  <text x="450" y="376" text-anchor="middle" font-family="'Georgia', serif" font-size="15" fill="#fed7aa" font-weight="700" letter-spacing="0.3">Python 1</text>
  <text x="450" y="396" text-anchor="middle" font-family="'Georgia', serif" font-size="10" fill="#fb923c" letter-spacing="1">PRIMER LENGUAJE DE ALTO NIVEL</text>

  <!-- ══ CONECTORES 2→3 ══ -->
  <line x1="330" y1="414" x2="150" y2="468" stroke="#4a5568" stroke-width="1" marker-end="url(#arr)"/>
  <line x1="395" y1="414" x2="363" y2="468" stroke="#4a5568" stroke-width="1" marker-end="url(#arr)"/>
  <line x1="505" y1="414" x2="537" y2="468" stroke="#4a5568" stroke-width="1" marker-end="url(#arr)"/>
  <line x1="570" y1="414" x2="750" y2="468" stroke="#4a5568" stroke-width="1" marker-end="url(#arr)"/>

  <!-- ══ CAPA 3: ESPECIALIZACIONES ══ -->
  <text x="880" y="504" text-anchor="end" font-family="'Georgia', serif" font-size="9" fill="#60a5fa" letter-spacing="1.5" fill-opacity="0.7">CAPA 3</text>

  <!-- Dev web -->
  <rect x="55" y="468" width="190" height="62" rx="8" fill="url(#spec-grad)" stroke="#2563eb" stroke-width="0.8" stroke-opacity="0.6"/>
  <rect x="55" y="468" width="190" height="2.5" rx="1.5" fill="#3b82f6" fill-opacity="0.5"/>
  <text x="150" y="492" text-anchor="middle" font-family="'Georgia', serif" font-size="12.5" fill="#93c5fd" font-weight="700">Desarrollo web</text>
  <text x="150" y="510" text-anchor="middle" font-family="'Georgia', serif" font-size="9" fill="#60a5fa" letter-spacing="0.5">HTML · CSS · JavaScript</text>

  <!-- Ciencia de datos -->
  <rect x="268" y="468" width="190" height="62" rx="8" fill="url(#spec-grad)" stroke="#2563eb" stroke-width="0.8" stroke-opacity="0.6"/>
  <rect x="268" y="468" width="190" height="2.5" rx="1.5" fill="#3b82f6" fill-opacity="0.5"/>
  <text x="363" y="492" text-anchor="middle" font-family="'Georgia', serif" font-size="12.5" fill="#93c5fd" font-weight="700">Ciencia de datos</text>
  <text x="363" y="510" text-anchor="middle" font-family="'Georgia', serif" font-size="9" fill="#60a5fa" letter-spacing="0.5">Pandas · NumPy · visualización</text>

  <!-- Sistemas -->
  <rect x="481" y="468" width="190" height="62" rx="8" fill="url(#spec-grad)" stroke="#2563eb" stroke-width="0.8" stroke-opacity="0.6"/>
  <rect x="481" y="468" width="190" height="2.5" rx="1.5" fill="#3b82f6" fill-opacity="0.5"/>
  <text x="576" y="492" text-anchor="middle" font-family="'Georgia', serif" font-size="12.5" fill="#93c5fd" font-weight="700">Sistemas</text>
  <text x="576" y="510" text-anchor="middle" font-family="'Georgia', serif" font-size="9" fill="#60a5fa" letter-spacing="0.5">C · memoria · compiladores</text>

  <!-- Ciberseguridad -->
  <rect x="694" y="468" width="190" height="62" rx="8" fill="url(#spec-grad)" stroke="#2563eb" stroke-width="0.8" stroke-opacity="0.6"/>
  <rect x="694" y="468" width="190" height="2.5" rx="1.5" fill="#3b82f6" fill-opacity="0.5"/>
  <text x="789" y="492" text-anchor="middle" font-family="'Georgia', serif" font-size="12.5" fill="#93c5fd" font-weight="700">Ciberseguridad</text>
  <text x="789" y="510" text-anchor="middle" font-family="'Georgia', serif" font-size="9" fill="#60a5fa" letter-spacing="0.5">Criptografía · ataques · defensa</text>

  <!-- ══ CONECTORES 3→4 ══ -->
  <line x1="150" y1="530" x2="150" y2="588" stroke="#4a5568" stroke-width="1" marker-end="url(#arr)"/>
  <line x1="363" y1="530" x2="363" y2="588" stroke="#4a5568" stroke-width="1" marker-end="url(#arr)"/>
  <line x1="576" y1="530" x2="576" y2="588" stroke="#4a5568" stroke-width="1" marker-end="url(#arr)"/>

  <!-- ══ CAPA 4: NODOS SECUELA ══ -->
  <text x="880" y="624" text-anchor="end" font-family="'Georgia', serif" font-size="9" fill="#4ade80" letter-spacing="1.5" fill-opacity="0.7">CAPA 4</text>

  <!-- Redes 2 -->
  <rect x="55" y="588" width="190" height="62" rx="8" fill="url(#seq-grad)" stroke="#16a34a" stroke-width="0.8" stroke-opacity="0.7"/>
  <rect x="55" y="588" width="190" height="2.5" rx="1.5" fill="#22c55e" fill-opacity="0.5"/>
  <text x="150" y="612" text-anchor="middle" font-family="'Georgia', serif" font-size="12.5" fill="#86efac" font-weight="700">Redes 2</text>
  <text x="150" y="630" text-anchor="middle" font-family="'Georgia', serif" font-size="9" fill="#4ade80" letter-spacing="0.5">Routing avanzado · SDN</text>

  <!-- Machine learning -->
  <rect x="268" y="588" width="190" height="62" rx="8" fill="url(#seq-grad)" stroke="#16a34a" stroke-width="0.8" stroke-opacity="0.7"/>
  <rect x="268" y="588" width="190" height="2.5" rx="1.5" fill="#22c55e" fill-opacity="0.5"/>
  <text x="363" y="612" text-anchor="middle" font-family="'Georgia', serif" font-size="12.5" fill="#86efac" font-weight="700">Machine learning</text>
  <text x="363" y="630" text-anchor="middle" font-family="'Georgia', serif" font-size="9" fill="#4ade80" letter-spacing="0.5">Modelos · entrenamiento</text>

  <!-- Arquitectura avanzada -->
  <rect x="481" y="588" width="213" height="62" rx="8" fill="url(#seq-grad)" stroke="#16a34a" stroke-width="0.8" stroke-opacity="0.7"/>
  <rect x="481" y="588" width="213" height="2.5" rx="1.5" fill="#22c55e" fill-opacity="0.5"/>
  <text x="587" y="612" text-anchor="middle" font-family="'Georgia', serif" font-size="12.5" fill="#86efac" font-weight="700">Arquitectura avanzada</text>
  <text x="587" y="630" text-anchor="middle" font-family="'Georgia', serif" font-size="9" fill="#4ade80" letter-spacing="0.5">RISC-V · pipelines · caché</text>

  <!-- ══ FLECHA SECUELA: Redes 1 → Redes 2 (curva lateral) ══ -->
  <path d="M340 259 Q30 259 30 619 L55 619" fill="none" stroke="#6b7a99" stroke-width="1" stroke-dasharray="5 4" marker-end="url(#arr-seq)" stroke-opacity="0.6"/>
  <text x="18" y="443" text-anchor="middle" font-family="'Georgia', serif" font-size="8" fill="#6b7a99" letter-spacing="1.5" transform="rotate(-90,18,443)" fill-opacity="0.7">SECUELA</text>

  <!-- ══ LEYENDA ══ -->
  <rect x="55" y="706" width="790" height="150" rx="10" fill="#ffffff" fill-opacity="0.03" stroke="#ffffff" stroke-width="0.4" stroke-opacity="0.08"/>
  <text x="450" y="730" text-anchor="middle" font-family="'Georgia', serif" font-size="10" fill="#94a3b8" letter-spacing="2">LEYENDA</text>
  <line x1="200" y1="737" x2="700" y2="737" stroke="#94a3b8" stroke-width="0.3" stroke-opacity="0.3"/>

  <!-- col 1 -->
  <rect x="90" y="752" width="14" height="14" rx="2" fill="#0d4f4a" stroke="#2dd4bf" stroke-width="1"/>
  <text x="112" y="763" font-family="'Georgia', serif" font-size="10" fill="#94a3b8">Raíz — base común del árbol</text>

  <rect x="90" y="776" width="14" height="14" rx="2" fill="#1e1b4b" stroke="#7c3aed" stroke-width="1"/>
  <text x="112" y="787" font-family="'Georgia', serif" font-size="10" fill="#94a3b8">Fundamentos transversales</text>

  <rect x="90" y="800" width="14" height="14" rx="2" fill="#3d1f00" stroke="#f97316" stroke-width="1"/>
  <text x="112" y="811" font-family="'Georgia', serif" font-size="10" fill="#94a3b8">Puente al alto nivel (primer lenguaje)</text>

  <!-- col 2 -->
  <rect x="420" y="752" width="14" height="14" rx="2" fill="#1a2535" stroke="#3b82f6" stroke-width="1"/>
  <text x="442" y="763" font-family="'Georgia', serif" font-size="10" fill="#94a3b8">Especializaciones (bifurcaciones)</text>

  <rect x="420" y="776" width="14" height="14" rx="2" fill="#0f2618" stroke="#22c55e" stroke-width="1"/>
  <text x="442" y="787" font-family="'Georgia', serif" font-size="10" fill="#94a3b8">Nodos secuela (profundización)</text>

  <line x1="420" y1="805" x2="434" y2="805" stroke="#6b7a99" stroke-width="1" stroke-dasharray="4 3"/>
  <text x="442" y="809" font-family="'Georgia', serif" font-size="10" fill="#94a3b8">Relación secuela (excepción al árbol)</text>

  <!-- Filosofía -->
  <line x1="150" y1="832" x2="750" y2="832" stroke="#ffffff" stroke-width="0.3" stroke-opacity="0.08"/>
  <text x="450" y="848" text-anchor="middle" font-family="'Georgia', serif" font-size="9.5" fill="#475569" font-style="italic">"Es mejor construir desde los cimientos que levantar tejados en el aire e intentar cimentarlos después."</text>
</svg>

2. La información tiene que ser fiable y verificable
3. Al hacer una aportación al directorio /categorías, ha de ubicarse también en el roadmap
4. Al ubicar nodos en el roadmap, hay que referenciar el archivo, no crear un "post-it"
