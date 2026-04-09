# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Die/FXListDie.cpp - Enhanced Analysis

## Architectural Role
This file implements the death effect system for game objects, bridging the game logic layer with the rendering effects system (FXList). It handles the conditional playback of death animations based on upgrade states and damage context, ensuring effects are synchronized across the network.

## Cross-References
### Incoming
- Called by the object destruction pipeline when an object dies (via `onDie`)
- Referenced during object initialization (via constructor)
- Used in upgrade activation checks (via `isUpgradeActive`)

### Outgoing
- Calls `FXList::doFXObj`/`doFXPos` to trigger visual/audio effects
- Queries `TheGameLogic` for damage source resolution
- Relies on `DieModule` base class for core functionality

## Design Patterns
- **Template Method**: Extends `DieModule` with specialized death behavior
- **Strategy**: Encapsulates death effect logic as a module for object composition
- **Observer**: Reacts to object death events via `onDie` callback

*Not inferable: No clear use of Factory, Decorator, or Visitor patterns.*
