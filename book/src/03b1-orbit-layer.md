# Orbit Layer

The orbit layer (O1) is where the player sees the orbital environment as a whole — the station, the planet below (if any), shuttle traffic, and the immediate space around them.

## Primary purpose

This layer is responsible for the orbit as a visible, connected environment.

It covers:

- the space station as a dockable, expandable structure visible from outside
- the planet below (if present) as a navigable destination
- shuttle and elevator traffic between station and planet
- solar arrays and exposed power systems
- docking interfaces and cargo exchange
- asteroid fields and local orbital resources
- vulnerability to damage and interruption

## What the player sees

The orbit layer presents two possible compositions:

### Station only (no planet)

The station floats in space, possibly near an asteroid belt or at a route junction. The player can:

- inspect and expand the station hull
- manage docking and external traffic
- enter the station interior (→ O2)

### Station + planet

The station orbits a planet. The player can:

- inspect and expand the station hull
- manage shuttle and elevator traffic between station and planet
- enter the station interior (→ O2)
- descend to the planet surface (→ P2)

The planet appears as a large navigable body below. If the planet is unexplored (zero regions), it is still visible but there is nothing to enter yet — the player must first explore it from the planet layer.

## Desired feel

This layer should feel:

- architectural
- exposed
- strategic
- throughput-driven

The player should feel that the station's shape matters because shape determines role, access, and survivability.

## Key gameplay questions

- where should docks be placed
- how should cargo enter and leave the station
- what external systems are worth armoring or duplicating
- when should the player enlarge the station shell instead of optimizing current traffic
- how dependent should this station remain on planetary imports
- is the planet below worth exploring, or should resources focus on orbital industry

## Orbit layer loops

### Expansion loop

1. identify an orbital bottleneck
2. add structural capacity
3. connect it to traffic and power
4. absorb the next growth threshold

### Traffic loop

1. watch docks and cargo queues
2. identify overloaded ingress or egress points
3. reorganize approach patterns or add external handling capacity
4. smooth throughput between planet, station, and space routes

### Exposure loop

1. place a critical external system
2. gain new throughput or energy capability
3. inherit new vulnerability
4. decide whether to harden, duplicate, or accept the risk

## Station identity

The station exterior should reveal its strategic identity at a glance:

- shipyard station
- cargo relay station
- orbital refinery station
- elevator anchor station
- frontier dispatch station

That identity should not be only cosmetic. It should emerge from real structural decisions.
