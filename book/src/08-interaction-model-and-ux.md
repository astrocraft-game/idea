# Interaction Model And UX

The interaction model should follow the scope framework rather than fight it.

The game does not merely have camera zoom levels. It has eight operational layers, grouped into four scopes. The UI should make moving between those layers feel natural and consequence-driven.

## Scope 1: Planet

### Region layer (P1) UX

Core verbs:

- place machines
- connect logistics
- balance ratios
- manage power
- inspect local bottlenecks
- build and maintain shrinkers (epoch 5+)

Important tools:

- throughput overlays
- congestion overlays
- starve and flood warnings
- one-click path tracing for belts and pull rails
- clear embodiment and chassis state indicators

### Planet layer (P2) UX

Core verbs:

- inspect deficits across regions
- assign specialization
- move goods between regions
- diagnose planetary bottlenecks
- explore unexplored terrain to discover new regions

Important tools:

- regional import and export ledger
- bandwidth and priority controls
- visible regional role labels
- shortage propagation alerts
- exploration and survey tools

## Scope 2: Orbit

### Orbit layer (O1) UX

Core verbs:

- inspect and expand the station from outside
- monitor docks and orbital traffic
- assess shuttle and elevator throughput
- manage exchange with planet below (if present)
- decide whether to descend to planet or enter station

Important tools:

- station silhouette or hull planner
- docking state panel
- orbital traffic overlay
- exposed infrastructure warnings
- planet access indicator (explorable vs unexplored)

### Station layer (O2) UX

Core verbs:

- design station production layouts
- manage module interiors
- build rockets, shuttles, and space miners
- tune high-value manufacturing lines
- build and maintain shrinkers (epoch 5+)

Important tools:

- persistent station sidebar
- fast switch between interior sectors
- internal transport overlays
- queue and capacity panels for shipyard production
- shrinker status and molecular descent readiness

## Scope 3: Space

### Star layer (S1) UX

Core verbs:

- survey asteroid belts and orbits
- assign mining operations
- create and manage routes within the solar system
- dispatch stations to new orbits and planets
- monitor flux proximity

Important tools:

- solar system map with orbit and route overlays
- asteroid prospecting panel
- station dispatch planner
- per-route risk and capacity visibility
- flux front proximity overlay

### Galaxy layer (S2) UX

Core verbs:

- plan interstellar routes
- place and manage star gates
- send stations on long-range journeys
- monitor galactic flux front advance
- manage the strategic network

Important tools:

- galactic map with star systems and gate network
- gate planner and construction queue
- per-system development summary
- flux front overlay
- strategic defense allocation panel

## Scope 4: Element

### Molecule layer (E1) UX

Core verbs:

- scan molecular environments
- place molecular anchors and stabilizer structures
- edit gene sequences
- manage biological tools and organisms
- build atomic shrinkers (epoch 8)

Important tools:

- molecular structure overlay
- biological system status indicators
- contamination and fracture map
- anchor stability indicators
- repair propagation preview

### Quantum layer (E2) UX

Core verbs:

- scan atomic fracture patterns
- place quantum stabilizer anchors
- tune field harmonics
- observe resonance spread
- prevent overload or inversion

Important tools:

- quantum field-flow visualizer
- harmonic tuning panel
- resonance conflict warnings
- macro-to-micro coupling display
- stabilizer network health overview

## Global UX principles

### 1. One consistent guidance channel

Tutorial and hint systems should not fragment by scope. The player should feel that they are learning one coherent game, not eight partially connected interfaces.

### 2. Persistent top-level context

A global top bar should remain visible across layers and expose:

- active mind location
- sync status
- critical alerts
- current logistics emergencies
- priority construction or research tasks

### 3. Alert-driven navigation

Clicking an alert should move the player to the correct scope and highlight the source of the problem.

### 4. Scale should preserve accounting

When the player moves from a region to a planet, or from a station interior to a solar system map, resource logic should remain legible. The UI should never make the simulation feel like it changes rules when the camera changes context.

## Navigation model

Navigation between layers is **entity-driven**, not menu-driven:

- **Drill down**: click an entity that represents a child scope (e.g. a star in S2, an orbit in S1, the station in O1, a region in P2, a shrinker in P1) → click "Enter" in the detail panel → the game transitions to the child layer and pushes the current layer onto a navigation stack.
- **Go back**: click the back button in the right-stack UI → pops the navigation stack and returns to the parent layer. Disabled at S2 (top of the hierarchy).
- **Level indicator**: the right-stack always displays the current level code (e.g. "P1", "O1", "S2") in the scope's accent color, as a non-clickable label.

There are no flat scope/layer selection buttons or direct-jump hotkeys. The player always moves through the hierarchy by interacting with entities or pressing back. This keeps navigation grounded in the fiction — you enter a planet by clicking a planet, not by pressing a number key.
