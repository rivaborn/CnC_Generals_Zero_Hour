# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/FlightDeckBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements the flight deck behavior module for aircraft carriers, managing aircraft parking, production, and healing. It bridges the gap between the AI system and the physical representation of flight decks in the game world, handling both logical operations and visual effects.

## Cross-References
### Incoming
- **AI System**: Calls `aiDoCommand` to handle AI orders for aircraft carriers
- **Production System**: Uses `ProductionUpdate` for aircraft creation
- **ThingFactory**: Creates new aircraft objects via `TheThingFactory`
- **GameLogic**: Queries object states through `TheGameLogic`

### Outgoing
- **AI System**: Propagates orders to aircraft via `propagateOrdersToPlanes()`
- **Particle System**: Manages catapult effects through `ParticleSys`
- **Serialization**: Uses `Xfer` system for save/load functionality
- **Bone System**: Accesses skeletal animations for runway positions

## Design Patterns
- **Module Pattern**: Encapsulates flight deck behavior as a reusable module attached to objects
- **Observer Pattern**: Tracks aircraft state changes (e.g., destruction via `purgeDead`)
- **State Machine**: Manages runway usage states (takeoff/landing/parking) implicitly through frame-based timers

*Not inferable*: Exact implementation of command propagation or healing rate calculation.
