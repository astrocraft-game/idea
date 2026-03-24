# Scope Framework

This chapter defines the main structural lens of the game.

The design is organized around **four major scopes**, and each scope contains **two layers**. Those eight layers are not arbitrary zoom levels. Each one changes what the player is responsible for, what information must be visible, and what kinds of logistical failure become common.

## The four scopes

| Scope | Layer A (Primary) | Layer B (Secondary) | Primary fantasy |
|---|---|---|---|
| Planet | P1 Region — local factory floor | P2 Planet — multiple regions on one world | Turn local industry into a planetary network |
| Orbit | O1 Orbit — orbital view with station and optional planet | O2 Station — station internals | Turn orbit into a productive industrial body |
| Space | S1 Star — solar system with asteroids and routes | S2 Galaxy — full galaxy view and star gates | Turn distance into infrastructure |
| Element | E1 Molecule — molecular-level construction and biology | E2 Quantum — atomic-level stabilization and flux repair | Turn matter itself into a repairable industrial system |

## Why this structure is better than a flat list of scales

A flat list of scales describes camera distance. A scope model describes responsibility.

For example:

- the region layer is about production topology and immediate logistics
- the planet layer is about deficits, exports, imports, and specialization across regions
- the orbit layer is about orbital structure, the station, and exchange with the planet below
- the station layer is about turning the station into a functioning factory
- the star layer is about deciding where movement and expansion should happen within a solar system
- the galaxy layer is about exploiting distant opportunities, star gates, and creating the next foothold
- the molecule layer is about direct biological and molecular-scale construction and repair
- the quantum layer is about propagating atomic stabilization through unstable matter

That means each scope has an inner operational layer and an outer organizational layer, but the exact character of those layers changes with the fiction.

## Scope 1: Planet

### Layer P1: Region

This is the place where the player first learns the grammar of the game:

- mining
- refining
- assembling
- routing items
- balancing power
- defending vulnerable infrastructure
- moving the embodied player between tasks

This layer should feel tactile, readable, and materially grounded. Machines occupy physical space. Belts are visible. Buffers matter. Travel time matters. Chassis specialization matters.

The region layer is where the player builds trust in the simulation.

### Layer P2: Planet

Once local industry works, the player should be pulled into macro management of a whole planet.

A planet contains zero or more regions. A planet with zero regions is **unexplored** — the player lands and sees barren, unknown terrain. They must explore (send probes, build outposts) to discover and create regions.

This layer handles:

- regional specialization
- long-distance transfers between regions
- macro deficits and surpluses
- strategic placement of new industrial nodes
- bandwidth and flow allocation for high-level transport systems
- resilience against local failures becoming planetary shortages

The core feeling here should be, "My factories are no longer isolated; they are organs in one planetary body."

## Scope 2: Orbit

### Layer O1: Orbit

The orbit layer is the orbital view around a celestial body. Every orbit contains exactly one space station. Some orbits also have a planet visible below.

This is where orbit becomes architecture and logistics at the same time. The player sees:

- the space station as a dockable, expandable structure
- the planet below (if present), with its regions as clickable entry points
- shuttle and elevator traffic between station and planet
- asteroid fields and local orbital resources

From this view the player can enter the station (→ O2) or descend to the planet surface (→ P2), if one exists.

### Layer O2: Station

The station interior layer is where the orbital shell becomes an industrial organism.

Primary concerns:

- module interiors and manufacturing lines
- rocket and shuttle production
- specialized refinement and advanced manufacturing
- storage, drones, and internal transport
- space miner construction
- molecular shrinking research (epoch 4 — unlocks E1 later)

The station should not feel like "just another factory map." The station interior should feel constrained by orbital design decisions. Internal efficiency depends on external capacity and vice versa.

## Scope 3: Space

### Layer S1: Star

The star layer is a solar system view. The player sees a star at center, orbiting bodies, asteroid belts, and routes between them.

Primary concerns:

- send miners to mine asteroids and satellites
- send space stations to orbit new planets for exploration
- route creation and traffic prioritization
- managing the shape of expansion within one star system

A planet can only be explored if there is a station in orbit nearby (before star gates).

### Layer S2: Galaxy

The galaxy layer is the full galactic view. Solar systems are clickable objects.

Primary concerns:

- interstellar route planning
- star gate construction and management
- sending stations on long journeys to other star systems
- strategic network topology across the galaxy
- flux material research and atomic-level shrinking discovery

Star gates (unlocked at this epoch) allow direct travel to any planet or orbit without needing a nearby station — this changes the entire access model for the game.

## Scope 4: Element

### Layer E1: Molecule

The molecule layer is entered through shrinkers built in stations (O2) or regions (P1).

This is where the game turns inward. Instead of building outward into space, the player shrinks into matter itself. At this scale:

- biological systems become the terrain — viruses, bacteria, molecular structures
- gene editing and molecular construction become the core verbs
- the player builds stabilizer structures at molecular scale
- shrinker machines in the macro world serve as entry points

