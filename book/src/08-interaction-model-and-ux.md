# Interaction Model And UX

The interaction model should follow the scope framework rather than fight it.

The game does not merely have camera zoom levels. It has eight operational layers, grouped into four scopes. The UI should make moving between those layers feel natural and consequence-driven.

## Scope 1: Planetary

### Region layer UX

Core verbs:

- place machines
- connect logistics
- balance ratios
- manage power
- inspect local bottlenecks

Important tools:

- throughput overlays
- congestion overlays
- starve and flood warnings
- one-click path tracing for belts and pull rails
- clear embodiment and chassis state indicators

### Inter-region / continental UX

Core verbs:

- inspect deficits
- assign specialization
- move goods between regions
- diagnose planetary bottlenecks

Important tools:

- regional import and export ledger
- bandwidth and priority controls
- visible regional role labels
- shortage propagation alerts

## Scope 2: Space station

### Exterior UX

Core verbs:

- place and upgrade exterior modules
- monitor docks and orbital traffic
- assess external power and cargo throughput
- manage exchange with planets and frontier routes

Important tools:

- station silhouette or hull planner
- docking state panel
- orbital traffic overlay
- exposed infrastructure warnings

### Interior UX

Core verbs:

- design station production
- manage module interiors
- build rockets and shuttles
- tune high-value manufacturing lines

Important tools:

- persistent station sidebar
- fast switch between interior sectors
- internal transport overlays
- queue and capacity panels for shipyard production

## Scope 3: Interplanetary frontier

### Route and gate UX

Core verbs:

- create routes
- assign trade flows
- place gates
- monitor strategic graph health

Important tools:

- route planner view
- gate network map
- per-link risk and capacity visibility
- Flux front proximity overlay

### Frontier operations UX

Core verbs:

- prospect and mine asteroids
- probe anomalies
- establish outposts
- stage new orbital footholds

Important tools:

- asteroid hub panel
- hazard and integrity indicators
- expedition readiness status
- colonization staging checklist

## Scope 4: Elemental stabilization

### Lattice layer UX

Core verbs:

- scan atomic fracture patterns
- place stabilizer anchors
- connect local repair meshes
- verify structural integrity under stress

Important tools:

- local lattice stress overlay
- contamination and fracture map
- anchor stability indicators
- repair propagation preview

### Flux field layer UX

Core verbs:

- tune harmonics
- route stabilization pressure
- observe resonance spread
- prevent overload or inversion

Important tools:

- field-flow visualizer
- harmonic tuning panel
- resonance conflict warnings
- macro-to-micro coupling display

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

When the player moves from a region to a continent, or from a station interior to a solar route map, resource logic should remain legible. The UI should never make the simulation feel like it changes rules when the camera changes context.

## Hotkey concept

A simple first pass:

- `1`: region layer
- `2`: inter-region layer
- `3`: station exterior
- `4`: station interior
- `5`: route and gate layer
- `6`: frontier operations layer
- `7`: lattice layer
- `8`: flux field layer

The exact mapping can change, but the conceptual rule matters: each operational layer should be reachable directly, and the player should not feel lost while moving between them.