This layer should feel strange but still recognizably industrial. The player is still solving placement, routing, reinforcement, and stabilization problems. The difference is that the terrain is now living matter.

### Layer E2: Quantum

The quantum layer is the deepest level — entered from within an E1 molecule instance.

Primary concerns:

- atomic-level stabilization
- flux field propagation and harmonic tuning
- resonance management across quantum structures
- coupling local atomic repairs into wider stabilization networks
- preventing overload, inversion, or cascade collapse

If the molecule layer is about constructing order at biological scale, the quantum layer is about making that order hold at the fundamental level where physical law itself is slipping.

This is where Dark Flux is finally confronted directly.

## Navigation hierarchy

The eight layers form a nested drill-down tree. The player navigates **down** by clicking an entity and choosing "Enter" in the click panel, and **up** via a single back button. There are no flat scope/layer selection buttons — movement is always entity-driven or via back.

```
S2 Galaxy — solar systems as clickable objects
 └─ S1 Star — orbits around a star, asteroid belts
      └─ O1 Orbit — station + optional planet below
           ├─ O2 Station — station internals
           │    └─ E1 Molecule (optional, shrinker needed)
           │         └─ E2 Quantum
           └─ P2 Planet (optional, 0 or 1 per orbit)
                └─ P1 Region (0..N per planet, 0 = unexplored)
                     └─ E1 Molecule (optional, shrinker needed)
                          └─ E2 Quantum
```

### Child count rules

| Parent | Child | Count |
|---|---|---|
| S2 Galaxy | S1 Star | 1..N |
| S1 Star | O1 Orbit | 1..N |
| O1 Orbit | O2 Station | exactly 1 (always) |
| O1 Orbit | P2 Planet | 0 or 1 |
| P2 Planet | P1 Region | 0..N (0 = unexplored) |
| P1 Region | E1 Molecule | 0..N (shrinker needed) |
| O2 Station | E1 Molecule | 0..N (shrinker needed) |
| E1 Molecule | E2 Quantum | 0..N (atomic shrinker needed) |

### Orbit composition rules

Every orbit has exactly one station. Some orbits also have a planet. Not every orbit has a planet — some are pure station outposts in asteroid fields or at strategic route junctions.

A planet with zero regions is unexplored. The player can enter it and see barren terrain, but there is nothing to do until they explore and establish regions.

### Planet access rules

Before star gates (epochs 1–6), a planet is only accessible from its parent orbit. The player must have a station nearby to look into a planet.

After star gates (epoch 7+), star gates from S2 allow direct travel to any planet, orbit, or star — bypassing the station requirement entirely.

### Code identifiers

| Name | Scope + Layer | Code | Description |
|---|---|---|---|
| Galaxy | Space Secondary | S2 | Solar systems as clickable objects, star gates |
| Star | Space Primary | S1 | Orbits around a star, asteroid belts, routes |
| Orbit | Orbit Primary | O1 | Orbital view with station and optional planet |
| Station | Orbit Secondary | O2 | Interior of the space station |
| Planet | Planet Secondary | P2 | Planet surface with 0..N regions |
| Region | Planet Primary | P1 | Machines, resources, belts, mind disk |
| Molecule | Element Primary | E1 | Molecular-level biological construction |
| Quantum | Element Secondary | E2 | Atomic-level flux stabilization |

### Key navigation rules

- **Down**: always through an entity interaction (click entity → "Enter" in click panel → push current level to navigation stack → transition to child level).
- **Up**: single back button in the right-stack UI (pops navigation stack). Disabled at S2 (top level).
- **Level indicator**: the right-stack always shows the current level code (e.g. "P1") in the scope's accent color, not clickable.
- Entities that serve as navigation portals carry a `NavigationTarget` component.

## Scope transition logic

The campaign should repeatedly follow a stable pattern:

1. Learn a new local layer.
2. Hit the scaling limit of that layer.
3. Unlock the outer layer that organizes many local instances.
4. Use the outer layer to support expansion into a new scope.
5. Re-enter local play inside the new scope.

That rhythm produces coherence.

Example:

1. Build a strong local planetary factory (P1).
2. Outgrow single-region logistics.
3. Unlock planet-wide transport and specialization (P2).
4. Use planetary scale to support launch and orbital construction (O1).
5. Enter the station interior and build new local industry there (O2).
6. Research molecular shrinking in the station.
7. Build shrinkers and descend into molecular terrain (E1).

The same pattern then repeats into space play (S1, S2), and finally the deepest inversion:

1. Build civilization-scale stabilizer networks.
2. Discover that macro stabilization is not enough.
3. Enter existing molecule instances and build atomic shrinkers.
4. Descend to quantum level (E2) and repair reality from the inside.

## Design constraint

No scope should invalidate the previous one.

The player should never feel that planetary play was merely early-game filler once stations exist, or that stations become irrelevant once gates exist, or that macro play becomes irrelevant once elemental descent begins. Older layers should remain active contributors inside the larger strategic machine.
